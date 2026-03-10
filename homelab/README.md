# Homelab

This directory contains the core homelab project structure used to document and automate the platform.

## Goals

- Present a clear architecture for portfolio review
- Keep implementation details organized by concern
- Make future automation easy to add without restructuring the repo

## Current Implementation Direction

The current implementation is a service-oriented Docker Compose estate rather than a single monolithic stack. That is useful for a portfolio project because it shows:

- service isolation by project
- public and private workload separation
- backup discipline
- admin access patterns
- platform support for both apps and tooling

## Real Environment Summary

- `nginx`: public ingress and routing
- `ssh_bastion`: bastion access with Cloudflared integration
- `kyle.15kmr.com` and `fairwaypueblo.com`: public web properties
- `bitwarden`, `immich`, `nimmich`, `jellyfin`, `overseerr`: self-hosted application services
- `cookbook` and `dl_app`: smaller utility and personal apps
- `oc_mirror` and `openshift-airgap-architect`: platform engineering and OpenShift support tooling
- `backups/docker-compose/*`: timestamped application backups

## Areas

- `architecture/`: design, diagrams, and decisions
- `infrastructure/`: Terraform, Ansible, Kubernetes, and Docker assets
- `services/`: application and stack-specific work
- `platform/`: cross-cutting platform capabilities
- `tooling/`: scripts and delivery pipelines
- `docs/`: operational documentation
