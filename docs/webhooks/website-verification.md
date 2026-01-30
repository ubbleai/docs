# Website Verification

## Body

  The webhook body contains the following information: 

  {% table %}

  - Attribute
  - Description

  ---

  - applicant_id
  - ID of the Business Applicant, useful to recognize them

  ---

  - external_applicant_id
  - Your Business Applicant ID, only if you updated it in the Business Applicant object

  ---

  - user_journey_id
  - ID of the user journey

  ---

  - website_verification_id
  - ID of the website verification

  ---

  - status
  - Status of the website verification

  ---

  - response_codes
  - List of response codes

  {% /table %}


  **Example**
  
  ```json
    {
        "specversion": "2.0",
        "type": "website_verification_completed",
        "subject": "wbv_5hxpdwegjcbujpth3wdo55d3vm",
        "id": "evnt_5hxpdwegjcbujpth3wdo55d3vm",
        "time": "2023-03-22T17:31:00Z",
        "datacontenttype": "application/json",
        "data": {
            "external_applicant_id": "9fj3lz918bujpth3wdolmc74s",
            "applicant_id": "bplt_5hxpdwegjcbujpth3wdo55d3vm",
            "user_journey_id": "usj_5hxpdwegjcbujpth3wdo55d3vm",
            "website_verification_id": "wbv_5hxpdwegjcbujpth3wdo55d3vm",
            "status": "approved",
            "response_codes": [
                {"code": 10000, "summary": "approved"}
            ]
        }
    }
  ```

## Events

  {% table %}

  - Events
  - Description

  ---

  - `website_verification_created`
  - You created a website verification

  ---

  - `website_verification_checks_in_progress`
  - Checkout.com is analyzing the website and processing the verification

  ---

  - `website_verification_completed`
  - We completed the website verification checks

  ---

  - `website_verification_inconclusive`
  - The website verification result is inconclusive

  ---

  - `website_verification_closed`
  - The verification has been forcibly closed

  ---

  - `website_verification_anonymized`
  - The website verification has been anonymized

  {% /table %}
