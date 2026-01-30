# Verify webhook notifications

You'll be notified of events that occur during the Website verification process via webhooks. Among other information, they will contain:

- the event `type` - for example, `website_verification_created`,
- the Website Verification `status` - for example, `created` or `approved`.

You can rely on this information to decide on follow-up actions.

{% table %}

- Event type
- Status
- Description

---

- `website_verification_created`
- `created`
- The Website Verification has been created.

---

- `website_verification_checks_in_progress`
- `checks_in_progress`
- The Website Verification is in progress.

---

- `website_verification_completed`
- `approved`
- The website is compliant.

---

- `website_verification_completed`
- `declined`
- The website is not compliant.

{% /table %}

You can also get this status by calling the following endpoint with the unique `id` returned in the create a Website Verification response:

**GET** `/v2/website-verifications/{website_verification_id}`

You can also use the `response_codes` to implement your own business rules. For more details and to decide on follow-up actions, see the [Reference info](../reference-info/index.md) section.
