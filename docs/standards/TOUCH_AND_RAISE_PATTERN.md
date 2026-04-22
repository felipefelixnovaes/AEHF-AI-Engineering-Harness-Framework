# Touch-and-Raise Pattern

Use this pattern for legacy, brownfield, or partially understood systems.

Its purpose is to improve the quality of a touched area without triggering unjustified redesign or destabilizing broad rewrite.

---

## Definition

When touching a component, raise its quality in place while preserving the smallest safe scope.

This means:
- fix what must be fixed
- improve what directly reduces current risk
- document what is discovered
- defer broader redesign into explicit follow-up work

Touch-and-raise is the default modernization posture when full rewrite is not clearly justified.

---

## When to use it

Use this pattern when:
- working in legacy code
- touching a hot spot with weak structure
- changing partially understood systems
- making bounded modernization progress
- reducing risk incrementally over time

It is especially useful when current delivery must continue while quality improves gradually.

---

## Goals

The pattern exists to:
- preserve delivery continuity
- reduce immediate local risk
- avoid speculative large rewrites
- make each touched area slightly easier to understand and maintain
- turn discovered knowledge into durable repository memory

---

## Core rules

### 1. Keep scope local
Keep the active change focused on the touched area and its direct dependencies.
Do not expand into adjacent cleanup unless it directly supports the current change.

### 2. Preserve observable behavior by default
If behavior is being changed intentionally, document that change explicitly.
Do not disguise behavior change as cleanup or refactor.

### 3. Improve what reduces immediate risk
Good touch-and-raise improvements include:
- clearer naming
- smaller functions or clearer structure
- safer boundaries
- better validation or tests
- removal of obvious duplication in the touched area
- clearer operational notes or domain documentation

### 4. Record hidden knowledge
If you discover implicit contracts, assumptions, workarounds, odd constraints, or discrepancies, record them in the appropriate repository memory.

### 5. Defer broad redesign explicitly
If the touched area reveals a larger structural problem, create a follow-up backlog item, gap entry, ADR candidate, or future spec.
Do not smuggle redesign into a local change without alignment.

---

## Typical execution flow

1. identify the smallest safe scope
2. understand current observable behavior
3. make the required change
4. improve the touched area where it directly reduces risk
5. add or strengthen validation around touched behavior
6. document newly discovered contracts, risks, or constraints
7. defer larger redesign into explicit follow-up work

---

## What “raise” usually means

Raising quality does not mean beautifying everything.
It usually means one or more of the following:

- code is easier to read than before
- local structure is less fragile than before
- behavior is better protected by tests or validation
- documentation is more accurate than before
- risk is more visible than before
- hidden contracts are more explicit than before

If none of these improved, the “raise” part likely did not happen.

---

## Anti-patterns

Avoid:

- full subsystem rewrite without evidence and alignment
- broad “cleanup” unrelated to the functional change
- mixing architectural redesign into a local bug fix without explicit justification
- undocumented behavior changes disguised as refactor
- touching many unrelated files for aesthetic consistency only
- assuming the touched area is fully understood because one change succeeded

---

## Relationship to task depth

Touch-and-raise is often used with:
- **Fast** for tiny safe local improvements
- **Standard** for bounded modernization
- **Reverse** when current behavior must be reconstructed first

It is compatible with **Deep**, but Deep work may require broader planning, stronger validation, and explicit architecture decisions.

---

## Final rule

Leave the touched area measurably better than you found it, but do so without turning a necessary change into uncontrolled redesign.
