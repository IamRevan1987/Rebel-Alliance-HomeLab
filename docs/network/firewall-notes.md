# Firewall Configuration Notes

## Purpose
This document outlines the firewall posture for RAS-lab systems. The intent is to demonstrate 
security-first defaults without overengineering.

No firewall rules are applied at this stage.

## Design Principles
- Default deny where feasible
- Explicit allow for required services only
- Visibility over silence (log meaningful events)

## Linux VM (RAS-lab-core-linux)
**Firewall Tool (Planned):**
- `ufw` (simplicity and interview familiarity)

**Baseline Posture**
- Inbound: Deny all by default
- Outbound: Allow all by default

**Planned Allows**
- SSH (administrative access)
- Log forwarding (if required by Splunk setup)

**Logging**
- Log denied inbound connections
- Avoid excessive outbound logging

## Windows 11 VM (RAS-lab-workstation-win11)
**Firewall Tool:**
- Windows Defender Firewall

**Baseline Posture**
- Inbound: Block unsolicited traffic
- Outbound: Allow standard user activity

**Planned Allows**
- OS updates
- Log forwarding / Splunk agent (if deployed)

**Logging**
- Security-relevant blocks only
- Focus on events useful for detection demos

## Host System (Out of Scope)
- Host firewall configuration is not modified
- Host is treated as trusted hypervisor only

## Security Rationale
This approach mirrors:
- Small enterprise defaults
- SOC lab expectations
- Junior IT operational realities

It avoids:
- Overly granular rules
- False sense of “perfect security”

## Status
- Documentation only
- No firewall rules implemented yet
