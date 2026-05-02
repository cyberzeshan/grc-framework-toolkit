# CIS Controls v8 — Implementation Guide

> **Framework:** CIS Controls Version 8 (May 2021)
> **Published By:** Center for Internet Security (CIS)
> **Audience:** Security teams implementing foundational cybersecurity controls — especially mid-market, SMB, and resource-constrained organizations
> **Purpose:** Practical IG1/IG2/IG3 prioritization guide for implementing all 18 CIS Controls

---

## Overview

The CIS Controls (formerly CIS Critical Security Controls / SANS Top 20) are a prioritized set of actions to protect organizations from the most pervasive cyber attacks. Version 8 consolidated 20 controls into **18 Controls** with **153 Safeguards**, organized into three Implementation Groups.

### Why CIS Controls?

- **Prioritized:** IG1 safeguards address 77% of the most common attack techniques
- **Prescriptive:** Unlike frameworks, CIS Controls tell you exactly what to do
- **Mapped:** Controls map to NIST CSF, ISO 27001, NIST SP 800-53, and SOC 2
- **Scalable:** IG1 = basic cyber hygiene achievable by any organization; IG3 = advanced enterprise controls

---

## Implementation Groups

| Group | Label | Audience | Safeguard Count | Priority |
|:---:|:---|:---|:---:|:---|
| **IG1** | Basic Cyber Hygiene | All organizations; essential minimum | 56 safeguards | Implement first |
| **IG2** | Foundational | Organizations with IT staff; moderate risk | 74 additional safeguards (130 total) | Implement second |
| **IG3** | Advanced | Mature security programs; high-value targets | 23 additional safeguards (153 total) | Implement third |

> **Practitioner Note:** IG1 is the absolute minimum. If your organization cannot demonstrate all 56 IG1 safeguards, do not invest in IG2 or IG3. Fix the foundation first.

---

## The 18 CIS Controls

| # | Control | IG1 Safeguards | IG2 Safeguards | IG3 Safeguards |
|:---:|:---|:---:|:---:|:---:|
| 1 | Inventory and Control of Enterprise Assets | 4 | 1 | 0 |
| 2 | Inventory and Control of Software Assets | 3 | 2 | 1 |
| 3 | Data Protection | 2 | 7 | 5 |
| 4 | Secure Configuration of Enterprise Assets and Software | 4 | 6 | 2 |
| 5 | Account Management | 4 | 2 | 1 |
| 6 | Access Control Management | 3 | 4 | 1 |
| 7 | Continuous Vulnerability Management | 3 | 3 | 1 |
| 8 | Audit Log Management | 2 | 5 | 3 |
| 9 | Email and Web Browser Protections | 2 | 5 | 0 |
| 10 | Malware Defenses | 3 | 4 | 0 |
| 11 | Data Recovery | 4 | 1 | 0 |
| 12 | Network Infrastructure Management | 0 | 4 | 4 |
| 13 | Network Monitoring and Defense | 0 | 5 | 6 |
| 14 | Security Awareness and Skills Training | 2 | 7 | 0 |
| 15 | Service Provider Management | 1 | 3 | 2 |
| 16 | Application Software Security | 0 | 8 | 4 |
| 17 | Incident Response Management | 1 | 4 | 4 |
| 18 | Penetration Testing | 0 | 2 | 5 |
| **Total** | | **56** | **73** | **39** |

---

## Control 1 — Inventory and Control of Enterprise Assets

> **Why it matters:** You cannot secure what you don't know exists. Asset inventory is the foundation of every other control.

### Safeguards

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 1.1 | Establish and maintain detailed enterprise asset inventory | IG1 | Active/passive discovery of hardware; update within 30 days of change |
| 1.2 | Address unauthorized assets | IG1 | Remediate or remove unauthorized devices within 1 week of detection |
| 1.3 | Utilize an active discovery tool | IG1 | Run network discovery on a schedule; compare against known inventory |
| 1.4 | Use DHCP logging to update enterprise asset inventory | IG1 | Leverage DHCP lease data to detect new/unknown devices |
| 1.5 | Use a passive asset discovery tool | IG2 | Passively monitor network traffic for undiscovered assets |

### Implementation Guidance

