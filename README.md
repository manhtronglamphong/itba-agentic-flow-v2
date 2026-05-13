---
name: ITBA Agentic Flow
version: 1.0.0
framework: BABOK v3
orchestration_model: BACCM (Business Analysis Core Concept Model)
role_persona: Senior ITBA — Strategic Consultant & Executive Expert
---

# ITBA Agentic Flow

A Markdown-native, BABOK v3-aligned operating system for Senior IT Business Analysis.
Designed to behave as a **Strategic Consultant** layer — not a passive note-taker.

## North Star

> Every analytical move is validated against the **6 BACCM concepts**
> (Change, Need, Solution, Stakeholder, Value, Context) **before** any
> Knowledge Area (KA) task is dispatched. Critical thinking gates execution.

## Repository Map

```
.
├── core/
│   ├── Senior_Orchestrator_Logic.md     # Critical-thinking gate + KA dispatcher
│   └── BACCM_Framework.md               # Canonical definitions of the 6 concepts
│
├── knowledge_base/
│   ├── knowledge_areas/                 # 6 BABOK v3 KAs (tasks, I/O, stakeholders)
│   │   ├── KA1_Business_Analysis_Planning_and_Monitoring.md
│   │   ├── KA2_Elicitation_and_Collaboration.md
│   │   ├── KA3_Requirements_Life_Cycle_Management.md
│   │   ├── KA4_Strategy_Analysis.md     # ★ Fully populated for first review
│   │   ├── KA5_Requirements_Analysis_and_Design_Definition.md
│   │   └── KA6_Solution_Evaluation.md
│   │
│   └── techniques/                      # 50 BABOK v3 techniques (T01..T50)
│       ├── T01..T50_*.md                # 47 skeleton, 3 fully populated:
│       ├── T46_SWOT_Analysis.md         # ★
│       ├── T07_Business_Cases.md        # ★
│       └── T38_Risk_Analysis_and_Management.md  # ★
│
├── execution_engine/                    # Dev-ready output standards
│   ├── Agile_User_Stories_Standard.md
│   ├── UML_Modeling_Standard.md
│   └── API_Specification_Standard.md
│
└── working_session/                     # Live session state (per engagement)
    ├── Context_Registry.md              # State of the 6 BACCM concepts
    └── Traceability_Matrix.md           # Business Need → Technical Spec log
```

## Operating Principles

1. **Strict Taxonomy** — KAs describe *what is produced* (tasks, I/O, stakeholders).
   Techniques describe *how it is produced*. They are never merged.
2. **BACCM-First Gating** — Any user request is first decomposed against the
   6 BACCM concepts in `core/Senior_Orchestrator_Logic.md`. Logic gaps are
   challenged *before* any KA work begins.
3. **Inputs/Outputs Integrity** — Each KA task lists its **explicit** BABOK v3
   inputs and outputs. No assumed or invented I/O.
4. **Traceability by Construction** — Every artifact produced is logged in
   `working_session/Traceability_Matrix.md` with its upstream Need and
   downstream Spec.
5. **Dev-Ready by Default** — Outputs that cross into delivery (stories, UML,
   API specs) follow the standards in `execution_engine/`.

## Population Status (Phase 1)

| Area                       | Status                           |
| -------------------------- | -------------------------------- |
| KA4 — Strategy Analysis    | **Fully populated** (for review) |
| KA1, KA2, KA3, KA5, KA6    | Skeleton (structurally complete) |
| T07 Business Cases         | **Fully populated**              |
| T38 Risk Analysis & Mgmt   | **Fully populated**              |
| T46 SWOT Analysis          | **Fully populated**              |
| 47 other techniques        | Skeleton (structurally complete) |
| Senior Orchestrator        | **Fully populated**              |
| Execution Engine standards | **Fully populated**              |
| Working Session            | **Fully populated** (templates)  |

## How to Use

1. Drop a user request into the conversation.
2. The Senior Orchestrator runs the **BACCM Logic Scan** (see
   `core/Senior_Orchestrator_Logic.md`) and either (a) challenges the request
   for missing concepts or (b) dispatches to the relevant KA(s).
3. KA tasks consume their declared inputs, invoke the listed techniques,
   and produce their declared outputs.
4. Outputs are logged into `working_session/Traceability_Matrix.md`.
5. When the output is dev-bound, it is shaped by the relevant
   `execution_engine/` standard.
