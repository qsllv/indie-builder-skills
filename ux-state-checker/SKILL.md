---
name: ux-state-checker
description: Check product UI and feature implementations for missing user states such as empty, loading, success, error, validation, disabled, permission, no-results, offline, partial success, long-running task, destructive confirmation, and retry states. Use when Codex needs to audit or implement complete product states before shipping.
---

# UX State Checker

## Purpose

Use this skill to prevent demo-only product UI. A feature is incomplete if it only handles the happy path.

## State Audit Workflow

1. Identify the user's primary task.
2. List all inputs, async operations, permissions, and side effects.
3. Generate the required state matrix.
4. Check what is implemented.
5. Add missing state behavior, copy, and recovery actions.
6. Verify the flow with realistic data and failures.

## Required Output

Return:

- Feature being checked.
- State matrix: required, present, missing, recommended behavior.
- P0 missing states.
- P1 missing states.
- Suggested UI copy for important states.
- Verification steps.

## Required States

Check these by default:

- Default
- Empty
- Loading
- Success
- Error
- Validation error
- Disabled
- No permission
- No results
- Partial success
- Offline/disconnected
- Long-running task
- Destructive confirmation
- Undo or recovery where relevant

## Severity

P0:
Missing state can trap users, lose data, cause duplicate side effects, expose unauthorized access, or hide destructive impact.

P1:
Missing state causes confusion, repeated attempts, poor activation, or support burden.

P2:
State exists but copy, polish, or affordance is weak.

Read `references/state-matrix.md` for patterns and examples.
