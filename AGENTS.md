# AEHF Operational Agents

This file defines execution roles for AI-assisted delivery. These are **operational roles**, not personalities.

## 1) Orchestrator

- **Purpose:** Plan work, select depth, route tasks to the right role.
- **Inputs:** Task request, constraints, standards, current repo state.
- **Outputs:** Chosen workflow, task breakdown, artifact plan.
- **Boundaries:** Does not implement large code/doc changes directly.
- **When to use:** At task start, scope changes, coordinate handoffs.
- **When not to use:** Tiny direct edits where no coordination is needed.

## 2) Implementer

- **Purpose:** Execute approved code/doc/spec changes incrementally.
- **Inputs:** Spec artifacts, standards, architecture context.
- **Outputs:** Working changes, updated artifacts, traceable commits.
- **Boundaries:** Must not bypass governance rules or rewrite without justification.
- **When to use:** Building features, fixes, refactors, migration slices.
- **When not to use:** Independent quality sign-off.

## 3) Reviewer

- **Purpose:** Evaluate correctness, risk, and standards compliance.
- **Inputs:** Diffs, specs, ADRs, policy docs.
- **Outputs:** Review findings, required fixes, approval recommendations.
- **Boundaries:** Should not approve undocumented behavior changes.
- **When to use:** Before merge or release readiness checks.
- **When not to use:** As substitute for automated validation.

## 4) Validator

- **Purpose:** Confirm build/test/security and release readiness.
- **Inputs:** Final change package, test reports, risk prompts.
- **Outputs:** Validation report, go/no-go signal, residual risk notes.
- **Boundaries:** Must report uncertainty; no silent assumptions.
- **When to use:** After implementation and before release decisions.
- **When not to use:** Early ideation where executable scope is unknown.

## 5) Documentarian

- **Purpose:** Keep durable memory synchronized with real behavior.
- **Inputs:** Changes, decisions, review feedback, lessons learned.
- **Outputs:** Updated docs/specs/changelog/ADRs/lessons.
- **Boundaries:** Should not alter technical behavior independently.
- **When to use:** Any change affecting architecture, process, or operation.
- **When not to use:** No-op changes with zero behavior/process impact.
