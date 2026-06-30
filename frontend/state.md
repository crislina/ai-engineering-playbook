# Frontend State

Load when deciding state ownership.

- Keep state at the narrowest owner that needs to change it.
- Separate remote server state, URL/navigation state, persisted client state, and ephemeral UI state.
- Derive values instead of storing synchronized copies.
- Model loading, empty, error, stale, and success states explicitly.
- Use the project's server-state tool for caching and revalidation when available.
- Duplicate server data locally only for an intentional editing or optimistic workflow with reconciliation.
