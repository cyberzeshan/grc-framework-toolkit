# System Security Plan (SSP) Template

> **Reference:** NIST SP 800-18 Rev 1 | NIST SP 800-53 Rev 5
> **Standard:** Required artifact for RMF Step 3 (Implement) and Step 5 (Authorize)
> **Purpose:** Document the security controls implemented for a specific information system
> **Classification:** Handle as Controlled Unclassified Information (CUI) — contains sensitive security details

---

## Document Control

| Field | Value |
|:---|:---|
| **System Name** | |
| **System Abbreviation** | |
| **SSP Version** | 1.0 |
| **Status** | Draft / In Review / Approved |
| **ISSO** | |
| **System Owner** | |
| **Authorizing Official** | |
| **Date Prepared** | |
| **Last Updated** | |
| **ATO Expiration Date** | |

---

# SECTION 1 — SYSTEM IDENTIFICATION

## 1.1 System Name and Identifier

| Field | Value |
|:---|:---|
| **System Name** | [Full official name] |
| **System Acronym** | |
| **System Identifier (UID)** | [Assigned by ISSO tracker or asset management] |
| **System Type** | Major Application / General Support System / Minor Application |
| **Operational Status** | Under Development / Operational / Undergoing Major Modification |
| **System Environment** | On-Premises / Cloud (IaaS/PaaS/SaaS) / Hybrid |
| **Cloud Service Provider (if applicable)** | [AWS / Azure / GCP / Other] |
| **FedRAMP Authorized CSP?** | Yes / No — [FedRAMP Package ID if yes] |

## 1.2 System Owner

| Field | Value |
|:---|:---|
| **Name** | |
| **Title** | |
| **Organization** | |
| **Email** | |
| **Phone** | |
| **Address** | |

## 1.3 Authorizing Official

| Field | Value |
|:---|:---|
| **Name** | |
| **Title** | |
| **Organization** | |
| **Email** | |
| **Phone** | |

## 1.4 Information System Security Officer (ISSO)

| Field | Value |
|:---|:---|
| **Name** | |
| **Title** | |
| **Organization** | |
| **Email** | |
| **Phone** | |

## 1.5 Other Key Roles

| Role | Name | Organization | Contact |
|:---|:---|:---|:---|
| Information System Security Manager (ISSM) | | | |
| Senior Agency IS Officer (SAISO) | | | |
| Privacy Officer / SAOP | | | |
| Database Administrator | | | |
| Network Administrator | | | |
| System Developer / Tech Lead | | | |

---

# SECTION 2 — SYSTEM CATEGORIZATION

## 2.1 Security Categorization (FIPS 199)

**Information Types Processed, Stored, or Transmitted:**

| Information Type | SP 800-60 ID | Confidentiality | Integrity | Availability |
|:---|:---:|:---:|:---:|:---:|
| [e.g., Personally Identifiable Information] | C.3.1.1 | Moderate | Moderate | Low |
| [e.g., Financial / Payment Information] | C.3.5.2 | High | Moderate | Low |
| [Add rows as needed] | | | | |

**System Security Categorization (High Water Mark):**

| Security Objective | Impact Level |
|:---|:---:|
| **Confidentiality** | Low / Moderate / High |
| **Integrity** | Low / Moderate / High |
| **Availability** | Low / Moderate / High |
| **Overall System Categorization** | **Low / Moderate / High** |

**Categorization Rationale:**
> [Provide a narrative explanation of why each security objective received the assigned impact level. Reference the information types and potential impacts above.]

**AO Concurrence with Categorization:**
> Authorized By: ___________________ Date: ___________

---

# SECTION 3 — SYSTEM OVERVIEW

## 3.1 System Description

> [Provide a detailed narrative description of the system. Include: purpose and function of the system; what mission it supports; who uses it; what data it processes; how it processes information; key technologies and platforms; and any notable architectural characteristics.]

[ENTER SYSTEM DESCRIPTION — minimum 2–3 paragraphs]

## 3.2 System Functions

| Function | Description | Criticality |
|:---|:---|:---:|
| [Primary function 1] | | High / Medium / Low |
| [Primary function 2] | | |
| [Supporting function] | | |

## 3.3 System Users

