# Launch Audit Checklist

## Critical Flows

Define 3-7 flows that must work. Examples:

- Visitor opens landing page and signs up.
- User signs in and reaches dashboard.
- User completes the main product action.
- User pays or starts trial.
- User receives required email.
- User cancels or manages subscription.
- Admin can recover or inspect failed operations.

## Product States

Check:

- Empty state explains next action.
- Loading state prevents duplicate submit.
- Error state gives recovery path.
- Success state confirms result.
- No-permission state explains access.
- Destructive actions require confirmation.

## Auth

Check:

- Login, logout, signup, password reset or magic link.
- Protected routes redirect correctly.
- Logged-in users do not see irrelevant auth prompts.
- Permissions are enforced server-side, not only in UI.

## Payments

Check:

- Test checkout works.
- Success and cancel URLs work.
- Webhook verifies signature.
- Paid state is reflected in app.
- Failed payment or cancelled subscription is handled.
- Pricing page matches actual configured products.

## Email and Notifications

Check:

- Required transactional emails send.
- Sender/domain is configured.
- Email content has correct links.
- Unsubscribe exists for marketing emails.
- Failures are logged.

## SEO and Public Pages

Check:

- Title and meta description.
- Open Graph image.
- Canonical URL if needed.
- Sitemap and robots if relevant.
- 404 page.
- Terms/privacy when collecting user data.

## Analytics

Track at least:

- Visit landing page.
- Signup started.
- Signup completed.
- Activation event.
- Payment started.
- Payment completed.
- Core feature used.

Avoid tracking sensitive content.

## Security and Config

Check:

- No secrets in client bundle or repo.
- Production env vars exist.
- Webhooks validate signatures.
- User input is validated server-side.
- File uploads have size/type limits.
- Rate limits exist for costly or abuse-prone endpoints.

## Deployment

Check:

- Build passes.
- Tests or smoke checks pass.
- Database migrations are safe.
- Background jobs are configured.
- Error logging is active.
- Rollback plan exists.
