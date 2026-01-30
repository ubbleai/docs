# Security

## Webhook IP whitelisting
For security purposes, if you need to whitelist our incoming API calls, please note that we are hosted in the cloudgouv-eu-west-1 region of our cloud provider. [You can find the public IP addresses here](https://docs.outscale.com/en/userguide/OUTSCALE-Public-IPs.html).

## User Agent
Our webhook calls are made with the following user agent: `CkoIdvNotifier`. Please make sure to allow this user agent in your firewall settings.

## Signature
For security reasons all our webhook calls are signed, please refer to [signature](../api-standard/index.md#signature) for more details.
