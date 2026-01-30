# Verify webhook notifications

Once you've configured your webhook receiver, you'll be notified of events that occur during the ID Document Verification flow via webhooks. 

Events include an event `type` and the verification `status`. The exhaustive list of event `type` is available in the [Webhook](../webhooks/index.md) section. 

You can rely on this information to decide on follow-up actions. 

{% table %}

- Event Type
- Status
- Description

---

- `id_document_verification_quality_checks_in_progress`
- `quality_checks_in_progress`
- You submitted the document and Checkout.com perfoms the quality checks.

---

- `id_document_verification_checks_in_progress`
- `checks_in_progress`
- Checkout.com has performed the quality checks and processes the security checks.

---

- `id_document_verification_completed`
- `approved`
- The applicant's document has been approved

---

- `id_document_verification_completed`
- `declined`
- The applicant's document has been declined

---

- `id_document_verification_quality_checks_aborted`
- `retry_required`
- The quality of the the images does not allow us to perform the checks, create a new attempt with other images

---

- `id_document_verification_checks_inconclusive`
- `retry_required`
- Result is inconclusive, create a new attempt with other images

{% /table %}

You can also use the `response_codes` to implement your own business rules. 
For more details and to decide on follow-up actions, see the [Reference info](../reference-info/index.md) section.
