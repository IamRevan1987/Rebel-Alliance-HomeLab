# RAS-lab Architecture Overview

## Purpose
Rebel Alliance Systems Home Lab (RAS-lab) is an interview-ready, security-focused home lab that 
demonstrates practical IT and junior cybersecurity fundamentals under real-world constraints.

## Scope and Constraints
- Single Windows 11 host running VMware
- Maximum of two VMs running at any time due to hardware constraints
- Freeware or free-tier tools only
- 2 legitimate emails tied to Proton and Zoho email servers, One for the "CEO"/Dev and one for the IT Admin
- Documentation-first: every build step should be reproducible from this repo

## High-Level Architecture
**Host (Physical)**
- BEELINK SER9 with AMD Ryzen 9 6900HX Radeon Graphics, 32GB RAM Microsoft Windows 11 Version 25H2 (OS Build 26200.7623)
- VirtualBox for VM lifecycle (creation, snapshots, networking)

**Virtual Machines (Planned)**
1. `RAS-Workstation-Alpha`
   - Primary “server” role for core services, logging sources, and security baseline, web hosting.
   - Primary Accouts are Administrator and IT Admin

2. `RASWorkstationB`
   - User/workstation role to simulate typical endpoint activity
   - Primary Accounts are IT Admin and HR
  
3. `RAS-Core-UbuntuLinux` 
   - "Dev" workstation
   - Primary accounts are IT Admin/Dev
  
4. `RAS-Core-KaliLinu`
   - "Cyber Security" workstation
   - Primary account for IT Admin

## Identity Model
**Organization:** Rebel Alliance Systems  
**Environment Tag:** `lab`  
**Usernames (role-first):**
- `admin_it`
- `ceo_exec`
- `sales_01`, `sales_02`
- `hr_home`
- `ux_web`
- `dev_py01`, `dev_py02`

Email identities are role-based and symbolic (documented in /docs/email).

## Logging and Security Evidence (Planned)
- Central logging and detections using TBD SIEM
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

