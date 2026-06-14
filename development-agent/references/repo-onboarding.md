# Repository Onboarding

Use this when starting in an unfamiliar repository or when the user request depends on project conventions.

## Fast Orientation

1. List top-level files and directories.
2. Read package/build manifests and README-like setup files.
3. Search for existing implementations similar to the request.
4. Identify test, lint, format, build, and dev commands.
5. Check whether the worktree is dirty before edits when version control is present.

## Signals To Capture

- Language, framework, package manager, and build tool.
- App boundaries and ownership: frontend, backend, mobile, packages, modules.
- Test stack and naming conventions.
- Where shared utilities, UI components, services, and types live.
- Existing style for errors, logging, configuration, and data access.

## Stop Conditions

Ask the user only when a decision cannot be inferred and a wrong assumption would be costly, such as destructive data changes, public API breaks, paid services, credentials, or publishing.
