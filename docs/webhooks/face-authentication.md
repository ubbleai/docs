# Face authentication

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

  - face_authentication_id
  - ID of the face authentication

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
    "type": "face_authentication_checks_completed",
    "subject": "fav_01hr7269mkxva7msc443jz4jbf",
    "id": "evnt_01hr7269ry3g8skc630q4ec75g",
    "time": "2024-03-05T10:22:48Z",
    "datacontenttype": "application/json",
    "data": {
      "external_applicant_id": "87ydky4g6eq144zkcvpoi54mtj"
      "applicant_id": "aplt_01jdky4g6eq144zkcv16vtymx7",
      "status": "declined",
      "face_authentication_id": "fav_01je8cdhrk5fwa5j5nb701sah7",
      "response_codes": [{"code": "62321", "summary": "face_face_mismatch"],
      "user_journey_id": "usj_01hyzdts3zxqjm8bvvne2a2qb3"
    }
  }
  ```

## Events

{% table %}

- Events
- Description

---

- `face_authentication_created`
- You created an face authentication

---

- `face_authentication_opened`
- You created a first attempt and the verification URL is available

---

- `face_authentication_started`
- The applicant has been redirected to the web application

---

- `face_authentication_reset`
- You created a new attempt while the status was `pending` or `capture_in_progress`

---

- `face_authentication_capture_completed`
- The applicant completed the capture

---

- `face_authentication_checks_completed`
- We completed the checks

---

- `face_authentication_link_expired`
- The link expired without applicant being redirected to the web application, please note the default expiration time is 15 minutes

---

- `face_authentication_capture_refused`
- The applicant explicitly refused to perform the face authentication

---

- `face_authentication_capture_aborted`
- The applicant terminated the capture without completing it

---

- `face_authentication_checks_inconclusive`
- The applicant did not provide the assets required to perform the checks

---

- `face_authentication_retry_requested`
- You requested a retry for this face authentication

---

- `face_authentication_closed`
- The face authentication has been forcibly closed

---

- `face_authentication_anonymized`
- The face authentication has been anonymized

---

- `face_authentication_audit_completed`
- The face authentication has been audited and the status may have been updated

{% /table %}
