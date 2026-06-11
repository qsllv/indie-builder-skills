# Pricing Patterns

## Model Selection

Use subscription when:

- Value repeats monthly.
- Product stores data or automates ongoing work.
- Teams use it continuously.

Use one-time purchase when:

- Product is a template, small tool, course, asset, or downloadable product.
- Ongoing server cost is low.

Use usage-based or credits when:

- Costs scale with usage, such as AI generation, email sending, or data processing.
- Power users receive much more value than light users.

Use freemium when:

- Users can self-serve.
- Activation is fast.
- Free users can become a distribution channel.

Use free trial when:

- Product value needs real access.
- Ongoing use should become paid after evaluation.

## Free/Paid Boundary Examples

AI feedback tool:

- Free: analyze 100 feedback messages once.
- Pro: more messages, saved projects, exports, weekly reports, integrations.

Resume tool:

- Free: one analysis.
- Pro: unlimited analyses, job-specific tailoring, PDF export.

Developer tool:

- Free: local use or small project.
- Pro: team projects, CI integration, history, alerts.

## Upgrade Triggers

Good upgrade triggers:

- User hits usage limit after seeing value.
- User tries to export, automate, integrate, or collaborate.
- User needs to save history or use more projects.

Weak upgrade triggers:

- Block core value before the user understands it.
- Interrupt onboarding before first result.
- Hide essential trust features behind paid plans.

## Billing States

Implement:

- Free
- Trialing
- Active paid
- Past due
- Canceled but active until period end
- Canceled and expired
- Payment failed
- Checkout canceled
- Webhook pending

Do not rely only on client-side payment success redirects.
