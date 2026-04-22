# Claude Adapter

Use `CLAUDE.md` as the primary context bootstrap contract.

## Adapter intent

- Keep startup context short, strict, and normative.
- Force stable reading order to reduce context ambiguity.
- Preserve AEHF method while adapting to Claude workflow patterns.

## Required entry sequence

1. `README.md`
2. `docs/constitution/CONSTITUTION.md`
3. `docs/architecture/INVENTORY.md`
4. `docs/standards/CODING_STANDARDS.md`
5. `docs/standards/DOC_UPDATE_POLICY.md`
6. `AGENTS.md`

## Notes

- `CLAUDE.md` should remain concise.
- Durable detail belongs in `docs/`, not in adapter bootstrap files.
