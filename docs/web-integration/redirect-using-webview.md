# Redirect using webview (Optional)

For a more integrated redirection from your mobile application, you can redirect the user with a webview. Webview redirection is supported by the following platforms:
- Android
- iOS 13 or later – via WebRTC running inside a <a href="https://developer.apple.com/documentation/webkit/wkwebview" target="_blank">WKWebView</a>
- iOS 12 or older – via the Safari browser by passing the `verificationUrl` to the `UIApplication.open()`
<a href="https://developer.apple.com/documentation/uikit/uiapplication/1648685-open" target="_blank">method</a> in your app code
- React Native
- Flutter – using the `flutter_inappwebview` <a href="https://inappwebview.dev/docs/intro/" target="_blank">dependency</a>,
with the <a href="https://inappwebview.dev/docs/web-rtc/" target="_blank">WebRTC API</a> so Identity Verification can launch a video stream

{% admonition type="info" %}
You can view [example webview integrations](https://github.com/ubbleai/integration_examples/tree/master) for each platform on our Identity Verification GitHub repository.
{% /admonition %}

{% admonition type="warning" %}
On iOS, you need to set the iOS-specific option `allowsInlineMediaPlayback` to `true`. See [this example](https://github.com/ubbleai/integration_examples/blob/master/UbbleReactNative/UbbleWebView.js#L14) in react-native.
{% /admonition %}

With a webview integration, you're expected to provide a deeplink to redirect the user on your mobile application.

## Handle user return in webview

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

- `identity_verification_capture_aborted`
- Request a [retry](#operation/retry_identity_verification).

---

- `identity_verification_capture_refused`
- Propose an alternative verification method to the user.

---

- `identity_verification_capture_completed`
- You can ask users to perform additional checks, or ask them to wait until results are available. In some instances, you may also simultaneously receive an `identity_verification_checks_completed` webhook. You can make your decision once you receive the `identity_verification_checks_completed` webhook.

{% /table %}
