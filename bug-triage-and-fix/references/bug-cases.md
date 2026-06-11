# Bug Cases

## Case 1: Duplicate Submit

Report:
"Clicking Import twice creates duplicate feedback rows."

Evidence:

- Import button remains enabled while request is pending.
- API does not use idempotency key or import hash.

Root cause:
Client allows duplicate submit and server accepts duplicate imports.

Fix:

- Disable button while uploading.
- Add import request ID or file hash dedupe server-side.
- Show "Importing..." state.

Verification:

- Double-click import button.
- Retry after failed import.
- Upload same file twice intentionally and confirm expected behavior.

## Case 2: Permission Leak

Report:
"Viewer can call API route and import data."

Evidence:

- UI hides button for viewers.
- API route checks session but not workspace role.

Root cause:
Authorization is enforced only in UI.

Fix:

- Add server-side role check.
- Return 403 with useful message.
- Add test for viewer role.

Verification:

- Viewer cannot import through UI.
- Viewer receives 403 when calling API.
- Editor still can import.

## Case 3: Lost Form Input

Report:
"After save fails, all form data disappears."

Evidence:

- Error handler resets form state.
- Server returns validation error after submit.

Root cause:
Client clears state before confirmed success.

Fix:

- Preserve dirty form values until successful save.
- Show field-level or form-level error.

Verification:

- Submit invalid data.
- Confirm values remain.
- Fix field and resubmit successfully.
