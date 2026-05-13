---
id: KA1
name: Business Analysis Planning and Monitoring
source: BABOK v3 §3
status: SKELETON
purpose: Organize and coordinate the efforts of BAs and stakeholders. Produces the artifacts that govern how BA work itself is done.
baccm_alignment:
  primary: [Stakeholder, Context]
  secondary: [Change, Value]
tasks: [Plan_BA_Approach, Plan_Stakeholder_Engagement, Plan_BA_Governance, Plan_BA_Information_Management, Identify_BA_Performance_Improvements]
---

# KA1 — Business Analysis Planning and Monitoring

## Purpose
Defines the work BAs do to **plan and monitor BA activities themselves**: approach, stakeholder engagement, governance, information management, and continuous improvement.

## Description
This KA is the "meta" KA — every other KA consumes its outputs. The deliverables here set the rules of engagement for the entire BA effort.

## Tasks

### Task 1.1 — Plan Business Analysis Approach
**Purpose.** Define the method of conducting BA activities.
**Inputs.** Needs.
**Elements.** Planning Approach (Predictive/Adaptive); Formality and Level of Detail; BA Activities; Timing of BA Work; Complexity and Risk; Acceptance.
**Outputs.** **Business Analysis Approach**.

### Task 1.2 — Plan Stakeholder Engagement
**Purpose.** Plan how stakeholders will be engaged.
**Inputs.** Business Analysis Approach; Needs.
**Elements.** Perform Stakeholder Analysis; Stakeholder List, Roles, and Responsibilities; Stakeholder Communication Needs; Stakeholder Collaboration; Stakeholder Engagement.
**Outputs.** **Stakeholder Engagement Approach**.

### Task 1.3 — Plan Business Analysis Governance
**Purpose.** Define how decisions about requirements and designs will be made.
**Inputs.** Business Analysis Approach; Stakeholder Engagement Approach.
**Elements.** Decision Making; Change Control Process; Plan Prioritization Approach; Plan for Approvals.
**Outputs.** **Governance Approach**.

### Task 1.4 — Plan Business Analysis Information Management
**Purpose.** Define how BA information (requirements, designs, etc.) will be captured, stored, and integrated.
**Inputs.** Business Analysis Approach; Stakeholder Engagement Approach; Governance Approach.
**Elements.** Organization of BA Information; Level of Abstraction; Plan Traceability Approach; Plan for Requirements Reuse; Storage and Access; Requirements Attributes.
**Outputs.** **Information Management Approach**.

### Task 1.5 — Identify Business Analysis Performance Improvements
**Purpose.** Assess BA work to identify problems and improve effectiveness.
**Inputs.** Business Analysis Approach; Performance Objectives (external).
**Elements.** Performance Analysis; Assessment Measures; Analyze Results; Recommend Actions for Improvement.
**Outputs.** **Business Analysis Performance Assessment**.

## KA1 Input/Output Map (canonical)

| Task | Required Inputs | Outputs |
| ---- | --------------- | ------- |
| 1.1 | Needs | Business Analysis Approach |
| 1.2 | Business Analysis Approach, Needs | Stakeholder Engagement Approach |
| 1.3 | Business Analysis Approach, Stakeholder Engagement Approach | Governance Approach |
| 1.4 | Business Analysis Approach, Stakeholder Engagement Approach, Governance Approach | Information Management Approach |
| 1.5 | Business Analysis Approach, Performance Objectives | Business Analysis Performance Assessment |

## Representative Techniques
Brainstorming; Business Cases; Document Analysis; Estimation; Financial Analysis; Functional Decomposition; Interviews; Item Tracking; Lessons Learned; Metrics and KPIs; Organizational Modelling; Process Modelling; Reviews; Risk Analysis and Management; Roles and Permissions Matrix; Stakeholder List/Map/Personas; Survey or Questionnaire; Workshops.

## Typical Stakeholders
Customer, Domain SME, End User, Implementation SME, Operational Support, Project Manager, Regulator, Sponsor, Supplier, Tester.

## BACCM Linkage
- **Stakeholder** drives Tasks 1.2/1.3.
- **Context** governs Task 1.1 approach selection (predictive vs adaptive).
- **Value** is the implicit lens for Task 1.5 performance improvement.
