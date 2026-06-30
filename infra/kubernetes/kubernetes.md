# Kubernetes

## Purpose

Guide Kubernetes deployment decisions.

## Rules

- Define resource requests and limits intentionally.
- Use readiness and liveness probes for service health.
- Store secrets in approved secret management systems.
- Prefer declarative manifests or package tools that can be reviewed.
- Keep deployment, service, ingress, and config responsibilities clear.
