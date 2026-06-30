# Java Boundary Serialization

Load when Jackson or Bean Validation behavior affects an API contract.

- Put structural Bean Validation constraints on request DTOs; keep business rules in use cases/domain code.
- Make JSON names and null, unknown-field, date/time, and enum behavior intentional.
- Do not serialize persistence entities directly.
- Avoid global serializer changes unless every affected contract accepts the change.
- Convert validation and deserialization failures into the project's standard error shape.
