# Security notes

This client can authenticate to a personal X/Twitter account and perform account actions. Login passwords, cookies, API credentials, and proxy settings can grant account access.

- Never commit real credentials or session cookies. Use a local secret store or protected environment.
- Review `.env.example` and the authentication code before configuring a real account.
- Prefer a dedicated test account and minimal permissions. Protect generated logs and state.
- Inspect write actions such as posting, following, and messaging before execution. Use rate limits and manual review appropriate to your use.
- Avoid sending credentials or private account data to third-party tools.

This is an unofficial client. Platform interfaces and account policies can change; check current terms and requirements before using it. This page is not a security audit or legal advice.

## Reporting

Do not post credentials or exploit details publicly. Use GitHub private vulnerability reporting if enabled; otherwise contact the maintainer through the current private method on the [GitHub profile](https://github.com/hmzainjamil).
