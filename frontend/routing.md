# Frontend Routing

Load when navigation or shareable state changes.

- Routes reflect user-visible structure, not component structure.
- Keep identifiers and route parameters stable and meaningful.
- Put state in the URL when users expect links, bookmarks, refresh, or back/forward navigation to preserve it.
- Define not-found, unauthenticated, forbidden, loading, and failed-navigation behavior.
- Avoid keeping major workflow state only in memory.
