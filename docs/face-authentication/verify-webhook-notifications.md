# Verify webhook notifications

Once you've configured your webhook receiver, you'll be notified of events that occur during the identity verification flow via webhooks. 

Events include an event `type` and the verification `status`. The exhaustive list of event `type` is available in the [Webhook](../webhooks/index.md) section. 

You can rely on this information to decide on follow-up actions. 

{% table %}

- Event Type
- Status
- Description

---

- `face_authentication_capture_completed`
- `checks_in_progress`
- The applicant completed the capture, Checkout.com processes the verification

---

- `face_authentication_checks_completed`
- `approved`
- The applicant's authentication has been approved

---

- `face_authentication_checks_completed`
- `declined`
- The applicant's authentication has been declined

---

- `face_authentication_capture_refused`
- `refused`
- The applicant refused to perform the authentication, propose an alternative verification method

---

- `face_authentication_capture_aborted`
- `retry_required`
- The applicant did not manage to complete the capture, create a new attempt

---

- `face_authentication_checks_inconclusive`
- `retry_required`
- Result is inconclusive, create a new attempt

{% /table %}

You can also use the `response_codes` to implement your own business rules. 
For more details and to decide on follow-up actions, see the [Reference info](../reference-info/index.md) section.
