# Development Agent Skill

Reusable development-agent instructions for Codex, with companion templates for Claude.

## Structure

```text
development-agent/
  SKILL.md
  agents/openai.yaml
  references/
templates/
  AGENTS.md
  CLAUDE.md
```

## Use With Codex

Install or copy the `development-agent/` folder into your Codex skills directory, then invoke it with:

```text
Use $development-agent to fix this bug and validate the change.
```

For repository-local behavior, copy `templates/AGENTS.md` to the target repository root and customize project-specific commands.

## Use With Claude

Copy `templates/CLAUDE.md` to the target repository root and customize project-specific commands, architecture notes, and validation expectations.

## GitHub Setup

Suggested repository name:

```text
development-agent-skill
```

Before publishing, choose whether the repository should be public or private.