**Step 1 (Immediate):** Run a network discovery scan (Nmap, Nessus, or similar). Export results and compare against your existing asset list — the gap is your unknown attack surface.

**Step 2 (30 days):** Implement automated discovery running at least weekly. Set up alerts for new devices appearing on the network.

**Step 3 (90 days):** Establish a process for handling unauthorized assets. Define: who is notified, how quickly must the device be investigated, what happens if the owner cannot be identified?

**Tools:** Nmap (free), Lansweeper (commercial), Rumble/runZero, Qualys, Rapid7 InsightVM

---

## Control 2 — Inventory and Control of Software Assets

> **Why it matters:** Unauthorized or unmanaged software is a primary malware delivery vector and a license compliance risk.

### Safeguards

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 2.1 | Establish and maintain a software inventory | IG1 | All software on managed endpoints; include version, publisher, install date |
| 2.2 | Ensure authorized software is currently supported | IG1 | Identify and remediate end-of-life software; no unsupported software in production |
| 2.3 | Address unauthorized software | IG1 | Remove or quarantine unauthorized software within 1 month of detection |
| 2.4 | Utilize automated software inventory tools | IG2 | Deploy agents or scan-based tools for continuous software inventory |
| 2.5 | Allowlist authorized software | IG2 | Implement application allowlisting on critical systems |
| 2.6 | Allowlist authorized libraries | IG3 | Restrict execution to approved libraries; address dependency risk |

### Implementation Guidance

**Priority actions:**
1. Deploy endpoint agent (e.g., Microsoft Intune, JAMF, Tanium) to collect installed software inventory
2. Identify end-of-life applications — Windows 7, older Java, Flash, IE, etc. — and create remediation plan
3. Set up alerts for installation of software not on the approved list

**Tools:** Microsoft Intune, Tanium, JAMF (macOS), ManageEngine Desktop Central, Qualys

---

## Control 3 — Data Protection

> **Why it matters:** Data is the target. Without classification and protection controls, you don't know what your crown jewels are or where they live.

### Safeguards

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 3.1 | Establish and maintain a data management process | IG1 | Document data sensitivity classification scheme |
| 3.2 | Establish and maintain a data inventory | IG1 | Identify sensitive data across all storage locations |
| 3.3 | Configure data access control lists | IG2 | Restrict access to sensitive data based on classification |
| 3.4 | Enforce data retention | IG2 | Define and enforce retention periods; dispose of data per schedule |
| 3.5 | Securely dispose of data | IG2 | Cryptographic erasure or physical destruction for sensitive data |
| 3.6 | Encrypt data on end-user devices | IG2 | Full-disk encryption on all managed endpoints (BitLocker, FileVault) |
| 3.7 | Establish and maintain a data classification scheme | IG2 | Formal classification: Public / Internal / Confidential / Restricted |
| 3.8 | Document data flows | IG2 | Map data flows for sensitive data; update when systems change |
| 3.9 | Encrypt data on removable media | IG2 | Encrypt all data stored on USB and removable media |
| 3.10 | Encrypt sensitive data in transit | IG2 | TLS 1.2+ for all sensitive data in transit; no unencrypted protocols |
| 3.11 | Encrypt sensitive data at rest | IG3 | Database-level encryption for sensitive data; key management required |
| 3.12 | Segment data processing and storage based on sensitivity | IG3 | Separate production data from dev/test; network segmentation |
| 3.13 | Deploy a data loss prevention solution | IG3 | DLP controls at endpoint, email, and cloud |
| 3.14 | Log sensitive data access | IG3 | Audit logging for access to classified data |

---

## Control 4 — Secure Configuration of Enterprise Assets and Software

> **Why it matters:** Default configurations are designed for usability, not security. Misconfigurations are the #1 cause of cloud breaches.

