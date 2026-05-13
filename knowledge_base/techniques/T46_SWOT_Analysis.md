---
id: T46
name: SWOT Analysis
source: BABOK v3 §10.46
status: FULLY_POPULATED
category: Strategy / Current-state assessment
used_by_KAs: [KA4]
used_by_tasks: [4.1_Analyze_Current_State, 4.2_Define_Future_State, 4.3_Assess_Risks, 4.4_Define_Change_Strategy]
---

# T46 — SWOT Analysis

## Purpose
SWOT (Strengths, Weaknesses, Opportunities, Threats) provides a **quick, structured framework** for evaluating an organization's strategic position so the BA can identify factors that drive — or constrain — the change.

## Description
SWOT places factors on **two axes**:

| Axis ↓ / Origin → | Internal (controllable) | External (not controllable) |
| ----------------- | :---------------------: | :-------------------------: |
| **Helpful**       |       Strengths         |        Opportunities        |
| **Harmful**       |      Weaknesses         |          Threats            |

It is a *positioning* technique, not a *decision* technique — it surfaces
factors that other techniques (Decision Analysis, Business Cases, Risk
Analysis) then act on.

## Elements

### 1. Strengths
**Internal**, helpful. Capabilities, assets, processes, brand, talent,
proprietary technology, and culture that the organization performs well today.
These are leveraged by the future state.

### 2. Weaknesses
**Internal**, harmful. Capability gaps, technical debt, talent shortages,
process drag, or organizational frictions that the change must work around
or correct.

### 3. Opportunities
**External**, helpful. Market shifts, regulatory openings, partnerships,
new customer segments, emerging technologies. The future state should
intentionally exploit at least one named opportunity.

### 4. Threats
**External**, harmful. Competitors, regulatory tightening, supply
disruptions, technology obsolescence, public sentiment, macroeconomic shocks.
Threats become the seed list for Task 4.3 (Assess Risks).

## How To Apply (procedure)

1. **Frame the scope.** "SWOT for what?" — the enterprise, a product line, a
   capability, or a single proposed change. A SWOT without a frame is noise.
2. **Source rigorously.** Each item should cite an underlying technique:
   Document Analysis, Interviews, Benchmarking, Data Mining, etc. Unsourced
   items are opinion and must be flagged.
3. **Quantify where possible.** Replace "strong brand" with "NPS 62, market
   share 31%". Replace "rising costs" with "raw-material index +14% YoY".
4. **Avoid the 4 traps** (see below).
5. **Cross-pair the quadrants** to generate strategic options:
   - **S × O** — leverage strengths to capture opportunities
   - **W × O** — close weaknesses by leveraging opportunities
   - **S × T** — leverage strengths to neutralize threats
   - **W × T** — defensive moves to limit downside

This pairing (the **TOWS matrix**) is what turns a SWOT into actionable input
for Task 4.4 (Define Change Strategy).

## Usage Considerations

### Strengths of the Technique
- Universally understood; low facilitation overhead.
- Surfaces stakeholder mental models quickly.
- Forces explicit separation of internal vs external factors.

### Limitations
- **Subjective by default.** Without sourcing, it reflects whoever was loudest in the room.
- **Static.** Captures a snapshot; does not model dynamics. Pair with Trend or Scenario analysis.
- **No prioritization.** A 30-item SWOT and a 4-item SWOT look equally valid; the technique gives no weights.
- **Quadrant confusion.** Teams routinely put internal items under Opportunities/Threats. Discipline the axis check.

### Common Failure Modes (the "4 traps")
1. **Solution-disguised-as-strength** ("our SSO project" — that is a *project*, not a strength).
2. **Vanity strengths** ("great culture") — unfalsifiable, drop or quantify.
3. **Threat = competitor's product** with no transmission mechanism stated.
4. **Symmetry padding** — adding weak items just to fill all 4 quadrants equally.

## BACCM Linkage

| Concept     | What SWOT supplies                                                |
| ----------- | ----------------------------------------------------------------- |
| Context     | The whole framework is a Context articulation.                    |
| Change      | TOWS pairing produces candidate change directions.                |
| Need        | Weaknesses + Threats often *are* the underlying need.             |
| Stakeholder | Source attribution names the stakeholder whose view this reflects.|
| Value       | Strengths × Opportunities is the value-capture hypothesis.        |
| Solution    | SWOT is **never** itself a solution — guard the line.             |

## Output Template

```
SWOT — [scope statement, dated]
Sourcing: [techniques cited]

Strengths
  - [item] [metric] [source]
Weaknesses
  - [item] [metric] [source]
Opportunities
  - [item] [metric] [source]
Threats
  - [item] [metric] [source]

TOWS pairing → candidate strategies:
  S×O: ...
  W×O: ...
  S×T: ...
  W×T: ...
```

## Related Techniques
Benchmarking and Market Analysis (T04); Business Capability Analysis (T06);
Business Model Canvas (T08); Business Cases (T07); Risk Analysis and Management (T38);
Root Cause Analysis (T40); Mind Mapping (T29).
