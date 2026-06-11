# User Flow Patterns

## Import Flow

Happy path:

1. User opens source page.
2. User clicks Import.
3. User selects file or connects source.
4. System validates input.
5. User maps fields if needed.
6. System imports data.
7. User sees summary and next action.

Required states:

- Empty source.
- Uploading.
- Parsing.
- Mapping required.
- Partial success.
- Error.
- Retry.

## Onboarding Flow

Goal: reach first value quickly.

Pattern:

1. Ask for only the information needed to personalize or create first value.
2. Offer demo data or skip path.
3. Guide one meaningful action.
4. Show success and next step.

Avoid multi-step tours before usefulness is visible.

## Checkout Flow

Pattern:

1. User hits upgrade trigger.
2. Product explains limit or paid value.
3. User selects plan.
4. Checkout opens.
5. Payment succeeds or fails.
6. App reflects entitlement.

Required states:

- Checkout loading.
- Payment canceled.
- Payment failed.
- Webhook pending.
- Paid access active.

## Invite Flow

Pattern:

1. User opens team settings.
2. User enters email and role.
3. System validates permission.
4. Invite sends.
5. Invitee accepts and joins correct workspace.

Edge cases:

- Existing member.
- Expired invite.
- No permission to invite.
- Seat limit reached.

## AI Generation Flow

Pattern:

1. User provides input.
2. Product confirms or previews input.
3. AI generates result.
4. User reviews output.
5. User edits, accepts, regenerates, exports, or rejects.

Do not skip review before external side effects.