### Safeguards

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 4.1 | Establish and maintain a secure configuration process | IG1 | Document hardening baselines; review annually and on major changes |
| 4.2 | Establish and maintain a secure configuration process for network infrastructure | IG1 | Hardening baselines for routers, switches, firewalls |
| 4.3 | Configure automatic session locking on enterprise assets | IG1 | Auto-lock after 15 minutes of inactivity |
| 4.4 | Implement and manage a firewall on servers | IG1 | Host-based firewall on all servers |
| 4.5 | Implement and manage a firewall on end-user devices | IG1 | Host-based firewall on all user devices |
| 4.6 | Securely manage enterprise assets and software | IG2 | Dedicated admin workstations for privileged management |
| 4.7 | Manage default accounts on enterprise assets and software | IG2 | Change default credentials; disable unused default accounts |
| 4.8 | Uninstall or disable unnecessary services on enterprise assets and software | IG2 | Remove or disable services not required for function |
| 4.9 | Configure trusted DNS servers on enterprise assets | IG2 | Use org-controlled or reputable DNS (DoH/DoT); block malicious domains |
| 4.10 | Enforce automatic device lockout on portable end-user devices | IG2 | Max 20 failed attempts before device lockout |
| 4.11 | Enforce remote wipe capability on portable end-user devices | IG2 | MDM with remote wipe capability for all mobile devices |
| 4.12 | Separate enterprise workspaces on mobile end-user devices | IG3 | MDM containerization to separate work and personal data |

**Reference:** CIS Benchmarks (free, downloadable) provide OS-specific hardening guidance for Windows, Linux, macOS, and cloud platforms.

---

## Control 5 — Account Management

> **Why it matters:** Compromised credentials are involved in over 80% of data breaches. Account hygiene is non-negotiable.

### Safeguards

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 5.1 | Establish and maintain an inventory of accounts | IG1 | All user, admin, and service accounts; update within 30 days of change |
| 5.2 | Use unique passwords | IG1 | No shared accounts; unique credentials per person and per service |
| 5.3 | Disable dormant accounts | IG1 | Disable accounts unused for 45+ days |
| 5.4 | Restrict administrator privileges to dedicated admin accounts | IG1 | Separate admin accounts from daily-use accounts |
| 5.5 | Establish and maintain an inventory of service accounts | IG2 | Document all service/system accounts with owner and purpose |
| 5.6 | Centralize account management | IG3 | All accounts managed via centralized IAM / directory service |

---

## Control 6 — Access Control Management

> **Why it matters:** Least privilege limits blast radius. Over-permissioned accounts turn every breach into a catastrophe.

### Safeguards

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 6.1 | Establish an access granting process | IG1 | Formal approval required for access to sensitive systems/data |
| 6.2 | Establish an access revoking process | IG1 | Automated or same-day revocation on termination |
| 6.3 | Require MFA for externally-exposed applications | IG1 | MFA on all internet-facing apps and remote access (VPN) |
| 6.4 | Require MFA for remote network access | IG2 | MFA enforced at VPN / zero-trust gateway |
| 6.5 | Require MFA for administrative access | IG2 | Phishing-resistant MFA (FIDO2 / hardware token) for all admin accounts |
| 6.6 | Establish and maintain an inventory of authentication and authorization systems | IG2 | Document all IAM, SSO, MFA, and PAM systems |
| 6.7 | Centralize access control | IG3 | SSO with SAML/OIDC for all applications |

---

## Control 7 — Continuous Vulnerability Management

> **Why it matters:** The average time to exploit a published vulnerability is now under 15 days. Manual, annual vulnerability assessments are insufficient.

### Safeguards

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 7.1 | Establish and maintain a vulnerability management process | IG1 | Document scope, frequency, SLAs, and ownership |
| 7.2 | Establish and maintain a remediation process | IG1 | Define SLAs by severity; track to closure |
| 7.3 | Perform automated operating system patch management | IG1 | Automated patching for OS; patches deployed within defined SLAs |
| 7.4 | Perform automated application patch management | IG2 | Automated patching for applications and software libraries |
| 7.5 | Perform automated vulnerability scans of internal enterprise assets | IG2 | Credentialed scans at least quarterly (weekly for critical assets) |
| 7.6 | Perform automated vulnerability scans of externally exposed enterprise assets | IG2 | Scan all internet-facing assets weekly or continuously |
| 7.7 | Remediate detected vulnerabilities | IG3 | Track remediation velocity; measure mean-time-to-remediate per severity |

**Patch SLA Guidance:**
| Severity | CVSS | Remediation Target |
|:---|:---:|:---|
| Critical | 9.0–10.0 | 15 days |
| High | 7.0–8.9 | 30 days |
| Medium | 4.0–6.9 | 90 days |
| Low | 0.1–3.9 | 180 days |
| Informational | N/A | Next planned cycle |

