# Access Examples

## Purpose
This document provides illustrative examples of how access is intended to function within RAS-lab. 
These examples support interview walkthroughs and security reasoning.

No access controls are enforced at this stage.

## Example 1: IT Administrator
**User:** admin_it  
**Access:**
- Full administrative access on Linux and Windows
- User and group management
- Firewall and logging configuration

**Security Considerations:**
- High-risk account
- Elevated monitoring recommended
- Critical in incident response scenarios

## Example 2: Developer Access
**Users:** dev_py01, dev_py02  
**Access:**
- User-level access on Linux and Windows
- Development tools
- Read/write access to project directories

**Restricted:**
- No system configuration rights
- No firewall modification

**Security Considerations:**
- Dependency risk exposure
- Source of potential misconfigurations

## Example 3: Sales User
**User:** sales_01  
**Access:**
- Standard Windows user
- Productivity applications only

**Restricted:**
- No development tools
- No admin access

**Security Considerations:**
- Common phishing target
- Credential misuse scenarios

## Example 4: Executive User
**User:** ceo_exec  
**Access:**
- Standard Windows user
- Business documents (simulated)

**Restricted:**
- No administrative access
- No development tools

**Security Considerations:**
- High-value target
- Sensitive data context

## Example 5: HR User
**User:** hr_people  
**Access:**
- Standard Windows user
- HR documentation (simulated)

**Security Considerations:**
- Sensitive data exposure
- Insider risk scenarios

## Purpose in Lab
These examples enable:
- Least privilege discussions
- Access review demonstrations
- Incident response narratives

## Status
- Illustrative only
- Enforced during later build phases
