---
id: KA6
name: Solution Evaluation
source: BABOK v3 §8
status: SKELETON
purpose: Assess the performance of and value delivered by a solution, and recommend removal of barriers or constraints preventing the full realization of value.
baccm_alignment:
  primary: [Solution, Value]
  secondary: [Stakeholder, Change]
tasks: [Measure_Solution_Performance, Analyze_Performance_Measures, Assess_Solution_Limitations, Assess_Enterprise_Limitations, Recommend_Actions_to_Increase_Solution_Value]
---

# KA6 — Solution Evaluation

## Purpose
Determine whether a proposed, in-progress, or implemented solution is **delivering the value** it was supposed to, identify barriers, and recommend remediation.

## Description
Evaluation is performed **at any stage** — proposed (pre-build), partial (in-build), or live (post-deploy). It closes the loop with KA4 by comparing realized value to potential value.

## Tasks

### Task 6.1 — Measure Solution Performance
**Purpose.** Determine the most appropriate way to assess solution performance.
**Inputs.** Business Objectives; Implemented (or Constructed) Solution.
**Elements.** Define Solution Performance Measures; Validate Performance Measures; Collect Performance Measures.
**Outputs.** **Solution Performance Measures**.

### Task 6.2 — Analyze Performance Measures
**Purpose.** Provide insights into the performance of the solution against its expected value.
**Inputs.** Solution Performance Measures.
**Elements.** Solution Performance versus Desired Value; Risks; Trends; Performance Variances.
**Outputs.** **Solution Performance Analysis**.

### Task 6.3 — Assess Solution Limitations
**Purpose.** Determine factors internal to the solution that restrict full value realization.
**Inputs.** Implemented (or Constructed) Solution; Solution Performance Analysis.
**Elements.** Identify Internal Solution Component Dependencies; Investigate Solution Problems; Impact Assessment.
**Outputs.** **Solution Limitations**.

### Task 6.4 — Assess Enterprise Limitations
**Purpose.** Determine factors external to the solution (in the enterprise) that restrict full value realization.
**Inputs.** Current State Description; Solution Performance Analysis.
**Elements.** Enterprise Culture Assessment; Stakeholder Impact Analysis; Organizational Structure Changes; Operational Assessment.
**Outputs.** **Enterprise Limitations**.

### Task 6.5 — Recommend Actions to Increase Solution Value
**Purpose.** Recommend actions to remove barriers and increase value delivered.
**Inputs.** Enterprise Limitations; Solution Limitations.
**Elements.** Adjust Solution Performance Measures; Recommended Actions (Do Nothing, Organizational Change, Reduce Complexity, Identify Additional Capabilities, Retire the Solution).
**Outputs.** **Recommended Actions**.

## KA6 Input/Output Map (canonical)

| Task | Required Inputs | Outputs |
| ---- | --------------- | ------- |
| 6.1 | Business Objectives, Implemented/Constructed Solution | Solution Performance Measures |
| 6.2 | Solution Performance Measures | Solution Performance Analysis |
| 6.3 | Implemented/Constructed Solution, Solution Performance Analysis | Solution Limitations |
| 6.4 | Current State Description, Solution Performance Analysis | Enterprise Limitations |
| 6.5 | Enterprise Limitations, Solution Limitations | Recommended Actions |

## Representative Techniques
Acceptance and Evaluation Criteria; Benchmarking and Market Analysis; Business Cases; Data Mining; Decision Analysis; Financial Analysis; Focus Groups; Interviews; Item Tracking; Lessons Learned; Metrics and KPIs; Observation; Organizational Modelling; Process Analysis; Prototyping; Risk Analysis and Management; Root Cause Analysis; Survey or Questionnaire; SWOT Analysis; Vendor Assessment.

## Typical Stakeholders
Customer, Domain SME, End User, Implementation SME, Operational Support, Project Manager, Regulator, Sponsor, Supplier, Tester.

## BACCM Linkage
- **Value** is the conserved quantity being measured.
- **Solution** performance is the immediate object of evaluation.
- **Change** is the corrective output (Recommended Actions).
