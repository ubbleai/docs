# Retrieve detailed results

To retrieve the detailed verification results, call the [Retrieve a website verification](#tag/Website-verifications-(Coming-soon)/operation/retrieve_website_verification) endpoint with the Website Verification `id` value returned in the Create a Website Verification response.

If the status of the verification is `approved` or `declined`, you will find all the information extracted from the website in the `website_data` object.
