---
name: product-design-principles
description: Guide AI coding agents when designing, building, improving, or reviewing software product experiences, including product requirements, user flows, information architecture, onboarding, dashboards, forms, settings, empty/error/loading states, feedback, permissions, AI product UX, and feature implementation decisions. Use when Codex needs to make product design choices while coding, judge whether a feature workflow is usable, or ensure UI implementation follows practical product principles instead of only visual styling.
---

# Product Design Principles

## Purpose

Use this skill when building software products, not only static interfaces. The goal is to help the agent make product decisions while coding: what the user should see, what path they should follow, what states must exist, what feedback is required, and what should be simplified or deferred.

Treat product design as task design. A good product lets users complete a valuable job with low cognitive load, clear control, reliable feedback, and trust.

## Product Design Workflow

Before implementing or reviewing a product feature:

1. Identify the target user, job-to-be-done, trigger moment, and desired outcome.
2. Define the shortest path to first value.
3. Map the primary flow before adding secondary settings, advanced options, or edge cases.
4. Decide the main action for each screen or component.
5. Design required states: default, empty, loading, success, error, disabled, partial, permission-limited, and destructive-confirmation states.
6. Add feedback and recovery for every meaningful user action.
7. Verify the flow against the checklist in `references/product-ux-checklist.md`.

## Core Principles

### Solve a real task

Start from a user problem, not a feature inventory. If the user request is vague, infer the practical task the feature supports and state the assumption.

Ask:

- Who is using this?
- What are they trying to finish?
- What causes them to open this product?
- What does success look like?
- What current workaround is being replaced?

### Shorten time to first value

Optimize the path from arrival to meaningful result. Avoid forcing configuration, account setup, onboarding steps, or conceptual learning before the user can see why the product is useful.

Prefer:

- Demo data or sample output.
- Progressive setup.
- Sensible defaults.
- Inline guidance at the moment of use.
- One valuable first action.

### Structure around user tasks

Organize navigation, screens, and labels around what users want to do, not internal architecture, database models, or team ownership.

Prefer task labels like "Import feedback", "Review issues", "Send report", and "Invite teammates" over vague labels like "Management", "Configuration", "Smart Center", or "Resources".

### Make the main action obvious

Each screen should have one dominant job and one primary action. Secondary actions may exist, but they should not compete visually or conceptually with the primary action.

If a screen has many equal buttons, clarify the user intent or split the flow.

### Reveal complexity progressively

Default paths should work for common use cases. Advanced settings should be discoverable without blocking first use.

Use progressive disclosure for:

- Advanced filters.
- Optional configuration.
- Bulk actions.
- Technical controls.
- Rare destructive actions.
- Admin-only capabilities.

### Design every state

Do not only implement the happy path. Empty, loading, error, offline, no-permission, partial-data, and long-running states are part of the product.

Each non-happy state should explain:

- What happened.
- Why it happened if known.
- What the user can do next.
- Whether the action is retryable, reversible, or still processing.

### Give specific feedback

Every meaningful action should produce clear feedback. Avoid silent failures and generic messages.

Weak: "Error occurred."

Better: "The CSV is over 20MB. Compress it or upload a smaller file."

### Reduce memory burden

Make important context visible. Do not require users to remember previous choices, hidden rules, IDs, commands, or formats.

Use:

- Examples in inputs.
- Inline validation.
- Clear selected states.
- Summaries before confirmation.
- Persistent progress indicators.
- Human-readable names and timestamps.

### Preserve user control

Users should understand what the product is doing and be able to adjust, undo, cancel, or inspect important actions.

This is especially important for AI features, automations, payments, data deletion, messaging, publishing, and integrations.

### Maintain consistency

Use consistent names, button hierarchy, layouts, icon meanings, state colors, and confirmation patterns. Do not rename the same concept across screens.

### Build trust into the workflow

Trust comes from accurate previews, transparent limits, reversible actions, clear data handling, permission boundaries, and honest copy.

Avoid dark patterns:

- Hidden cancellation.
- Forced consent for unnecessary permissions.
- Ambiguous pricing.
- Preselected paid options.
- Misleading urgency.
- Overstated AI capability.

## AI Product Rules

When implementing AI features:

- Show input, output, and enough reasoning or source context for the user to judge quality.
- Make generated content editable unless immutability is required.
- Provide regenerate, refine, accept, copy/export, and undo paths where relevant.
- Indicate uncertainty, missing context, or limitations.
- Avoid presenting AI output as guaranteed truth.
- Keep users in control before sending, publishing, deleting, charging, or changing production data.

## Implementation Guidance

When coding product UI:

- Create stable, reachable flows before polishing visuals.
- Use existing design system components and patterns when present.
- Add the states and copy needed for real use, not just the ideal demo state.
- Keep forms short; group fields by decision, not database schema.
- Validate as early as possible and explain how to fix errors.
- Use safe defaults and make dangerous actions explicit.
- Ensure keyboard, focus, and screen-reader basics are not broken.
- Avoid placeholder-only interfaces that look complete but cannot complete the user's task.

For detailed implementation patterns, read `references/product-patterns.md`.

## Review Output Format

When reviewing or improving a product flow, return:

- Overall judgment: the biggest product experience issue.
- Primary user task: what the flow is supposed to help users complete.
- P0 issues: blockers to understanding, completion, trust, or data safety.
- P1 issues: usability, hierarchy, state, or feedback weaknesses.
- P2 issues: polish and optimization.
- Recommended changes: concrete UI, flow, copy, or implementation fixes.
- Missing states: list the states that must be implemented.

## Definition of Done

A product feature is not done until:

- The primary user task is clear.
- The first-value path is short and visible.
- The screen has a clear main action.
- Required states are implemented.
- User actions produce feedback.
- Errors are specific and recoverable where possible.
- Destructive or irreversible actions require confirmation.
- Labels match user language.
- The implementation supports real use, not only a polished screenshot.
