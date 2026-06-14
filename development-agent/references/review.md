# Review Workflow

Use this workflow for code review, PR review, design review, or risk assessment.

## Review Stance

Lead with findings. Prioritize correctness, regressions, security, data loss, concurrency, performance cliffs, accessibility, and missing tests. Keep style comments secondary unless they affect maintainability or violate clear project conventions.

## Steps

1. Understand the intended behavior and changed files.
2. Inspect tests and validation claims.
3. Review risky boundaries first: inputs, auth, persistence, migrations, network calls, async flows, state transitions, and error handling.
4. Check backward compatibility and edge cases.
5. Report findings ordered by severity with file and line references.
6. If no findings exist, say so clearly and mention residual risk or unrun checks.

## Finding Format

```text
[P1] Guard against missing tenant before querying invoices
file/path.ts:42
When tenantId is undefined, this query now returns all invoices. Add an early error or scoped fallback before calling the repository.
```

## Avoid

- Do not rewrite the PR in review mode unless the user asks for fixes.
- Do not bury serious findings below summaries.
- Do not claim a test gap is a bug unless it creates real risk.
