# Error Handling

## Purpose

Provide consistent backend error behavior.

## Principles

- Return clear, stable errors to clients.
- Log enough context for debugging without exposing sensitive data.
- Distinguish validation, authorization, conflict, not-found, and unexpected errors.

## Global Exception Handler

- Use a global exception handler for consistent API errors.
- Map known exceptions to stable status codes and error codes.
- Let unexpected exceptions become controlled `500` responses.
- Do not expose stack traces to clients.

## API Errors

- Use a consistent error response format.
- Include machine-readable error codes when clients need branching behavior.
- Avoid returning stack traces or internal exception names.

## Structured Logging

- Log structured fields when possible.
- Include request path, method, user or actor ID when safe, correlation ID, and error code.
- Do not log secrets, tokens, passwords, or sensitive payloads.

## Log Level

- `DEBUG` for diagnostic details during development.
- `INFO` for meaningful business or lifecycle events.
- `WARN` for recoverable abnormal behavior.
- `ERROR` for failures requiring investigation.

## Correlation ID

- Accept or generate a correlation ID for each request.
- Include correlation ID in logs and error responses when available.
- Propagate correlation ID to downstream service calls.

## Retry

- Retry only transient failures.
- Use bounded retries with backoff.
- Avoid retrying validation, authorization, or permanent business errors.
- Ensure retries do not duplicate side effects.

## Operational Errors

- Add alerts for repeated failures in critical paths.
- Make failed background work observable and recoverable.
