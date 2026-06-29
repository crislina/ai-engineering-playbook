# Components

## Purpose

Define expectations for reusable frontend components.

## Core Components

### Button

- Support primary, secondary, destructive, ghost, disabled, loading, and icon-only states when relevant.
- Use accessible labels for icon-only buttons.
- Keep button text concise.

### Table

- Support loading, empty, error, and populated states.
- Support sorting, pagination, and row actions when required.
- Keep dense enterprise data readable.

### Modal

- Use for focused decisions or forms.
- Trap focus and support keyboard dismissal when appropriate.
- Avoid using modals for large multi-step workflows unless approved.

### Pagination

- Use consistent controls and metadata.
- Show current page, page size, and total when available.
- Enforce sensible page-size limits.

### Form

- Use clear labels, validation messages, and submission states.
- Preserve user input on validation errors.
- Distinguish client validation from server validation.

## Component Rules

- Give components a clear responsibility and stable API.
- Prefer composition over large option-heavy components.
- Keep styling consistent with the existing design system.
- Support disabled, loading, focused, and error states where relevant.

## Props

- Use descriptive prop names.
- Avoid boolean combinations that create unclear states.
- Document non-obvious behavior with examples.

## Reuse

- Extract shared components when reuse is real or imminent.
- Keep domain-specific behavior out of generic UI primitives.
- Prefer composition with small components over inheritance or deeply nested configuration.
