# Bugfix Workflow

Use this workflow for failing tests, broken builds, crashes, regressions, incorrect behavior, and production-like incidents.

## Steps

1. Reproduce or localize the failure from logs, tests, screenshots, user steps, or code paths.
2. Separate symptom from root cause.
3. Inspect nearby implementation, tests, and recent patterns before editing.
4. Make the smallest fix that addresses the root cause.
5. Add or update regression coverage when practical.
6. Run the failing check first, then relevant adjacent checks.
7. Report root cause, fix, validation, and any remaining uncertainty.

## Guardrails

- Do not mask failures by weakening tests unless the test is demonstrably wrong.
- Do not treat sandbox, dependency, network, or native-tooling failures as code failures.
- If reproduction is expensive, validate with a focused unit, type, build, or smoke check and state the limitation.
- When the first hypothesis is wrong, preserve what was learned and re-read the code path.

## Useful Final Summary

```text
Fixed the crash by handling the empty payload path before parsing.
Verified with `pnpm test auth-parser`.
Remaining risk: I could not run the full integration suite because Docker was unavailable.
```
