# Monitor a search

If an applicant is monitored, you be notified if an alert is raised. 

The `status` of the AML verification will switch to `review_required`.

In this case, you will get a notification with the `event_type` field set to `aml_monitoring_alert` and the body will include the new `status`.

You can then use the ComplyAdvantage case management tool to manually investigate the results. 

When the review is completed, you will get a notification with the `event_type` field set to `aml_monitoring_review_completed` and the body will include the new `status, depending of you decision to accept or not the risk related to the monitoring case.
