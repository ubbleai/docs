# Create an AML verification

To use it, you will first need an `applicant_id` and an approved identity verification. 

You can then request an AML verification and include the following fields:

- `applicant_id` - the unique identifier of the applicant.

- `webhook_url` - the URL where you want to be notified when the status of the AML verification change.

- `screening_configuration_identifier` - the identifier of the configuration you want to use to screen the applicant. It can be defined and retrieved via the ComplyAdvantage dashboard.

**POST** `/v2/aml-verifications`

Request example

```json
{
    "webhook_url": "{{WEBHOOK_URL}}",
    "applicant_id": "aplt_01hr4p9j0etqw34wyv2h4ac27k",
    "search_parameters": {
        "configuration_identifier": "e3b6c5b6-fcc2-43e3-9e8c-7e378e320a2p"
    }
}
```

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
            "href": "https://api.ubble.ai/api/v2/aml-verifications/amlv_01hr7269mkxva7msc443jz4jbf"
        }
    }
}
```

Make a note of the AML verification `id` value in the response. You'll need this to retrieve the detailed results later.
