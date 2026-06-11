# Scope Cut Cases

## Case 1: Feedback Analyzer

Proposed features:

- CSV upload
- Slack integration
- Intercom integration
- AI clustering
- Export to Notion
- Team comments
- Multi-workspace permissions
- Weekly email digest
- Billing

Core promise:
"Turn scattered feedback into ranked themes."

First-value event:
User uploads or pastes feedback and sees grouped themes with example quotes.

Decisions:

- CSV upload: Must. It enables first input.
- Paste text: Must if CSV parsing is not reliable yet.
- AI clustering: Must. It creates core value.
- Example quotes: Must. It builds trust in the result.
- Export to Notion: Later. Copy/export Markdown is enough.
- Slack integration: Later. Manual CSV export from Slack can work.
- Intercom integration: Later. Founder can onboard first users manually.
- Team comments: Remove for MVP. Single-player use case comes first.
- Multi-workspace permissions: Remove for MVP unless selling to teams immediately.
- Weekly digest: Later. Needs repeated usage first.
- Billing: Must only if charging from day one; otherwise Later.

Reduced MVP:
Paste or upload feedback, analyze themes, show ranked list, quote examples, copy/export result.

## Case 2: AI Resume Reviewer

Keep:

- Upload resume.
- Paste job description.
- Generate score and specific improvement suggestions.
- Download revised bullet suggestions.

Defer:

- Full resume builder.
- Multiple templates.
- Recruiter marketplace.
- LinkedIn sync.
- Interview coaching.

Reason:
The first value is knowing how to improve one resume for one job. Everything else expands the product into a career platform.
