# Create an ID Document Verification

To create an ID Document verification, call the Create an ID Document Verification endpoint, and provide the following fields:
- `applicant_id` – The applicant id from the Create an applicant response
- `declared_data.name` (optional) – The applicant's name to be compared with the extracted name
- `webhook_url` (optional) - The URL you want to be notified on
- `user_journey_id` – Your specific configuration ID

Make a note of the ID Document Verification `id` value in the response. You'll need it to create an attempt and retrieve the detailed results.
