# ID Document Verification

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

  - id_document_verification_id
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
        "type": "id_document_verification_checks_completed",
        "subject": "iddv_5hxpdwegjcbujpth3wdo55d3vm",
        "id": "evnt_5hxpdwegjcbujpth3wdo55d3vm",
        "time": "2023-03-22T17:31:00Z",
        "datacontenttype": "application/json",
        "data": {
            "external_applicant_id": "9fj3lz918bujpth3wdolmc74s"
            "applicant_id": "aplt_5hxpdwegjcbujpth3wdo55d3vm",
            "user_journey_id": "usj_5hxpdwegjcbujpth3wdo55d3vm",
            "id_document_verification_id": "idv_5hxpdwegjcbujpth3wdo55d3vm",
            "status": "declined",
            "response_codes": [
                {"code": 62301, "summary": "document_counterfeit"},
  
            ]
        }
    }
  ```

## Events

  {% table %}

  - Events
  - Description

  ---

  - `id_document_verification_created`
  - You created a document verification

  ---

  - `id_document_verification_quality_checks_in_progress`
  - You created a first attempt and we assess the quality of the images

  ---

  - `id_document_verification_checks_in_progress`
  - We completed the quality assessment and perform the safety checks

  ---

  - `id_document_verification_checks_completed`
  - We completed the safety checks

  ---

  - `id_document_verification_quality_checks_aborted`
  - The applicant did not provide assets of good enough quality to perform the verification

  ---

  - `id_document_verification_checks_inconclusive`
  - The applicant did not provide the assets required to perform the checks

  ---

  - `id_document_verification_retry_requested`
  - You requested a retry for this document verification

  ---

  - `id_document_verification_closed`
  - The verification has been forcibly closed

  ---

  - `id_document_verification_anonymized`
  - The document verification has been anonymized

  ---

  - `id_document_verification_audit_completed`
  - The verification has been audited and the status may have been updated

  ---

  - `id_document_verification_report_created`
  - The pdf report is available

  {% /table %}
