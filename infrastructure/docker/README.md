# Docker

This directory contains the first executable version of the homelab platform.

## Current Layout

- `compose.yaml`: starter shared platform stack

## Initial Services

- Traefik for ingress
- Prometheus for metrics collection
- Grafana for dashboards
- Loki for log aggregation

## Notes

- Secrets and production credentials are intentionally not committed here
- Service-specific stacks can be split into separate compose files later
- Volumes are mapped to local directories under `./volumes/`
