# Demo Path — Rebel Alliance Systems Home Lab

This document outlines a recommended walkthrough order for reviewers.

## 1. Architecture Overview
- `docs/architecture/overview.md`
- `docs/architecture/vm-roles.md`

Explains the lab’s scope, VM roles, and design constraints.

## 2. Network Design
- `docs/network/vmware-networking.md`
- `docs/network/ip-hostname-map.md`
- `docs/network/firewall-notes.md`

Shows how a simple, constrained network is intentionally designed and documented.

## 3. Identity and Roles
- `docs/users-roles/org-structure.md`
- `docs/users-roles/account-mapping.md`
- `docs/users-roles/access-examples.md`

Demonstrates role-based thinking and least-privilege concepts.

## 4. Email Strategy
- `docs/email/email-strategy.md`
- `docs/email/address-list.md`

Documents symbolic, role-based email identities without real mail flow.

## 5. Security and Logging
- `security/`
- `splunk/`

Covers baseline hardening, logging strategy, and detection concepts.

## 6. Dependency Security
- `dependency-security/`

Shows awareness of software supply chain risk using free tooling.

## 7. Build Journal
- `journal/build-log.md`

Chronological record of decisions and changes made during the build.
