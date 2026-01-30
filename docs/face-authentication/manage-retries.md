# Manage retries

If the first attempt is unsuccessful and the authentication status changes to `retry-required`, you can create a new attempt for the user to retry the flow.
You can use the [Create an attempt](#tag/Face-authentication/operation/create_attempt) endpoint. 

We recommend sharing guidance from the [response codes](../reference-info/response-codes.md) with the applicant to help them succeed in their next attempt. 
For example, if the user's data connection is poor, let them know so they can try to improve it.

If authentication status changes to `declined`, you will have to create a new face authentication if you want to allow the applicant to retry.
