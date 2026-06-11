# AI Coding Review Rubric

## Scope Control

Flag when:

- The change edits unrelated modules.
- The AI rewrites working code without a functional reason.
- New abstractions are introduced for a single use.
- Dependencies are added without clear need.

## Product Completeness

Flag when:

- The happy path works but empty/error/loading states are missing.
- Buttons or links are present but not wired.
- The UI uses mock data in production code.
- The feature cannot complete the user's task end-to-end.

## Data and Auth

Flag when:

- Authorization exists only in UI.
- Users can access or mutate another user's data.
- Ownership is not checked on server operations.
- Input validation relies only on client code.

## Reliability

Flag when:

- Async operations can fail silently.
- Race conditions can cause duplicate writes.
- Long-running operations have no progress or retry.
- Network failures leave the UI in a stuck state.

## Security

Flag when:

- Secrets appear in client code or logs.
- Webhooks do not verify signatures.
- File uploads lack type or size limits.
- User-provided HTML is rendered unsafely.
- Payment or subscription state can be spoofed.

## Maintainability

Flag when:

- Business logic is duplicated across client and server.
- Components become too large to reason about.
- Naming hides intent.
- Error handling is inconsistent with local patterns.

## Verification

Look for:

- Unit tests for pure logic.
- Integration tests for API/database behavior.
- E2E or manual steps for critical user flows.
- Regression tests for fixed bugs.

If tests are missing, state the risk and the minimum useful test.
