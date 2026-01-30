# Create an identity verification

To create an identity verification, call the [Create an identity verification](#tag/Identity-verifications/operation/create_identity_verification) endpoint, and provide the following fields:
- `applicant_id` – The applicant id from the Create an applicant response
- `declared_data.name` – The applicant's name to be compared with the extracted name
- `webhook_url` - The URL you want to be notified on
- `user_journey_id` – Your configuration ID

Make a note of the identity verification `id` value in the response. You'll need it to create an attempt and retrieve the detailed results.
