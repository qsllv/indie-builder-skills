# New User Product Review Rubric

Use this rubric when a review needs more depth than the default workflow.

## 1. Understanding

Check whether a new user can answer:

- What is this product, page, or feature?
- Who is it for?
- What problem does it solve?
- What result will I get?
- Why does this matter now?
- What is the difference between this and similar-looking tools?

Common problems:

- The page leads with a slogan instead of a product category or use case.
- The UI exposes internal concepts before user outcomes.
- The screen title names a system object rather than a user task.
- The first viewport has multiple competing messages.
- Important context is hidden behind hover, docs, or settings.

Good fixes:

- Name the product category or task plainly.
- Put the primary outcome near the main action.
- Replace internal labels with task labels.
- Add a short example or sample result.
- Show one concrete workflow instead of a generic feature grid.

## 2. Action

Check whether the next step is obvious and safe:

- Is there one primary action?
- Does the primary button describe the action or result?
- Does the user know what happens after clicking?
- Is setup deferred until needed?
- Are irreversible or expensive actions clearly marked?
- Can users back out, skip, undo, or try with sample data?

Common problems:

- Multiple equally prominent CTAs.
- Buttons like "Submit", "Continue", "Confirm", or "Get Started" without context.
- Required setup appears before value is visible.
- Disabled buttons do not explain what is missing.
- The first action feels risky because impact is unclear.

Good fixes:

- Use action-specific button labels.
- Put setup behind progressive disclosure.
- Add previews or sample data.
- Explain disabled states inline.
- Add confirmation for destructive or external actions.

## 3. Discovery

Check whether users can find the product's important capabilities:

- Are core features visible from the first-use path?
- Are navigation labels based on user tasks?
- Are advanced controls hidden without hiding essential controls?
- Are similar actions grouped logically?
- Does the product teach key concepts when they become relevant?

Common problems:

- Feature names depend on company jargon.
- Navigation mirrors data models or team structure.
- Important functions only appear after data exists.
- Empty states fail to reveal what the product can do.
- The UI assumes users know the order of operations.

Good fixes:

- Rename navigation around user jobs.
- Use empty states to expose the first action.
- Add inline examples near complex controls.
- Make first-use checklists short and task-based.
- Put advanced settings behind "Advanced" or secondary controls.

## 4. Feedback And States

Check whether the product tells users what happened:

- Loading: Does the user know progress, wait time, or background status?
- Empty: Does the user know why it is empty and how to start?
- Success: Does the user know what changed and what to do next?
- Error: Does the user know the cause and recovery path?
- Permission: Does the user know who can grant access or what plan is needed?
- Long-running tasks: Can the user leave, cancel, retry, or inspect status?

Common problems:

- Silent actions.
- Generic errors like "Something went wrong."
- Empty tables with no explanation.
- Success messages that disappear before users understand the result.
- AI generation, import, sync, or payment states without progress or recovery.

Good fixes:

- Add state-specific messages with next actions.
- Persist important status until resolved.
- Provide retry and contact/support paths when useful.
- Show partial results when full completion is slow.
- Explain what data was changed, created, sent, deleted, or charged.

## 5. Copy

Check whether the copy is clear, specific, and actionable:

- Does it use user language instead of internal language?
- Does it avoid vague claims and filler?
- Does each heading help users decide what to do?
- Does every button say what action will happen?
- Does helper text explain constraints before the user fails?

Common problems:

- Marketing copy inside operational screens.
- Abstract terms like "optimize", "streamline", "unlock", or "manage" without specifics.
- Feature labels that sound similar but behave differently.
- Error text that blames the user.
- Tooltips used to hide essential information.

Good fixes:

- Replace claims with concrete outcomes.
- Put examples inside complex inputs.
- Name objects consistently.
- Write errors as cause plus recovery.
- Keep button labels short but specific.

For detailed copy patterns, use `copy-clarity-checklist.md`.

## 6. Trust

Check whether users feel safe continuing:

- Does the product explain data access, sharing, publishing, deletion, and billing impact?
- Are AI outputs presented with appropriate uncertainty or source context?
- Are users warned before irreversible actions?
- Are limits, trials, credits, and upgrades transparent?
- Are permissions requested only when needed?
- Are users shown previews before sending, posting, charging, or deleting?

Common problems:

- Asking for broad permissions before value is clear.
- Hiding pricing, usage limits, or credit consumption.
- Presenting generated content as guaranteed truth.
- Destructive actions without object names or impact.
- External sends, publishes, syncs, or automations without preview.

Good fixes:

- Explain why a permission is needed at the moment of request.
- Show previews and summaries before high-impact actions.
- Add reversible paths where possible.
- Make pricing and limits visible before commitment.
- Cite sources or show confidence limits for AI-heavy workflows.
