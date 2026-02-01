# Account Mapping

## Purpose
This document maps organizational roles to operating system user accounts within the RAS-lab environment. 
The goal is to demonstrate clear, role-based identity management.

No accounts are created at this stage.

## Naming Rules
- Role-first usernames
- No personal names
- Consistent across Linux and Windows where applicable

## Account List
| Role | Username | System(s) | Privilege Level |
|----|---------|----------|-----------------|
| IT Administrator | admin_it | Linux / Windows | Admin |
| CEO | ceo_exec | Windows | Standard |
| Sales | sales_01 | Windows | Standard |
| Sales | sales_02 | Windows | Standard |
| HR | hr_people | Windows | Standard |
| UX / Web | ux_web | Windows | Standard |
| Developer | dev_py01 | Linux / Windows | Standard |
| Developer | dev_py02 | Linux / Windows | Standard |

## Privilege Rationale
- Only `admin_it` has administrative rights
- Developers do not receive admin by default
- Executive account intentionally limited
- Supports least-privilege demonstrations

## Security Scenarios Enabled
- Privilege escalation attempts
- Credential misuse detection
- Role-based access review
- Incident response tied to specific users

## Constraints
- No shared accounts
- No real credentials
- Password policies documented later

## Status
- Design only
- Accounts to be created during build phase
