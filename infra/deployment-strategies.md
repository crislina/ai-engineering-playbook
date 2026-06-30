# Deployment Strategies

## Purpose

Guide release approaches that reduce user impact.

## Strategies

- Rolling deployments for low-risk stateless services.
- Blue-green deployments when fast rollback matters.
- Canary deployments when gradual exposure reduces risk.
- Feature flags when release and activation need to be separated.

## Rules

- Define rollback or forward-fix behavior before high-risk releases.
- Validate health checks before shifting traffic.
- Keep migrations compatible with old and new application versions during rolling deploys.
