# VM Roles and Responsibilities

## Overview
This document defines the intended roles, responsibilities, and security posture of each virtual machine 
in the RAS-lab environment. No VMs are built at this stage; this is a documentation-first design artifact.

## VM: RAS-lab-core-linux
**Role:** Core services, logging source, and security baseline

**Purpose**
- Acts as the primary “server” system
- Centralizes authentication logs and application logs
- Serves as a realistic Linux administration target

**Planned Responsibilities**
- Linux user account hosting (role-based users)
- SSH access management
- System and auth logging
- Python-based service or utility logging (lab-safe)

**Security Expectations**
- Minimal package install
- Principle of least privilege
- SSH hardening (key-based auth planned)
- Local firewall enabled
- Central log forwarding to Splunk

**Primary Log Sources**
- `/var/log/auth.log`
- `/var/log/syslog`
- Application logs under `/var/log/ras/`

---

## VM: RAS-lab-workstation-win11
**Role:** End-user workstation and event-generation source

**Purpos**