---

## Control 8 — Audit Log Management

> **Why it matters:** Without logs, you cannot detect, investigate, or prove what happened. Logs are your forensic record.

### Safeguards

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 8.1 | Establish and maintain an audit log management process | IG1 | Define what is logged, retention periods, and review process |
| 8.2 | Collect audit logs | IG1 | Enable logging on all enterprise assets |
| 8.3 | Ensure adequate audit log storage | IG2 | Minimum 90 days hot retention; 1 year total |
| 8.4 | Standardize time synchronization | IG2 | NTP configured on all assets; consistent timezone (UTC recommended) |
| 8.5 | Collect detailed audit logs | IG2 | Include: timestamp, source, user, action, outcome, destination |
| 8.6 | Collect DNS query audit logs | IG2 | DNS logging for threat hunting and incident investigation |
| 8.7 | Collect URL request audit logs | IG2 | Web proxy or DNS logging for URL-level visibility |
| 8.8 | Collect command-line audit logs | IG2 | Command-line logging on servers and admin workstations (Sysmon, auditd) |
| 8.9 | Centralize audit logs | IG3 | SIEM or centralized log management; all logs shipped to central store |
| 8.10 | Retain audit logs | IG3 | Immutable log retention for 12+ months; tamper-evident storage |
| 8.11 | Conduct audit log reviews | IG3 | Automated alerting + manual review process |

---

## Control 9 — Email and Web Browser Protections

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 9.1 | Ensure use of only fully supported browsers and email clients | IG1 | Only supported, patched browser versions; retire unsupported versions |
| 9.2 | Use DNS filtering services | IG1 | DNS filtering to block malicious domains (e.g., Cisco Umbrella, Cloudflare Gateway) |
| 9.3 | Maintain and enforce network-based URL filters | IG2 | Web proxy with URL categorization; block malicious/inappropriate categories |
| 9.4 | Restrict unnecessary or unauthorized browser and email client extensions | IG2 | Allowlist of approved browser extensions; disable others |
| 9.5 | Implement DMARC | IG2 | DMARC (+ DKIM + SPF) on all sending domains; reject or quarantine policy |
| 9.6 | Block unnecessary file types | IG2 | Block email attachments by dangerous file types (.exe, .vbs, .js, macros) |
| 9.7 | Deploy and maintain email server anti-malware protections | IG2 | Email gateway scanning; sandbox detonation for attachments |

---

## Control 10 — Malware Defenses

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 10.1 | Deploy and maintain anti-malware software | IG1 | EDR/AV on all managed endpoints; signatures/models updated within 24 hours |
| 10.2 | Configure automatic anti-malware signature updates | IG1 | Automatic updates; no endpoints with outdated definitions >24 hours |
| 10.3 | Disable autorun and autoplay for removable media | IG1 | Group Policy to disable autorun on all endpoints |
| 10.4 | Configure automatic anti-malware scanning of removable media | IG2 | Scan USB media on insertion |
| 10.5 | Enable anti-exploitation features | IG2 | Enable ASLR, DEP, CFG; EDR exploit protection enabled |
| 10.6 | Centrally manage anti-malware software | IG2 | Central management console; visibility into all endpoint protection status |
| 10.7 | Use behavior-based anti-malware software | IG3 | EDR with behavioral detection (not just signature-based) |

---

## Control 11 — Data Recovery

| ID | Safeguard | IG | Description |
|:---|:---|:---:|:---|
| 11.1 | Establish and maintain a data recovery process | IG1 | Documented backup and recovery procedures; define RPO/RTO |
| 11.2 | Perform automated backups | IG1 | Automated backups for all in-scope systems; frequency per RPO |
| 11.3 | Protect recovery data | IG1 | Backup data encrypted; offsite or cloud copies; immutable backup for ransomware |
| 11.4 | Establish and maintain an isolated instance of recovery data | IG1 | Air-gapped or offline backup copy; cannot be encrypted by ransomware |
| 11.5 | Test data recovery | IG2 | Restore testing at least quarterly; document results; measure against RTO |

---

## Controls 12–18 Summary

### Control 12 — Network Infrastructure Management (IG2+)
Secure network devices, implement network management controls, segment management traffic, and manage all network infrastructure through approved change management.

