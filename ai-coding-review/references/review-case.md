# Review Case

Scenario:
An AI added CSV import to a feedback app.

Example findings:

P1: Duplicate import risk
The upload button stays enabled during the upload request. A user can click twice and create duplicate feedback records. Disable the button while uploading and make the server operation idempotent by import ID or file hash.

P1: Missing server-side permission check
The UI hides import controls from viewers, but the API route does not check workspace role. A viewer could call the endpoint directly. Add server-side role enforcement before parsing the file.

P1: Partial failure not handled
If 20 rows fail validation and 80 succeed, the UI only says "Import failed." Users lose useful information. Return imported, skipped, and failed counts, and let users download failed rows.

P2: Weak empty state
The empty page says "No data." It should tell users to upload a CSV and mention what will appear after import.

Verification:

- Test valid CSV.
- Test missing feedback column.
- Test viewer role hitting API.
- Test double-click upload.
- Test partial invalid rows.
