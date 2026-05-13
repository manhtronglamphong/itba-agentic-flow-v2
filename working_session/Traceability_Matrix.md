---
name: Traceability Matrix — Business Need → Technical Spec
type: working_session
purpose: Single source of truth linking every artifact in the engagement, from Business Need down to API endpoint and test case.
update_rule: Every artifact created in any KA must be logged here within the same turn it is produced. Untraceable artifacts are treated as defects.
relationships_modeled: [Derives, DependsOn, Satisfies, Validates]
---

# Traceability Matrix

> An artifact that is not in this matrix **does not exist** from a governance
> perspective. KA3 Task 3.1 (Trace Requirements) is enforced here.

## ID Conventions

| Prefix | Artifact                  | Owning KA      |
| ------ | ------------------------- | -------------- |
| NEED-  | Business Need             | KA4 (4.1)      |
| BO-    | Business Objective        | KA4 (4.2)      |
| RISK-  | Identified Risk           | KA4 (4.3)      |
| CHG-   | Change Strategy entry     | KA4 (4.4)      |
| STK-   | Stakeholder               | KA1 (1.2)      |
| REQ-   | Requirement (any state)   | KA5 (5.1)      |
| DES-   | Design                    | KA5 (5.1/5.5)  |
| DGM-   | UML / Model Diagram       | KA5            |
| US-    | User Story                | KA5 → backlog  |
| API-   | API endpoint / event      | execution_engine |
| TST-   | Test case                 | KA5 (5.3)      |
| METRIC- | Solution Performance Measure | KA6 (6.1)  |

IDs are **never reused** even after retirement.

## Primary Trace (Down)

| Need-ID | Business Objective | Requirement | Design / Model | Story | API / Event | Test | Metric (KA6) |
| ------- | ------------------ | ----------- | -------------- | ----- | ----------- | ---- | ------------ |
|         |                    |             |                |       |             |      |              |

> Every Need-ID must trace to at least one Business Objective and at least one Metric.
> Rows where any required column is empty are flagged in the **Gaps** section.

## Reverse Trace (Up)

| Story-ID | Requirement | Need | Business Objective | Sponsor sign-off |
| -------- | ----------- | ---- | ------------------ | ---------------- |
|          |             |      |                    |                  |

> Run this view before every sprint planning: any Story-ID that does not trace
> up to a signed Business Objective is **not ready** (violates the Agile User
> Stories Standard, Definition of Ready).

## Relationship Log

| Relationship   | From-ID | To-ID | Rationale (1 line)                  | Date       |
| -------------- | ------- | ----- | ----------------------------------- | ---------- |
| Derives-from   |         |       |                                     |            |
| Depends-on     |         |       |                                     |            |
| Satisfies      |         |       |                                     |            |
| Validates      |         |       |                                     |            |

Relationship vocabulary is fixed (BABOK v3 §5.1):

- **Derive** — a requirement is *derived from* another requirement (typically a lower-level requirement from a higher-level one).
- **Depend-on (Necessity)** — A is implementable only if B is.
- **Depend-on (Effort)** — A is easier if B is done first; not a hard block.
- **Satisfy** — a design/component/test *satisfies* a requirement.
- **Validate** — a test/measure *validates* a requirement or design.

## Approval Trail

| Artifact-ID | Approver (Stakeholder-ID) | Date       | Version | Notes |
| ----------- | ------------------------- | ---------- | ------- | ----- |
|             |                           |            |         |       |

## Gaps (auto-generated checklist — review every iteration)

- [ ] Needs without a Business Objective
- [ ] Business Objectives without a Metric
- [ ] Requirements without an upstream Need
- [ ] Designs without a downstream Test
- [ ] Stories without an API or UI surface mapped
- [ ] APIs without a Requirement
- [ ] Metrics without a baseline value captured
- [ ] Approved artifacts older than 90 days without re-validation

## Change Log (append-only)

| Date       | Action            | IDs touched | Author       |
| ---------- | ----------------- | ----------- | ------------ |
| 2026-05-13 | Matrix initialized| —           | Senior ITBA  |
