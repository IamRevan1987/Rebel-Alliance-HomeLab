# IP Address and Hostname Mapping

## Purpose
This document defines the logical IP addressing and hostname conventions for the RAS-lab environment.

Actual IPs will be assigned dynamically via DHCP; this mapping exists for documentation, troubleshooting, and interview walkthrough purposes.

## Naming Convention
**Hostname Format:**  
`RAS-<role>-<os>`

Examples:
- `RAS-WorkstationB-Win11`
- `RAS-WorkstationZ-Ubuntu`

## Planned Network Range
- VirtualBox NAT subnet (auto-assigned)
- Example range: `10.0.1.20` - `10.0.1.50`
- Gateway: RAS_Holonet

# RAS Lab – Logical Infrastructure Mapping

## Overview
This repository documents the logical layout of the **RAS Lab** virtualized environment running on a single physical host using Oracle VirtualBox. The lab is designed for Active Directory, DNS, DHCP, IIS, Windows client integration, Web Hosting Capabilities, Linux domain authentication and AI Integration with Cybersecurity.

## Host System
| Item | Details |
|----|----|
| Hostname | BEELINK-SER9 |
| Hardware | AMD Ryzen 9 6900HX, 32GB RAM |
| OS | Windows 11 Pro 25H2 (Build 26200.7623) |
| Hypervisor | Oracle VirtualBox |


## Domain Configuration
| Item | Value |
|----|------|
| Domain Name | **RAS-Lab.net** |
| Forest | RAS-Lab.net |
| Functional Level | Windows Server 2022 |
| Primary Domain Controller | RAS-Workstation-Alpha |
| DNS Provider | Windows Server 2022 |
| DHCP Provider | Windows Server 2022 |


## Network Configuration
| Item | Value |
|----|------|
| VirtualBox Network Type | **Internal Network** |
| Network Name | RAS-LAB |
| IP Addressing | Server = Static, Clients = DHCP |
| Default Gateway | Provided by Server DHCP |
| DNS Resolution | Internal (AD-integrated DNS) |


## Server Role Mapping (VM1)
**RAS-Workstation-Alpha**
- Active Directory Domain Services
- DNS (AD-integrated)
- DHCP
- IIS (Test / Lab Website)


## Snapshot Strategy
* Take Snapshots after computers shut down to conserve disk space.
Recommended checkpoints:
- Pre-domain configuration (Saved as `Initialized`)
- Post-AD/DNS/DHCP/Website installation (Saved as `Server Ready`)
- Post-client domain join/Website Confirmation (Saved as `Server Established`)
- Post-Linux AD integration (Saved as `Dev Computer Operational`)
- Stable baseline snapshot (Saved as `RAS Established`)


## Status
- Active during lab working hours.





