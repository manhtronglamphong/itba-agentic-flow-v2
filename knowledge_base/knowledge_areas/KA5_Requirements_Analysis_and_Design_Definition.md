---
id: KA5
name: Requirements Analysis and Design Definition
source: BABOK v3 §7
status: SKELETON
purpose: Structure and refine elicited information into requirements and designs that represent the solution.
baccm_alignment:
  primary: [Solution, Need]
  secondary: [Value, Context]
tasks: [Specify_and_Model_Requirements, Verify_Requirements, Validate_Requirements, Define_Requirements_Architecture, Define_Design_Options, Analyze_Potential_Value_and_Recommend_Solution]
---

# KA5 — Requirements Analysis and Design Definition (RADD)

## Purpose
Organize and structure information discovered during elicitation; **specify and model requirements and designs**; validate and verify them; identify solution options; and recommend the option that best delivers value.

## Description
RADD is iterative and progressive. It turns stakeholder needs into a *coherent, verifiable, value-justified specification* — bridging KA4 (problem) and KA6 (built solution).

## Tasks

### Task 5.1 — Specify and Model Requirements
**Purpose.** Analyze, synthesize, and refine elicitation results into requirements and designs.
**Inputs.** Elicitation Results (any state).
**Elements.** Model Requirements; Analyze Requirements; Represent Requirements and Attributes; Implement the Appropriate Levels of Abstraction.
**Outputs.** **Requirements (specified and modeled)**; **Designs (specified and modeled)**.

### Task 5.2 — Verify Requirements
**Purpose.** Ensure requirements and designs are of sufficient quality.
**Inputs.** Requirements; Designs.
**Elements.** Characteristics of Requirements and Designs Quality; Verification Activities; Checklists.
**Outputs.** **Requirements (verified)**; **Designs (verified)**.

### Task 5.3 — Validate Requirements
**Purpose.** Ensure requirements and designs deliver the expected business value and align with goals.
**Inputs.** Requirements; Designs.
**Elements.** Identify Assumptions; Define Measurable Evaluation Criteria; Evaluate Alignment with Solution Scope.
**Outputs.** **Requirements (validated)**; **Designs (validated)**.

### Task 5.4 — Define Requirements Architecture
**Purpose.** Synthesize requirements into an architecture that supports the overall solution.
**Inputs.** Requirements (any state); Solution Scope; Information Management Approach.
**Elements.** Requirements Viewpoints and Views; Template Architectures; Completeness; Relate and Verify Requirements Relationships.
**Outputs.** **Requirements Architecture**.

### Task 5.5 — Define Design Options
**Purpose.** Identify and develop alternative design approaches that meet business needs.
**Inputs.** Change Strategy; Requirements (validated); Requirements Architecture.
**Elements.** Define Solution Approaches; Identify Improvement Opportunities; Requirements Allocation; Describe Design Options.
**Outputs.** **Design Options**.

### Task 5.6 — Analyze Potential Value and Recommend Solution
**Purpose.** Estimate the value delivered by each design option and recommend the one that delivers the greatest overall value.
**Inputs.** Potential Value; Design Options.
**Elements.** Expected Benefits; Expected Costs; Determine Value; Assess Design Options and Recommend Solution.
**Outputs.** **Solution Recommendation**.

## KA5 Input/Output Map (canonical)

| Task | Required Inputs | Outputs |
| ---- | --------------- | ------- |
| 5.1 | Elicitation Results | Requirements (specified/modeled), Designs (specified/modeled) |
| 5.2 | Requirements, Designs | Requirements (verified), Designs (verified) |
| 5.3 | Requirements, Designs | Requirements (validated), Designs (validated) |
| 5.4 | Requirements, Solution Scope, Information Management Approach | Requirements Architecture |
| 5.5 | Change Strategy, Requirements (validated), Requirements Architecture | Design Options |
| 5.6 | Potential Value, Design Options | Solution Recommendation |

## Representative Techniques
Acceptance and Evaluation Criteria; Business Rules Analysis; Concept Modelling; Data Dictionary; Data Flow Diagrams; Data Modelling; Decision Modelling; Functional Decomposition; Glossary; Interface Analysis; Non-Functional Requirements Analysis; Process Modelling; Prototyping; Roles and Permissions Matrix; Scope Modelling; Sequence Diagrams; State Modelling; Use Cases and Scenarios; User Stories; Reviews.

## Typical Stakeholders
Customer, Domain SME, End User, Implementation SME, Operational Support, Project Manager, Regulator, Sponsor, Supplier, Tester.

## BACCM Linkage
- **Solution** is the principal output.
- **Need** is the conserved invariant — every requirement must trace back to one.
- **Value** governs Task 5.6 recommendation.
