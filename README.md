# Rebel Alliance Systems Home Lab (RAS-lab)

This repository documents a narrative-driven, security-focused IT home lab designed to demonstrate junior system administration and cybersecurity fundamentals under realistic constraints.<br>

The lab represents an **imaginary startup**, *Rebel Alliance Systems*, and is intentionally built with limited resources, free-tier tooling, and strict operational boundaries to mirror real-world small-environment decision making.

---

## Lab Objectives

- Demonstrate Systems Administration and Cybersecurity skills in a reproducible way
- Practice documentation-first infrastructure design
- Show evidence of security thinking: identity, logging, hardening, and detection
- Produce interview-ready artifacts recruiters can review quickly
- Demonstrate Local-First AI Integration and RAG Repository

## Core Constraints

- Single Windows 11 host using VirtualBox
- Maximum of **two running VMs at any time**
- Free or free-tier tools only
- No real personal email accounts tied to services
- Documentation-first, reproducible build

## Environment Overview

- **Domain Information**: RAS-Lab.net (**Netbios**: RAS-LAB)
- **Windows 2022 Server VM**: central services, logging, security tooling, web hosting
- **Windows 10 VM**: workstation simulation
- **Linux Ubuntu**: dev workstation simulation, AI Hosting, Cybersecurity Applications
- **Kali Linus**: Cybersecurity Applications
- **Role-based identities** only (admin, exec, dev, sales, HR)
- NAT-only networking baseline

## Security Focus Areas

- Log Parsing
- System Alerts
- System Hardening
- Local-First AI Integration

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

# Status

This lab is actively developed in phases.  
The `main` branch reflects review-ready states; active work occurs in feature branches.

## Disclaimer

This project is for educational and portfolio demonstration purposes only.  
All identities, systems, and organizations are fictional.
