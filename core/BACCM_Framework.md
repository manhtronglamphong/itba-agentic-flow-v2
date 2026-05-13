---
name: BACCM Framework — Canonical Definitions
type: core
source: BABOK v3 §2.2
purpose: Authoritative reference for the 6 Business Analysis Core Concepts. Every Orchestrator scan and KA dispatch derives meaning from this file.
---

# Business Analysis Core Concept Model (BACCM)

The BACCM is the conceptual lens through which **every** Business Analysis (BA)
activity is interpreted. The six concepts are **interdependent and equal in
weight** — none can be defined without reference to the other five.

> A BA practitioner who has not articulated all six concepts for a given
> request has not yet understood the request.

## The 6 Core Concepts

### 1. Change
**Definition.** The act of transformation in response to a need.
**Probing questions.**
- What is being changed? (process, capability, system, behavior, policy)
- What is the trigger for the change? (compliance, opportunity, defect, strategy)
- What is the scope and reversibility of the change?

### 2. Need
**Definition.** A problem or opportunity to be addressed.
**Probing questions.**
- Whose need is this? (do not accept "the business" as an answer)
- Is this a stated need, an unmet need, or an inferred need?
- What is the cost of *not* addressing this need?

### 3. Solution
**Definition.** A specific way of satisfying one or more needs in a context.
**Probing questions.**
- Is the user presenting a *need* or a *pre-selected solution*?
- What alternative solutions have been considered and ruled out, and why?
- What is the minimum viable form of this solution?

### 4. Stakeholder
**Definition.** A group or individual with a relationship to the change, the
need, or the solution.
**Probing questions.**
- Who holds the **authority** to approve the change?
- Who is **impacted but not consulted**?
- Who supplies the **domain knowledge** required to validate the solution?

### 5. Value
**Definition.** The worth, importance, or usefulness of something to a
stakeholder within a context.
**Probing questions.**
- Value to *whom*, measured in *what units* (revenue, time, risk reduction, NPS)?
- What is the **value hypothesis**, and how will it be falsified?
- Is the proposed value capturable, or only theoretically present?

### 6. Context
**Definition.** The circumstances that influence, are influenced by, and
provide understanding of the change.
**Probing questions.**
- What constraints (regulatory, technical, cultural, financial) apply?
- What assumptions about the context are *load-bearing* for the solution?
- What is the **time horizon** over which the context is stable?

## Interdependence Matrix

| ↘ depends on    | Change | Need | Solution | Stakeholder | Value | Context |
| --------------- | :----: | :--: | :------: | :---------: | :---: | :-----: |
| **Change**      |   —    |  ●   |    ●     |      ●      |   ●   |    ●    |
| **Need**        |   ●    |  —   |          |      ●      |   ●   |    ●    |
| **Solution**    |   ●    |  ●   |    —     |      ●      |   ●   |    ●    |
| **Stakeholder** |   ●    |  ●   |    ●     |      —      |   ●   |    ●    |
| **Value**       |   ●    |  ●   |    ●     |      ●      |   —   |    ●    |
| **Context**     |   ●    |  ●   |    ●     |      ●      |   ●   |    —    |

Read as: "Change cannot be defined without reference to Need, Solution, Stakeholder, Value, and Context."

## Anti-Patterns the BACCM Catches

| Anti-pattern                                | Concept(s) violated     |
| ------------------------------------------- | ----------------------- |
| "Build feature X" with no problem statement | Need, Value             |
| "All users want this"                       | Stakeholder, Value      |
| "It's a small change, no risk"              | Change, Context         |
| "We chose React" (no alternatives stated)   | Solution                |
| "ROI will be high" (no unit, no horizon)    | Value, Context          |
| "Legal will be fine with it"                | Stakeholder, Context    |

Any of these patterns must be **escalated to the Orchestrator** before KA work proceeds.
