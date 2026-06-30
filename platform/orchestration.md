# Kubernetes

Load only for Kubernetes deployment behavior.

- Set resource requests from observed demand and limits with awareness of throttling or OOM behavior.
- Use readiness for traffic eligibility, liveness for unrecoverable process failure, and startup probes for slow initialization.
- Keep deployment, service, ingress, configuration, and secret ownership explicit.
- Store secrets in the project's approved secret system.
- Define disruption, rollout, autoscaling, and graceful shutdown behavior for availability requirements.
- Prefer declarative, reviewable configuration.
