# Copy Clarity Checklist

Use this checklist when reviewing or rewriting product UI copy for first-time users.

## Headings

Good headings answer one of these:

- What is this screen?
- What task can I complete here?
- What result will I get?
- What decision do I need to make?

Weak:

- "Dashboard"
- "Smart Center"
- "Management"
- "Configuration"
- "Unlock your potential"

Better:

- "Review customer feedback"
- "Create your first report"
- "Connect a data source"
- "Choose what the automation can change"
- "Import feedback to find common themes"

## Buttons

Button copy should name the action or outcome.

Weak:

- Submit
- Continue
- Confirm
- Save
- Get Started

Better:

- Upload CSV
- Create report
- Connect Slack
- Send test email
- Save billing address
- Analyze feedback
- Invite teammates

Use "Continue" only when the surrounding step label makes the next action obvious.

## Empty States

An empty state should explain:

1. Why it is empty.
2. What value appears after starting.
3. The first action.

Pattern:

`No [objects] yet. [Short value explanation]. [Primary action].`

Example:

`No feedback imported yet. Upload a CSV to group customer messages by theme.`

Avoid:

- "No data."
- "Nothing here yet."
- Blank tables.
- Empty illustrations without action.

## Errors

An error should explain cause plus recovery.

Pattern:

`We could not [action] because [cause]. [How to fix or retry].`

Examples:

- `We could not import the CSV because the feedback column is missing. Choose a column and try again.`
- `Slack disconnected before we could send the alert. Reconnect Slack and retry.`
- `This file is over 20MB. Upload a smaller file or split it into multiple files.`

Avoid:

- "Something went wrong."
- "Invalid input."
- "Failed."
- "Please try again" without a likely cause.

## Success Messages

A success message should confirm what changed and optionally offer the next step.

Pattern:

`[Object/action] completed. [Next useful step].`

Examples:

- `Report created. Review the summary before sharing it.`
- `CSV imported. We found 126 feedback items across 8 themes.`
- `Teammate invited. They will get an email with workspace access.`

## Confirmation Dialogs

A confirmation should name:

- The object.
- The impact.
- Whether it can be undone.
- The exact destructive action.

Weak:

`Are you sure?`

Better:

`Delete "Q2 Customer Feedback"? This removes the report for everyone in the workspace. This cannot be undone.`

Use destructive button labels such as:

- Delete report
- Remove integration
- Cancel subscription
- Revoke access

## AI Feature Copy

AI copy should preserve user control.

Prefer:

- "Generate draft"
- "Review sources"
- "Regenerate summary"
- "Apply suggestion"
- "This may miss details. Review before sending."

Avoid:

- "Guaranteed accurate"
- "Fully automated"
- "No review needed"
- "Perfect results"

## Upgrade And Limit Copy

Upgrade prompts should be transparent:

- What limit was reached?
- What can the user still do?
- What changes after upgrading?

Example:

`You have used 3 of 3 monthly reports. Upgrade to create more reports, or wait until your limit resets on July 1.`

Avoid hidden pressure, false urgency, or implying the product is broken when the user has reached a plan limit.
