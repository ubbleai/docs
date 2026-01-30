# Introduction

Welcome to [Checkout.com](https://www.checkout.com/) Identities API documentation. 

The Identities solutions enable you to verify identities, perform anti-money laundering (AML) screenings, and authenticate with biometrics. This helps meet compliance requirements and reduce the risk of fraud.

- [Applicants](/docs/applicant-profiles) – Create a profile for each physical person applying to use your services, where you can manage their identity.
- [Business Applicants](/docs/business-applicant-profiles) – Create a profile for each business entity applying to use your services.
- [Identity Verification](/docs/identity-verification) – Verify an applicant's identity using their identity document and face.
- [ID Document Verification](/docs/id-document-verification) - Alternatively verify applicant's identity using document images. 
- [AML Screening](/docs/aml-screening) – Check if an applicant appears in politically exposed persons, sanctions, or adverse media databases.
- [Face Authentication](/docs/face-authentication) – Confirm an applicant is who they say using facial biometrics.
- [Website Verification](/docs/website-verification) (Coming soon) – Verify a business' website compliance and extract relevant information from the website.

The dedicated IDV Dashboard enables you to view and manage your identities activity, data, and metrics.

## Before You Begin

- Contact your Account Manager or email support.idv@checkout.com to obtain a test account. 
- Access the [dashboard](https://dashboard.ubble.ai/) to create your API credentials:
    - Generate your mutual Transport Layer Security (mTLS) certificate in the "API credentials" tab
    - Include your mTLS certificate in all API calls
- Define a [webhook URL](/docs/webhooks) to receive identity verification event notifications.

### Example API Calls (TO DELETE AFTER TESTING)

Here are examples to test the API.

{% code-group %}
  ```js {% title="index.js" %}
  import { foo } from "./foo.js";
  console.log("Hello, JavaScript!"); // comment
  ```

  ```js {% title="foo.js" %}
  export const foo = "foo";
  ```

  ```python {% title="index.py" %}
  print("Hello, Python!")
  ```

  ```curl {% title="index.curl" %}
  curl -X POST https://api.ubble.ai/identity-verifications \
  -H "Content-Type: application/json" \
  -d '{"external_applicant_id": "eaplt_10000000000000000000000000"}'
  ```
{% /code-group %}