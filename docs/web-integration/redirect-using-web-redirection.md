# Redirect using web redirection (Optional)

For web redirection, we support the following environments and minimum browser versions:

{% table %}

- Desktop
- Chrome
- Firefox
- Safari
- Internet Explorer
- Edge
- Opera

---

- Min. Version
- ≥ 53
- ≥ 52
- ≥ 11.1
- -
- ≥ 16
- ≥ 58

{% /table %}

{% table %}

- Android
- Chrome for Android
- Firefox for Android
- Samsung Internet
- IE Mobile

---

- Min. Version
- ≥ 73
- ≥ 66
- ≥ 6.2
- -

{% /table %}

{% table %}

- iOS
- Safari Mobile
- Chrome
- All other browsers

---

- Min. Version
- ≥ 11.0
- ≥ 14.3
- -

{% /table %}

After you create an identity verification in your backend, you can integrate it within your website by passing the `verificationUrl` to your web app and adding it as a link:

```html
<a href="`${verificationUrl}`"></a>
```

{% admonition type="info" %}
You can view an [example web integration](https://github.com/ubbleai/integration_examples/tree/master/web) on our Identity Verification GitHub repository.
{% /admonition %}

## Handle user return in web redirection

When the user completes or terminates their verification, they'll be redirected to the `redirect_url` you specified when you requested an identity verification.

The event associated with the user's verification is returned in the webhook notification, and as a URL parameter in the `redirect_url`. If verification was unsuccessful, the URL will also contain a `response_code` URL parameter. For example:

```
https://your-redirect-url.com?id=idv_01h2623ysfkhpn7czed0bw8fd6&event=identity_verification_capture_aborted&response_code=61101
```

Your follow-up action is determined by the [webhook event](../webhooks/index.md#events) you receive:

{% table %}

- Webhook event
- Follow-up action

---

- `identity_verification_capture_aborted` or `identity_verification_link_expired`
- Request a [retry](#operation/retry_identity_verification).

---

- `identity_verification_capture_refused`
- Propose an alternative verification method to the user.

---

- `identity_verification_capture_completed`
- You can ask users to perform additional checks or ask them to wait until results are available. In some instances, you may also simultaneously receive an `identity_verification_checks_completed` webhook. You can make your decision once you receive the `identity_verification_checks_completed` webhook.

{% /table %}
