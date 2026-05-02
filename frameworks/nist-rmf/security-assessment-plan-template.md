# Security Assessment Plan (SAP) Template

> **Reference:** NIST SP 800-53A Rev 5 | NIST SP 800-37 Rev 2
> **Purpose:** Define the scope, methodology, schedule, and procedures for assessing security controls
> **Required By:** RMF Step 4 (Assess) — must be approved before assessment begins
> **Classification:** Handle as Controlled Unclassified Information (CUI)

---

## Document Control

| Field | Value |
|:---|:---|
| **System Name** | |
| **SAP Version** | 1.0 |
| **Status** | Draft / Approved |
| **Lead Assessor** | |
| **Assessment Organization** | |
| **System Owner** | |
| **ISSO** | |
| **Authorizing Official** | |
| **SAP Approval Date** | |
| **Planned Assessment Start Date** | |
| **Planned Assessment End Date** | |
| **SAR Delivery Date** | |

---

# SECTION 1 — PURPOSE AND SCOPE

## 1.1 Purpose

This Security Assessment Plan (SAP) describes the approach for assessing the security controls implemented in **[System Name]**. The assessment will determine whether controls are implemented correctly, operating as intended, and producing the desired outcome in meeting the security requirements of the system.

This assessment supports the **[initial authorization / reauthorization / annual assessment]** of [System Name] under the NIST Risk Management Framework (RMF).

## 1.2 Assessment Scope

**System Being Assessed:** [System Name]
**System Categorization:** [Low / Moderate / High]
**Control Baseline:** [SP 800-53 Rev 5 Low / Moderate / High Baseline + tailoring]
**Authorization Boundary:** [Brief description — see SSP Section 4.1 for detail]

**Controls in Scope for This Assessment:**

| Assessment Type | Controls Included | Count |
|:---|:---|:---:|
| Full Assessment (initial ATO or triennial) | All selected controls in the baseline | |
| Annual Subset Assessment | High-impact controls + any controls with findings | |
| Targeted Assessment (significant change) | Controls affected by the change | |

**Controls Excluded from This Assessment (with justification):**

| Control | Reason for Exclusion |
|:---|:---|
| [e.g., PE-1 through PE-20] | Physical controls inherited from [data center owner]; separately authorized |
| [e.g., AT-1] | Assessed in previous cycle; no changes; carryover accepted by AO |

## 1.3 Assessment Objectives

1. Determine the extent to which controls in the SSP are implemented correctly
2. Determine the extent to which controls are operating as intended
3. Determine the extent to which controls are producing the desired outcome
4. Identify security weaknesses and deficiencies
5. Provide findings and recommendations to support the authorization decision

---

# SECTION 2 — ASSESSMENT TEAM

## 2.1 Lead Assessor

| Field | Value |
|:---|:---|
| **Name** | |
| **Title** | |
| **Organization** | |
| **Certification(s)** | [e.g., CISSP, CISM, CAP, CEH] |
| **Email** | |
| **Phone** | |

## 2.2 Assessment Team Members

| Name | Role | Expertise | Organization |
|:---|:---|:---|:---|
| | Technical Assessor | Network / Infrastructure | |
| | Technical Assessor | Application Security | |
| | Technical Assessor | Cloud Security | |
| | Documentation Reviewer | SSP / Policy review | |
| | Privacy Assessor | PII / Privacy controls | |

## 2.3 Independence Statement

> [Document assessor independence. The SCA must be independent from the development and operational teams responsible for the system. Describe how independence is established.]

The assessment team is **independent** of the system development and operations teams. Specifically:
- No assessment team member has been involved in the development, implementation, or operation of [System Name]
- No assessment team member reports to the System Owner of [System Name]
- The assessment organization has no financial interest in the outcome of the assessment

**Independence verification:** _________________________________ Date: __________

## 2.4 Organizational Support Contacts

| Role | Name | Responsibility During Assessment |
|:---|:---|:---|
| ISSO | | Primary POC; schedule interviews; provide evidence |
| System Owner | | Approve assessment schedule; review draft SAR |
| Database Administrator | | Support database-related testing |
| Network Administrator | | Support network testing; provide firewall rules |
| Developer / Architect | | Support application testing; code review if needed |
| IT Help Desk Lead | | Support account management testing |

---

# SECTION 3 — ASSESSMENT METHODOLOGY

## 3.1 Assessment Methods

In accordance with NIST SP 800-53A Rev 5, controls will be assessed using three methods:

| Method | Description | Application |
|:---|:---|:---|
| **Examine** | Review, inspect, observe, study, and analyze documentation, configurations, and mechanisms | Policies, procedures, SSP descriptions, configurations, scan results |
| **Interview** | Conduct discussions with individuals or groups | System Owner, ISSO, administrators, end users |
| **Test** | Exercise and observe the operation of mechanisms and controls | Technical controls, automated tools, penetration tests |

