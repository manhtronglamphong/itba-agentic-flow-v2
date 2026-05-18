---
id: T03
name: Balanced Scorecard
source: BABOK v3 §10.03
status: COMPLETE
category: Strategy / Measurement
used_by_KAs: [KA4]
used_by_tasks: [4.2, 4.4]
version: 1.0
last_updated: 2026-05-18
updated_by: phong.manh
changelog:
  - version: 1.0
    date: 2026-05-18
    author: phong.manh
    note: Initial population from SKELETON — all sections completed per BABOK v3 §10.03
---

# T03 — Balanced Scorecard

## Purpose
Translate an organization's vision and strategy into a set of performance measures across four perspectives so that business analysts can assess current state, define success metrics for a future state, and validate whether a proposed change delivers strategic value.

## Description
The Balanced Scorecard (BSC) — developed by Kaplan and Norton — is a strategic performance management framework that complements lagging financial indicators with leading non-financial measures across **Customer**, **Internal Process**, and **Learning & Growth** perspectives. In BABOK v3, BAs use it primarily during Strategy Analysis to bridge high-level organizational goals with measurable outcomes, providing a shared language for stakeholders across all levels of the organization.

The BSC is not merely a measurement dashboard. Its core mechanism is a **Strategy Map** — a causal chain that makes explicit how improvements in learning and growth capabilities drive better processes, which drive customer outcomes, which ultimately produce financial results.

## Elements

**1. Financial Perspective**
- Answers: *How do we look to shareholders/sponsors?*
- Typical measures: Revenue growth, cost reduction, ROI, EVA, profit margin
- BA relevance: Baseline financial KPIs used to justify or reject a proposed change

**2. Customer Perspective**
- Answers: *How do customers perceive us?*
- Typical measures: Customer satisfaction index, NPS, retention rate, market share, on-time delivery
- BA relevance: Maps customer needs to solution value propositions

**3. Internal Process Perspective**
- Answers: *What processes must we excel at?*
- Sub-domains (Kaplan & Norton, cited in BABOK v3): Innovation processes, customer management processes, operational processes, regulatory/environmental processes
- BA relevance: Identifies process changes and solution capabilities required to meet customer and financial targets

**4. Learning & Growth Perspective**
- Answers: *Can we sustain our ability to change and improve?*
- Dimensions: Human capital (skills, training), Information capital (systems, data), Organizational capital (culture, leadership, alignment)
- BA relevance: Identifies capability gaps and organizational readiness factors

**5. Strategy Map**
- Visual causal diagram linking objectives across all four perspectives (bottom-up: Learning → Process → Customer → Financial)
- Key BA deliverable; exposes hidden assumptions about how change produces value

**6. Objectives**
- Specific strategic goals assigned to each perspective (typically 3–5 per perspective)

**7. Measures (KPIs)**
- Quantifiable indicators tied to each objective; distinguish *lagging* (outcome) from *leading* (driver) indicators

**8. Targets**
- Numeric thresholds defining success within a defined time horizon

**9. Initiatives**
- Programs, projects, or changes required to close the gap between current and target performance; this is the primary linkage to BA work

## How To Apply (procedure)

1. **Obtain or clarify organizational strategy** — Identify the vision, mission, and strategic themes. Source: Stakeholder interviews, existing strategy documents, enterprise architecture artifacts.
2. **Map objectives to the four perspectives** — Work with strategy-level stakeholders to articulate 3–5 objectives per perspective.
3. **Build the Strategy Map** — Draw cause-and-effect links upward through perspectives; validate logic with stakeholders. Gaps in the causal chain reveal missing capabilities or unstated assumptions.
4. **Define measures and targets** — For each objective, identify at least one leading and one lagging KPI; negotiate baseline (current state) and target (future state) values.
5. **Identify initiatives (change portfolio)** — Map in-flight and proposed projects/changes to the objectives they support. Surface conflicts and gaps.
6. **Use the BSC to validate solution options** — During Define Change Strategy (Task 4.4), score solution alternatives against each perspective to assess strategic fit.
7. **Cascade and monitor** — Align BSC with operating-level metrics; review on a defined cadence to track solution performance post-implementation.

