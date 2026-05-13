---
id: KA3
name: Requirements Life Cycle Management
source: BABOK v3 §5
status: SKELETON
purpose: Manage and maintain requirements and design information from inception to retirement.
baccm_alignment:
  primary: [Change, Solution]
  secondary: [Stakeholder, Value]
tasks: [Trace_Requirements, Maintain_Requirements, Prioritize_Requirements, Assess_Requirements_Changes, Approve_Requirements]
---

# KA3 — Requirements Life Cycle Management

## Purpose
Govern requirements and designs **across their entire life cycle** — from initial elicitation through retirement — preserving traceability, integrity, and approval status.

## Description
This KA does **not** decide *what* the requirements should be (that is KA4 and KA5). It decides how requirements and designs are *organized, prioritized, changed, and approved* over time.

## Tasks

### Task 3.1 — Trace Requirements
**Purpose.** Create and maintain relationships between requirements, designs, solution components, and other artifacts.
**Inputs.** Requirements; Designs.
**Elements.** Level of Formality; Relationships (Derive, Depends On — Necessity/Effort, Satisfy, Validate); Traceability Repository.
**Outputs.** **Requirements (traced)**; **Designs (traced)**.

### Task 3.2 — Maintain Requirements
**Purpose.** Retain accuracy and consistency of requirements and designs over time, support reuse.
**Inputs.** Requirements; Designs.
**Elements.** Maintain Requirements; Maintain Attributes; Reusing Requirements.
**Outputs.** **Requirements (maintained and reusable)**; **Designs (maintained and reusable)**.

### Task 3.3 — Prioritize Requirements
**Purpose.** Rank requirements in the order most appropriate to the stakeholders.
**Inputs.** Requirements; Designs; Business Analysis Approach; Governance Approach.
**Elements.** Basis for Prioritization (Benefit, Penalty, Cost, Risk, Dependencies, Time Sensitivity, Stability, Regulatory/Policy Compliance); Challenges of Prioritization; Continual Prioritization.
**Outputs.** **Requirements (prioritized)**; **Designs (prioritized)**.

### Task 3.4 — Assess Requirements Changes
**Purpose.** Evaluate proposed changes to requirements and designs.
**Inputs.** Proposed Change; Requirements; Designs.
**Elements.** Assessment Formality; Impact Analysis (Benefit, Cost, Impact, Schedule, Urgency); Impact Resolution.
**Outputs.** **Requirements Change Assessment**; **Designs Change Assessment**.

### Task 3.5 — Approve Requirements
**Purpose.** Obtain agreement on and approval of requirements and designs.
**Inputs.** Requirements (verified); Designs.
**Elements.** Understand Stakeholder Roles; Conflict and Issue Management; Gain Consensus; Track and Communicate Approval.
**Outputs.** **Requirements (approved)**; **Designs (approved)**.

## KA3 Input/Output Map (canonical)

| Task | Required Inputs | Outputs |
| ---- | --------------- | ------- |
| 3.1 | Requirements, Designs | Requirements (traced), Designs (traced) |
| 3.2 | Requirements, Designs | Requirements (maintained), Designs (maintained) |
| 3.3 | Requirements, Designs, BA Approach, Governance Approach | Requirements (prioritized), Designs (prioritized) |
| 3.4 | Proposed Change, Requirements, Designs | Requirements Change Assessment, Designs Change Assessment |
| 3.5 | Requirements (verified), Designs | Requirements (approved), Designs (approved) |

## Representative Techniques
Business Cases; Business Rules Analysis; Decision Analysis; Document Analysis; Estimation; Financial Analysis; Interface Analysis; Interviews; Item Tracking; Reviews; Risk Analysis and Management; Workshops; Prioritization (informally); Backlog Management.

## Typical Stakeholders
Customer, Domain SME, End User, Implementation SME, Operational Support, Project Manager, Regulator, Sponsor, Tester.

## BACCM Linkage
- **Change** is governed by Task 3.4 (assessment) and 3.5 (approval).
- **Solution** integrity is preserved by Task 3.1 (trace) and 3.2 (maintain).
- **Value** drives Task 3.3 prioritization.
