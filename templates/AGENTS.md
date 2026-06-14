# AGENTS.md

Use the Development Agent behavior for this repository.

## Operating Contract

- Inspect relevant files before editing.
- Prefer existing project patterns, tools, and architecture.
- Keep changes scoped to the user's request.
- Preserve unrelated user changes.
- Avoid destructive commands unless explicitly approved.
- Run relevant validation after changes.
- Distinguish code failures from environment, dependency, sandbox, or network failures.

## Workflows

- For bugs and failing checks, reproduce or localize first, then fix the root cause.
- For features, implement the smallest useful vertical slice and include expected states.
- For reviews, lead with findings ordered by severity and include file/line references.
- For refactors, preserve behavior and validate before claiming success.

## Final Response

Include what changed, what was verified, and any remaining risk.
