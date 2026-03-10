# Service Inventory

This is the current known Docker Compose estate based on the provided directory inventory.

## Edge and Access

- `nginx`: public ingress and routing
- `ssh_bastion`: bastion host with `cloudflared` configuration

## Public Web Properties

- `kyle.15kmr.com`: personal portfolio application
- `fairwaypueblo.com`: static business website
- `reneau.me`: additional hosted site

## Private and Utility Applications

- `bitwarden`: password management
- `cookbook`: recipe or personal utility application with SQLite data
- `dl_app`: download-related utility application
- `immich`: photo management
- `nimmich`: additional photo-related deployment or variant
- `jellyfin`: media streaming
- `overseerr`: media request workflow

## Platform Tooling

- `oc_mirror`: OpenShift disconnected content tooling
- `openshift-airgap-architect`: OpenShift air-gapped planning and UI workflow

## Backup and Operations

- `backup.sh`: backup orchestration script
- `backups/docker-compose/20260226-215921`: root archive snapshot set
- `backups/docker-compose/20260226-220207`: root plus selected data archive snapshot set

## Follow-Up Work

- classify each service as public, private, or admin-only
- record domain names and ingress routes
- capture restart policy, ports, and storage dependencies
- add sanitized Compose excerpts for the most representative stacks
