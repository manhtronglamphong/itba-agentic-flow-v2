---
id: T07
name: Business Cases
source: BABOK v3 §10.7
status: FULLY_POPULATED
category: Strategy / Decision support
used_by_KAs: [KA1, KA3, KA4, KA6]
used_by_tasks: [4.1_Analyze_Current_State, 4.2_Define_Future_State, 4.3_Assess_Risks, 4.4_Define_Change_Strategy, 3.4_Assess_Requirements_Changes, 6.5_Recommend_Actions]
---

# T07 — Business Cases

## Purpose
A Business Case captures the **justification** for a proposed change. It
provides the basis for an *investment decision*: it sets out the need, the
options considered, the recommended option, the expected value, the cost,
and the risk — in a form that an accountable decision-maker can sign.

## Description
The Business Case is a **living document**, not a one-time pitch. It is
created in Task 4.4, but is referenced — and revised — throughout the change.
KA3 (Approve Requirements / Assess Requirements Changes) and KA6 (Recommend
Actions) both consult it.

A Business Case answers, in order:

1. *What problem or opportunity exists?* → **Business Need**
2. *What is the desired result?* → **Business Objectives** (measurable)
3. *What options have been considered?* → **Alternatives** (incl. "do nothing")
4. *Which option is recommended, and why?* → **Recommendation**
5. *What will it cost and deliver?* → **Cost / Benefit / Net value**
6. *What could go wrong?* → **Risks**
7. *How will success be measured after the fact?* → **Evaluation criteria**

## Elements

### 1. Need Assessment
- The business need stated in *problem* terms, not solution terms.
- Quantified pain (cost, lost revenue, risk exposure, NPS, churn, cycle time).
- Stakeholders affected and their value at stake.

### 2. Desired Outcomes
- Business Objectives: SMART (Specific, Measurable, Achievable, Relevant, Time-bound).
- Linked to enterprise-level Organizational Strategy.

### 3. Alternatives (mandatory plural)
- "Do nothing" is **always** option 0. If it is not modeled, the case is incomplete.
- 2–4 viable alternatives, each described with scope, cost envelope, and value envelope.
- Comparative criteria stated up front (avoid post-hoc criteria-shopping).

### 4. Recommendation
- The chosen alternative, with the explicit **reason** the others were rejected.
- Sensitivity statement: what would have to be true for the recommendation to flip?

### 5. Assessment of Results
- The measurable signals that will be collected post-implementation (links to KA6).
- The decision rule for "succeeded / partially succeeded / failed".

## How To Apply (procedure)

1. Confirm the **Business Need** with the Sponsor; do not write a case for a need that has not been validated.
2. Run **Financial Analysis** (T20) on each alternative — NPV, IRR, payback, TCO.
3. Run **Risk Analysis and Management** (T38) on each alternative — risk-adjust the value.
4. Run **Decision Analysis** (T16) on the alternative set — make the comparison explicit.
5. Draft, **circulate to dissenting stakeholders**, and revise. A Business Case that has not been actively challenged is unfinished.
6. Have the Sponsor sign. Store as a baseline in `working_session/Traceability_Matrix.md`.
7. **Reopen** the case whenever a material change request hits Task 3.4.

## Usage Considerations

### Strengths
- Forces disciplined thinking about alternatives — closes the "we already decided" loophole.
- Creates an accountable artifact for sponsor sign-off and audit trail.
- Anchors KA6 evaluation in pre-stated criteria, preventing goalpost-moving.

### Limitations
- **Theatre risk.** A retrofit case written to defend a chosen solution adds no value.
- **Precision illusion.** Financial models can mask the size of underlying assumptions.
- **Time horizon.** Long-horizon NPVs are sensitive to discount rate; show sensitivity ranges.
- **Single-currency view.** Some value (compliance, brand, talent) is hard to monetize; do not omit it — annotate it.

### Anti-patterns
- A Business Case with one option.
- A Business Case with no cited risks.
- A Business Case that has never been revised.
- A Business Case whose recommendation does not match its own scoring.

## BACCM Linkage

| Concept     | What the Business Case supplies                          |
| ----------- | -------------------------------------------------------- |
| Need        | The case **starts** from the Need; without it, no case.  |
| Value       | The case **monetizes/quantifies** value per alternative. |
| Solution    | Each alternative is a candidate solution boundary.       |
| Change      | The recommendation defines the *direction* of change.    |
| Context     | Assumptions about the context are explicitly listed.     |
| Stakeholder | Sponsor signs; impacted stakeholders are listed.         |

## Output Template

```
Business Case — [scope] — v[##] — [date] — sponsor: [name]

1. Business Need (problem statement, quantified)
2. Business Objectives (SMART)
3. Alternatives
   0. Do Nothing — cost, value, risk
   1. [Option A]   — cost, value, risk
   2. [Option B]   — cost, value, risk
4. Comparative Analysis (table)
5. Recommendation + rationale + sensitivity statement
6. Risks (top 5 with response strategies)
7. Assumptions (with shelf-life)
8. Success Criteria (measured by KA6)
9. Approvals
```

## Related Techniques
Financial Analysis (T20); Decision Analysis (T16); Risk Analysis and Management (T38);
SWOT Analysis (T46); Estimation (T19); Benchmarking and Market Analysis (T04);
Metrics and KPIs (T28); Vendor Assessment (T49).
