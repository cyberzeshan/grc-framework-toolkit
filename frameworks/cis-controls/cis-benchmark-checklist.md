# CIS Benchmark Hardening Verification Checklist

> **Framework:** CIS Controls v8 | CIS Benchmarks
> **Purpose:** Verification checklist for hardening key platforms per CIS Benchmark recommendations
> **Usage:** Run against each system type; document compliance status and deviations; use as evidence for audits and assessments

---

## How to Use This Checklist

1. **Select the applicable platform sections** for each system type in your environment
2. **Score each item** using the status codes below
3. **Document deviations** with a compensating control or remediation plan
4. **Retain completed checklists** as audit evidence — date-stamp each run
5. **Re-verify** after every major change and at least quarterly for critical systems

### Status Codes

| Code | Status | Meaning |
|:---:|:---|:---|
| ✅ | Pass | Control is configured per CIS guidance |
| ❌ | Fail | Control is not configured; remediation required |
| ⚠️ | Partial | Partially compliant; documented deviation |
| N/A | Not Applicable | Control not applicable to this system/environment |
| C | Compensating | Alternate control provides equivalent protection (must be documented) |

---

## Section 1 — Windows Endpoint Hardening (CIS Benchmark: Windows 10/11)

**System Assessed:** _____________ **Assessor:** _____________ **Date:** _____________

### 1.1 Account Policies

| # | Check | CIS Ref | Status | Notes |
|:---:|:---|:---:|:---:|:---|
| 1.1.1 | Password history: 24 or more | 1.1.1 | | |
| 1.1.2 | Maximum password age: 365 or fewer days | 1.1.2 | | |
| 1.1.3 | Minimum password age: 1 or more days | 1.1.3 | | |
| 1.1.4 | Minimum password length: 14 or more characters | 1.1.4 | | |
| 1.1.5 | Password complexity requirements enabled | 1.1.5 | | |
| 1.1.6 | Account lockout duration: 15 or more minutes | 1.2.1 | | |
| 1.1.7 | Account lockout threshold: 5 or fewer invalid attempts | 1.2.2 | | |
| 1.1.8 | Reset account lockout counter after: 15 or more minutes | 1.2.3 | | |

### 1.2 Local Policies — User Rights

| # | Check | CIS Ref | Status | Notes |
|:---:|:---|:---:|:---:|:---|
| 1.2.1 | Access Credential Manager as trusted caller: No one | 2.2.1 | | |
| 1.2.2 | Allow log on locally: restricted to authorized users | 2.2.6 | | |
| 1.2.3 | Deny access to this computer from network: Guests, Local admin | 2.2.20 | | |
| 1.2.4 | Deny log on as batch job: Guests | 2.2.21 | | |
| 1.2.5 | Deny log on through Remote Desktop Services: Guests | 2.2.24 | | |
| 1.2.6 | Take ownership of files or objects: Administrators only | 2.2.38 | | |

### 1.3 Security Options

| # | Check | CIS Ref | Status | Notes |
|:---:|:---|:---:|:---:|:---|
| 1.3.1 | Accounts: Block Microsoft accounts | 2.3.1.1 | | |
| 1.3.2 | Accounts: Guest account status: Disabled | 2.3.1.4 | | |
| 1.3.3 | Interactive logon: Do not display last signed-in: Enabled | 2.3.7.4 | | |
| 1.3.4 | Interactive logon: Machine inactivity limit: 900 seconds | 2.3.7.3 | | |
| 1.3.5 | Microsoft network client: Digitally sign communications (always): Enabled | 2.3.8.1 | | |
| 1.3.6 | Network access: Do not allow anonymous enumeration of SAM accounts: Enabled | 2.3.11.2 | | |
| 1.3.7 | Network security: LAN Manager authentication: NTLMv2 only | 2.3.11.7 | | |
| 1.3.8 | Network security: Minimum session security for NTLM: 128-bit | 2.3.11.9 | | |
| 1.3.9 | Shutdown: Allow system to be shut down without logging on: Disabled | 2.3.15.1 | | |
| 1.3.10 | UAC: Admin Approval Mode for built-in Administrator: Enabled | 2.3.17.1 | | |
| 1.3.11 | UAC: Behavior of elevation prompt for standard users: Deny | 2.3.17.5 | | |

