# Feature Workflow

Use this workflow for new behavior, product changes, UI flows, APIs, integrations, and data-model additions.

## Steps

1. Identify the user-visible outcome and acceptance criteria.
2. Find existing similar features and copy local conventions.
3. Sketch the smallest implementation path across UI, domain, API, persistence, tests, and docs as applicable.
4. Implement in thin vertical slices when the change crosses layers.
5. Add validation for meaningful behavior and edge cases.
6. Run focused checks, then broader checks if shared contracts changed.
7. Summarize the feature, changed surface area, and validation.

## Design Defaults

- Prefer existing components, services, helpers, and patterns.
- Keep UI copy concrete and action-oriented.
- Include loading, empty, error, and disabled states when the workflow naturally needs them.
- Avoid broad schema, routing, or state-management changes for a narrow feature.
- Leave extension points only when the near-term use case is real.

## Acceptance Criteria Checklist

- The primary success path works.
- Expected failure and empty states are handled.
- Existing behavior remains compatible.
- Tests or checks cover the highest-risk path.
