# Authentication

Load when a boundary establishes actor identity.

- Keep identity verification separate from permission decisions.
- Treat tokens, sessions, passwords, and credentials as sensitive.
- Validate identity at a trusted boundary; pass downstream only required identity and claims.
- Isolate provider-specific behavior when it would otherwise spread through use cases.
- Define expiration, rotation, revocation, and secure transport according to the project's threat model.
- Never log raw credentials or tokens.
