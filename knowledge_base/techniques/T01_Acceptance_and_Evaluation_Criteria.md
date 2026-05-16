---
id: T01
name: Acceptance and Evaluation Criteria
source: BABOK v3 §10.01
status: COMPLETE
category: Requirements / Validation
used_by_KAs: [KA5,KA6]
used_by_tasks: [5.3,6.1]
---

# T01 — Acceptance and Evaluation Criteria

## Purpose
Define measurable conditions that a solution must satisfy to be accepted by stakeholders, or to compare and select among solution options.

## Description
Acceptance and Evaluation Criteria are verifiable conditions established before a solution is deployed or assessed. This technique serves two parallel purposes:

- **Acceptance Criteria**: Pass/fail conditions that confirm a solution fulfills its requirements — typically tied to UAT or Definition of Done.
- **Evaluation Criteria**: A scoring framework for comparing multiple solution options, often weighted when a selection decision must be made.

This technique sits at the intersection of Requirements Analysis (deriving criteria from requirements) and Solution Evaluation (applying criteria to assess outcomes).

## Elements (per BABOK v3 §10.01)

1. **Acceptance Criteria** — Minimum, pass/fail conditions that a solution must satisfy to be accepted by stakeholders. Must be measurable and testable.
2. **Evaluation Criteria** — A set of criteria used to compare solution options or assess how well a solution addresses the business need. May be weighted to reflect stakeholder priorities.

## How To Apply

1. Identify which stakeholders will act as acceptors or evaluators of the solution.
2. Trace each requirement to a corresponding criterion — every criterion must link to at least one requirement or business need.
3. Write criteria in measurable form: "System processes ≥ 500 transactions/second under peak load" rather than "system must be fast."
4. When evaluating multiple options: assign weights and construct a weighted scoring matrix.
5. Validate criteria with stakeholders before use — prevent criteria from being "gamed" (met in letter but not in spirit).
6. Store criteria as a versioned artifact, linked to the requirements traceability structure.

## Usage Considerations

### Strengths
- Provides an objective, low-dispute basis for accepting or rejecting a solution.
- Reduces ambiguity around the definition of "done" and "success."
- Supports stakeholder expectation management from the outset.
- Enables comparison of solution options on a consistent scale.

### Limitations
- Difficult to define measurable criteria for qualitative requirements.
- Criteria may become stale if requirements change without parallel updates.
- Weighting negotiation is time-consuming when stakeholders have conflicting interests.

### Anti-patterns
- Vague, non-testable criteria ("user-friendly," "fast," "easy to use").
- Criteria built without stakeholder input — rejected at evaluation time.
- Conflating criteria with requirements — criteria are test conditions, not functional descriptions.
- Criteria set too strict (unreachable) or too loose (no filtering value).

## BACCM Linkage

| Concept | Manifestation |
|---|---|
| **Change** | Criteria define the threshold of change that is sufficient — "how far must this solution change things to be accepted" |
| **Need** | Criteria validate that the need is being addressed, preventing solution drift from the original business need |
| **Solution** | Criteria are the direct measurement instrument for deciding whether a solution is acceptable |
| **Stakeholder** | Criteria must reflect the expectations of the correct stakeholders — BA must not set criteria unilaterally |
| **Value** | Criteria can quantify value: "ROI ≥ 15% within 12 months" |
| **Context** | Criteria must align with regulatory, cultural, and operational context — the same solution in a different context requires different criteria |

## Used By

- **Knowledge Areas:** KA5 (Requirements Analysis and Design Definition), KA6 (Solution Evaluation)
- **Tasks:** 5.3 (Validate Requirements), 6.1 (Measure Solution Performance)

## Related Techniques
- **T17 — Decision Analysis**: apply when evaluation criteria must be combined with risk analysis to select an option.
- **T27 — Functional Decomposition**: trace criteria down to specific functions or components.
- **T32 — Non-functional Requirements Analysis**: primary source of performance, security, and usability criteria.
- **T35 — Prioritization**: determines weights assigned to evaluation criteria.

## Output Template

```
Acceptance/Evaluation Criteria — [Solution/Feature Name]

| ID    | Criterion | Type       | Measurement Method | Threshold  | Weight | Stakeholder Owner | Status |
|-------|-----------|------------|--------------------|------------|--------|-------------------|--------|
| AC-01 | ...       | Acceptance | ...                | Pass/Fail  | N/A    | ...               | Draft  |
| EC-01 | ...       | Evaluation | Weighted Score     | ≥ 7/10     | 30%    | ...               | Draft  |

Notes:
- Traceability: AC-01 → REQ-xxx
- Review date: ...
- Approved by: ...
```
