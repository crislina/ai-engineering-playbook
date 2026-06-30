# Pagination

Load for collections that can grow beyond a bounded small result.

- Enforce a maximum page size and deterministic ordering with a unique tie-breaker.
- Use offset pagination for modest, stable datasets where random page access matters.
- Use cursor/keyset pagination for large or frequently changing datasets.
- Define cursor opacity, sort compatibility, navigation metadata, and total-count behavior.
- Avoid expensive exact counts unless clients require them.
