# Verify webhook notifications

Once you've configured your webhook receiver, you'll be notified of events that occur during the identity verification flow via webhooks. 
For more details see the [Webhook](../webhooks/index.md) section. 

Depending on the scenario you would like to test, you should consider the following events: 

  {% table %}

  - #
  - Scenario
  - event type

  ---

  - 1
  - Approved verification
  - `identity_verification_checks_completed`

  ---

  - 2
  - Approved verification on retry after capture aborted
  - `identity_verification_capture_aborted`

  ---

  - 3
  - Approved verification on retry after checks inconclusive
  - `identity_verification_checks_inconclusive`

  ---

  - 4
  - Declined verification
  - `identity_verification_checks_completed`

  ---

  - 5
  - Declined verification on retry after capture aborted
  - `identity_verification_capture_aborted`

  ---

  - 6
  - Declined verification on retry after checks inconclusive
  - `identity_verification_checks_inconclusive`

  {% /table %}   

For the **Approved scenario**, webhook for the final verdict is triggered. 
The identity_verification_checks_completed webhook will return the status `approved` and the response code `10000`. 
You can call the [Retrieve an identity verification](#tag/Identity-verifications/operation/retrieve_identity_verification) endpoint to get the detailed results. 

For the **Declined scenario**, webhook for the final verdict is triggered. 
The identity_verification_checks_completed webhook will return the status `declined` and the response code starting with 62 that you passed as part of the `external_applicant_id`.
You can call the [Retrieve an identity verification](#tag/Identity-verifications/operation/retrieve_identity_verification) endpoint to get the detailed results. 

For other scenarios, the webhook will return the status `retry_required` and the response code starting with 61 that you passed as part of the `external_applicant_id`. 
For these scenarios you should create a new attempt.
