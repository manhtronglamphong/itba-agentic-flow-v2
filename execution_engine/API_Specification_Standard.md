---
name: API Specification Standard
type: execution_engine
consumes: KA5 outputs (Interface Analysis, Requirements Architecture, Design Options)
produces: Dev-ready API contracts (OpenAPI 3.1 / AsyncAPI 2.x / gRPC .proto)
authority: BABOK v3 §10.24 (Interface Analysis) + OpenAPI 3.1 / AsyncAPI 2.6 / gRPC + RFC 9110 (HTTP semantics) + RFC 7807 (Problem Details)
---

# API Specification Standard

Every interface that crosses a service or organizational boundary is specified
in this format **before** implementation begins. Drift between spec and code
is a defect to be fixed, not tolerated.

## Format by Style

| Style                 | Spec format       | Notes                                                              |
| --------------------- | ----------------- | ------------------------------------------------------------------ |
| Synchronous HTTP/REST | **OpenAPI 3.1**   | JSON Schema 2020-12 compatible; default for resource-style APIs.   |
| Synchronous RPC       | **gRPC .proto3**  | When low-latency / strongly-typed contracts are required.          |
| Asynchronous events   | **AsyncAPI 2.6**  | For Kafka, SQS, MQTT, WebSocket fan-out.                           |
| GraphQL               | **SDL**           | Schema + persisted queries; document allowed operations.           |

Pick **one** style per surface and stay consistent. Mixed styles inside one
domain are a smell.

## Required Header (every spec)

```
API-ID:        API-####
Owning service: <service-name>
Owner:         <team>
Stability:     [experimental | beta | stable | deprecated]
Versioning:    semver — current: vX.Y.Z
Auth model:    [OAuth2-AuthCode | OAuth2-CC | mTLS | API-Key | None]
SLA:           availability X%, p99 latency Yms, RPS budget Z
Traceability:  Requirement-IDs: REQ-####, Design-IDs: DES-####
```

## Resource & URL Conventions (REST)

- **Resources are plural nouns:** `/orders`, `/orders/{orderId}/items`.
- **Identifiers are stable and opaque** (UUID, ULID, or KSUID) — never DB primary keys exposed numerically.
- **Verbs live in HTTP, not URLs.** `GET /orders/{id}` not `GET /getOrder?id=...`.
- **Nesting depth ≤ 2.** Beyond 2 levels, return references and let the client compose.
- **Filtering/sorting/pagination** are query parameters with reserved names: `?filter=...`, `?sort=...`, `?cursor=...&limit=...`. Default `limit` ≤ 100.

## HTTP Method Semantics

| Method  | Safe | Idempotent | Use for                                  |
| ------- | :--: | :--------: | ---------------------------------------- |
| GET     |  ✓   |     ✓      | Retrieve. No body, no side effects.      |
| POST    |  ✗   |     ✗      | Create or non-idempotent action.         |
| PUT     |  ✗   |     ✓      | Replace whole resource.                  |
| PATCH   |  ✗   |     —      | Partial update (JSON Patch / Merge Patch).|
| DELETE  |  ✗   |     ✓      | Remove resource.                         |

## Status Codes

| Code | When                                                                              |
| ---- | --------------------------------------------------------------------------------- |
| 200  | Success with body.                                                                |
| 201  | Created — return `Location` header pointing to new resource.                      |
| 202  | Accepted — async work, return progress URL.                                       |
| 204  | Success, no body (typically DELETE).                                              |
| 400  | Validation error — body conforms to RFC 7807.                                     |
| 401  | Missing/invalid authentication.                                                   |
| 403  | Authenticated but not authorized.                                                 |
| 404  | Resource does not exist (do **not** leak existence via 403/401 mix).              |
| 409  | Conflict — concurrent modification or business-rule violation.                    |
| 422  | Semantic validation failure (vs 400 syntax failure).                              |
| 429  | Rate-limited — return `Retry-After`.                                              |
| 500  | Server fault — never leak stack traces.                                           |
| 503  | Dependency down or maintenance — return `Retry-After`.                            |

## Error Body (RFC 7807 Problem Details)

