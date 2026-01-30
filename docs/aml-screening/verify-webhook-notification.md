# Verify webhook notification

You'll be notified of events that occur during the AML verification process via webhooks. Among other information, the webhooks will contain:

- the event `type` - for example, `aml_verification_created`,

- the AML verification `status` - for example, `created` or `review_required`.

Example

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

When the AML verification is completed, you will receive a webhook notification with the event `type` field set to `aml_verification_completed`, and the body will include the `status` of the AML verification. See the section below.
