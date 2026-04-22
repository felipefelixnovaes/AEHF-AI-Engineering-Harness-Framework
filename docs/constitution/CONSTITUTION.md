# AEHF Constitution

This constitution defines the non-negotiable principles of AEHF.

These principles exist to keep AI-assisted software delivery fast enough to be useful, structured enough to be reliable, and flexible enough to work across tools, teams, and repository types.

If a workflow, prompt, adapter, or implementation choice conflicts with this constitution, the constitution wins.

---

## 1. Clarity over ambiguity

Every meaningful deliverable must make scope, assumptions, tradeoffs, and intended outcomes explicit.

This applies to:
- specs
- architecture decisions
- implementation changes
- review findings
- validation results
- documentation updates

Hidden assumptions create operational debt.
If something is unknown, it must be surfaced clearly instead of implied.

---

## 2. Incremental evolution over rewrite

Prefer small, reversible, comprehensible change over broad rewrite.

Rewrite is allowed only when it is intentionally justified by evidence such as:
- unacceptable complexity or coupling
- severe maintainability failure
- contract redesign
- migration constraints that make incremental change unsafe or wasteful

The default stance is:
**touch-and-raise before rewrite**.

---

## 3. Stable memory over repeated context dumping

`docs/` is durable operational memory.
The framework must not depend on transient chat context, human recollection, or scattered prompt repetition to remain understandable.

Architecture, domains, decisions, gaps, standards, and lessons must be preserved in repository memory.

A strong system should become easier to reason about over time, not harder.

---

## 4. Depth on demand over one-size-fits-all process

Not every change deserves the same ritual.

AEHF requires task depth to be classified before deciding how much process, planning, and governance is appropriate.

The default goal is:
- enough structure to reduce risk
- not so much structure that delivery collapses into bureaucracy

Fast, Standard, Deep, and Reverse are not labels for prestige.
They are routing mechanisms for choosing the smallest reliable operating mode.

---

## 5. Explicit assumptions over hallucinated certainty

Unknowns must be labeled as unknowns.
Assumptions must be declared as assumptions.
Evidence must be distinguishable from inference.

AEHF rejects false confidence.
A believable answer is not enough; traceability matters.

When certainty is unavailable:
- state what is known
- state what is assumed
- state what must be validated

---

## 6. No silent drift between code, specs, and docs

Behavior, specs, architecture docs, and operational guidance must not silently diverge.

When meaningful change occurs, the corresponding sources of truth must be updated.

This includes changes to:
- observable behavior
- architecture understanding
- domain rules
- delivery standards
- known gaps
- decisions and tradeoffs

Silently stale documentation is a quality failure, not a cosmetic issue.

---

## 7. Governance must be lightweight and actionable

Governance exists to improve delivery quality, not to create ritual theater.

AEHF uses lightweight mechanisms such as:
- ADRs
- changelog updates
- review artifacts
- validation artifacts
- release checklists
- risk prompts

Governance should answer real delivery questions:
- what changed
- why it changed
- what risk was accepted
- what still needs validation

If governance stops being actionable, it should be simplified.

---

## 8. Tool adapters may vary; the method remains universal

Different AI tools consume context differently.
That is expected.

Adapters may change how repository memory is delivered, but they must not change the underlying AEHF method.

The method stays constant across tools:
- classify depth
- consult durable memory
- execute incrementally
- review and validate appropriately
- update project memory

Adapters exist to improve context delivery, not fragment the framework.

---

## 9. The repository is part of the execution system

In AEHF, the repository is not just a container for code.
It is an operational system for delivery.

That means:
- `docs/` carries durable memory
- `specs/` carries change intent and execution structure
- `prompts/` carries reusable workflows
- `CHANGELOG.md` carries visible evolution
- adapters carry tool-specific context delivery

The repository itself must help reduce ambiguity, not amplify it.

---

## 10. Human judgment remains part of the system

AEHF is designed for AI-assisted software delivery, not blind automation.

Human validation remains necessary when:
- risk is high
- ambiguity is unresolved
- contracts may change
- business impact is significant
- evidence is incomplete

Automation should increase leverage, not erase accountability.

---

## Final rule

AEHF exists to create governed progress.

When in doubt, choose the path that best preserves:
- clarity
- traceability
- incremental reliability
- durable memory
- honest uncertainty