## Usage Considerations

### Strengths
- Provides a single framework linking strategy, operations, and measurement — reduces misalignment between BA findings and executive priorities
- Forces explicit articulation of causal assumptions between perspectives, exposing analytical gaps early
- Distinguishes leading indicators (actionable) from lagging indicators (confirming), enabling proactive intervention
- Widely recognized by senior stakeholders; lowers communication friction when presenting findings

### Limitations
- Requires significant stakeholder access and time commitment to build correctly; often resisted in organizations with weak strategic planning culture
- The four-perspective model may not fit all contexts (e.g., non-profits may need a "mission/beneficiary" perspective; regulated industries may need compliance as a fifth perspective)
- Cause-and-effect assumptions in the Strategy Map are hypotheses, not guarantees — must be validated over time with data
- Risk of metric proliferation: when every business unit adds measures, the scorecard loses focus

### Anti-patterns
- Using BSC only as a reporting tool (filling in numbers) without a Strategy Map — loses the causal reasoning value
- Treating all four perspectives as equally weighted; financial and customer perspectives typically dominate for commercial organizations
- Setting targets without baselines — makes current-state assessment (Task 4.2) impossible to execute objectively
- Cascading the BSC without stakeholder ownership of each objective — metrics without accountable owners stagnate

## BACCM Linkage

| Concept | Manifestation |
| ----------- | ------------- |
| **Change** | Initiatives column maps directly to the change portfolio; BSC tracks whether a change produces its intended strategic outcomes |
| **Need** | Objectives within each perspective formalize organizational needs at the strategic level |
| **Solution** | Solutions are evaluated by how well they close the gap between current measures and targets |
| **Stakeholder** | Customer and Financial perspectives represent primary external stakeholders; Internal Process and L&G represent internal stakeholders |
| **Value** | The primary instrument for defining and measuring value delivery across financial and non-financial dimensions |
| **Context** | The choice of perspectives, measures, and targets reflects competitive, regulatory, and cultural context |

## Used By

- **Knowledge Areas:** KA4 — Strategy Analysis
- **Tasks:**
  - **4.2 Assess Current State** — Use existing BSC (or build a baseline BSC) to quantify current performance gaps
  - **4.4 Define Change Strategy** — Use BSC targets to specify measurable success criteria for proposed changes; compare solution options against each perspective

## Related Techniques
- **T02 Backlog Management** — Initiatives identified in the BSC feed directly into the strategic backlog
- **T08 Business Cases** — BSC measures form the benefit realization section of a business case
- **T12 Decision Analysis** — BSC perspectives can serve as evaluation criteria when scoring solution alternatives
- **T17 Key Performance Indicators** — KPIs are the measurement instrument within each BSC objective
- **T30 Risk Analysis & Management** — Strategy Map causal assumptions are sources of strategic risk
- **T36 SWOT Analysis** — Provides environmental context that informs which BSC perspectives to weight more heavily

## Output Template

```
BALANCED SCORECARD — [Organization / Program Name]
Period: [Q/Year]   Owner: [BA / Strategy Lead]   Status: [Draft | Approved | Active]

STRATEGY MAP: [Attach visual or embed Mermaid diagram]

| Perspective       | Objective | Measure (KPI) | Baseline | Target | Owner | Initiative(s) | Status |
|-------------------|-----------|---------------|----------|--------|-------|---------------|--------|
| Financial         |           |               |          |        |       |               |        |
| Customer          |           |               |          |        |       |               |        |
| Internal Process  |           |               |          |        |       |               |        |
| Learning & Growth |           |               |          |        |       |               |        |
```
