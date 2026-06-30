# Authorization

Load when actions or data visibility depend on an actor.

- Deny when policy is absent or ambiguous.
- Enforce authorization server-side at the protected use-case or data boundary.
- Cover both action permission and row/field visibility.
- Prefer explicit, testable policies over scattered conditionals.
- Keep unauthenticated and forbidden outcomes distinct unless the project intentionally conceals resource existence.
- Test role, ownership, tenant, and escalation boundaries relevant to the workflow.
