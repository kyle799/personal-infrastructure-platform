# Scaling

## Objective

Capture the path from a simple single-node homelab to a more capable multi-service platform.

## Likely Scaling Stages

1. single host with Docker Compose
2. split services across dedicated hosts
3. introduce centralized storage and better ingress
4. adopt orchestration where justified

## Decision Questions

- when operational overhead outweighs simplicity
- which workloads justify clustering
- how storage and networking change with scale

## Current Position

The project is intentionally Compose-first, but it is no longer a toy single-stack setup. It already shows how separate services can be managed as independent projects before moving to stronger central automation or orchestration.

## Real Scaling Pressure Points

- too many hand-managed Compose files
- inconsistent secrets and credential handling
- manual ingress and certificate changes
- backup and restore steps that depend on tribal knowledge
