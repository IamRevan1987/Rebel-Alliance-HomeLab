# VM Roles and Responsibilities

## Overview
This document defines the intended roles, responsibilities, and security posture of each virtual machine 
in the RAS-lab environment. No VMs are built at this stage; this is a documentation-first design artifact.

## VM: RAS-Workstation-Alpha
**Role:** Core services, web hosting, logging source, security baseline, AI Integration

**Purpose**
- Acts as the primary “server” system
- Centralizes authentication logs and application logs
- Hosts faux website to demonstrate network connectivity/shares.

**Planned Responsibilities**
- Active Directory user and group management
- Web Services
- SOC Logging and tests

**Security Expectations**
- Minimal package install
- Principle of least privilege
- SSH hardening (key-based auth planned)
- Local firewall enabled
- Central log forwarding to TBD SIEM

**Primary Log Sources**
- `/var/log/auth.log`
- `/var/log/syslog`
- Application logs under `/var/log/ras/`

---

## VM: RAS-Workstation-Beta
**Role:** End-user workstation and event-generation source

**Purpose**
- Dummy Windows setup, available for sandboxing
- Potential for practice with ticketing systems
- Quick startup makes it easy to confirm network stability

---

## VM: RAS-Workstation-Zeta
**Role:** End-user workstation and lab sandboxing

**Purpose**
- SIEM and AI setup and Lab environment
