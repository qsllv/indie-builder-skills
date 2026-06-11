# Example Plan

Feature request:
"Add CSV import for customer feedback."

Feature summary:
Users can upload a CSV of feedback messages and see an import summary before analysis.

User flow:

1. User opens Feedback page.
2. User clicks Import CSV.
3. User selects a CSV file.
4. System validates file type, size, and required columns.
5. User maps the feedback text column if needed.
6. System imports rows and shows counts: imported, skipped, failed.
7. User starts analysis.

Impacted areas:

- UI: Feedback page, import modal, column mapping step, import summary.
- API: Upload endpoint, validation endpoint, import endpoint.
- Data: FeedbackImport, FeedbackItem.
- Permissions: Only workspace owners or editors can import.
- States: empty, uploading, parsing, mapping required, success, partial success, error.

Build phases:

1. Add data types and server validation.
2. Implement upload/import API.
3. Add import modal with states.
4. Render import summary and retry path.
5. Add tests for valid CSV, missing column, large file, partial failures.

Manual verification:

- Upload valid CSV.
- Upload non-CSV.
- Upload CSV with missing feedback column.
- Upload CSV with 1000 rows.
- Confirm failed rows do not block successful rows unless required.
