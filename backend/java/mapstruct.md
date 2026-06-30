# MapStruct

## Purpose

Use MapStruct for explicit DTO and entity mapping when it reduces repetitive code.

## Rules

- Keep mappings close to the boundary they serve.
- Review generated mappings for nullable fields and nested objects.
- Use explicit mappings when source and target names differ.
- Avoid hiding business decisions inside mapping code.
- Test mappings when they contain non-trivial transformations.
