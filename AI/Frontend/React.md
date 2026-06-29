# React

## Purpose

Guide React implementation.

## Folder Structure

- Keep feature code close to where it is used.
- Separate reusable components from feature-specific components.
- Keep API clients, hooks, types, and utilities discoverable.
- Avoid large folders that mix unrelated concerns.

## Component Design

- Keep components focused and composable.
- Lift state only when multiple components need it.
- Keep derived data derived instead of duplicating it in state.
- Prefer controlled inputs for forms that need validation or submission logic.

## Hooks

- Use hooks for reusable stateful behavior.
- Keep hooks focused and testable.
- Do not hide unrelated side effects inside generic hooks.
- Include dependencies explicitly.

## State

- Keep state as local as possible.
- Use server state tools for remote data when the project has them.
- Avoid duplicating server data into local state unless needed for editing workflows.
- Model loading, error, empty, and success states explicitly.

## API

- Keep API calls in dedicated client or service modules.
- Keep request and response types explicit.
- Handle errors consistently.
- Avoid calling APIs directly from deeply nested presentational components.

## TypeScript

- Prefer precise types over `any`.
- Define domain and API types clearly.
- Use discriminated unions for complex UI state when useful.
- Avoid over-generic components that make types harder to understand.

## Performance

- Avoid unnecessary memoization until there is a measured reason.
- Keep expensive calculations outside render or memoize them intentionally.
- Split large components when it improves readability and testability.

## Testing

- Test user-visible behavior instead of implementation details.
- Cover important states: loading, empty, error, and success.
