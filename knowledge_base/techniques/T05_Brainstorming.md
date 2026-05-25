---
id: T05
name: Brainstorming
source: BABOK v3 §10.05
status: COMPLETE
category: Elicitation / Idea generation
used_by_KAs: [KA2, KA4]
used_by_tasks: [2.2, 4.2, 4.3]
version: 1.0.0
last_updated: 2026-05-20
updated_by: phong.manh@mservice.com.vn
changelog:
  - "1.0.0 | 2026-05-20 | Initial population from BABOK v3 §10.05"
---

# T05 — Brainstorming

## Purpose

Generate a large number of new ideas or compile existing ideas within a short time, leveraging group energy to produce more options than individuals working in isolation could achieve.

## Description

Brainstorming is a facilitated group (or individual) creativity technique that operates in two distinct cognitive phases:

1. **Divergent phase** — Unconstrained idea generation. All ideas are recorded without evaluation. Quantity over quality is the explicit goal.
2. **Convergent phase** — Ideas are consolidated, grouped by affinity, duplicates removed, and the shortlist prepared for subsequent analysis (e.g., Decision Analysis, Prioritization).

The technique is most effective when the framing question is specific enough to focus energy but open enough not to anchor the group prematurely. It is frequently the entry-point elicitation technique before more structured techniques (process modelling, user stories, business rules) are applied.

## Elements

Per BABOK v3 §10.05:

1. **Preparation** — The facilitator defines the objective/question, selects a diverse set of participants (typically 5–15), establishes a neutral environment, and communicates ground rules before the session begins. Ground rules: *defer judgement, encourage wild ideas, build on others' ideas, go for quantity*.
2. **Idea Generation** — Participants freely offer ideas; the facilitator captures all ideas visibly (whiteboard, sticky notes, virtual board) in real time. No criticism, filtering, or discussion of feasibility is permitted during this phase. The phase is time-boxed (typically 15–30 minutes).
3. **Consolidation** — After generation, the group reviews the raw list: groups related ideas into themes (affinity clustering), removes exact duplicates, and clarifies ambiguous entries. The output is a clean, themed idea list ready for analysis.

## How To Apply (procedure)

1. **Frame the question** — Write a single, clear problem or opportunity statement. Validate it with the sponsor before the session.
2. **Select participants** — Include diverse stakeholders (business, IT, operations, end-users). Avoid groups where hierarchy will suppress participation; consider anonymous digital tools if needed.
3. **Appoint a neutral facilitator** — The facilitator does not contribute ideas; their role is pacing, encouragement, and capturing.
4. **State ground rules** — Explicitly recite the four rules at the start of every session.
5. **Run the divergent phase** — Time-box. Facilitator prompts with "What else?" if energy drops. All ideas captured verbatim.
6. **Run the convergent phase** — Affinity-cluster ideas on the board. Label clusters. Remove duplicates. Flag ideas needing clarification.
7. **Prioritize (optional)** — Apply dot voting or a MoSCoW pass to identify the top candidates for deeper analysis.
8. **Document and hand off** — Produce the Consolidated Idea List (see Output Template) and route to the appropriate follow-on technique (Decision Analysis, Risk Analysis, Business Case, etc.).

## Usage Considerations

### Strengths
- Rapidly surfaces a broad option space; mitigates premature convergence on the first solution proposed.
- Low cost and low tooling requirements — can be run with nothing more than a whiteboard.
- Inclusive format gives quieter stakeholders an equal voice when properly facilitated.
- Group energy typically yields more ideas than parallel individual work (nominal group effect).
- Builds shared ownership of the solution space among participants.

### Limitations
- **Social loafing** — In large groups, individuals may contribute less than they would alone.
- **Anchoring/HiPPO effect** — If a senior leader speaks first, the group tends to cluster around that idea; anonymous formats (brainwriting, digital tools) mitigate this.
- **Vague outputs** — Without a strong convergent phase, the raw list is not actionable.
- **Facilitator dependency** — Poor facilitation (allowing criticism, no time-boxing, no convergent phase) renders the technique ineffective.
- **Not suitable for complex analytical problems** — Brainstorming generates candidates; it does not evaluate them. Pairing with a decision technique is mandatory.

### Anti-patterns
- Criticising or debating ideas during the generation phase — immediately kills psychological safety.
- Skipping the convergent phase and treating the raw idea dump as a deliverable.
- Insufficient framing of the question → off-topic or overlapping ideas.
- Homogeneous participant group → groupthink, narrow solution space.
- Dominant voice problem: allowing one participant to anchor the session without anonymous mitigation.
- Running brainstorming as a substitute for stakeholder analysis — the *who is in the room* decision must come first.

## BACCM Linkage

| Concept      | Manifestation |
| ------------ | ------------- |
| Change       | Generates candidate approaches for how a change can be designed or implemented; expands the option space before a change path is committed. |
| Need         | Surfaces implicit and unarticulated needs; participants often voice needs they would not raise in a structured interview format. |
| Solution     | Primary output: candidate solutions or solution components that feed downstream design and analysis activities. |
| Stakeholder  | Engages diverse stakeholders simultaneously; the facilitated format captures perspectives that structured surveys miss. |
| Value        | Helps identify potential sources of value and trade-offs, but *cannot quantify value alone* — must hand off to Decision Analysis or Business Case. |
| Context      | Useful for exploring contextual constraints informally, but does not replace formal context modelling (ecosystem maps, PESTLE). |

## Used By

- **Knowledge Areas:** KA2 (Elicitation & Collaboration), KA4 (Requirements Analysis & Design Definition)
- **Tasks:**
  - 2.2 — Elicit Elicitation Information *(primary usage)*
  - 4.2 — Analyze Current State
  - 4.3 — Define Future State

## Related Techniques

| Technique | Relationship |
| --------- | ------------ |
| Affinity Diagram | Post-processing tool for the convergent phase; clusters raw brainstorming output into themes. |
| Collaborative Games | Complementary; structured games can warm up a group before or substitute for a free-form brainstorming session. |
| Decision Analysis | Downstream; evaluates and ranks the shortlist produced by brainstorming. |
| Mind Mapping | Visual alternative or complement; useful when ideas have strong hierarchical relationships. |
| Prioritization | Applied in the convergent phase to rank the idea shortlist before handing off. |
| Risk Analysis & Management | Brainstorming is frequently used to generate the initial risk register during risk identification. |
| Focus Groups | Alternative elicitation technique when a moderated discussion with targeted probing is preferred over free-form generation. |

## Output Template

**1. Raw Idea List**
```
Session topic: <question framing>
Date / participants: <metadata>
[Unfiltered, verbatim list of all ideas captured]
```

**2. Consolidated Idea List**
```
| # | Idea (refined) | Theme/Cluster | Notes / Owner |
|---|----------------|---------------|---------------|
| 1 | ...            | ...           | ...           |
```

**3. Shortlist (optional — post-prioritization)**
```
| Rank | Idea | Priority (MoSCoW / Votes) | Next Action |
|------|------|--------------------------|-------------|
| 1    | ...  | Must                     | → Decision Analysis |
```
