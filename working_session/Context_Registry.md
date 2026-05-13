---
name: Context Registry — Live BACCM State
type: working_session
purpose: The canonical, *current* state of the 6 BACCM concepts for the active engagement. Read by the Senior Orchestrator before every dispatch.
update_rule: Append-only with version stamps. Never silently overwrite a value — annotate the change and the source.
---

# Context Registry

> The Senior Orchestrator reads this file **first** on every turn. If any
> concept has confidence "L" or has not been updated since the last
> material event, the Orchestrator pauses and emits a Challenge Memo.

## Engagement Header

| Field             | Value                              |
| ----------------- | ---------------------------------- |
| Engagement-ID     | ENG-0001                           |
| Sponsor           | *(to be set)*                      |
| Lead BA           | *(to be set)*                      |
| Created           | 2026-05-13                         |
| Last updated      | 2026-05-13                         |
| Current phase     | INITIATION                         |

## 1. Change

| Field          | Value | Confidence (H/M/L) | Source / Date |
| -------------- | ----- | :----------------: | ------------- |
| What is changing |     | L                  |               |
| Trigger          |     | L                  |               |
| Scope boundary   |     | L                  |               |
| Reversibility    |     | L                  |               |
| Time horizon     |     | L                  |               |

## 2. Need

| Field                  | Value | Confidence | Source / Date |
| ---------------------- | ----- | :--------: | ------------- |
| Problem (not solution) |       | L          |               |
| Whose need is it       |       | L          |               |
| Quantified pain        |       | L          |               |
| Cost of doing nothing  |       | L          |               |

## 3. Solution

| Field                  | Value | Confidence | Source / Date |
| ---------------------- | ----- | :--------: | ------------- |
| Solution-in-mind       |       | L          |               |
| Alternatives surfaced  |       | L          |               |
| MVP boundary           |       | L          |               |
| Solution Scope (KA4)   |       | L          |               |

## 4. Stakeholder

| ID  | Name / Role | Type (Sponsor / SME / End User / Regulator / Operator / Customer / Supplier / Tester / PM / Implementation SME) | Authority (Approve / Consult / Inform) | Confidence |
| --- | ----------- | --------------------------------------------------------------------------------------------------------------- | -------------------------------------- | :--------: |
| S1  |             |                                                                                                                 |                                        | L          |

## 5. Value

| Field                    | Value | Unit (currency, time, %, count, qualitative) | Confidence | Source / Date |
| ------------------------ | ----- | --------------------------------------------- | :--------: | ------------- |
| Value to whom            |       |                                               | L          |               |
| Value hypothesis         |       |                                               | L          |               |
| Falsification criterion  |       |                                               | L          |               |
| Time horizon for value   |       |                                               | L          |               |

## 6. Context

| Field                                | Value | Confidence | Source / Date |
| ------------------------------------ | ----- | :--------: | ------------- |
| Regulatory constraints               |       | L          |               |
| Technical constraints                |       | L          |               |
| Cultural / organizational constraints|       | L          |               |
| Financial constraints                |       | L          |               |
| Load-bearing assumptions             |       | L          |               |
| Context shelf-life                   |       | L          |               |

## BACCM Scan Summary

| Concept     | Confidence | Last gap raised | Resolved? |
| ----------- | :--------: | --------------- | --------- |
| Change      | L          |                 |           |
| Need        | L          |                 |           |
| Solution    | L          |                 |           |
| Stakeholder | L          |                 |           |
| Value       | L          |                 |           |
| Context     | L          |                 |           |

**Dispatch authorization:** ❌ Blocked — all rows at Low confidence. Awaiting elicitation.

## Change Log (append-only)

| Date | Concept | Field | Old → New | Source | Author |
| ---- | ------- | ----- | --------- | ------ | ------ |
| 2026-05-13 | — | Registry initialized | — | template | Senior ITBA |
