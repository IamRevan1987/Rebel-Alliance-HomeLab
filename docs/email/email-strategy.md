# Email Strategy

## Purpose
This document describes the email identity strategy for the RAS-lab environment. Email is treated as a documentation and identity artifact, not as a fully operational mail system.

The goal is to demonstrate realistic identity planning without introducing unnecessary risk or external dependencies.

## Design Principles
- Role-based identities only
- No personal or real email accounts
- Free-tier or symbolic usage
- Documented, not production-grade

## Model
Emails represent:
- Organizational identity
- Common enterprise roles
- Security discussion points (phishing, spoofing, access)

They do NOT represent:
- Live mail infrastructure
- Persistent communication systems

## Role-Based Addresses
- `admin@rebelalliancelab`
- `ceo@rebelalliancelab`
- `sales@rebelalliancelab`
- `hr@rebelalliancelab`
- `dev@rebelalliancelab`

Individual user mailboxes are intentionally avoided.

## Usage in Lab
Email identities may be referenced in:
- Documentation
- Screenshots (redacted)
- Security scenarios
- Incident response walkthroughs

## Security Rationale
This approach:
- Avoids exposure of real accounts
- Prevents trial lock-in
- Keeps focus on identity and security concepts

## Constraints
- No Gmail or personal providers
- No paid services
- No live mail flow required

## Status
- Documentation only
- No email services configured