| User Type | Access Level | Authentication Method | Approximate Count |
|:---|:---|:---|:---:|
| Privileged Administrators | Full system access | MFA + PAM | |
| Application Administrators | Application-level admin | MFA | |
| Standard Users | Read/write per role | MFA | |
| Read-Only Users | Read access only | Username + Password | |
| External Users / Partners | Limited, role-based | MFA / Federation | |
| API / Service Accounts | Programmatic access | API keys / certificates | |

---

# SECTION 4 — SYSTEM ENVIRONMENT AND ARCHITECTURE

## 4.1 Authorization Boundary

> [Describe the authorization boundary — what is included in this ATO and what is explicitly excluded. Reference the boundary diagram below.]

**In-Scope Components:**
- [List system components within the boundary]

**Out-of-Scope / Inherited:**
- [List what is inherited from common control providers or FedRAMP CSPs]

**Authorization Boundary Diagram:**
> [INSERT DIAGRAM — attach as Appendix A or embed here]
> Diagram should show: all system components, data flows, external connections, boundary demarcation, and cloud services.

## 4.2 Network Architecture

> [Describe the network architecture. Include: network segments, VLANs, DMZ, VPN, firewall placement, load balancers, and any interconnections with other systems.]

**Network Diagram:**
> [INSERT NETWORK DIAGRAM — attach as Appendix B]

## 4.3 System Components

| Component | Type | Function | Location | IP / Hostname | OS / Software Version |
|:---|:---|:---|:---|:---|:---|
| Web Server | Server | Application delivery | AWS us-east-1 | | |
| Application Server | Server | Business logic | AWS us-east-1 | | |
| Database Server | Server | Data storage | AWS us-east-1 | | |
| Load Balancer | Network | Traffic distribution | AWS | | |
| [Add rows] | | | | | |

## 4.4 Data Flows

| Data Type | Source | Destination | Protocol / Port | Encrypted? | Classification |
|:---|:---|:---|:---|:---:|:---|
| User Authentication | Client | App Server | HTTPS/443 | ✅ TLS 1.3 | Internal |
| PII Data | App Server | Database | PostgreSQL/5432 | ✅ TLS | Confidential |
| Audit Logs | All components | SIEM | Syslog/514 | ✅ TLS | Internal |
| [Add rows] | | | | | |

## 4.5 Interconnections with Other Systems

| Connected System | Organization | Data Exchanged | Direction | MOU/ISA Status | Security Contact |
|:---|:---|:---|:---|:---|:---|
| [System Name] | [Org] | [Data type] | Inbound / Outbound / Bi-directional | In place / Needed | |
| [Add rows] | | | | | |

## 4.6 Ports, Protocols, and Services

| Port | Protocol | Service | Direction | Justification |
|:---:|:---|:---|:---|:---|
| 443 | HTTPS/TLS 1.3 | Web application | Inbound | Required for user access |
| 22 | SSH | Admin access | Inbound (restricted) | Admin access via VPN only |
| 5432 | PostgreSQL/TLS | Database | Internal | App-to-DB communication |
| 514 | Syslog/TLS | Log shipping | Outbound | SIEM integration |
| [Add rows] | | | | |

---

# SECTION 5 — APPLICABLE LAWS, REGULATIONS, AND STANDARDS

| Requirement | Citation | Applicability |
|:---|:---|:---|
| Federal Information Security Modernization Act (FISMA) | 44 U.S.C. § 3551 et seq. | Mandatory for federal systems |
| OMB Circular A-130 | OMB A-130 (2016) | Federal information management |
| NIST SP 800-53 Rev 5 | NIST SP 800-53r5 | Security controls baseline |
| FIPS 199 | FIPS 199 | Security categorization |
| FIPS 200 | FIPS 200 | Minimum security requirements |
| Privacy Act of 1974 | 5 U.S.C. § 552a | If PII is processed |
| E-Government Act of 2002 | Pub. L. 107-347 | If publicly accessible |
| [Agency-specific policy] | | |
| [Contractual requirements] | | |

---

# SECTION 6 — CONTROL IMPLEMENTATION DESCRIPTIONS

> **Instructions:** Document each control selected in the control baseline (from Step 2: Select). For each control, describe how it is specifically implemented for this system.

> **Format for each control:**
> - **Control Statement:** [Full NIST SP 800-53 Rev 5 text]
> - **Implementation:** [Specific description of how this system implements the control]
> - **Control Origin:** System-specific / Hybrid / Inherited (from: ________)
> - **Responsible Role:** [Who owns this control implementation]

