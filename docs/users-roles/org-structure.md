# Organizational Structure

## Purpose
This document defines the fictional organizational structure for Rebel Alliance Systems. It provides 
context for user accounts, access decisions, logging behavior, and security scenarios demonstrated in 
the lab.

The structure is intentionally small to reflect a startup or small business environment.

## Organization Overview
**Company Name:** Rebel Alliance Systems  
**Environment:** Lab (`ras-lab`)  
**Headcount:** 8 users

This mirrors a lean organization where individuals may wear multiple hats but access is still role-scoped.

## Roles and Functions
### Executive
**CEO**
- Strategic oversight
- Minimal technical access
- High-value account for security scenarios

### IT / Administration
**IT Administrator**
- System administration
- Account management
- Security tooling configuration
- Elevated privileges (documented and constrained)

### Sales
**Sales Users (2)**
- Standard user permissions
- Typical productivity workflows
- Common phishing and credential-risk profile

### Human Resources
**HR**
- Access to people-related documentation
- Sensitive data context (simulated)
- Non-technical role with moderate risk exposure

### UX / Web
**UX / Web**
- Design and web-related workflows
- Limited development tools
- No infrastructure-level access

### Development
**Python Developers (2)**
- Development tools access
- Non-admin by default
- Potential source of dependency-related risk (intentional)

## Security Perspective
From a security standpoint, this structure enables:
- Role-based access control examples
- Privilege separation demonstrations
- Realistic logging and alerting scenarios
- Incident response walkthroughs tied to user roles

## Constraints
- No real personal data
- No real business operations
- Roles exist solely for lab realism and documentation

## Status
- Design only
- Accounts will be documented and created later
