# Create an applicant

To create an applicant, call the [Create an applicant](#tag/Applicants/operation/create_applicant) endpoint. 

Optionally, provide the following fields:

- `external_applicant_id` – Your identifier for this applicant
- `external_applicant_name` – The name of the applicant
- `email` – The applicant's email address

Make a note of the applicant `id` value in the response. You'll need it to create verifications later.

Once you have created an applicant, you can start creating verifications as described in the sections below.
You can [retrieve](#tag/Applicants/operation/retrieve_applicant) or [update](#tag/Applicants/operation/update_applicant) the profile.
If requested under the GDPR, you can [remove the applicant's personal data](#tag/Applicants/operation/anonymize_applicant) from the profile.

