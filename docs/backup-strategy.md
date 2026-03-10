# Backup Strategy

## Goals

- protect configuration and state
- support fast recovery for critical services
- document retention and verification

## Backup Categories

- infrastructure code and documentation
- service configuration
- application data
- database snapshots

## Initial Strategy

- back up Compose project roots as tar archives
- back up selected service data directories separately where needed
- store backups under `backups/docker-compose/<timestamp>/`
- keep both configuration and application data snapshots for critical services

## Observed Backup Pattern

Based on the current inventory:

- one snapshot set from February 26, 2026 at `20260226-215921` contains root archives
- one snapshot set from February 26, 2026 at `20260226-220207` contains root archives plus selected data archives
- services with separate data archives include Bitwarden, Immich, Jellyfin, NGINX, and nimmich

## To Document

- what is backed up
- where backups are stored
- how often backups run
- how restores are tested
