# Retrieve detailed results

To retrieve the detailed verification results, call the [Retrieve an identity verification](#tag/Identity-verifications/operation/retrieve_identity_verification) endpoint with the identity verification id value returned in the Create an identity verification response. 

If the status of the verification is `approved` or `declined`, you will find all the information extracted from the document in the `document` object. 

You will also receive the `identity_verification_report_created` event. 
Call the [Retrieve PDF report](#tag/Identity-verifications/operation/pdf_identity_verification) to retrieve a PDF report containing all the information of the identity verification.
