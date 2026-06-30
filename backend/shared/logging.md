# Logging

## Purpose

Make system behavior understandable without exposing sensitive data.

## Principles

- Log meaningful lifecycle and business events.
- Use structured fields when possible.
- Include request path, method, actor ID when safe, correlation ID, and error code.
- Do not log secrets, tokens, passwords, or sensitive payloads.

## Levels

- `DEBUG` for diagnostic details during development.
- `INFO` for meaningful business or lifecycle events.
- `WARN` for recoverable abnormal behavior.
- `ERROR` for failures requiring investigation.
