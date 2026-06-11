---
name: user-flow-designer
description: Design complete user flows for software products before implementation, including entry points, screens, primary actions, decisions, empty/loading/error/success states, edge paths, permissions, onboarding, imports, checkout, invitations, and activation flows. Use when Codex needs to turn a feature or product idea into a step-by-step user journey and screen map.
---

# User Flow Designer

## Purpose

Use this skill to design the path a user takes to complete a product task. The output should be specific enough for an AI coding agent to implement screens, states, and transitions.

## Workflow

1. Define the target user and the job they want to complete.
2. Identify the entry point and trigger moment.
3. Map the happy path from entry to success.
4. Add decision points, failures, permissions, and recovery paths.
5. Define screens, primary actions, secondary actions, and required states.
6. Identify the activation moment or completion signal.
7. Produce an implementation-ready flow.

## Required Output

Return:

- Flow goal.
- User and trigger.
- Happy path.
- Alternate paths.
- Error and recovery paths.
- Screen map.
- State requirements.
- Event or analytics suggestions.
- Implementation notes.

## Flow Rules

- Start with one primary user and one primary job.
- Keep the path to first value short.
- Avoid asking for setup before showing value unless setup is the value.
- Every screen needs one primary action.
- Every failure path needs a recovery action.
- Every long-running step needs progress or expectation-setting.

Read `references/flow-patterns.md` for common flows and examples.