### 1.4 Windows Firewall

| # | Check | CIS Ref | Status | Notes |
|:---:|:---|:---:|:---:|:---|
| 1.4.1 | Domain Profile: Firewall state: On | 9.1.1 | | |
| 1.4.2 | Domain Profile: Inbound connections: Block | 9.1.2 | | |
| 1.4.3 | Private Profile: Firewall state: On | 9.2.1 | | |
| 1.4.4 | Private Profile: Inbound connections: Block | 9.2.2 | | |
| 1.4.5 | Public Profile: Firewall state: On | 9.3.1 | | |
| 1.4.6 | Public Profile: Inbound connections: Block | 9.3.2 | | |

### 1.5 Advanced Audit Policy

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 1.5.1 | Audit Account Logon Events: Success and Failure | | |
| 1.5.2 | Audit Account Management: Success and Failure | | |
| 1.5.3 | Audit Logon Events: Success and Failure | | |
| 1.5.4 | Audit Policy Change: Success and Failure | | |
| 1.5.5 | Audit Privilege Use: Success and Failure | | |
| 1.5.6 | Audit System Events: Success and Failure | | |
| 1.5.7 | Audit Object Access: Failure | | |
| 1.5.8 | Audit Process Creation: Success | | |

**Section 1 Score:** _____ / _____ items passing &nbsp;&nbsp; **Compliance %:** _____%

---

## Section 2 — Linux Server Hardening (CIS Benchmark: Ubuntu 20.04/22.04 LTS)

**System Assessed:** _____________ **Assessor:** _____________ **Date:** _____________

### 2.1 Filesystem Configuration

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 2.1.1 | /tmp is a separate partition | | |
| 2.1.2 | nodev option set on /tmp | | |
| 2.1.3 | nosuid option set on /tmp | | |
| 2.1.4 | noexec option set on /tmp | | |
| 2.1.5 | Sticky bit on world-writable directories | | |
| 2.1.6 | Disable automounting (autofs): disabled | | |
| 2.1.7 | Disable USB storage | | |

### 2.2 Software Updates

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 2.2.1 | Ensure package manager repositories are configured | | |
| 2.2.2 | Ensure updates are installed | | |
| 2.2.3 | Automatic security updates enabled (unattended-upgrades) | | |

### 2.3 Network Configuration

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 2.3.1 | IP forwarding disabled (unless router) | | |
| 2.3.2 | Packet redirect sending disabled | | |
| 2.3.3 | Source routed packets not accepted | | |
| 2.3.4 | ICMP redirects not accepted | | |
| 2.3.5 | TCP SYN Cookies enabled | | |
| 2.3.6 | IPv6 router advertisements not accepted | | |
| 2.3.7 | Wireless interfaces disabled | | |

### 2.4 Firewall (UFW or iptables)

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 2.4.1 | UFW (or nftables/iptables) installed and enabled | | |
| 2.4.2 | Default deny inbound policy | | |
| 2.4.3 | Default deny outbound policy | | |
| 2.4.4 | Loopback traffic configured | | |
| 2.4.5 | Only required ports open (verify with: ss -tlnp) | | |

### 2.5 Access, Authentication, and Authorization

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 2.5.1 | SSH Protocol 2 only | | |
| 2.5.2 | SSH LogLevel: INFO or VERBOSE | | |
| 2.5.3 | SSH MaxAuthTries: 4 or less | | |
| 2.5.4 | SSH IgnoreRhosts: yes | | |
| 2.5.5 | SSH HostbasedAuthentication: no | | |
| 2.5.6 | SSH PermitRootLogin: no | | |
| 2.5.7 | SSH PermitEmptyPasswords: no | | |
| 2.5.8 | SSH PermitUserEnvironment: no | | |
| 2.5.9 | SSH warning banner configured | | |
| 2.5.10 | Password hashing algorithm: SHA-512 | | |
| 2.5.11 | Password expiration: 365 days or less | | |
| 2.5.12 | Password minimum days: 7 or more | | |
| 2.5.13 | Password warning days: 7 or more | | |
| 2.5.14 | Default password complexity configured (libpam-pwquality) | | |
| 2.5.15 | Password reuse limited (5 or more) | | |
| 2.5.16 | System accounts non-login | | |
| 2.5.17 | Default group for root: GID 0 | | |
| 2.5.18 | root is the only UID 0 account | | |

