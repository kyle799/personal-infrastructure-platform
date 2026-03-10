# Architecture Overview

## Purpose

This homelab is intended to model a small self-hosted platform that demonstrates:

- infrastructure automation
- secure service exposure
- observability and recovery practices
- practical platform engineering decisions

## High-Level Design

The platform is organized around a few major layers:

1. Hardware and host operating systems
2. Networking, DNS, and ingress
3. Container or cluster runtime
4. Shared platform services like monitoring and backups
5. User-facing services such as AI, media, and home automation

## Current Reference Architecture

- One or more Linux hosts run Docker Engine with many service-specific Compose projects
- NGINX is used as the primary public ingress layer
- An SSH bastion provides controlled remote administrative access
- Cloudflared is present in the bastion path for remote connectivity
- Public websites and private internal apps are managed as separate Compose projects
- Application state is stored in per-service directories and selected bind-mounted data paths
- Backups are captured as timestamped tarballs of service roots and key data directories

## Actual Service Groups

- `edge`: `nginx`, `ssh_bastion`
- `public-sites`: `kyle.15kmr.com`, `fairwaypueblo.com`, `reneau.me`
- `private-apps`: `bitwarden`, `immich`, `nimmich`, `jellyfin`, `overseerr`, `cookbook`, `dl_app`
- `platform-tooling`: `oc_mirror`, `openshift-airgap-architect`
- `operations`: `backup.sh`, `backups/docker-compose/*`

## Network Model

- Public traffic terminates at the NGINX reverse proxy
- Administrative entry is separated through the bastion service
- Sensitive applications such as password management and media services can remain privately routed or selectively exposed
- Each application stack is independently deployed through its own Compose file, which limits blast radius during changes

## Why This Design

- It reflects a real self-hosted environment rather than a synthetic demo
- It shows experience operating multiple independent services over time
- It demonstrates public web hosting, private applications, and platform tooling in one environment
- It is readable enough to work as a portfolio artifact for platform, DevOps, and systems roles

## To Replace With Real Data

- physical hardware inventory
- storage capacity and disk layout
- network segments and VLANs
- actual domain-to-service mapping
- sanitized ingress and secret management details
