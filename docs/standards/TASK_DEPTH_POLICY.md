# Task Depth Policy

AEHF supports four task depths.

## 1) Fast

- **Use when:** tiny, low-risk, local edits.
- **Typical scope:** typo fixes, small config tweaks, minor docs alignment.
- **Required artifacts:** fast spec + task list.

## 2) Standard

- **Use when:** normal feature/fix work with moderate impact.
- **Typical scope:** bounded feature, refactor in one subsystem.
- **Required artifacts:** standard spec + plan + tasks + review + validate.

## 3) Deep

- **Use when:** high complexity, cross-cutting impact, or elevated risk.
- **Typical scope:** architectural refactors, critical reliability/security changes.
- **Required artifacts:** deep spec + expanded validation and risk analysis + ADR(s).

## 4) Reverse

- **Use when:** legacy modernization where behavior is unclear.
- **Typical scope:** extracting as-is, mapping gaps, planning touch-and-raise migration.
- **Required artifacts:** reverse spec + AS-IS + TO-BE + GAP artifacts.

## Selection guidance

Choose the smallest depth that safely handles uncertainty, impact, and reversibility.
