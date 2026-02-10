# IP Address and Hostname Mapping

## Purpose
This document defines the logical IP addressing and hostname conventions for the RAS-lab environment.

Actual IPs will be assigned dynamically via DHCP; this mapping exists for documentation, troubleshooting, and interview walkthrough purposes.

## Naming Convention
**Hostname Format:**  
`ras-<role>-<os>`

Examples:
- `ras-core-linux`
- `ras-workstation-win11`

## Planned Network Range
- VirtualBox NAT subnet (auto-assigned)
- Example range: `10.0.1.20` - `10.0.1.50`
- Gateway: RAS_Holonet

# RAS Lab – Logical Infrastructure Mapping

## Overview
This repository documents the logical layout of the **RAS Lab** virtualized environment running on a single physical host using Oracle VirtualBox. The lab is designed for Active Directory, DNS, DHCP, IIS, Windows client integration, and Linux domain authentication.

---

## Host System

| Item | Details |
|----|----|
| Hostname | BEELINK-SER9 |
| Hardware | AMD Ryzen 9 6900HX, 32GB RAM |
| OS | Windows 11 Pro 25H2 (Build 26200.7623) |
| Hypervisor | Oracle VirtualBox |

---

## Domain Configuration

| Item | Value |
|----|------|
| Domain Name | **RAS-Lab.net** |
| Forest | RAS-Lab.net |
| Functional Level | Windows Server 2022 |
| Primary Domain Controller | RAS-Workstation-Alpha |
| DNS Provider | Windows Server 2022 |
| DHCP Provider | Windows Server 2022 |

---

## Network Configuration

| Item | Value |
|----|------|
| VirtualBox Network Type | **Internal Network** |
| Network Name | RAS-LAB |
| IP Addressing | Server = Static, Clients = DHCP |
| Default Gateway | Provided by Server DHCP |
| DNS Resolution | Internal (AD-integrated DNS) |

---

## Logical VM Mapping

| System | Hostname | OS | IP Type | Resources | Notes |
|------|----------|----|---------|----------|------|
| Host Machine | BEELINK-SER9 | Windows 11 | N/A | Ryzen 9 / 32GB RAM | Physical host |
| VM1 – Core Server | **RAS-Workstation-Alpha** | Windows Server 2022 | **Static IP** | 4 vCPU / 8GB RAM / 75GB Disk | AD DS, DNS, DHCP, IIS |
| VM2 – Workstation | RASWorkstationB | Windows 10 | DHCP | 4 vCPU / 8GB RAM / 50GB Disk | Domain-joined user workstation |
| VM3 – Linux Core | RAS-Core-UbuntuLinux | Ubuntu 24.02 LTS | DHCP | TBD | Linux AD integration, sudo via domain |
| VM4 – Kali (Deferred) | RAS-Core-KaliLinux | Kali Linux | TBD | TBD | Security testing (future phase) |

---

## VM Storage Locations

| VM | Disk Location |
|----|--------------|
| RAS-Workstation-Alpha | `C:\Users\Rebel Alliance Lab\.VirtualBox\RAS-Workstation-Alpha` |
| RASWorkstationB | `E:\01 Active VMs\RASWorkstationB` |
| RAS-Core-UbuntuLinux | `E:\01 Active VMs\` |
| RAS-Core-KaliLinux | TBD |

---

## Server Role Mapping (VM1)

**RAS-Workstation-Alpha**
- Active Directory Domain Services
- DNS (AD-integrated)
- DHCP
- IIS (Test / Lab Website)

---

## Snapshot Strategy

Recommended checkpoints:
- Pre-domain configuration
- Post-AD/DNS/DHCP installation
- Pre-client domain join
- Pre-Linux AD integration
- Stable baseline snapshot

---

## Notes
- All client systems receive IP configuration via DHCP.
- Server maintains a static IP for domain stability.
- Linux and Kali systems are intended for advanced authentication and security labs.
- This lab is designed for learning, testing, and portfolio demonstration.


## Rationale
- DHCP avoids unnecessary complexity
- Hostnames provide human-readable identity
- Mapping supports log analysis and Splunk searches

## Logging Context
Logs should reference:
- **Hostname**: RAS-WorkstationAlpha
- **Domain Name**: RAS-Lab.net
- **DNS**: RAS-WORKSTATION
- **DNS Address**: 10.0.1.5

This allows:
- Correlation across Linux and Windows logs
- Easier incident walkthroughs

## Constraints
- No static IPs required
- Hostname resolution handled locally per OS

## Status
- Active during lab working hours.


