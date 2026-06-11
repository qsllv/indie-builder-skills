# Product Patterns

Use these implementation patterns when designing product screens and flows.

## Onboarding

Goal: get the user to first value quickly.

Prefer:

- One guided first action.
- Demo data or examples.
- Optional setup steps.
- Progress indicators only when there are meaningful steps.
- Skip paths for users who already know what they need.

Avoid:

- Long tours before value.
- Asking for integrations before showing the outcome.
- Empty dashboards with no next action.

## Dashboard

Goal: show status, priority, and next actions.

A good dashboard answers:

- What changed?
- What needs attention?
- What is healthy or unhealthy?
- What should I do next?

Avoid turning dashboards into decorative metric grids. Every chart or card should support a decision.

## Lists and Tables

Goal: help users find, compare, and act on records.

Include:

- Search or filtering when data can grow.
- Sorting for important columns.
- Row-level actions.
- Bulk actions when users repeat the same action.
- Empty and no-results states.
- Clear pagination, infinite scroll, or load-more behavior.

Avoid:

- Hiding primary identifiers.
- Making every row visually heavy.
- Using icons without labels for unfamiliar actions.

## Detail Pages

Goal: help users understand one object and act on it.

Include:

- Clear title and status.
- Key metadata.
- Primary action.
- History or activity when relevant.
- Related records or dependencies.
- Dangerous actions separated from routine actions.

## Forms

Goal: collect correct information with minimal friction.

Use:

- Human labels.
- Inline examples.
- Sensible defaults.
- Field grouping by decision.
- Real-time validation for format issues.
- Submit-time validation for server or business rules.
- Clear cancel and save behavior.

Avoid:

- Mirroring database fields directly.
- Asking for optional data too early.
- Resetting user input after validation errors.

## Settings

Goal: let users adjust behavior without making the product feel fragile.

Use:

- Grouping by user intent.
- Short descriptions for risky settings.
- Save confirmation.
- Reset or restore defaults where useful.
- Permission-aware visibility.

Avoid:

- Dumping all configuration into one page.
- Using technical names without explanation.
- Applying high-impact changes without confirmation.

## Empty States

Goal: explain why nothing is shown and what to do next.

Include:

- Reason for emptiness.
- Primary next action.
- Example of what will appear after setup.

Examples:

- "No feedback imported yet. Upload a CSV to group customer messages by theme."
- "No matching results. Try removing the date filter or searching by customer name."

## Loading and Long-Running Tasks

Goal: prevent uncertainty.

Use:

- Skeletons for short loading.
- Progress or step messaging for long tasks.
- Background processing when the user can leave.
- Completion notification or status record.

Avoid:

- Infinite spinners for operations longer than a few seconds.
- Letting users submit the same action repeatedly.

## Error States

Goal: help the user recover.

A useful error says:

- What failed.
- Why it likely failed.
- Whether anything was saved.
- What to do next.

Examples:

- "We could not connect to Stripe because the API key is invalid. Paste a live secret key and try again."
- "The report was not sent. Your changes are saved as a draft."

## Destructive Actions

Goal: prevent irreversible mistakes.

Require confirmation when actions delete, publish, charge, send, overwrite, revoke access, or change production data.

Confirmation should show:

- Object name.
- Impact.
- Whether the action can be undone.
- Safer alternative if one exists.

For high-risk actions, require typed confirmation or an explicit checkbox.

## AI Features

Goal: make automation useful without removing user control.

Include:

- Source context or inputs used.
- Editable output.
- Regenerate/refine options.
- Accept/reject path.
- Confidence, limitations, or missing data where relevant.
- Review before external side effects.

Avoid:

- Sending AI-generated content without preview.
- Hiding why the AI reached a conclusion.
- Blocking manual correction.

## Permissions

Goal: make access rules understandable.

Use:

- Role names users recognize.
- Clear explanation for disabled controls.
- Requests for access when possible.
- Audit trails for sensitive actions.

Avoid:

- Showing broken screens for missing permissions.
- Hiding everything without explaining why.