---

## AC — Access Control Family

### AC-1 — Policy and Procedures
**Control:** The organization develops, documents, and disseminates access control policy and procedures.

**Implementation:**
> [Describe: What access control policy exists? Where is it documented? How is it communicated to relevant personnel? How often is it reviewed?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

### AC-2 — Account Management
**Control:** The organization manages information system accounts, including: identifying account types; establishing conditions for group membership; identifying authorized users; requiring appropriate approvals; managing, creating, enabling, modifying, disabling, and removing accounts; monitoring use of information system accounts; notifying account managers; authorizing access based on valid access authorization; and establishing an account review process.

**Implementation:**
> [Describe: What system is used for account management (AD, LDAP, IAM)? What is the provisioning process? Who approves access? How are accounts reviewed? What are the timelines for disabling accounts after termination? How are service accounts managed?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

### AC-3 — Access Enforcement
**Control:** The system enforces approved authorizations for logical access to information and system resources.

**Implementation:**
> [Describe: What access control model is used (RBAC, ABAC, DAC)? How are access rights technically enforced? What roles exist? How is least privilege implemented?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

### AC-17 — Remote Access
**Control:** The organization establishes and documents usage restrictions, configuration, and connection requirements for remote access.

**Implementation:**
> [Describe: Is remote access permitted? What technology is used (VPN, Zero Trust, Jump host)? What authentication is required for remote access? Are remote sessions encrypted and monitored?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

## AU — Audit and Accountability Family

### AU-2 — Event Logging
**Control:** The organization determines events to be logged, coordinates the event logging function, and provides rationale for events determined not to be logged.

**Implementation:**
> [Describe: What events are logged (authentication, authorization, data access, admin actions, errors)? What logging tool is used? Where are logs stored? What log format is used?]

**Logged Events:**
| Event Type | Logged? | Log Source | Retention |
|:---|:---:|:---|:---|
| Successful login | ✅ | App server, AD | 1 year |
| Failed login | ✅ | App server, AD | 1 year |
| Privilege escalation | ✅ | AD, PAM | 3 years |
| Data access (confidential) | ✅ | Database audit | 3 years |
| Admin actions | ✅ | All systems | 3 years |
| System errors | ✅ | Application logs | 90 days |

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

### AU-9 — Protection of Audit Information
**Control:** The system protects audit information and audit tools from unauthorized access, modification, and deletion.

**Implementation:**
> [Describe: How are logs protected from tampering? Who has access to logs? Are logs shipped to an immutable log store or SIEM? Are log integrity controls in place?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

## IA — Identification and Authentication Family

### IA-2 — Identification and Authentication (Organizational Users)
**Control:** The system uniquely identifies and authenticates organizational users and implements multifactor authentication.

**Implementation:**
> [Describe: What authentication system is used? Is MFA enforced for all users? What MFA methods are supported? What is the authentication flow for privileged vs. standard users?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

### IA-5 — Authenticator Management
**Control:** The organization manages system authenticators, including: verifying identity before distribution; establishing administrative procedures for compromised authenticators; changing default authenticators; and refreshing authenticators at defined intervals.

**Implementation:**
> [Describe: What is the password policy (length, complexity, expiration)? How are credentials distributed? How are compromised credentials handled? How are service account credentials rotated?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

## SC — System and Communications Protection Family

### SC-8 — Transmission Confidentiality and Integrity
**Control:** The system implements cryptographic mechanisms to prevent unauthorized disclosure of information during transmission.

**Implementation:**
> [Describe: What encryption protocols are used (TLS version)? Which interfaces/connections are encrypted? Are there any unencrypted data flows? How are certificates managed?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

### SC-28 — Protection of Information at Rest
**Control:** The system implements cryptographic mechanisms to prevent unauthorized disclosure and modification of information at rest.

**Implementation:**
> [Describe: What encryption is applied to data at rest (database, file storage, backups)? What encryption algorithm and key size are used? How are encryption keys managed?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

## SI — System and Information Integrity Family

### SI-2 — Flaw Remediation
**Control:** The organization identifies, reports, and corrects information system flaws; tests software updates before installation; incorporates flaw remediation into configuration management.

**Implementation:**
> [Describe: What vulnerability scanning tools are used? What is the patch SLA by severity (Critical/High/Medium/Low)? How are patches tested before deployment? Who is responsible for patching?]

**Patch SLA:**
| Severity | Remediation SLA |
|:---:|:---|
| Critical (CVSS 9.0+) | 15 days |
| High (CVSS 7.0–8.9) | 30 days |
| Medium (CVSS 4.0–6.9) | 90 days |
| Low (CVSS <4.0) | 180 days |

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

### SI-3 — Malicious Code Protection
**Control:** The system implements malicious code protection mechanisms at system entry and exit points.

**Implementation:**
> [Describe: What anti-malware or EDR tool is deployed? What is the update frequency for signatures/models? Are email and web gateway protections in place? How are alerts handled?]

**Control Origin:** ☐ System-specific &nbsp; ☐ Hybrid &nbsp; ☐ Inherited from: _____________
**Responsible Role:**

---

> **[Continue with all remaining selected controls following the same format]**
> Reference NIST SP 800-53 Rev 5 for full control text. All controls in the approved baseline must be documented.

---

# SECTION 7 — INHERITED CONTROLS

> List all controls inherited from common control providers (e.g., agency infrastructure, FedRAMP CSP).

| Control | Control Name | Inherited From | Authorization Status |
|:---|:---|:---|:---|
| PE-1 through PE-20 | Physical and Environmental Protection | [Facility / Data Center Owner] | Authorized |
| CP-7 | Alternate Processing Site | [Agency BCP] | Authorized |
| IR-1 | Incident Response Policy | [Agency CISO] | Authorized |
| [Add all inherited controls] | | | |

---

# SECTION 8 — PLAN OF ACTION AND MILESTONES (POA&M) SUMMARY

> The full POA&M is maintained as a separate document. This section summarizes open items.

| POA&M ID | Control | Finding | Risk Rating | Scheduled Completion | Status |
|:---:|:---|:---|:---:|:---|:---|
| POA-001 | AC-2 | Access reviews not conducted quarterly | Moderate | [Date] | In Progress |
| POA-002 | AU-6 | SIEM alerting not configured for all event types | High | [Date] | In Progress |
| [Add rows] | | | | | |

---

# SECTION 9 — PRIVACY

## 9.1 Privacy Act System of Records

- Does the system maintain a System of Records under the Privacy Act? **Yes / No**
- System of Records Notice (SORN) Number (if applicable): _______________
- Privacy Impact Assessment (PIA) completed? **Yes / No** — Date: ___________

## 9.2 PII Inventory

| PII Element | Purpose | Minimization Applied? |
|:---|:---|:---:|
| Full Name | User identification | ✅ |
| Email Address | Authentication, notification | ✅ |
| SSN / National ID | [If applicable — justify] | |
| [Add rows] | | |

---

# SECTION 10 — SYSTEM INTERCONNECTION AGREEMENTS

> List all Memoranda of Understanding (MOUs) and Interconnection Security Agreements (ISAs).

| Agreement | Connected System | Agreement Type | Date Signed | Expiration | Review Due |
|:---|:---|:---|:---|:---|:---|
| | | MOU / ISA | | | |

---

# APPENDIX A — Authorization Boundary Diagram

> [Attach or embed diagram]

---

# APPENDIX B — Network Architecture Diagram

> [Attach or embed diagram]

---

# APPENDIX C — Acronyms

| Acronym | Definition |
|:---|:---|
| AO | Authorizing Official |
| ATO | Authorization to Operate |
| CUI | Controlled Unclassified Information |
| FIPS | Federal Information Processing Standard |
| FISMA | Federal Information Security Modernization Act |
| ISSO | Information System Security Officer |
| MFA | Multi-Factor Authentication |
| NIST | National Institute of Standards and Technology |
| PAM | Privileged Access Management |
| PII | Personally Identifiable Information |
| POA&M | Plan of Action and Milestones |
| RBAC | Role-Based Access Control |
| RMF | Risk Management Framework |
| SAR | Security Assessment Report |
| SIEM | Security Information and Event Management |
| SSP | System Security Plan |

---

# APPENDIX D — Revision History

| Version | Date | Author | Changes |
|:---:|:---|:---|:---|
| 1.0 | | | Initial draft |
| | | | |

---

*Template Reference: NIST SP 800-18 Rev 1 | NIST SP 800-53 Rev 5 | SP 800-37 Rev 2*
