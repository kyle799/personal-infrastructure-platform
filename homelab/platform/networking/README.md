# Networking

Use this directory for network design notes, DNS, VLAN planning, ingress, and connectivity documentation.

## Initial Networking Approach

- public routing through NGINX
- bastion-based administrative access
- domain-based routing for multiple websites and apps
- Compose project separation to reduce cross-service impact

## Future Enhancements

- VLAN separation for IoT devices and automation workloads
- split internal and external DNS resolution
- stricter firewall policy between service zones
