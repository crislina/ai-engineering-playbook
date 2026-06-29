# API

## Purpose

Define API design expectations.

## API Convention

### REST

- Use resource-oriented routes.
- Use nouns for resources and HTTP methods for actions.
- Avoid RPC-style endpoints unless the operation is not naturally resource-based.

### URI

- Use lowercase path segments.
- Use plural nouns for collections.
- Keep nesting shallow.
- Example: `/api/v1/templates/{templateId}/placeholders`.

### Status Code

- `200 OK` for successful reads and updates with a body.
- `201 Created` for successful creation.
- `204 No Content` for successful deletion or update without a body.
- `400 Bad Request` for malformed requests.
- `401 Unauthorized` for missing authentication.
- `403 Forbidden` for insufficient permission.
- `404 Not Found` for missing resources.
- `409 Conflict` for state conflicts.
- `422 Unprocessable Entity` for semantic validation errors when used by the project.
- `500 Internal Server Error` for unexpected failures.

### Pagination

- Use pagination for collection endpoints.
- Include page, size, total count, and sorting metadata when relevant.
- Enforce maximum page size.

### Naming

- Use consistent JSON field names.
- Match domain vocabulary from `AI/Project/Domain.md`.
- Avoid leaking database column names when they are not domain terms.

### Versioning

- Version public APIs when breaking changes are possible.
- Prefer URI versioning such as `/api/v1` unless the project chooses another convention.

## API Behavior

### Validation

- Validate structure at request boundaries.
- Validate business rules in services.
- Return stable error codes and field-level details where useful.

### Idempotency

- Make retryable write operations idempotent when clients may retry.
- Use idempotency keys for operations that create side effects when needed.
- Document which operations are safe to retry.

### Retry

- Clients may retry transient failures.
- Servers should avoid duplicate side effects.
- Retry behavior must not hide permanent validation or authorization failures.

### Timeout

- Set explicit timeouts for external calls.
- Return controlled errors when dependencies time out.
- Avoid unbounded waits in request processing.

### Error Response

- Use a consistent error response shape.
- Include a machine-readable code.
- Include a human-readable message.
- Include field errors for validation failures.
- Include correlation ID when available.

## Documentation

- Document endpoints, parameters, response bodies, and error cases.
- Include examples for important workflows.
