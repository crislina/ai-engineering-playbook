# Lombok

## Purpose

Use Lombok carefully to reduce boilerplate without hiding important behavior.

## Rules

- Prefer Lombok for simple immutable values or repetitive accessors when the project accepts it.
- Avoid annotations that obscure constructor, equality, or mutability behavior.
- Be careful with `@Data` on entities.
- Keep generated behavior understandable to readers and tools.
