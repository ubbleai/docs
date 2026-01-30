# Before you begin

- Set up your webhook receiver and prepare to [handle webhooks](../webhooks/index.md).
- Contact your account manager to obtain a configuration ID. 
- [Create a profile](../applicant-profiles/index.md) for the applicant whose identity you want to verify.

## Configuration

When you request an account, your account manager provides you a configuration ID, prefixed usj_. Provide this ID every time you create a verification. It configures the following elements of the solution:

- The service level agreement for receiving the result from Checkout.com
- Identity documents: 
    - The documents you want to accept, if supported by Checkout.com
    - Whether you require one document or two – primary and secondary
    - The data you want to extract from documents
- Whether you require a video of the applicant's face
- Processing type:
    - Fast – Highly automated processing, with human review if required
    - Expert – Systematic human review
    - Certified – Certified by the French Government for merchants with a French banking license
