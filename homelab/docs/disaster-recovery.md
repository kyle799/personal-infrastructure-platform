# Disaster Recovery

## Objective

Define how the homelab can be restored after host failure, storage loss, or configuration drift.

## Recovery Priorities

1. restore core networking and access
2. restore secrets and configuration
3. restore platform services
4. restore user-facing applications

## Initial Recovery Order

1. rebuild the Docker host
2. restore service root directories from the latest backup set
3. restore service data archives for stateful workloads
4. restore ingress and bastion access first
5. bring up critical public and administrative services
6. restore private application services and developer tooling

## To Document

- backup source locations
- recovery order
- estimated recovery times
- manual steps that still need automation
