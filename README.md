# Rebel Alliance Systems Home Lab (RAS-lab)

This repository documents a narrative-driven, security-focused IT home lab designed to demonstrate junior system administration and cybersecurity fundamentals under realistic constraints.

The lab represents an **imaginary startup**, *Rebel Alliance Systems*, and is intentionally built with limited resources, free-tier tooling, and strict operational boundaries to mirror real-world small-environment decision making.

---

## Lab Objectives

- Demonstrate foundational IT and cybersecurity skills in a reproducible way
- Practice documentation-first infrastructure design
- Show evidence of security thinking: identity, logging, hardening, and detection
- Produce interview-ready artifacts recruiters can review quickly

---

## Core Constraints

- Single Windows 11 host using VMware
- Maximum of **two running VMs at any time**
- Free or free-tier tools only
- No real personal email accounts tied to services
- Documentation-first, reproducible build

---

## Environment Overview

- **Core Linux VM**: central services, logging, security tooling
- **Windows 11 VM**: workstation simulation
- **Role-based identities** only (admin, exec, dev, sales, HR)
- NAT-only networking baseline

---

## Security Focus Areas

- Account and role modeling
- Baseline system hardening
- Centralized logging (Splunk)
- Simple detection logic
- Dependency security (Dependabot, optional Snyk)

---

## Repository Structure

This repository is intentionally structured so reviewers can explore it top-down:

- `docs/` — architecture, network, users, email, demo walkthrough
- `infra/` — VM and OS configuration notes
- `security/` — hardening, threat modeling, incident response
- `splunk/` — inputs, sources, detections
- `dependency-security/` — software supply chain evidence
- `journal/` — build log and decision tracking

See **docs/demo-path.md** for a guided walkthrough.

---

## Status

This lab is actively developed in phases.  
The `main` branch reflects review-ready states; active work occurs in feature branches.

---

## Disclaimer

This project is for educational and portfolio demonstration purposes only.  
All identities, systems, and organizations are fictional.
