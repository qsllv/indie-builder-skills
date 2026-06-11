# Product UX Checklist

Use this checklist before shipping or reviewing a software feature.

## Severity

- P0: Blocks task completion, trust, safety, or comprehension.
- P1: Causes friction, confusion, avoidable mistakes, or weak adoption.
- P2: Improves polish, speed, accessibility, or consistency.

## 1. User Task

Pass if the feature clearly supports a user job.

Flag as P0 when:

- The user cannot tell what the screen is for.
- The feature exists because it is technically possible, not because it helps a task.
- The workflow has no clear success state.

Flag as P1 when:

- The task is real but buried under internal concepts.
- The screen mixes several unrelated jobs.

## 2. First Value

Pass if a new user can reach a meaningful result quickly.

Flag as P1 when:

- Onboarding asks too much before showing value.
- Empty products require manual setup without examples.
- Users must understand internal concepts before trying the product.

Good fixes:

- Add sample data.
- Add import shortcuts.
- Add a guided first action.
- Show a preview before requiring full setup.

## 3. Information Architecture

Pass if navigation and labels match user tasks.

Flag as P1 when:

- Labels reflect database objects, internal teams, or technical layers.
- Related actions are scattered across screens.
- Critical settings are hidden far from the workflow they affect.

## 4. Screen Hierarchy

Pass if each screen has one clear purpose and main action.

Flag as P1 when:

- Too many buttons have the same visual weight.
- Primary action is below low-priority metadata.
- Dangerous, secondary, and primary actions are visually similar.

## 5. Forms and Inputs

Pass if forms are short, grouped by user decision, and validated clearly.

Flag as P0 when:

- Required fields are unclear.
- Validation errors prevent completion without explaining how to fix them.
- Users can submit destructive or expensive actions by mistake.

Flag as P1 when:

- Field labels are internal or ambiguous.
- The form asks for data before explaining why it is needed.
- Examples, defaults, constraints, or accepted formats are missing.

## 6. States

Pass if the feature implements relevant states:

- Default
- Empty
- Loading
- Success
- Error
- Disabled
- No permission
- Partial data
- Offline or disconnected integration
- Long-running task
- Confirmation for destructive actions

Flag as P0 when:

- Error or loading states can trap the user.
- A destructive action has no confirmation or undo.
- Permission failures look like broken UI.

Flag as P1 when:

- Empty states do not explain how to start.
- Loading states provide no progress or expectation for long tasks.

## 7. Feedback and Recovery

Pass if every meaningful action tells the user what happened and what to do next.

Flag as P0 when:

- Saving, publishing, charging, deleting, or sending can fail silently.
- Users cannot recover from common mistakes.

Flag as P1 when:

- Error messages are generic.
- Success messages do not confirm the resulting state.
- Retry paths are missing.

## 8. Trust and Safety

Pass if risky actions are transparent and controlled.

Flag as P0 when:

- Users can lose data without warning.
- Payment, privacy, permission, or publishing actions are ambiguous.
- AI or automation can act on production data without user review.

Flag as P1 when:

- Pricing, cancellation, data use, or security details are hard to find.
- The product overstates certainty.

## 9. Consistency

Pass if concepts, patterns, and controls behave consistently.

Flag as P1 when:

- The same concept has multiple names.
- Buttons move unpredictably across similar screens.
- Icons or colors have inconsistent meaning.
- Similar flows use different confirmation patterns.

## 10. Accessibility Basics

Pass if the UI remains usable with keyboard and assistive technologies.

Flag as P1 when:

- Focus states are missing.
- Modals trap or lose focus incorrectly.
- Inputs have no labels.
- Color is the only way to understand state.
- Contrast is too low for core text and controls.

## 11. Real-Use Completeness

Pass if the implemented feature can complete the intended task with realistic data.

Flag as P0 when:

- The UI is mostly placeholder content.
- Buttons exist but do not perform the promised action.
- Realistic long names, empty data, large data sets, or failed requests break the flow.

Flag as P1 when:

- Edge cases are visually broken.
- Tables, cards, or charts cannot handle real content lengths.
