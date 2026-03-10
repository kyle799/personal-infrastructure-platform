# Security

Use this directory for security baselines, hardening notes, secrets handling, and access control decisions.

## Baseline Controls

- no secrets committed to git
- minimal public exposure through NGINX
- private admin access through the bastion path
- backups for configuration and stateful data

## Next Security Work

- choose a secrets manager
- add host hardening with Ansible
- define patching and image update policy
