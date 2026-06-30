# API Routing

Load first for HTTP API work. This file selects concerns; it is not a REST tutorial.

- Match the project's established resource naming, status, media type, and compatibility conventions.
- Keep transport mapping in the controller and business decisions behind the use-case boundary.
- Define client-visible behavior for success, validation, absence, conflict, authorization, and unexpected failure.

Then load only what the endpoint needs:

| Concern | File |
|---|---|
| Request/response contract | `dto.md` |
| Input or business constraints | `validation.md` |
| Custom failure envelope | `errors.md` |
| Identity | `authentication.md` |
| Permission or data visibility | `authorization.md` |
| Collection size | `pagination.md` |
| Breaking evolution | `versioning.md` |

Load framework guidance only after these decisions require implementation detail.
