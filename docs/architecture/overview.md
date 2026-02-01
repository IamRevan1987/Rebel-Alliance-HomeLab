# RAS-lab Architecture Overview

## Purpose
Rebel Alliance Systems Home Lab (RAS-lab) is an interview-ready, security-focused home lab that 
demonstrates practical IT and junior cybersecurity fundamentals under real-world constraints.

## Scope and Constraints
- Single Windows 11 host running VMware
- Maximum of two VMs running at any time
- Freeware or free-tier tools only
- No real personal email accounts tied to trials
- Documentation-first: every build step should be reproducible from this repo

## High-Level Architecture
**Host (Physical)**
- Windows 11 (primary workstation and hypervisor host)
- VMware for VM lifecycle (creation, snapshots, networking)

**Virtual Machines (Planned)**
1. `RAS-lab-core-linux`
   - Primary “server” role for core services, logging sources, and security baseline
   - Linux user accounts map to org roles (documented in /docs/users-roles)

2. `RAS-lab-workstation-win11`
   - User/workstation role to simulate typical endpoint activity
   - Windows event logging source for detections and troubleshooting scenarios

## Identity Model
**Organization:** Rebel Alliance Systems  
**Environment Tag:** `lab`  
**Usernames (role-first):**
- `admin_it`
- `ceo_exec`
- `sales_01`, `sales_02`
- `hr_people`
- `ux_web`
- `dev_py01`, `dev_py02`

Email identities are role-based and symbolic (documented in /docs/email).

## Logging and Security Evidence (Planned)
- Central logging and detections using Splunk
- Naming targets:
  - Index: `ras_lab`
  - Source types:
    - `ras:linux:auth`
    - `ras:windows:event`
    - `ras:app:python`

Dependency security evidence will be captured via GitHub Dependabot (baseline) and optional Snyk integration (documented in /dependency-security).

## Repository-as-Portfolio Principle
This repo is the primary artifact. Reviewers should be able to:
- Understand the architecture quickly
- Follow a guided demo path (see /docs/demo-path.md)
- See constraints and decisions documented
- Verify security-minded practices (hardening notes, detections, dependency security)

## Phase Status
- Phase 1: Complete (repo scaffold, branches, protections, README, demo path)
- Phase 2: In progress (architecture & identity docs only — no VMware/VM build yet)
