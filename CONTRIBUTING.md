# Contributing to AEHF

Thanks for contributing to AEHF.

This repository is not just a collection of templates and prompts.
It is a framework repository, so contribution quality depends on clarity, consistency, and respect for the method.

Contributions should make the framework:
- more useful
- more coherent
- more portable
- more trustworthy
- easier to adopt in real repositories

---

## Contribution principles

All contributions should follow these principles:

- keep changes incremental and reviewable
- preserve existing behavior unless change is intentional and documented
- align every change with the AEHF constitution and standards
- prefer clarity over novelty
- prefer durable improvements over clever local hacks
- treat documentation as part of delivery, not an afterthought

Before contributing, read:
- `README.md`
- `docs/constitution/CONSTITUTION.md`
- `docs/standards/TASK_DEPTH_POLICY.md`
- `docs/standards/DOC_UPDATE_POLICY.md`

---

## What kinds of contributions are welcome

Examples of valuable contributions:

- stronger templates
- clearer standards
- better prompt files
- improved adapter guidance
- additional examples
- cross-platform repository guidance
- governance improvements that remain lightweight
- fixes to ambiguity, inconsistency, or drift in the framework itself

Less valuable contributions include:
- unnecessary verbosity
- tool-specific lock-in without a good reason
- speculative expansion with no clear adoption value
- cosmetic changes that reduce clarity or increase noise

---

## Basic workflow

1. Align on the problem or scope.
2. Classify task depth using `docs/standards/TASK_DEPTH_POLICY.md`.
3. Create or update the appropriate change package from `specs/templates/` when needed.
4. Implement in small, reviewable slices.
5. Update documentation per `docs/standards/DOC_UPDATE_POLICY.md`.
6. Add an ADR when the decision is architecture-significant or process-significant.
7. Update `CHANGELOG.md` for notable framework changes.
8. Submit a PR using `.github/pull_request_template.md`.

---

## Contribution guidance by change type

### Documentation and standards changes
These should:
- improve clarity
- reduce ambiguity
- remain consistent with the AEHF method
- avoid introducing contradictions across files

### Prompt library changes
These should:
- be reusable
- be outcome-oriented
- clearly define purpose, inputs, expected outputs, and completion criteria
- avoid shallow prompt theater

### Adapter changes
These should:
- preserve the universal AEHF method
- improve context delivery for a specific ecosystem
- avoid changing core principles just because a tool behaves differently

### Example changes
These should:
- reduce abstraction
- show practical adoption paths
- remain realistic and scenario-driven

---

## Quality expectations

Do not submit contributions that:
- rely on speculative rewrites
- introduce undocumented behavior shifts
- leave repository memory stale
- add complexity without improving adoption or clarity
- fragment the framework into incompatible tool-specific versions

Strong contributions usually:
- improve usability without bloating the framework
- make repository memory more durable
- strengthen the relationship between docs, specs, prompts, and adapters
- help future contributors make better decisions faster

---

## Pull request acceptance criteria

A pull request is more likely to be accepted when:

- scope is clear and bounded
- the selected task depth is appropriate
- required artifacts are present for that depth
- docs, specs, and repository memory are synchronized
- risks and assumptions are explicit
- the change improves clarity, utility, or reliability
- the framework remains portable and method-consistent

---

## Review mindset

Review in this repository is not just about whether text or structure looks good.
It is about whether the contribution strengthens the framework as an operating method.

Reviewers may reject changes that are technically correct but:
- bloat the framework
- weaken portability
- create contradiction between artifacts
- optimize for novelty over durable usefulness

---

## Final rule

Contribute in a way that makes AEHF easier to trust, easier to adopt, and easier to evolve.

If a change makes the repository louder but not clearer, it is probably not a good contribution.