```json
{
  "type": "https://errors.example.com/orders/insufficient-funds",
  "title": "Insufficient funds",
  "status": 422,
  "detail": "Wallet balance 12.50 is less than charge 25.00",
  "instance": "/orders/01H8X...",
  "errors": [
    { "field": "amount", "code": "insufficient_funds" }
  ]
}
```

Reject any error body that is just `{ "error": "..." }`.

## Versioning

- Major version in URL (`/v1/orders`) **or** `Accept` header (`application/vnd.example.v1+json`) — pick one and stay consistent across all APIs.
- Breaking changes require a new major version + an explicit **deprecation policy** with sunset date in the spec.
- Minor/patch changes must be backward-compatible (additive only).

## Idempotency, Concurrency, Pagination

- **Idempotency for unsafe verbs:** `Idempotency-Key` header on POST when a duplicate retry could cause double-charging.
- **Concurrency:** `ETag` + `If-Match` for PUT/PATCH; `412 Precondition Failed` on mismatch.
- **Pagination:** cursor-based by default; offset only for small bounded sets.

## Security Defaults

- TLS 1.2+ required; no plaintext.
- OAuth2 scopes named per resource+action (`orders:read`, `orders:write`).
- PII fields marked in the schema with `x-pii: true` and redacted in logs.
- Rate limit per credential; return `X-RateLimit-Remaining` and `X-RateLimit-Reset`.

## OpenAPI 3.1 Skeleton

```yaml
openapi: 3.1.0
info:
  title: Orders API
  version: 1.0.0
  x-api-id: API-0017
  x-owner: orders-team
servers:
  - url: https://api.example.com/v1
security:
  - oauth2: [orders:read]
paths:
  /orders/{orderId}:
    get:
      summary: Retrieve an order
      operationId: getOrder
      parameters:
        - name: orderId
          in: path
          required: true
          schema: { type: string, format: ulid }
      responses:
        '200':
          description: OK
          content:
            application/json:
              schema: { $ref: '#/components/schemas/Order' }
        '404':
          description: Not found
          content:
            application/problem+json:
              schema: { $ref: '#/components/schemas/Problem' }
components:
  schemas:
    Order:
      type: object
      required: [id, status, items, total]
      properties:
        id:     { type: string, format: ulid }
        status: { type: string, enum: [PENDING, PAID, FAILED, REFUNDED] }
        total:  { type: string, pattern: '^[0-9]+\\.[0-9]{2}$' }
        items:
          type: array
          items: { $ref: '#/components/schemas/OrderItem' }
    Problem:
      type: object
      required: [type, title, status]
      properties:
        type:    { type: string, format: uri }
        title:   { type: string }
        status:  { type: integer }
        detail:  { type: string }
        instance:{ type: string }
```

## Asynchronous APIs (AsyncAPI)

- Topics named `<domain>.<aggregate>.<event>` in past tense (`orders.order.created`).
- Events are **immutable**, **versioned** (`x-event-version`), and contain a **schema id**.
- Idempotency by `event_id`; consumers MUST be safe under at-least-once delivery.
- Schema registry is the source of truth — not the inline contract in the producer.

## Acceptance Checklist (per API)

- [ ] Header block complete and traceability filled.
- [ ] All paths/operations have `summary`, `operationId`, and tags.
- [ ] All request/response bodies have schemas (no `additionalProperties: true` unless intentional).
- [ ] All error responses use Problem Details.
- [ ] Auth scopes mapped to operations.
- [ ] NFRs (latency, RPS, payload size) stated in `info.x-*` extensions.
- [ ] Deprecation policy stated for any field/operation marked `deprecated: true`.
- [ ] Spec lints clean (Spectral or equivalent) in CI.
- [ ] Logged in `Traceability_Matrix.md`: API-ID ↔ Requirement-IDs.

## Anti-Patterns

- **RPC-in-REST** (`/createOrder`, `/getOrders`).
- **Status code 200 with `{"success": false}`** in the body — use HTTP status correctly.
- **Schemaless arrays of `object`** — define the item schema.
- **Untyped IDs** (`type: string` with no format and no pattern).
- **Multiple shapes per response code** ("sometimes returns A, sometimes B") — use `oneOf` explicitly.
- **Breaking change disguised as minor** — semver violations break consumer trust irreparably.
