# Component Design

## Purpose

Define expectations for reusable frontend components independent of framework.

## Principles

- Give components a clear responsibility and stable API.
- Prefer composition over large option-heavy components.
- Support disabled, loading, focused, empty, and error states where relevant.
- Keep domain-specific behavior out of generic UI primitives.
- Extract shared components when reuse is real or imminent.

## Common Components

- Buttons should support primary, secondary, destructive, ghost, disabled, loading, and icon-only states when relevant.
- Tables should support loading, empty, error, populated, sorting, pagination, and row action states when required.
- Forms should use clear labels, validation messages, and submission states.
- Modals should trap focus and support keyboard dismissal when appropriate.
