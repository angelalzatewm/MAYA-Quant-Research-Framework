# Security Policy

Do not commit:

- passwords;
- broker/API credentials;
- private keys;
- access tokens;
- database credentials;
- proprietary datasets that you are not licensed to publish.

Use environment variables or local secret stores for credentials.

If sensitive information is accidentally committed, remove it from Git history as soon as possible and rotate the credential.
