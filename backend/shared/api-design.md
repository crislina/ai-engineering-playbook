# API Design

## Purpose

Define API design expectations independent of programming language or framework.

## REST

- Use resource-oriented routes.
- Use nouns for resources and HTTP methods for actions.
- Avoid RPC-style endpoints unless the operation is not naturally resource-based.
- Use lowercase path segments and plural nouns for collections.
- Keep nesting shallow.

## Status Codes

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

## Behavior

- Validate structure at request boundaries.
- Validate business rules in services or domain operations.
- Use stable error response shapes.
- Set explicit timeouts for external calls.
- Document which operations are safe to retry.
