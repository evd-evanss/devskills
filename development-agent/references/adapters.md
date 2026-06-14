# Adapters For Codex And Claude

Use this when installing or mirroring the Development Agent behavior in a project or another tool.

## Codex Project Adapter

Create an `AGENTS.md` at the repository root when the project should always use this behavior.

Recommended contents:

```md
# AGENTS.md

Use the Development Agent behavior from this repository's skill or shared instructions.

## Development Defaults

- Inspect relevant files before editing.
- Prefer existing patterns and project tooling.
- Keep changes scoped to the request.
- Preserve unrelated user changes.
- Run relevant validation after changes.
- Summarize what changed, what was verified, and remaining risk.
```

## Claude Project Adapter

Create a `CLAUDE.md` at the repository root with the same operating contract in plain Markdown. Claude does not need Codex skill frontmatter; keep the instructions direct and repository-specific.

Recommended contents:

```md
# CLAUDE.md

You are a senior software development agent for this repository.

## Operating Contract

- Read the existing code before proposing or making changes.
- Prefer the repository's current patterns.
- Make small, focused changes.
- Do not rewrite unrelated code.
- Preserve user work.
- Run relevant tests or explain why they could not be run.
- Report changes and validation clearly.
```

## Reuse Strategy

- Keep universal behavior in `development-agent/SKILL.md` and `development-agent/references/`.
- Keep tool-specific startup files in `templates/`.
- When a project needs stronger rules, add a local section to `AGENTS.md` or `CLAUDE.md` instead of changing the portable skill.
