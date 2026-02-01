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
- VMware NAT subnet (auto-assigned)
- Example range: `192.168.x.0/24`
- Gateway: VMware NAT gateway

## Logical Mapping (Example)
| System | Hostname | IP Type | Notes |
|------|----------|---------|-------|
| Core Linux VM | ras-core-linux | DHCP | Primary server role |
| Windows 11 VM | ras-workstation-win11 | DHCP | User workstation |

## Rationale
- DHCP avoids unnecessary complexity
- Hostnames provide human-readable identity
- Mapping supports log analysis and Splunk searches

## Logging Context
Logs should reference:
- Hostname (preferred)
- IP address (secondary)

This allows:
- Correlation across Linux and Windows logs
- Easier incident walkthroughs

## Constraints
- No static IPs required
- No DNS server deployed
- Hostname resolution handled locally per OS

## Status
- Design only
- No networking configuration performed
