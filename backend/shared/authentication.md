# Authentication Concepts

## Purpose

Define reusable authentication concepts independent of a specific provider.

## Principles

- Authentication proves who the actor is.
- Keep identity verification separate from authorization decisions.
- Treat tokens, passwords, session cookies, and credentials as sensitive data.
- Use secure defaults for expiration, rotation, and transport.
- Avoid logging secrets or raw credentials.

## Boundaries

- Validate authentication at system boundaries.
- Propagate only the identity and claims needed by downstream code.
- Keep provider-specific details isolated behind an authentication abstraction when practical.
