# Documentation Update Policy

Documentation is part of delivery, not post-work.

## Required updates

Update relevant docs in the same change when any of the following change:

- behavior visible to users or integrators
- architecture or module boundaries
- standards/process rules
- release or operation procedures

## Minimum sync set

- `specs/` change package
- affected files in `docs/`
- `CHANGELOG.md` entry for notable changes
- ADR for architecture/process-significant decisions

## Drift prevention checklist

- Does code reflect the described behavior?
- Does doc describe current assumptions and constraints?
- Is changelog updated for externally meaningful changes?
