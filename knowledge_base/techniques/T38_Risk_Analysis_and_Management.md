---
id: T38
name: Risk Analysis and Management
source: BABOK v3 §10.38
status: FULLY_POPULATED
category: Strategy / Risk
used_by_KAs: [KA1, KA3, KA4, KA6]
used_by_tasks: [4.1_Analyze_Current_State, 4.2_Define_Future_State, 4.3_Assess_Risks, 4.4_Define_Change_Strategy, 1.5_Identify_Performance_Improvements]
---

# T38 — Risk Analysis and Management

## Purpose
Identify uncertainties that could affect value delivery, **analyze** their
likelihood and impact, and **plan and execute a response** consistent with the
organization's risk tolerance.

## Description
"Risk" is uncertainty that matters. The technique handles both **threats**
(uncertainties with negative consequences) and **opportunities** (uncertainties
with positive consequences). The output is **not a list of risks** — it is a
posture: which risks are accepted, which are mitigated, and at what cost.

## Elements

### 1. Risk Identification
Sources: stakeholder elicitation, document review, expert judgement,
lessons learned, SWOT (Threats column), assumption analysis, dependency
mapping. Each risk is written as a *cause → uncertain event → consequence*
sentence ("Because we depend on a single vendor for X, if the vendor delays
release, then go-live slips by 6 weeks").

### 2. Analysis
For each identified risk:
- **Probability** (numerical or categorical: VL/L/M/H/VH).
- **Impact** in *named units* — financial, schedule, reputation, regulatory.
- **Exposure** = Probability × Impact (or qualitative matrix lookup).
- **Velocity / proximity** — how fast does the impact materialize?
- **Owner** — a *named person*, not a team.

### 3. Evaluation
Compare exposure to **risk tolerance** (must be set explicitly before evaluation).
Tolerance has three regions:
- **Acceptable** — no action required; monitor.
- **Tolerable with treatment** — must respond.
- **Unacceptable** — must escalate or refuse the change.

### 4. Treatment (Response Strategies)
For threats:
- **Avoid** — change the plan to remove the risk source.
- **Transfer** — shift consequence to another party (insurance, contract clause).
- **Mitigate** — reduce probability or impact.
- **Accept** — actively choose to bear the risk; budget a contingency.

For opportunities:
- **Exploit** — make it certain.
- **Enhance** — increase probability or impact.
- **Share** — partner to capture jointly.
- **Accept** — take the upside if it occurs.

### 5. Monitoring
Each risk has a **trigger condition** (an observable signal) and a **review cadence**.
Without these, the risk register is dead weight.

## How To Apply (procedure)

1. **Set tolerance first.** Document acceptable/tolerable/unacceptable thresholds with the Sponsor.
2. **Identify** broadly — quantity beats quality at this step. Use Brainstorming, SWOT, Lessons Learned, Document Analysis, Interviews.
3. **Deduplicate and merge** — group risks that share a cause.
4. **Analyze** each merged risk for P, I, exposure, velocity, owner.
5. **Plot** on a 5×5 (or 3×3) matrix; isolate top quartile.
6. **Decide response** per risk; cost the response; net the cost against the exposure reduction.
7. **Bake responses into the plan** — a response not in the schedule/budget will not happen.
8. **Set triggers and cadence**; assign monitors.
9. **Re-run** at every state change (new requirement, new vendor, scope shift).

## Usage Considerations

### Strengths
- Forces explicit treatment of uncertainty that teams otherwise discuss verbally and forget.
- Creates auditable accountability via named owners and triggers.
- Surfaces hidden assumptions (every risk implies an assumption that *could* fail).

### Limitations
- **GIGO.** Probability estimates are often opinion; calibrate where possible (reference-class forecasting, historical base rates).
- **Cognitive bias.** Recency bias inflates last quarter's incident; availability bias suppresses rare-but-catastrophic risks.
- **Matrix overconfidence.** 5×5 grids hide the difference between "low-probability/high-impact survivable" and "low-probability/extinction-event".
- **Static register.** Without scheduled review, the register decays. Always set cadence.

### Anti-patterns
- A risk register with no **owner** column.
- All risks at exposure level "Medium" (the register has not done its job).
- "Mitigate" used as default with no plan attached.
- Risk = Issue. *Risk* is uncertain; an *issue* has already materialized — track separately.

## BACCM Linkage

| Concept     | How risk analysis manifests it                                |
| ----------- | ------------------------------------------------------------- |
| Change      | Risk is largely a property of *the change* itself.            |
| Need        | Some risks are the risk of *not* changing — model these too.  |
| Solution    | Each solution option has a distinct risk profile.             |
| Stakeholder | Tolerance is a stakeholder property; ownership is a stakeholder assignment. |
| Value       | Risk is the volatility of expected value.                     |
| Context     | Context shifts (regulatory, market) can invalidate analysis.  |

## Output Template

```
Risk Register — [scope] — v[##] — [date]
Tolerance thresholds: acceptable < X | tolerable < Y | escalate > Y

| ID | Cause → Event → Consequence | P | I | Exposure | Velocity | Owner | Response (Avoid/Transfer/Mitigate/Accept) | Cost of response | Trigger | Review cadence | Status |
|----|------------------------------|---|---|----------|----------|-------|-------------------------------------------|------------------|---------|----------------|--------|
| R1 |                              |   |   |          |          |       |                                           |                  |         |                |        |

Top-quartile risks: R#, R#, R#  →  feed into Business Case (T07).
```

## Related Techniques
Brainstorming (T05); SWOT Analysis (T46); Lessons Learned (T27);
Decision Analysis (T16); Financial Analysis (T20); Business Cases (T07);
Root Cause Analysis (T40); Document Analysis (T18); Interviews (T25);
Workshops (T50); Estimation (T19); Mind Mapping (T29).
