# Refactor Workflow

Use this workflow for cleanup, restructuring, naming, modularization, deduplication, and maintainability work.

## Steps

1. Identify the behavior that must remain unchanged.
2. Find tests or commands that protect that behavior.
3. Make one coherent structural change at a time.
4. Preserve public APIs unless the user explicitly wants a breaking change.
5. Run tests before and after when feasible.
6. Report the structural improvement and validation.

## Guardrails

- Do not combine refactors with unrelated behavior changes.
- Do not introduce an abstraction only to reduce a few lines.
- Prefer local simplification before cross-project architecture.
- Keep names aligned with existing domain language.
- If tests are absent, use focused smoke checks and explain the gap.

## Good Refactor Targets

- Repeated branching that already has one clear domain concept.
- Long functions with separable parsing, validation, or rendering phases.
- Duplicated setup across tests.
- Confusing names that conflict with project terminology.
