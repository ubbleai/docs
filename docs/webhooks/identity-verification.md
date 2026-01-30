# Identity Verification

## Body

  The webhook body contains the following information: 

  {% table %}

  - Attribute
  - Description

  ---

  - applicant_id
  - ID of the applicant, useful to recognize them

  ---

  - external_applicant_id
  - Your applicant ID, only if you updated it in the applicant object

  ---

  - user_journey_id
  - ID of the user journey

  ---

  - identity_verification_id
  - ID of the identity verification

  ---

  - status
  - status of the identity verification

  ---

  - response_codes
  - list of response codes

  {% /table %}


  **Example**
  
  ```json
    {
        "specversion": "2.0",
        "type": "identity_verification_capture_completed",
        "subject": "idv_5hxpdwegjcbujpth3wdo55d3vm",
        "id": "evnt_5hxpdwegjcbujpth3wdo55d3vm",
        "time": "2023-03-22T17:31:00Z",
        "datacontenttype": "application/json",
        "data": {
            "external_applicant_id": "9fj3lz918bujpth3wdolmc74s"
            "applicant_id": "aplt_5hxpdwegjcbujpth3wdo55d3vm",
            "user_journey_id": "usj_5hxpdwegjcbujpth3wdo55d3vm",
            "identity_verification_id": "idv_5hxpdwegjcbujpth3wdo55d3vm",
            "status": "declined",
            "response_codes": [
                {"code": 62301, "summary": "document_counterfeit"},
                {"code": 62304, "summary": "face_mismatch"}
  
            ]
        }
    }
  ```

## Events

  {% table %}

  - Events
  - Description

  ---

  - `identity_verification_created`
  - You created an identity verification

  ---

  - `identity_verification_opened`
  - You created a first attempt and the verification URL is available

  ---

  - `identity_verification_started`
  - The applicant has been redirected to the web application

  ---

  - `identity_verification_reset`
  - You created a new attempt while the status was `pending` or `capture_in_progress`

  ---

  - `identity_verification_capture_completed`
  - The applicant completed the capture

  ---

  - `identity_verification_checks_completed`
  - We completed the checks

  ---

  - `identity_verification_link_expired`
  - The link expired without applicant being redirected to the web application, please note the default expiration time is 15 minutes

  ---

  - `identity_verification_capture_refused`
  - The applicant explicitly refused to perform the verification

  ---

  - `identity_verification_capture_aborted`
  - The applicant terminated the capture without completing it

  ---

  - `identity_verification_checks_inconclusive`
  - The applicant did not provide the assets required to perform the checks

  ---

  - `identity_verification_retry_requested`
  - You requested a retry for this identity verification

  ---

  - `identity_verification_closed`
  - The verification has been forcibly closed

  ---

  - `identity_verification_anonymized`
  - The verification has been anonymized

  ---

  - `identity_verification_audit_completed`
  - The verification has been audited and the status may have been updated

  ---

  - `identity_verification_report_created`
  - The pdf report is available

  {% /table %}
