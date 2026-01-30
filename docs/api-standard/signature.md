# Signature

## What is signed ?
**Webhook notifications** are signed by default.

To enable signature verification for **API responses**, contact your account manager.

## Cko-Signature Header
The `Cko-Signature` header contains:
- **Timestamp**: The time of the request (e.g., `1635236316.377888`).
- **Signing Key ID and Version**: Unique key identifier and version (e.g., `3456-live-v1`).
- **Signature**: The digital signature (e.g., `5257a869a7ecebeda35affa62cdcb3fa51cad7e77a0e56ff546d0ae8e108d8bd`).

## Signature Format
```
  <timestamp>:<organization_id>-<test or live verification>-<key version>:<signature>
```

### Signature example
```
  1635236316.377888:3456-production-v1:5257a869a7ecebeda35affa62cdcb3fa51cad7e77a0e56ff546d0ae8e108d8bd
```

### Signing Algorithm
We use **ECDSA** with **SHA-512** to create signatures.

## Verifying the Signature
1. **Download the Public Key**: Separate keys for test and live environments are available in the [dashboard security section](https://dashboard.ubble.ai/security). 
2. **Recreate the Signed Data**: Combine the request body and the `Cko-Signature` timestamp.
3. **Verify the Signature**: Use ECDSA with the downloaded public key to verify the signature.

For code samples, visit our [repository](https://github.com/ubbleai/code-samples).
