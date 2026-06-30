# React

## Purpose

Guide React implementation.

## Component Design

- Keep components focused and composable.
- Lift state only when multiple components need it.
- Prefer controlled inputs for forms that need validation or submission logic.
- Keep request and response types explicit when using TypeScript.

## API Calls

- Keep API calls in dedicated client or service modules.
- Handle errors consistently.
- Avoid calling APIs directly from deeply nested presentational components.

## Performance

- Avoid unnecessary memoization until there is a measured reason.
- Keep expensive calculations outside render or memoize them intentionally.
- Split large components when it improves readability and testability.
