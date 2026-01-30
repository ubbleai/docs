# Create a face authentication

To create a face auhentication call the [Create a face authentication](#Wtag/Identity-verifications/operation/create_face_authentication) endpoint, and provide the following fields:
- `applicant_id` – The applicant id from the Create an applicant response
- `webhook_url` - The URL you want to be notified on
- `user_journey_id` – Your Face Authentication configuration ID

Make a note of the face authentication `id` value in the response. You'll need it to create an attempt and retrieve the detailed results.
