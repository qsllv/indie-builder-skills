---
name: feature-spec-to-code-plan
description: Convert a feature request, PRD, user story, bug-sized enhancement, or product requirement into a concrete coding plan. Use when Codex needs to plan implementation before editing code, identify files and components, API routes, database changes, states, tests, rollout risks, and step-by-step build order for a software product feature.
---

# Feature Spec To Code Plan

## Purpose

Use this skill to turn a product feature into an implementation plan that an AI coding agent can execute safely. The plan should reduce vague instructions, prevent broad unrelated edits, and make verification explicit.

## Planning Workflow

1. Restate the feature in one sentence.
2. Identify the user flow and primary success state.
3. Inspect the existing codebase before naming files or patterns.
4. Map impacted surfaces: UI, API, data, jobs, integrations, auth, billing, analytics.
5. Define required product states.
6. Decide implementation phases in dependency order.
7. Specify tests and manual verification.
8. List risks, migrations, and rollback considerations.

## Required Output

Return:

- Feature summary.
- Assumptions.
- User flow.
- Impacted areas:
  - UI/components
  - Routes/pages
  - API/server
  - Database/models
  - Auth/permissions
  - External services
  - Analytics/logging
- State matrix.
- Implementation phases.
- Test plan.
- Manual verification steps.
- Risks and rollback.

## State Matrix

Include relevant states:

- Empty
- Loading
- Success
- Error
- Disabled
- No permission
- Validation error
- Partial success
- Long-running task
- Destructive confirmation

## Implementation Phase Rules

Prefer this order:

1. Data contract and types.
2. Server/API behavior.
3. UI structure and states.
4. Integration wiring.
5. Tests and validation.
6. Polish and copy.

Do not plan broad refactors unless needed for the feature. If refactor is needed, isolate it as a separate phase with a reason.

## Codebase Inspection Rules

Before finalizing a plan, inspect:

- Existing routes and page patterns.
- Component library or design system.
- State management approach.
- Data fetching and mutation patterns.
- Validation conventions.
- Test setup.
- Existing auth and permission checks.

## References

Read `references/implementation-plan-template.md` for a full template.
Read `references/example-plan.md` for a concrete example.