## 3.2 Assessment Depth and Coverage

| Depth | Definition | Applied To |
|:---|:---|:---|
| **Basic** | Single examiner, limited scope | Low-impact inherited controls |
| **Focused** | Multiple examiners, defined test cases | Moderate-impact controls |
| **Comprehensive** | Multiple examiners, extensive test cases, automated and manual testing | High-impact controls, controls with prior findings |

## 3.3 Evidence Collection

Evidence collected during the assessment will be documented and retained for a minimum of **3 years** or through the next ATO reauthorization, whichever is longer.

Evidence types:
- **Documents:** Policies, procedures, SSP, configuration guides, training records
- **Configurations:** System configurations, firewall rules, IAM settings, scan outputs
- **Screenshots:** Visual evidence of control implementation
- **Interview notes:** Notes from all interviews, signed by interviewer
- **Test results:** Output from automated tools, manual test results
- **Logs:** Sample log excerpts demonstrating control operation

---

# SECTION 4 — RULES OF ENGAGEMENT

> **Critical:** All parties must sign the rules of engagement before assessment activities begin.

## 4.1 Authorized Activities

The following activities are authorized during this assessment:

| Activity | Authorized? | Restrictions |
|:---|:---:|:---|
| Review of SSP, policies, and procedures | ✅ | None |
| Examination of system configurations | ✅ | Read-only access only |
| Interviews with system personnel | ✅ | Scheduled in advance |
| Automated vulnerability scanning | ✅ | Non-production environment first; production only with SO approval |
| Manual web application testing | ✅ | Non-production environment; no automated exploits |
| Penetration testing / exploitation | ❌ | Not authorized under this SAP — requires separate authorization |
| Review of source code | ✅ | Limited to security-relevant modules; read-only |
| Database query for evidence | ✅ | Read-only; no sensitive data extraction |
| Physical access / walkthrough | ✅ | Escorted; notify facility manager 48 hours in advance |

## 4.2 Out-of-Bounds Activities

The following are explicitly **not authorized** without separate written approval:

- Exploiting any identified vulnerability
- Accessing systems outside the authorization boundary
- Extracting or copying production data
- Modifying any system configuration
- Social engineering of system personnel
- Denial of service testing

## 4.3 Emergency Stop Procedures

If any assessment activity causes or risks causing a system outage or data breach:

1. **Immediately stop** the activity
2. **Notify the ISSO** by phone within 15 minutes
3. **Notify the System Owner** within 30 minutes
4. **Document the incident** in the assessment log
5. **Do not resume** that activity until written re-authorization is received

**Emergency Contact (ISSO):** ______________________________ Phone: ______________
**Emergency Contact (System Owner):** ______________________ Phone: ______________

## 4.4 Signatories

| Role | Name | Signature | Date |
|:---|:---|:---|:---|
| Lead Assessor | | | |
| System Owner | | | |
| ISSO | | | |
| Authorizing Official | | | |

---

# SECTION 5 — ASSESSMENT SCHEDULE

| Phase | Activity | Start Date | End Date | Lead |
|:---|:---|:---|:---|:---|
| **Pre-Assessment** | Evidence request and document collection | | | ISSO |
| **Pre-Assessment** | SSP review and control mapping | | | Lead Assessor |
| **Assessment Week 1** | Policy and procedure examination | | | Assessment Team |
| **Assessment Week 1** | Access control and IA interviews | | | Technical Assessor |
| **Assessment Week 2** | Technical testing (scanning, configuration review) | | | Technical Assessor |
| **Assessment Week 2** | Audit and logging examination | | | Technical Assessor |
| **Assessment Week 3** | Application security testing | | | App Security Assessor |
| **Assessment Week 3** | Continuity and incident response review | | | Assessment Team |
| **Assessment Week 4** | Physical assessment walkthrough | | | Lead Assessor |
| **Post-Assessment** | Evidence review and finding validation | | | Lead Assessor |
| **Post-Assessment** | Draft SAR preparation | | | Lead Assessor |
| **Post-Assessment** | ISSO / System Owner SAR review | | | System Owner, ISSO |
| **Post-Assessment** | Final SAR delivery | | | Lead Assessor |

---

# SECTION 6 — ASSESSMENT PROCEDURES

> The following procedures apply to each control. Use the SP 800-53A Rev 5 assessment procedures as the basis, tailored to the system environment.

## Control Assessment Tracking Table

