# Manage retries

Once you have receceived the `identity_verification_capture_aborted` or `identity_verification_checks_inconclusive` events, you can request a retry. 

To do that you should create a new attempt using the [Create an attempt](#tag/Identity-verifications/operation/create_attempt) endpoint. 
You'll be notified of events that occur during this second attempt flow via webhooks and a `identity_verification_checks_completed` webhook will be triggered with the final verdict. 

For the **Approved verification on retry after capture aborted**, the identity_verification_checks_completed webhook will return the status `approved` and the response code `10000`. 
You can call the [Retrieve an identity verification](#tag/Identity-verifications/operation/retrieve_identity_verification) endpoint to get the detailed results. 

For the **Approved verification on retry after checks inconclusive**, the identity_verification_checks_completed webhook will return the status `approved` and the response code `10000`. 
You can call the [Retrieve an identity verification](#tag/Identity-verifications/operation/retrieve_identity_verification) endpoint to get the detailed results. 

For the **Declined verification on retry after capture aborted**, the identity_verification_checks_completed webhook will return the status `declined` and the response code starting with 62 that you passed as part of the `external_applicant_id`.
You can call the [Retrieve an identity verification](#tag/Identity-verifications/operation/retrieve_identity_verification) endpoint to get the detailed results. 

For the **Declined verification on retry after checks inconclusive**, the identity_verification_checks_completed webhook will return the status `declined` and the response code starting with 62 that you passed as part of the `external_applicant_id`.
You can call the [Retrieve an identity verification](#tag/Identity-verifications/operation/retrieve_identity_verification) endpoint to get the detailed results.
