# Handle AML verification results

The webhooks also return the current `status` of the AML verification. The follow-up action you should take depends on the `status` value returned:

{% table %}

- Status
- Description
- Recommended action

---

- `created`
- The AML verification has been created.
- Wait for a change in `status`.

---

- `screening_in_progress`
- The risk scoring or AML verification is in progress.
- Wait for a change in `status`.

---

- `approved`
- The initial risk scoring is not `PROHIBITED` and there are no alerts.
- Accept the applicant's request.

---

- `declined`
- The initial risk scoring is `PROHIBITED`.
- Refuse the applicant's request.

---

- `review_required`
- The initial risk scoring is not `PROHIBITED` but there are screening alerts and a case has been created.
- Manually investigate the case.

{% /table %}

You can also get this status by calling the following endpoint with the unique `id` returned in the create AML verification response:

**GET** `/v2/aml-verifications/{aml_verification_id}`

Response example

```json
{
    "id": "amlv_01hr7269mkxva7msc443jz4jbf",
    "applicant_id": "aplt_01hr7269ksxqjgqxbh4vaqmry8",
    "created_on": "2024-03-05T10:22:48.481031Z",
    "modified_on": "2024-03-05T10:22:49.327277Z",
    "status": "review_required",
    "webhook_url": "https://my.api/events/",
    "monitored": false,
    "search_parameters": {
        "configuration_identifier": "e3b6c5b6-fcc2-43e3-9e8c-7e378e320a2p"
    },
    "_links": {
        "self": {
            "href": "https://myweb.site/?query-param=hello"
        }
    }
}
```
