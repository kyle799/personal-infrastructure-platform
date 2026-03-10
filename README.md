# Personal Infrastructure Platform

This repository documents and automates my homelab platform. It is structured to show both the technical implementation and the architectural reasoning behind it so it can serve as a working infrastructure repo and a portfolio artifact.

The platform is currently built as a multi-stack Docker Compose environment. It mixes personal infrastructure, public-facing websites, private applications, media services, remote admin access, and development tooling.

## Current Target Stack

- Runtime: Docker Engine with many service-specific Compose projects
- Public ingress: NGINX-based reverse proxy
- Remote admin path: SSH bastion with Cloudflared
- Public apps: portfolio site, business site, and personal sites
- Private apps: Bitwarden, Jellyfin, Immich, Overseerr, and utility services
- Platform tooling: `oc_mirror` and `openshift-airgap-architect`
- Backup model: timestamped tarball snapshots of service roots and selected data volumes

## Structure

- `homelab/architecture/`: diagrams, design notes, and architecture decisions
- `homelab/infrastructure/`: infrastructure-as-code and deployment automation
- `homelab/services/`: service-level docs and implementation areas
- `homelab/platform/`: shared platform capabilities like networking and security
- `homelab/tooling/`: scripts, CI/CD, and automation helpers
- `homelab/docs/`: operations, recovery, and scaling documentation

## Next Steps

1. Capture the real host, storage, and domain layout for each Compose project.
2. Add sanitized versions of the most representative Compose files to this repo.
3. Translate recurring operational tasks like backups and deployment into Ansible or scripted automation.
