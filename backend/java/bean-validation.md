# Bean Validation

## Purpose

Use Bean Validation for structural validation at Java application boundaries.

## Rules

- Validate request DTOs at controller boundaries.
- Use annotations for structural constraints such as required values, length, ranges, and formats.
- Put business validation in services or domain operations.
- Return consistent validation errors.
- Avoid duplicating validation rules across layers unless the duplication protects a real boundary.
