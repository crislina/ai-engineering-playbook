# Backend Layering

Load only when responsibility placement is disputed.

| Layer | Owns | Must not own |
|---|---|---|
| Controller | Transport mapping, boundary validation trigger, status/headers | Business decisions, persistence queries |
| Service/use case | Business orchestration, transaction boundary, policy | HTTP details, ORM serialization |
| Repository | Query and persistence mechanics | Business policy |
| DTO | External contract | Persistence behavior, business logic |
| Entity/model | Persisted state and persistence invariants | Public API shape |

Adapt these roles to the project's chosen architecture; do not introduce layers merely to match this table.
