# AML verification

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

  - aml_verification_id
  - ID of the AML verification

  ---

  - status
  - status of the AML verification

  {% /table %}


  **Example**
  
  ```json
  {
    "specversion": "2.0",
    "type": "aml_verification_created",
    "subject": "amlv_01hr7269mkxva7msc443jz4jbf",
    "id": "evnt_01hr7269ry3g8skc630q4ec75g",
    "time": "2024-03-05T10:22:48Z",
    "datacontenttype": "application/json",
    "data": {
      "aml_verification_id": "amlv_01hr7269mkxva7msc443jz4jbf",
      "status": "created",
      "applicant_id": "aplt_01hr7269ksxqjgqxbh4vaqmry8"
    }
  }
  ```

## Events

{% table %}

- Events
- Description

---

- `aml_verification_created`
- A verification has been created

---

- `aml_verification_onboarding_started`
- Screening has begun

---

- `aml_verification_onboarding_completed`
- Screening has been completed

---

- `aml_verification_onboarding_reviewed`
- Manual review has been completed, customer `status` was updated

---

- `aml_verification_monitoring_alert`
- A monitoring alert has been detected

---

- `aml_verification_monitoring_reviewed`
- Manual review has been completed, customer status was updated

---

- `aml_verification_status_changed`
- Manual review has been reopened, customer status was updated

{% /table %}
