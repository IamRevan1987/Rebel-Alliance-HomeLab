# VMware Networking Baseline

## Purpose
This document defines the VMware networking model for RAS-lab. It is intentionally simple, constrained, and security-oriented to reflect junior IT / SOC-relevant environments.

No VMware configuration is performed at this stage.

## Networking Model (Planned)
**Mode:** NAT-only  
**Rationale:**
- Prevents exposure to the physical LAN
- Simplifies routing and troubleshooting
- Reduces risk while still enabling realistic traffic

## Components
**VMware Virtual Network**
- Single NAT network
- DHCP enabled
- Host-only visibility via VMware NAT gateway

**Host System**
- Windows 11 host acts only as hypervisor
- No inbound services exposed from VMs
- No port forwarding unless explicitly documented

## VM Network Placement
| VM Name | Network Mode | Notes |
|-------|--------------|-------|
| RAS-lab-core-linux | NAT | Server-style role |
| RAS-lab-workstation-win11 | NAT | Endpoint-style role |

## Traffic Rules (Conceptual)
- VM ↔ VM: Allowed only if explicitly required
- VM → Internet: Allowed for updates and tooling
- Internet → VM: Blocked by default
- Host → VM: Administrative access only

## Logging Considerations
- Network activity should generate logs but not excessive noise
- Firewall events are in-scope for detection exercises
- Splunk ingestion points documented separately

## Security Rationale
This model mirrors:
- Small org lab setups
- SOC training environments
- Entry-level enterprise segmentation principles

It intentionally avoids:
- Bridged networking
- Complex VLANs
- External exposure

## Status
- Documentation only
- No VMware changes applied yet
