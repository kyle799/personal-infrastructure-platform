# Decision: Reverse Proxy

## Status

Accepted

## Context

The homelab will expose selected internal services through a controlled ingress layer. The reverse proxy will need to handle routing, TLS termination, and simple operational management.

## Decision Drivers

- ease of configuration
- TLS support
- Docker or Kubernetes compatibility
- observability support

## Options

- Traefik
- NGINX
- Caddy

## Decision

Use NGINX.

## Rationale

- It matches the currently deployed environment
- It supports hosting multiple public websites behind a familiar ingress layer
- It keeps routing under direct configuration control
- It reflects practical operations experience rather than an aspirational redesign