### Control 13 — Network Monitoring and Defense (IG2+)
Centralize security event alerting; deploy IDS/IPS; collect NetFlow data; deploy network traffic analysis (NTA); operate a Security Operations Center (SOC) or MDR for IG3.

### Control 14 — Security Awareness and Skills Training
**IG1:** Establish a security awareness program; conduct training at least annually. **IG2:** Role-based training (developers, admins, finance — phishing simulation quarterly). **Advanced:** Measure training effectiveness; culture assessment.

### Control 15 — Service Provider Management
**IG1:** Maintain a service provider inventory with security classification. **IG2:** Establish security requirements in contracts; assess providers annually. **IG3:** Continuous monitoring of provider security posture.

### Control 16 — Application Software Security (IG2+)
Implement secure SDLC; conduct SAST and DAST; manage third-party and open source components; train developers on secure coding; establish a vulnerability disclosure program.

### Control 17 — Incident Response Management
**IG1:** Designate an incident response contact. **IG2:** Establish, maintain, and test an IRP; designate a CSIRT. **IG3:** Annual red team exercises; threat intelligence integration; formal CSIRT with 24/7 capability.

### Control 18 — Penetration Testing (IG2+)
**IG2:** Annual penetration test of infrastructure and web applications. **IG3:** Red team operations; adversary simulation; continuous attack surface monitoring.

---

## Implementation Roadmap by Phase

### Phase 1 — IG1 Baseline (0–6 months)

| Priority | Control | Key Actions |
|:---:|:---|:---|
| 1 | CIS 1 | Deploy network discovery; build hardware inventory |
| 2 | CIS 5 | Inventory all accounts; disable dormant accounts; separate admin accounts |
| 3 | CIS 6 | MFA on all internet-facing systems; formal access provisioning/revocation |
| 4 | CIS 10 | Deploy EDR on all endpoints; centralize management |
| 5 | CIS 11 | Automated backups; isolated/immutable backup copy |
| 6 | CIS 4 | Implement host-based firewalls; auto-lock screens |
| 7 | CIS 2 | Build software inventory; identify end-of-life software |
| 8 | CIS 7 | Automated patching (OS and applications) |
| 9 | CIS 9 | DNS filtering; DMARC/DKIM/SPF; disable dangerous file types |
| 10 | CIS 14 | Annual security awareness training for all staff |

### Phase 2 — IG2 Foundation (6–18 months)

- Full-disk encryption on all endpoints (CIS 3.6)
- Vulnerability scanning weekly on internet-facing assets (CIS 7.6)
- Centralized logging with 90-day retention (CIS 8.9)
- Network segmentation and VLAN implementation (CIS 12)
- IDS/IPS deployment and tuning (CIS 13)
- Role-based security training and phishing simulations (CIS 14)
- Vendor security assessments (CIS 15)
- First penetration test (CIS 18)

### Phase 3 — IG3 Advanced (18+ months)

- SIEM with automated alerting and SOC or MDR (CIS 8, 13)
- Application security program: SAST, DAST, SCA (CIS 16)
- Red team exercises (CIS 18)
- Continuous vendor monitoring (CIS 15)
- Phishing-resistant MFA (FIDO2) for all admin accounts (CIS 6)

---

## CIS Benchmark Resources

CIS publishes free hardening benchmarks for:

| Platform | Benchmark Available |
|:---|:---|
| Windows 10/11 | ✅ |
| Windows Server 2019/2022 | ✅ |
| macOS | ✅ |
| Ubuntu Linux | ✅ |
| Red Hat / CentOS | ✅ |
| AWS Foundations | ✅ |
| Microsoft Azure | ✅ |
| Google Cloud Platform | ✅ |
| Kubernetes | ✅ |
| Docker | ✅ |
| Microsoft 365 | ✅ |

Download free at: [https://www.cisecurity.org/cis-benchmarks](https://www.cisecurity.org/cis-benchmarks)

---

## References

- [CIS Controls v8 Official Publication](https://www.cisecurity.org/controls/v8)
- [CIS Controls Assessment Specification (CCAS)](https://www.cisecurity.org/controls/assessment-specification)
- [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks)
- Cross-framework mapping: `cis-benchmark-checklist.md` | `../cross-framework/master-control-mapping.md`
