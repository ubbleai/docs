# Retrieve detailed results

To retrieve the detailed verification results, call the Retrieve an ID Document Verification endpoint with the ID Document Verification id value returned in the Create an ID document verification response. 

If the status of the verification is `approved` or `declined`, you will find all the information extracted from the document in the `document` object. 

You will also receive the `id_document_verification_report_created` event. 
Call the Retrieve PDF report to retrieve a PDF report containing all the information of the ID Document Verification.
