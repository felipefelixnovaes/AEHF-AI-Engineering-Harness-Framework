# Task Depth Policy

AEHF supports four task depths:

- Fast
- Standard
- Deep
- Reverse

The purpose of this policy is to choose the **smallest reliable level of process** for a task.

This is not a maturity ladder and not a prestige system.
A deeper level is not automatically better.
The correct level is the one that matches risk, ambiguity, scope, and reversibility.

---

## Core rule

Always classify task depth before deciding:
- which artifacts to create
- how much planning is needed
- how much review is needed
- how much validation is needed
- whether human escalation is required

If the selected depth is too shallow, important risks go unmanaged.
If it is too deep, the process becomes wasteful and slows adoption.

---

## 1) Fast

### Use when
Use Fast for tiny, low-risk, highly local changes where behavior is already well understood.

### Typical scope
- typo fixes
- local documentation alignment
- minor configuration edits
- very small low-risk bug fixes
- tiny refactors with no external contract impact

### Typical characteristics
- touches one small area
- low ambiguity
- low blast radius
- easy to review quickly
- easy to validate directly

### Required artifacts
At minimum:
- a small spec or intent note
- a task list or execution checklist
- any directly affected doc updates

### Review expectation
- light review
- confirm no silent behavior change
- confirm docs are still aligned

### Validation expectation
- direct observable check
- lightweight testing or equivalent evidence

### Do not use Fast when
- multiple modules are involved
- external behavior may change
- legacy behavior is unclear
- the task seems small but has hidden coupling

---

## 2) Standard

### Use when
Use Standard for normal feature work, bounded refactors, and moderate-impact fixes where the repository understanding is reasonably reliable.

### Typical scope
- a feature in one subsystem
- a bounded workflow change
- a moderate refactor
- a normal bug fix with visible user or system impact

### Typical characteristics
- limited but meaningful impact
- moderate ambiguity
- one or two main modules or domains involved
- normal review and validation required

### Required artifacts
Typically:
- `spec.md`
- `plan.md`
- `tasks.md`
- `review.md`
- `validate.md`

### Review expectation
- confirm alignment with intended behavior
- check standards compliance
- check docs/spec/code alignment
- identify missing risks or gaps

### Validation expectation
- appropriate tests or equivalent evidence
- explicit validation of changed observable behavior

### Do not use Standard when
- risk is materially high
- architecture or contracts are changing broadly
- current behavior is not well understood
- migration complexity is significant

---

## 3) Deep

### Use when
Use Deep for high-risk, cross-cutting, high-cost, or contract-affecting work.

### Typical scope
- architectural refactors
- critical reliability or security changes
- migrations across modules or boundaries
- data model or interface changes
- operationally sensitive delivery work

### Typical characteristics
- multiple modules or domains involved
- elevated blast radius
- higher cost of failure
- more coordination needed
- stronger governance and validation needed

### Required artifacts
Typically:
- deep `spec.md`
- `plan.md`
- `tasks.md`
- `review.md`
- `validate.md`
- risk analysis notes
- rollout or release considerations
- ADRs when architectural or policy decisions are being made

### Review expectation
- stronger scrutiny for architecture, contracts, and rollback strategy
- explicit identification of residual risk
- confirmation that broader system effects were considered

### Validation expectation
- stronger evidence
- broader testing or verification
- explicit readiness assessment
- human validation if risk remains high

### Do not use Deep when
- the task is truly small and local
- the extra ritual would add no real control value

---

## 4) Reverse

### Use when
Use Reverse for legacy or opaque systems where current behavior must be reconstructed before safe change can happen.

### Typical scope
- modernization of poorly documented modules
- high-risk hot spots with unclear behavior
- inherited systems with conflicting expectations
- areas where the team lacks trustworthy as-is understanding

### Typical characteristics
- uncertainty is the main risk
- existing behavior may be implicit or contradictory
- documentation is missing, stale, or untrusted
- safe change requires discovery first

### Required artifacts
Typically:
- reverse `spec.md`
- as-is artifacts
- to-be artifacts when appropriate
- discrepancy analysis
- gap backlog
- touch-and-raise plan

### Review expectation
- verify that current behavior was distinguished from desired behavior
- verify that assumptions were made explicit
- check whether gaps and discrepancies were captured honestly

### Validation expectation
- validate discovered behavior before relying on it
- confirm that proposed change path preserves safety
- escalate when reconstructed understanding remains uncertain

### Do not use Reverse when
- current behavior is already clear and well documented
- the task can be safely handled with Standard or Deep

---

## Selection guidance

Choose the smallest depth that safely handles:
- uncertainty
- impact
- coupling
- reversibility
- validation burden

A useful rule of thumb:
- if it is tiny and obvious, use **Fast**
- if it is normal product or engineering work, use **Standard**
- if it is risky or cross-cutting, use **Deep**
- if the current system is unclear, use **Reverse**

---

## Escalation rules

Move to a deeper level when any of the following becomes true:
- scope expands beyond the original boundary
- hidden coupling appears
- current behavior is less understood than expected
- validation becomes more complex than expected
- external contracts may change
- risk is higher than originally assumed

It is acceptable to start at one depth and escalate later.
It is not acceptable to stay shallow after the risk picture changes.

---

## Final rule

Task depth is a control mechanism.
Use it to keep delivery proportional, reviewable, and reliable.

AEHF works best when the process is neither too light nor too heavy, but matched to reality.
