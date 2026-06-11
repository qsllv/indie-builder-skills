# Events And Feedback

## Example: AI Feedback Analyzer

Core question:
Do users reach a useful analysis result?

Funnel:

- landing_page_viewed
- signup_completed
- feedback_import_started
- feedback_import_completed
- analysis_started
- analysis_completed
- result_exported
- upgrade_clicked
- checkout_completed

Activation event:
analysis_completed with at least 3 themes and 1 example quote per theme.

Retention signal:
User runs another analysis or returns to view/export results within 7 days.

Useful properties:

- import_source: csv, paste, integration
- feedback_count_bucket: 1-50, 51-200, 201-1000
- analysis_duration_bucket
- result_theme_count
- plan: free, pro

Avoid:

- Tracking raw feedback content.
- Tracking customer names or emails inside event properties.

## Feedback Capture

Ask after value moment:

- "Was this analysis useful?"
- "What theme was wrong or missing?"
- "What would you do next with this result?"

Ask after failed or abandoned flow:

- "What stopped you from finishing?"
- "Was anything unclear?"

## Decision Rules

- If many users start import but few complete it: fix input and validation.
- If users complete analysis but do not export/share: result may not be actionable.
- If users hit limits but do not upgrade: pricing boundary or upgrade copy may be wrong.
- If users return weekly: invest in saved history and automation.
