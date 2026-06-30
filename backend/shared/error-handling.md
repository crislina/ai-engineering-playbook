# Error Handling

## Purpose

Provide consistent backend error behavior.

## Principles

- Return clear, stable errors to clients.
- Log enough context for debugging without exposing sensitive data.
- Distinguish validation, authorization, conflict, not-found, and unexpected errors.

## API Errors

- Use a consistent error response format.
- Include a machine-readable code when clients need branching behavior.
- Include a human-readable message.
- Include field errors for validation failures.
- Include correlation ID when available.

## Unexpected Failures

- Convert unexpected exceptions into controlled `500` responses.
- Do not expose stack traces to clients.
- Alert on repeated failures in critical paths.
