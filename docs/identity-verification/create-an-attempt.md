# Create an attempt

To create an attempt, call the [Create an attempt](#tag/Identity-verifications/operation/create_attempt) endpoint with the `identity_verification_id` and provide the following fields:
- `redirect_url` – Provide your return page URL to redirect the applicant to after completing the verification.
- Optionally `client_information` object – Used to pre-select fields in the web flow. This shortens the web flow and improves the experience.
