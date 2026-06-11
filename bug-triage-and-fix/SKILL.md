---
name: bug-triage-and-fix
description: Reproduce, diagnose, and fix software bugs with an evidence-first workflow. Use when Codex needs to investigate failing behavior, test failures, runtime errors, broken UI flows, regressions, production issues, logs, stack traces, or user bug reports, and then apply the smallest safe fix with verification.
---

# Bug Triage And Fix

## Purpose

Use this skill to prevent guess-driven bug fixing. The agent should reproduce or gather evidence, identify the likely root cause, make the smallest safe change, and verify the fix.

## Workflow

1. Restate the observed bug and expected behavior.
2. Gather evidence: reproduction steps, logs, stack traces, failing tests, screenshots, network responses, or user report details.
3. Reproduce the issue when feasible.
4. Identify the smallest affected area.
5. Form a root-cause hypothesis and check it against the code.
6. Apply the smallest fix that addresses the root cause.
7. Add or update tests when the risk justifies it.
8. Verify the original bug path and nearby regression paths.
9. Report what changed and what remains unverified.

## Required Output

Return:

- Bug summary.
- Evidence gathered.
- Root cause.
- Fix applied.
- Files changed.
- Verification performed.
- Regression risk.
- Follow-up if needed.

## Fix Rules

- Do not rewrite large areas unless the bug is caused by the architecture.
- Do not mask errors with broad catch blocks.
- Do not remove validation, auth, or safety checks to make a failure disappear.
- Preserve user data and existing behavior outside the bug path.
- If reproduction is impossible, state the limitation and make the fix conditional on evidence.

## Triage Questions

Ask or infer:

- What exact action triggers the bug?
- What did the user expect?
- What happened instead?
- Is it new or existing behavior?
- Does it affect all users or a segment?
- Is data lost, duplicated, exposed, or corrupted?
- Is there a failing test or log line?

Read `references/bug-cases.md` for example triage patterns.
