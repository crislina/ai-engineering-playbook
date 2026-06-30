# React

Load only for React-specific implementation behavior.

- Keep components focused; move reusable stateful behavior into narrowly scoped hooks.
- Lift state only to the nearest shared owner.
- Keep effects synchronized with external systems; derive render data without effects.
- Make effect dependencies explicit and clean up subscriptions or async work.
- Keep API access in the project's client/server-state boundary, not deep presentational components.
- Add memoization only for measured cost or required referential stability.
- Test user-visible behavior and accessible interaction, not component internals.
