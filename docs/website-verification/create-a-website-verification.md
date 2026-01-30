# Create a Website Verification

To create a Website Verification, call the [Create a website verification](#tag/Website-verifications-(Coming-soon)/operation/create_website_verification) endpoint, and provide the following fields:

- `applicant_id` – The Business Applicant ID from the Create a Business Applicant response
- `website_url` - The URL of the Business Applicant website
- `user_journey_id` – Your configuration ID
- `webhook_url` - The URL you want to be notified on

Make a note of the Website Verification `id` value in the response. You'll need it to retrieve the detailed results.
