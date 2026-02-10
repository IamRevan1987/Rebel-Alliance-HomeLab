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

## Logical Mapping (Example)
| System | Hostname | IP Type | Notes |
|------|----------|---------|-------|
| Windows 2022 Server | **INSERT** | DHCP | Primary server role |
| Windows 10 VM | rasworkstationb | DHCP | User workstation |

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

