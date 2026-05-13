---
name: Agile User Stories Standard
type: execution_engine
consumes: KA5 outputs (Requirements specified/modeled, Designs)
produces: Dev-ready user stories in the team backlog
authority: BABOK v3 §10.48 (User Stories) + INVEST + Definition of Ready
---

# Agile User Stories Standard

This standard governs **every** user story produced or accepted by this ITBA flow.
Stories that fail the checks below are returned to KA5 for refinement; they are
**not** allowed into the team backlog.

## Canonical Story Form

```
As a   <persona — a specific stakeholder type from the Stakeholder List>
I want <a capability — observable from the persona's perspective>
So that <a value statement — measurable, linked to a Business Objective>
```

Reject:
- Personas like "user", "admin", "the system" — these are role placeholders, not personas.
- "So that we can…" — value must accrue to the **persona**, not the team.
- Implementation verbs in "I want…" ("I want a Kafka queue") — describe the capability, not the technology.

## INVEST Quality Gate

| Letter | Criterion       | What to check                                                                                  |
| ------ | --------------- | ---------------------------------------------------------------------------------------------- |
| **I**  | Independent     | Story can be sequenced without depending on another story landing in the same sprint.          |
| **N**  | Negotiable      | Scope is open to refinement; story is not a fixed-shape spec.                                   |
| **V**  | Valuable        | Value statement maps to a specific Business Objective (KA4 Task 4.2).                          |
| **E**  | Estimable       | Team can estimate within ±50% confidence; otherwise spike first.                                |
| **S**  | Small           | Fits comfortably in one sprint; > ~8 story points → split.                                      |
| **T**  | Testable        | Acceptance criteria are objectively verifiable.                                                 |

## Acceptance Criteria (Gherkin-preferred)

Every story carries **explicit, testable** acceptance criteria. Default form:

```
Scenario: <one observable outcome>
  Given <precondition / state>
  When  <event / action>
  Then  <observable result>
```

Rules:
- **Minimum 1, typical 3–6 scenarios per story.** Below 1: story is not testable. Above ~8: story is too big.
- Include at least one **negative path** (what should *not* happen, error case, boundary).
- Reference data should be named, not numeric magic ("for a customer with tier=GOLD" not "for customer ID 42").
- NFRs that constrain the scenario (latency, accessibility) are stated explicitly, not assumed.

## Definition of Ready (DoR)

A story may enter sprint planning only when **all** of the following are true:

- [ ] Persona is a named entry in `working_session/Context_Registry.md`.
- [ ] Story value links to a Business Objective ID from KA4 Task 4.2.
- [ ] Acceptance criteria meet the Gherkin rules above.
- [ ] Dependencies are explicit and either (a) already met or (b) scheduled to land first.
- [ ] NFRs are listed or stated as N/A with reason.
- [ ] Affected interfaces have a draft entry in the API spec (see `API_Specification_Standard.md`).
- [ ] Tracked into `working_session/Traceability_Matrix.md`: Need → Story.

## Definition of Done (DoD)

A story is closed only when:

- [ ] All acceptance scenarios are automated (or formally waived with reason).
- [ ] Code passes CI; no new lint or test regressions.
- [ ] Observability hooks (logs, metrics, traces) exist where DoR specified.
- [ ] Documentation updated (runbook, API spec, glossary).
- [ ] Demo'd to the persona's representative; sign-off recorded.
- [ ] Solution Performance Measures (KA6 Task 6.1) updated if the story moves a tracked metric.

## Splitting Heuristics

When a story violates **S** (too large):

| Pattern        | Apply                                                            |
| -------------- | ---------------------------------------------------------------- |
| Workflow       | Split by step in the user's flow.                                |
| Data variation | Split by data class (one tier first, others next).               |
| CRUD           | Split by verb (read first, then write).                          |
| Interface      | Split by surface (API first, then UI).                           |
| Happy/Edge     | Split happy path from edge cases.                                |
| Defer NFR      | Split functional acceptance from NFR hardening (with risk note). |

## Anti-Patterns

- **Solution-as-story.** "As a developer, I want a Redis cache…" — that is a task, not a story.
- **No persona.** Stories owned by no one in the Stakeholder List are speculative.
- **Implicit dependencies.** "Depends on the platform team" without a named ticket is a future blocker.
- **Acceptance = checklist of UI elements.** AC is about *observable behavior*, not visual layout.
- **NFRs stuffed into one mega-story.** NFRs are first-class and split out.

## Traceability Contract

Every story carries these tags, mirrored in `working_session/Traceability_Matrix.md`:

```
Story-ID:        US-####
Need-ID:         NEED-####
Business-Obj-ID: BO-####
Requirement-ID:  REQ-####
Design-ID:       DES-#### (if applicable)
API-Endpoint-ID: API-####  (if applicable)
```

This is non-optional: a story without these tags is **not** dev-ready.