### 2.6 Logging and Auditing

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 2.6.1 | auditd installed and enabled | | |
| 2.6.2 | auditd log file size configured | | |
| 2.6.3 | Audit system is not disabled when full | | |
| 2.6.4 | Date and time changes audited | | |
| 2.6.5 | User and group modifications audited | | |
| 2.6.6 | Network environment changes audited | | |
| 2.6.7 | MAC policy changes audited | | |
| 2.6.8 | Login and logout events audited | | |
| 2.6.9 | Session initiation audited | | |
| 2.6.10 | Privilege escalation (sudo) audited | | |
| 2.6.11 | Kernel modules audited | | |
| 2.6.12 | rsyslog or syslog-ng installed and enabled | | |
| 2.6.13 | Logs sent to remote log server | | |

**Section 2 Score:** _____ / _____ items passing &nbsp;&nbsp; **Compliance %:** _____%

---

## Section 3 — Cloud Security (CIS AWS Foundations Benchmark)

**Account/Environment:** _____________ **Assessor:** _____________ **Date:** _____________

### 3.1 Identity and Access Management

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 3.1.1 | Root account MFA enabled | | |
| 3.1.2 | No root account access keys | | |
| 3.1.3 | MFA enabled for all IAM users with console access | | |
| 3.1.4 | IAM password policy: minimum 14 characters | | |
| 3.1.5 | IAM password policy: requires numbers | | |
| 3.1.6 | IAM password policy: requires symbols | | |
| 3.1.7 | IAM password policy: password expiration 90 days | | |
| 3.1.8 | IAM password policy: prevents password reuse (5+) | | |
| 3.1.9 | No unused credentials (>90 days) | | |
| 3.1.10 | Access keys rotated within 90 days | | |
| 3.1.11 | IAM users receive permissions only through groups | | |
| 3.1.12 | Support role created for AWS Support | | |

### 3.2 Logging

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 3.2.1 | CloudTrail enabled in all regions | | |
| 3.2.2 | CloudTrail log file validation enabled | | |
| 3.2.3 | S3 bucket for CloudTrail logs not publicly accessible | | |
| 3.2.4 | CloudTrail integrated with CloudWatch Logs | | |
| 3.2.5 | AWS Config enabled in all regions | | |
| 3.2.6 | S3 bucket access logging enabled | | |
| 3.2.7 | VPC Flow Logs enabled | | |

### 3.3 Monitoring (CloudWatch Alarms)

| # | Alert | Status | Notes |
|:---:|:---|:---:|:---|
| 3.3.1 | Unauthorized API calls | | |
| 3.3.2 | Management Console sign-in without MFA | | |
| 3.3.3 | Root account usage | | |
| 3.3.4 | IAM policy changes | | |
| 3.3.5 | CloudTrail configuration changes | | |
| 3.3.6 | Authentication failures | | |
| 3.3.7 | Disabling or scheduled deletion of CMKs | | |
| 3.3.8 | S3 bucket policy changes | | |
| 3.3.9 | AWS Config changes | | |
| 3.3.10 | Security Group changes | | |
| 3.3.11 | Network ACL changes | | |
| 3.3.12 | Network gateway changes | | |
| 3.3.13 | Route table changes | | |
| 3.3.14 | VPC changes | | |

### 3.4 Networking

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 3.4.1 | No Security Groups allow 0.0.0.0/0 to port 22 (SSH) | | |
| 3.4.2 | No Security Groups allow 0.0.0.0/0 to port 3389 (RDP) | | |
| 3.4.3 | VPC flow logging enabled for all VPCs | | |
| 3.4.4 | Default Security Group restricts all traffic | | |
| 3.4.5 | No public subnets except for load balancers/NAT GW | | |