| Control ID | Control Name | Method(s) | Depth | Assessor | Scheduled Date | Evidence Request | Status |
|:---|:---|:---|:---|:---|:---|:---|:---|
| AC-1 | Policy and Procedures | E, I | Basic | | | Access control policy; review log | Pending |
| AC-2 | Account Management | E, I, T | Focused | | | AD user report; provisioning workflow; review records | Pending |
| AC-3 | Access Enforcement | E, T | Focused | | | RBAC config; access matrix | Pending |
| AC-6 | Least Privilege | E, I, T | Focused | | | Admin account list; privilege justification | Pending |
| AC-7 | Unsuccessful Login Attempts | T | Focused | | | Account lockout test | Pending |
| AC-11 | Session Lock | T | Basic | | | Session timeout test | Pending |
| AC-17 | Remote Access | E, I, T | Focused | | | VPN config; remote access policy | Pending |
| AU-2 | Event Logging | E, T | Focused | | | Log configuration; sample logs | Pending |
| AU-3 | Content of Audit Records | E | Basic | | | Sample log records | Pending |
| AU-6 | Audit Record Review | E, I | Focused | | | Alert configuration; review records | Pending |
| AU-9 | Protection of Audit Info | E, T | Focused | | | Log storage permissions; SIEM access controls | Pending |
| AU-11 | Audit Record Retention | E | Basic | | | Retention policy; log storage configuration | Pending |
| CA-2 | Control Assessments | E | Basic | | | Prior SAR; assessment schedule | Pending |
| CA-5 | POA&M | E | Focused | | | Current POA&M; closure evidence | Pending |
| CA-7 | Continuous Monitoring | E, I | Focused | | | Monitoring plan; scan reports | Pending |
| CM-2 | Baseline Configuration | E, T | Focused | | | Configuration baseline; compliance scan | Pending |
| CM-6 | Configuration Settings | E, T | Focused | | | Hardening guide; drift detection reports | Pending |
| CM-7 | Least Functionality | E, T | Focused | | | Enabled services list; port scan results | Pending |
| CM-8 | System Component Inventory | E | Focused | | | CMDB export; network discovery output | Pending |
| IA-2 | Identification and Authentication | E, T | Focused | | | MFA configuration; authentication test | Pending |
| IA-5 | Authenticator Management | E, I | Focused | | | Password policy; PAM configuration | Pending |
| IA-8 | Identification/Auth (Non-Org Users) | E, T | Basic | | | External user auth config | Pending |
| IR-4 | Incident Handling | E, I | Focused | | | IRP; tabletop exercise records | Pending |
| IR-6 | Incident Reporting | E, I | Basic | | | Reporting procedure; notification SLAs | Pending |
| MA-2 | Controlled Maintenance | E | Basic | | | Maintenance records; access logs | Pending |
| MP-6 | Media Sanitization | E | Basic | | | Media disposal records; ITAD certificates | Pending |
| PE-2 | Physical Access Authorizations | E, I | Basic | | | Badge access list; visitor log | Pending |
| PE-6 | Physical Access Monitoring | E, T | Basic | | | CCTV coverage; badge access logs | Pending |
| PL-2 | SSP | E | Focused | | | SSP; review records | Pending |
| PS-3 | Personnel Screening | E | Basic | | | Background check policy; HR records sample | Pending |
| PS-4 | Personnel Termination | E, T | Focused | | | Offboarding procedure; account deactivation test | Pending |
| RA-3 | Risk Assessment | E | Focused | | | Risk register; risk assessment report | Pending |
| RA-5 | Vulnerability Monitoring | E, T | Focused | | | Scan reports; remediation tracking | Pending |
| SA-8 | Security Engineering Principles | E | Basic | | | Architecture documentation; SDLC security gates | Pending |
| SA-11 | Developer Testing | E | Basic | | | SAST/DAST results; security test reports | Pending |
| SC-5 | Denial of Service Protection | E | Basic | | | DDoS protection configuration | Pending |
| SC-7 | Boundary Protection | E, T | Focused | | | Firewall ruleset; network diagram | Pending |
| SC-8 | Transmission Confidentiality | E, T | Focused | | | TLS configuration; certificate details | Pending |
| SC-12 | Cryptographic Key Management | E, I | Focused | | | Key management procedure; KMS configuration | Pending |
| SC-28 | Protection of Information at Rest | E, T | Focused | | | Encryption configuration; key management | Pending |
| SI-2 | Flaw Remediation | E, T | Focused | | | Patch reports; remediation SLAs; open vulnerabilities | Pending |
| SI-3 | Malicious Code Protection | E, T | Focused | | | AV/EDR configuration; update frequency | Pending |
| SI-4 | System Monitoring | E, T | Focused | | | SIEM configuration; alert rules | Pending |
| SI-7 | Software, Firmware, Integrity | E, T | Basic | | | Integrity checking tool; baseline comparison | Pending |

