# Manually investigate the results

If the `status` is `review_required` you might want to investigate the case and determine if the applicant can access your service or not. You can do it via the ComplyAdvantage case management tool. 

You will be able to review the alerts and to determine if you accept the risk associated to the case or not.

If you accept it, the status will switch to `approved`.

If you refuse it, the status will switch to `declined`.

You will be notified if you change the `status` of an AML verification. The `event_type` field will be set to `aml_onboarding_review_completed` and the body will include the new `status`.

Example

```json
{
  "specversion": "2.0",
  "type": "aml_onboarding_review_completed",
  "subject": "amlv_01hr7269mkxva7msc443jz4jbf",
  "id": "evnt_01hr7269ry3g8skc630q4ec75g",
  "time": "2024-03-05T10:22:48Z",
  "datacontenttype": "application/json",
  "data": {
    "status": "approved"
  }
}
```
