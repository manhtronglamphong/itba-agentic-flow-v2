---
id: T02
name: Backlog Management
source: BABOK v3 §10.02
status: COMPLETE
category: Requirements Life Cycle
used_by_KAs: [KA3,KA5]
used_by_tasks: [3.3,5.1]
version: 1.0
last_updated: 2026-05-17
updated_by: phong.manh
changelog:
  - version: 1.0
    date: 2026-05-17
    author: phong.manh
    note: Initial population from SKELETON — all sections completed per BABOK v3 §10.02
---

# T02 — Backlog Management

## Purpose

Record, track, and prioritize all remaining work (requirements, user stories, defects, technical debt) so the team consistently focuses on the highest-value items within each delivery cycle.

## Description

A backlog is a prioritized, living artifact containing all work items a team is expected to complete. In adaptive/agile contexts, the backlog is the primary vehicle through which a business analyst manages the requirements lifecycle from inception to delivery.

Backlog management is not a single event — it is a **continuous activity** that encompasses: receiving, analyzing, estimating, ordering, and decomposing items. Items are organized by increasing granularity:

**Epics → Features → User Stories → Tasks**

The BA's role is to elaborate, size, and order items sufficiently so the delivery team is never blocked — not to fully analyze every item before development begins.

## Elements (per BABOK v3 §10.02)

1. **Manage Product Backlog** — The ongoing process of adding, removing, updating, and reordering items as business context evolves. Includes: backlog refinement/grooming sessions, intake of new items from stakeholders, and re-prioritization when priorities shift.

2. **Product Backlog** — The aggregated, priority-ordered list of all work. Each item must have a clear definition, acceptance criteria (ref T01), and an effort estimate sufficient for planning. Items near the top must be more refined than items lower in the backlog.

3. **Releases** — Groups of backlog items delivered together at a defined milestone. The BA plans releases by clustering related items to ensure each release delivers independent business value.

4. **Iterations** — Fixed-length delivery cycles (sprints) in which the team pulls a subset of the backlog (iteration backlog) and commits to completing it. After each iteration, the backlog is updated based on actual velocity and stakeholder feedback.

## How To Apply

1. **Initialize the backlog**: Collect initial requirements, user stories, and known defects from stakeholders into a centralized artifact (JIRA, ADO, Notion, spreadsheet).
2. **Classify items**: Assign a type (Epic / Story / Task / Defect / Spike) and domain (functional, non-functional, technical debt) to each item.
3. **Define acceptance criteria**: For every story of meaningful scope, apply T01 to write criteria before the item enters a sprint.
4. **Estimate effort**: Use relative sizing (story points, t-shirt sizes) to compare items. Only estimate in detail the items expected in the next 1–2 sprints.
5. **Order by priority**: Apply a prioritization technique (T35) combining business value, risk, effort, and dependencies to determine sequence.
6. **Groom on a cadence**: Hold refinement sessions before each iteration (typically 2× per sprint) to ensure the top of the backlog is always ready to pull.
7. **Update after each iteration**: Close completed items, adjust priorities based on feedback and velocity, and incorporate newly discovered items.

## Usage Considerations

### Strengths
- Provides a single source of truth for all pending work — reduces requirements that fall through the cracks.
- Enables continuous re-prioritization without replanning the entire project.
- Creates transparency for stakeholders on what is committed and in what order.
- Naturally accommodates changing requirements — items can be added, modified, or removed at any time.
- Supports delivery-date forecasting based on actual team velocity.

### Limitations
- The backlog can balloon and become unmanageable without a regular hygiene policy (grooming overhead increases linearly with backlog size).
- Requires continuous stakeholder engagement — if the Product Owner is insufficiently involved, ordering will reflect technical preference rather than business value.
- Prioritization can trigger political conflict when multiple stakeholder groups have competing interests.
- Not well-suited to projects with fixed scope, strict regulatory sequencing, or waterfall contractual constraints.
- Relative sizing via story points requires experienced teams — the technique does not transfer immediately to newly formed teams.

### Anti-patterns
- **Backlog as inbox**: Items are added but never groomed or removed — the backlog becomes a graveyard of stale work.
- **Ordering by requester seniority**: Items are elevated to the top because the requester has organizational authority, not because they deliver business value.
- **Over-specification upfront**: All items are fully analyzed before work begins — eliminates the adaptive advantage and wastes effort on items that may never be built.
- **Missing acceptance criteria at sprint entry**: Items enter a sprint without clear AC → definition of "done" is disputed at the sprint review.
- **Backlog as a substitute for traceability**: The backlog manages **delivery sequence**, not requirements traceability — it does not replace a requirements traceability matrix.

## BACCM Linkage

| Concept | Manifestation |
|---|---|
| **Change** | Each backlog item represents a specific change request; ordering the backlog is the act of deciding which changes are implemented first |
| **Need** | Items originate from business needs — every item must be traceable to at least one need; items with no traceable need are candidates for removal |
| **Solution** | The backlog is the roadmap for building the solution incrementally; item ordering determines how solution capabilities emerge across iterations |
| **Stakeholder** | Stakeholders both supply items and drive ordering — the BA must ensure the right stakeholders participate in grooming, preventing any single group from monopolizing backlog control |
| **Value** | Ordering by value is the core activity — items delivering the highest value at the lowest effort are done first; the backlog is the primary tool for optimizing value delivery |
| **Context** | Velocity, team capacity, regulatory constraints, and market timing all influence ordering — the same set of items in a different context produces a different optimal sequence |

## Used By

- **Knowledge Areas:** KA3 (Requirements Life Cycle Management), KA5 (Requirements Analysis and Design Definition)
- **Tasks:** 3.3 (Prioritize Requirements), 5.1 (Specify and Model Requirements)

## Related Techniques

- **T35 — Prioritization**: primary mechanism for ordering items (MoSCoW, weighted scoring, Kano model).
- **T01 — Acceptance and Evaluation Criteria**: provides the definition of done for each backlog item.
- **T18 — Estimation**: sizes item effort to support iteration planning and delivery forecasting.
- **T17 — Decision Analysis**: applied when trade-offs between items are complex and involve multiple risk dimensions.
- **T36 — Process Modelling**: decomposes epics into user stories small enough to complete within a single iteration.
- **T06 — Business Case**: provides strategic context for assessing the relative value of competing items.

## Output Template

```
Product Backlog — [Product / Initiative Name]
Last groomed: [Date] | Sprint velocity: [points/sprint] | Next review: [Date]

| ID     | Title             | Type   | Epic | Priority | Points | Sprint Target  | Status          | Acceptance Criteria | Dependencies |
|--------|-------------------|--------|------|----------|--------|----------------|-----------------|---------------------|--------------|
| US-001 | ...               | Story  | E-01 | Must     | 3      | Sprint 4       | Ready           | ref T01 AC-01       | US-002       |
| US-002 | ...               | Story  | E-01 | Should   | 5      | Sprint 5       | Needs Grooming  | —                   | —            |
| DE-003 | ...               | Defect | —    | Must     | 2      | Sprint 4       | Ready           | Bug reproduced      | —            |
| SP-004 | Spike: Evaluate X | Spike  | E-02 | Should   | 1      | Sprint 4       | Ready           | Output: recommendation doc | —     |

Priority scale : Must / Should / Could / Won't  (MoSCoW)
Status        : Icebox | Needs Grooming | Ready | In Progress | Done | Rejected
```
