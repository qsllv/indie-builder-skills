# State Matrix Patterns

## File Upload

Required:

- Empty: explain accepted file type and show upload CTA.
- Uploading: disable duplicate upload and show progress.
- Validation error: explain file type, size, or missing columns.
- Partial success: show imported, skipped, and failed rows.
- Success: show import summary and next action.
- Error: keep selected context and offer retry.

## Table or List

Required:

- Loading skeleton.
- Empty state for no records.
- No-results state for filters.
- Error state with retry.
- Permission state if hidden by role.
- Long text handling.
- Pagination or loading more for large data.

## Form

Required:

- Initial state.
- Dirty state.
- Field validation.
- Submitting state.
- Submit success.
- Submit failure with preserved input.
- Cancel confirmation if unsaved changes matter.

## AI Task

Required:

- Waiting or queued.
- Generating.
- Generated.
- Failed with retry.
- Low confidence or missing context.
- User review before publish/send/delete.

## Destructive Action

Required:

- Confirmation showing affected object.
- Clear irreversible/reversible status.
- Disabled state while processing.
- Success confirmation.
- Failure with no false success.
- Undo when feasible.