---

# SECTION 7 — EVIDENCE REQUEST LIST

> Provide this list to the ISSO at kickoff. Allow 5–10 business days for collection.

## Required Documents

| # | Document | Purpose | Needed By |
|:---:|:---|:---|:---|
| 1 | System Security Plan (SSP) — current version | Baseline for all assessment | Kickoff |
| 2 | Authorization boundary diagram | Scope verification | Kickoff |
| 3 | Network architecture diagram | Architecture assessment | Kickoff |
| 4 | All security policies referenced in SSP | Policy examination | Week 1 |
| 5 | POA&M — current | Open findings review | Week 1 |
| 6 | Prior SAR (if reauthorization) | Finding carryover review | Pre-assessment |
| 7 | Risk assessment / risk register | Risk context | Pre-assessment |
| 8 | Privacy Impact Assessment (PIA) | Privacy controls | Pre-assessment |

## Required Configurations and Reports

| # | Item | System | Purpose |
|:---:|:---|:---|:---|
| 9 | Active Directory user list (full, with last login) | Active Directory | AC-2 |
| 10 | Admin / privileged account list with justifications | AD / PAM | AC-6, IA-2 |
| 11 | MFA enrollment report | IAM system | IA-2 |
| 12 | Password policy configuration export | AD Group Policy | IA-5 |
| 13 | Firewall ruleset export | Firewall | SC-7 |
| 14 | TLS/SSL configuration (SSLLabs or equivalent) | Web services | SC-8 |
| 15 | Encryption configuration for databases and storage | Database/Cloud | SC-28 |
| 16 | Last 3 vulnerability scan reports | Scanner | RA-5, SI-2 |
| 17 | Patch management reports (90-day history) | SCCM / patch tool | SI-2 |
| 18 | EDR/AV deployment coverage report | EDR platform | SI-3 |
| 19 | SIEM alert rules and monitoring configuration | SIEM | SI-4, AU-6 |
| 20 | Log retention configuration | SIEM / log storage | AU-11 |
| 21 | Configuration baseline and compliance scan results | SCAP / scanner | CM-2, CM-6 |
| 22 | Network port scan results | Nmap / scanner | CM-7 |
| 23 | System component inventory | CMDB | CM-8 |
| 24 | Backup configuration and last restore test results | Backup system | CP-9 |
| 25 | Incident response plan | IRP document | IR-4 |
| 26 | Last tabletop exercise report | IRP records | IR-4 |
| 27 | Background check policy and sample (redacted) | HR | PS-3 |
| 28 | Offboarding checklist with completed examples | HR/IT | PS-4 |

---

# SECTION 8 — REPORTING

## 8.1 Finding Classification

| Classification | Definition |
|:---|:---|
| **Satisfied (S)** | Control is implemented correctly and operating as intended |
| **Other than Satisfied (O)** | Control is not implemented, partially implemented, or has deficiencies |

## 8.2 Risk Ratings for Findings

| Rating | CVSS Range | Description | POA&M SLA |
|:---:|:---:|:---|:---|
| **Critical** | 9.0–10.0 | Immediate exploitation risk; severe impact | 30 days |
| **High** | 7.0–8.9 | Likely exploitation; significant impact | 60 days |
| **Moderate** | 4.0–6.9 | Exploitation possible; limited impact | 90 days |
| **Low** | 0.1–3.9 | Unlikely exploitation; minimal impact | 180 days |
| **Informational** | N/A | Observation or recommendation; no direct risk | Next planning cycle |

## 8.3 SAR Delivery

| Deliverable | Format | Recipient | Due Date |
|:---|:---|:---|:---|
| Draft SAR | DOCX / PDF | ISSO, System Owner | [Date] |
| System Owner Review Period | — | System Owner, ISSO | 5 business days |
| Final SAR | DOCX / PDF | AO, ISSO, System Owner | [Date] |
| POA&M with all findings | XLSX | ISSO | With final SAR |

---

# APPENDIX A — Acronyms

| Acronym | Definition |
|:---|:---|
| AO | Authorizing Official |
| ATO | Authorization to Operate |
| CUI | Controlled Unclassified Information |
| ISSO | Information System Security Officer |
| POA&M | Plan of Action and Milestones |
| RMF | Risk Management Framework |
| SAP | Security Assessment Plan |
| SAR | Security Assessment Report |
| SCA | Security Control Assessor |
| SSP | System Security Plan |

---

*Template Reference: NIST SP 800-53A Rev 5 | NIST SP 800-37 Rev 2*
