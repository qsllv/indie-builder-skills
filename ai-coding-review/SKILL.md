---
name: ai-coding-review
description: Review AI-generated code changes, pull requests, diffs, or implementation attempts for correctness, scope creep, regressions, missing states, security risks, product gaps, maintainability issues, and missing verification. Use when Codex needs to inspect code written by an AI agent or a rapid prototype before accepting, merging, or continuing development.
---

# AI Coding Review

## Purpose

Use this skill to review AI-written code with a skeptical engineering lens. Prioritize real bugs, regressions, unsafe behavior, and product completeness over style preferences.

## Review Workflow

1. Understand the intended change and user-facing behavior.
2. Inspect the diff or changed files before judging.
3. Check whether the implementation matches the requested scope.
4. Trace data flow, auth, error handling, states, and side effects.
5. Look for overbroad refactors, demo-only code, and placeholder behavior.
6. Verify tests or run relevant checks when possible.
7. Report findings first, ordered by severity.

## Severity

P0:
Data loss, security exposure, broken core flow, payment/auth failure, production crash, destructive behavior without safeguards.

P1:
Likely bug, missing required state, incorrect permissions, broken edge case, unhandled async failure, incomplete implementation.

P2:
Maintainability, clarity, duplication, weak tests, minor UX polish.

## Review Checklist

Check:

- Does the code actually satisfy the requested product behavior?
- Did the AI edit unrelated files or refactor without need?
- Are all user states handled: loading, empty, error, success, disabled, permission?
- Are server-side validation and permission checks present?
- Are secrets, tokens, or private data exposed?
- Are destructive, paid, publishing, or external side effects guarded?
- Are async failures handled?
- Does the implementation work with realistic data sizes and long text?
- Are tests updated or is manual verification clear?
- Are placeholders, mock data, or TODOs left in production paths?

## Required Output

Return:

- Findings first, ordered by severity.
- Each finding must include file and line when available.
- Explain impact, not just code style.
- Include suggested fix or direction.
- Then list verification performed.
- Then summarize residual risk.

If no issues are found, say so clearly and mention any test gaps.

## Review Style

Be concrete:

Good:
"P1: The import button remains enabled while upload is in progress, so users can submit duplicate imports."

Weak:
"The UX could be better."

Avoid broad rewrites unless the implementation is fundamentally wrong.

Read `references/review-rubric.md` for deeper review categories.
Read `references/review-case.md` for an example review.
