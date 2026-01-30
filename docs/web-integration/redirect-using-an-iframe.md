# Redirect using an iframe (Optional)

If you use desktop to mobile redirection, we recommend using our iframe integration.

Include the SDK as a script tag:

```html
<script
  src="https://cdn.ubble.ai/iframe-sdk-1.0.0.js"
  type="application/javascript"
></script>
```

Add a global method called `onUbbleReady` to the page. The method should be triggered when the SDK is loaded:

```js
function onUbbleReady() {

}
```

Initialize a new `IDV` object:

```js
function onUbbleReady() {
  const ubbleIDV = new Ubble.IDV(document.getElementById("ubble"), options);
}
```

## API

### Events

`onComplete(completeEvent)`: Triggered when a user completes the capture

```json
{
  "type": "COMPLETE",
  "event": "identity_verification_capture_completion",
  "redirectUrl": "https://your-redirect-url.com?id=<identity verification id>&event=identity_verification_capture_completed"
}
```

`onRefused(refusedEvent)`: Triggered when the applicant refuses to complete the verification

```json
{
  "type": "REFUSED",
  "event": "identity_verification_capture_refusal",
  "responseCode": 63001,
  "redirectUrl": "https://your-redirect-url.com?id=<identity verification id>&event=identity_verification_capture_refused"
}
```

`onAbort(abortEvent)`: Triggered when the verification is terminated

```json
{
  "type": "ABORT",
  "event": "identity_verification_capture_abortion",
  "responseCode": 61111,
  "redirectUrl": "https://your-redirect-url.com?id=<identity verification id>&event=identity_verification_capture_aborted&response_code=63001"
}
```

`onExpired`: Triggered when the verification link has expired

```json
{
  "type": "EXPIRED",
  "event": "identity_verification_expiration",
  "redirectUrl": "https://your-redirect-url.com?id=<identity verification id>&event=identity_verification_link_expired&response_code=63001"
}
```

### Methods

`destroy()`: Ends the Identity Verification flow

### Full example

```js
const ubbleIDV = new Ubble.IDV("idv", {
  width: "500",
  height: "600",
  allowCamera: true,
  verificationUrl: "https://idv.ubble.ai/4hryu5cei5",
  events: {
    onComplete(event) {
      ubbleIDV.destroy();
    },
    onAbort(event) {
      ubbleIDV.destroy();
    },
    onExpired(event) {
      ubbleIDV.destroy();
    }
    onRefused(event) {
      ubbleIDV.destroy();
    }
  },
});
```

{% admonition type="warning" %}
If you encounter issues, ensure that you've:

- included a semicolon in the `Content-Security-Policy: frame-src https://*.domain_name.fr;` header
- allowed the use of the camera
{% /admonition %}

### Handle user redirection in iframe

When the user completes or terminates their verification, use the `destroy()` method for handling user redirection.
