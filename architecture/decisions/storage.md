# Decision: Storage

## Status

Accepted

## Context

Stateful workloads such as media, automation, and monitoring will require a storage strategy that balances cost, resilience, and operational overhead.

## Considerations

- local disk versus network-attached storage
- backup frequency and retention
- restore time objectives
- persistent volume support for containers

## Decision

Use per-service directories and bind-mounted data paths, backed up as timestamped tar archives.

## Rationale

- It matches the current operating model
- It supports straightforward service-level backup and restore workflows
- It makes each Compose project portable and easy to archive
- It is good enough for a practical homelab without introducing storage orchestration complexity