**Section 3 Score:** _____ / _____ items passing &nbsp;&nbsp; **Compliance %:** _____%

---

## Section 4 — Microsoft 365 Hardening (CIS M365 Foundations Benchmark)

**Tenant:** _____________ **Assessor:** _____________ **Date:** _____________

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 4.1 | MFA enabled for all users | | |
| 4.2 | MFA enabled for all Global Administrators | | |
| 4.3 | Legacy authentication protocols blocked | | |
| 4.4 | Conditional Access: block sign-in from legacy auth | | |
| 4.5 | Unified Audit Log enabled | | |
| 4.6 | Admin audit logging enabled | | |
| 4.7 | Mailbox auditing enabled for all users | | |
| 4.8 | Microsoft Defender anti-phishing enabled | | |
| 4.9 | Safe Attachments policy enabled | | |
| 4.10 | Safe Links policy enabled | | |
| 4.11 | DKIM enabled for all sending domains | | |
| 4.12 | SPF configured for all sending domains | | |
| 4.13 | DMARC policy configured (p=reject or quarantine) | | |
| 4.14 | External email warning banner enabled | | |
| 4.15 | Teams: Anonymous join disabled | | |
| 4.16 | SharePoint: External sharing limited or disabled | | |
| 4.17 | OneDrive: External sharing limited | | |
| 4.18 | Password expiration set (or passwordless enabled) | | |
| 4.19 | Microsoft Secure Score reviewed monthly | | |
| 4.20 | Privileged Identity Management (PIM) enabled for admin roles | | |

**Section 4 Score:** _____ / _____ items passing &nbsp;&nbsp; **Compliance %:** _____%

---

## Section 5 — Network Device Hardening (CIS Benchmark: Network Devices)

**Device Type / Model:** _____________ **Assessor:** _____________ **Date:** _____________

| # | Check | Status | Notes |
|:---:|:---|:---:|:---|
| 5.1 | Default credentials changed | | |
| 5.2 | Unnecessary services disabled (Telnet, HTTP management, SNMP v1/v2) | | |
| 5.3 | SSH v2 used for management (Telnet disabled) | | |
| 5.4 | HTTPS-only for web management | | |
| 5.5 | Management access restricted to management VLAN | | |
| 5.6 | Console port password protected | | |
| 5.7 | Login banner configured | | |
| 5.8 | Session timeout configured (≤15 minutes) | | |
| 5.9 | NTP configured for accurate time synchronization | | |
| 5.10 | Syslog configured and sending to central log server | | |
| 5.11 | SNMP v3 with authentication and encryption (or disabled) | | |
| 5.12 | Unused ports disabled | | |
| 5.13 | Firmware up to date (check vendor advisory) | | |
| 5.14 | Access control lists restrict management traffic | | |

**Section 5 Score:** _____ / _____ items passing &nbsp;&nbsp; **Compliance %:** _____%

---

## Overall Compliance Summary

| Section | Platform | Items Checked | Items Passing | Compliance % | Critical Fails |
|:---|:---|:---:|:---:|:---:|:---:|
| 1 | Windows Endpoint | | | | |
| 2 | Linux Server | | | | |
| 3 | AWS Cloud | | | | |
| 4 | Microsoft 365 | | | | |
| 5 | Network Devices | | | | |
| **Total** | | | | | |

---

## Findings Requiring Immediate Remediation

| # | Platform | Finding | Risk | Owner | Target Date |
|:---:|:---|:---|:---:|:---|:---|
| | | | Critical / High / Medium | | |

---

## Remediation Tracking

| Finding | Remediation Action | Owner | Status | Completion Date |
|:---|:---|:---|:---|:---|
| | | | Open / In Progress / Closed | |

---

## Deviation Log

> Document all items marked ⚠️ Partial or C (Compensating) — these require formal justification.

| Item | Platform | Deviation | Business Justification | Compensating Control | Approved By | Expiry |
|:---|:---|:---|:---|:---|:---|:---|
| | | | | | | |

---

*Reference: CIS Controls v8 | CIS Benchmarks (cisecurity.org) | Reassess after major changes and at least quarterly for critical systems*
