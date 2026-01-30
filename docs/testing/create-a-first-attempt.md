# Create a first attempt

Create an identity verification by calling  the [Create an identity verification](#tag/Identity-verifications/operation/create_identity_verification) endpoint. 
Set the `id` you received in the Create an applicant response as the `applicant_id` value. Make a note of the identity verification `id` value in the response. 

You can then create a first attempt by calling the [Create an attempt](#tag/Identity-verifications/operation/create_attempt) endpoint. 
Pass the `id` value from Create an identity verification response as the `identity_verification_id` path parameter.
