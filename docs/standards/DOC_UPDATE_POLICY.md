# Documentation Update Policy

Documentation is part of delivery.
It is not post-work, decoration, or optional cleanup.

In AEHF, repository memory must stay synchronized with meaningful change.
This policy defines when documentation must be updated, what should be updated, and how to prevent silent drift.

---

## Core rule

When behavior, architecture, decisions, standards, or operational understanding change, the relevant documentation must be updated in the same change package.

Do not merge meaningful changes while knowingly leaving core repository memory stale.

---

## What requires documentation updates

Update relevant documentation whenever any of the following changes:

- behavior visible to users, operators, or integrators
- architecture or module boundaries
- domain rules or assumptions
- standards, process, or governance rules
- release, validation, or operational procedures
- known gaps, discrepancies, or risks
- architecture understanding discovered during brownfield or reverse work
- lessons that should influence future execution

---

## Minimum sync set

For a meaningful change, review and update the smallest correct set of these artifacts:

- affected files in `docs/`
- affected change package in `specs/`
- `CHANGELOG.md` for externally or operationally meaningful changes
- ADRs for architecture-significant or policy-significant decisions
- gap or discrepancy records when newly discovered issues appear
- lessons when reusable insight was generated

The goal is not to update everything.
The goal is to update every source of truth that would otherwise become misleading.

---

## Typical update mapping

### If observable behavior changes
Usually update:
- relevant spec package in `specs/`
- relevant domain files in `docs/domains/`
- relevant architecture docs if boundaries or flows changed
- `CHANGELOG.md`

### If architecture understanding changes
Usually update:
- `docs/architecture/`
- relevant domain docs
- ADRs if a decision was made
- relevant gaps if tradeoffs or limitations remain

### If a new rule or standard is introduced
Usually update:
- `docs/standards/`
- `README.md` if contributor-facing expectations changed
- `CONTRIBUTING.md` if contribution workflow changed

### If legacy behavior is discovered during reverse work
Usually update:
- `docs/as-is/`
- `docs/gaps/`
- relevant domain docs
- related spec package

### If a reusable lesson emerges
Usually update:
- `docs/lessons/`
- relevant standards if the lesson becomes a durable rule

---

## Drift prevention checklist

Before completing a change, ask:

- Does the implementation still match the described behavior?
- Do the docs still describe current assumptions and constraints?
- Did the architecture understanding change?
- Was a decision made that deserves an ADR?
- Was a gap, discrepancy, or operational risk discovered?
- Is the changelog updated for meaningful change?
- Would a new contributor be misled if docs were left as-is?

If the answer to any of these is yes, update the relevant repository memory.

---

## Anti-patterns

Avoid:

- postponing obvious doc updates to a vague later cleanup
- treating stale docs as acceptable because the code is “the real source of truth”
- changing behavior under the label of refactor without updating memory
- over-updating unrelated documents just to look thorough
- writing aspirational docs that do not reflect current reality

---

## Quality bar

Good documentation updates are:

- factual
- targeted
- durable
- aligned with actual implementation and decisions
- useful for future contributors and AI tools

Poor documentation updates are:

- vague
- overly broad
- disconnected from reality
- missing the actual source of truth that changed

---

## Final rule

If a meaningful change would cause future readers, contributors, or AI tools to form the wrong understanding of the system, the documentation update is not optional.
