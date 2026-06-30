# API Errors

Load when defining non-default client failure behavior.

- Use the project's stable error envelope; do not invent one per controller.
- Distinguish malformed input, unauthenticated, forbidden, absent, conflict, dependency failure, and unexpected failure.
- Include a machine code when clients branch on it, a safe message, field errors when useful, and a correlation ID when available.
- Map unexpected exceptions to controlled responses and retain diagnostic context internally.
- Do not expose stack traces, implementation names, secrets, or sensitive payloads.
