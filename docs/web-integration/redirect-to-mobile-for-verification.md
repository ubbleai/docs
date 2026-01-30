# Redirect to mobile for verification

All desktop users are redirected to their mobile device to perform verification. This allows the verification to be performed in a more secure environment, and ensures that users are more likely to complete the verification journey.

After a user has completed the verification on their mobile, we redirect them back to their desktop environment by providing them with a QR code or SMS link.

For the SMS link, you can provide a `phone_number` value in your [identity verification request](#operation/create_identity_verification) to pre-fill the phone number associated with the redirection.
