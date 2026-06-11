# Case Guide

## Example: AI Feedback Analyzer

Raw idea:
"I want to build a tool that uses AI to analyze customer feedback."

Better product framing:

- Target user: indie SaaS founders and product managers.
- Trigger moment: after collecting feedback from support, chat, surveys, or app reviews.
- Current workaround: manually reading messages and copying patterns into spreadsheets.
- Pain: repeated issues are easy to miss; prioritization is based on memory.
- Desired outcome: know the most repeated problems and which ones are worth fixing.

Core promise:
"Help indie SaaS founders turn scattered customer feedback into a ranked issue list without reading every message manually."

MVP must have:

- Upload CSV or paste text feedback.
- Extract themes and repeated issues.
- Show ranked themes with example quotes.
- Allow export or copy of the issue list.
- Show empty, loading, error, and success states.

Later:

- Slack integration.
- Intercom integration.
- Team comments.
- Revenue-weighted prioritization.
- Automated weekly reports.

Not now:

- Full CRM.
- Roadmap voting portal.
- Multi-workspace enterprise permissions.

Acceptance criteria:

- When a user uploads a valid CSV with feedback text, the app groups messages into themes and shows at least one example quote per theme.
- If the CSV has no recognized feedback column, the app asks the user to map the column.
- If analysis fails, the app keeps the uploaded file state and provides a retry action.
