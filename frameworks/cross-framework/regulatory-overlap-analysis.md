# Regulatory Overlap Analysis — Multi-Framework Efficiency Matrix

> **Purpose:** Identify control implementation overlaps across frameworks to eliminate redundant work and maximize compliance ROI
> **Audience:** GRC program managers, CISOs, compliance leads planning multi-framework programs
> **Frameworks Covered:** NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC | GDPR | HIPAA | PCI-DSS v4 | FedRAMP

---

## Executive Summary

Organizations often pursue multiple certifications or frameworks simultaneously — or discover they are already required to comply with several due to regulatory, contractual, or customer demands. This analysis answers the critical question: **Where can one control implementation satisfy multiple frameworks, and where must you implement distinct controls?**

**Key findings:**
- **~70% of controls overlap** between ISO 27001, SOC 2, and NIST CSF in major domains (IAM, logging, incident response)
- **GDPR adds ~15 net-new control requirements** beyond a baseline ISO 27001 implementation (primarily privacy-specific)
- **HIPAA adds ~20 net-new requirements** for healthcare organizations on top of ISO 27001
- **PCI-DSS adds the most net-new requirements** (~35+) due to its highly prescriptive, cardholder-data-specific controls
- **FedRAMP adds the most documentation burden** — not necessarily more controls, but far more evidence and documentation specificity

---

## Part 1 — Framework-to-Framework Overlap Matrix

> Legend: **H** = High overlap (>70% of requirements covered) | **M** = Moderate overlap (40–70%) | **L** = Low overlap (<40%) | **—** = Same framework

| | NIST CSF 2.0 | ISO 27001:2022 | CIS v8 (IG2) | SOC 2 TSC | GDPR | HIPAA | PCI-DSS v4 | FedRAMP |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **NIST CSF 2.0** | — | H | H | H | M | M | M | H |
| **ISO 27001:2022** | H | — | H | H | M | M | M | H |
| **CIS v8 (IG2)** | H | H | — | H | L | L | M | M |
| **SOC 2 TSC** | H | H | H | — | M | M | M | H |
| **GDPR** | M | M | L | M | — | M | M | L |
| **HIPAA** | M | M | L | M | M | — | M | L |
| **PCI-DSS v4** | M | M | M | M | M | M | — | M |
| **FedRAMP** | H | H | M | H | L | L | M | — |

---

## Part 2 — Control Domain Efficiency Analysis

For each major control domain, this table shows which frameworks require it and how much overlap exists between their requirements.

### Domain: Access Control and Identity Management

| Requirement | CSF 2.0 | ISO 27001 | CIS v8 | SOC 2 | GDPR | HIPAA | PCI-DSS | FedRAMP |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Unique user accounts | ✅ PR.AA-01 | ✅ A.5.16 | ✅ CIS 5.2 | ✅ CC6.1 | ✅ Art.5(f) | ✅ §164.312(a) | ✅ Req 8.2 | ✅ AC-2 |
| MFA for users | ✅ PR.AA-03 | ✅ A.5.17, A.8.5 | ✅ CIS 6.3 | ✅ CC6.1 | ⚠️ Implied | ✅ §164.312(d) | ✅ Req 8.4 | ✅ IA-2 |
| MFA for admins | ✅ PR.AA-03 | ✅ A.5.17 | ✅ CIS 6.5 | ✅ CC6.3 | ⚠️ Implied | ✅ §164.312(d) | ✅ Req 8.4.2 | ✅ IA-2(1) |
| Privileged access management | ✅ PR.AA-05 | ✅ A.8.2 | ✅ CIS 5.4 | ✅ CC6.3 | — | ✅ §164.312(a) | ✅ Req 7.2 | ✅ AC-6 |
| Access reviews / recertification | ✅ PR.AA-05 | ✅ A.5.18 | ✅ CIS 6.1 | ✅ CC6.2 | — | ✅ §164.312(a) | ✅ Req 7.3 | ✅ AC-2 |
| Least privilege | ✅ PR.AA-05 | ✅ A.5.15 | ✅ CIS 6.1 | ✅ CC6.3 | ✅ Art.5 | ✅ §164.312(a) | ✅ Req 7.2 | ✅ AC-6 |
| Session management / timeout | ✅ PR.PS-01 | ✅ A.8.9 | ✅ CIS 4.3 | ✅ CC6.1 | — | ✅ §164.312(a)(2)(iii) | ✅ Req 8.6 | ✅ AC-11 |

**Overlap efficiency:** A single IAM implementation satisfies **all 8 frameworks** for most requirements. Key differentiation: PCI-DSS requires **vendor-supplied default credential** changes (Req 2.2.2) and specific **session timeout values** (Req 8.6.3) not mandated by other frameworks.

---

### Domain: Encryption

| Requirement | CSF 2.0 | ISO 27001 | CIS v8 | SOC 2 | GDPR | HIPAA | PCI-DSS | FedRAMP |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Encryption in transit (TLS) | ✅ PR.DS-02 | ✅ A.8.24 | ✅ CIS 3.10 | ✅ CC6.7 | ✅ Art.32 | ✅ §164.312(e) | ✅ Req 4.2.1 | ✅ SC-8 |
| Encryption at rest | ✅ PR.DS-01 | ✅ A.8.24 | ✅ CIS 3.11 | ✅ CC6.7 | ✅ Art.32 | ✅ §164.312(a) | ✅ Req 3.5 | ✅ SC-28 |
| Full-disk encryption | ✅ PR.DS-01 | ✅ A.8.24 | ✅ CIS 3.6 | ✅ CC6.7 | ✅ Art.32 | ✅ §164.312(a) | ✅ Req 3.5.1 | ✅ SC-28 |
| Key management | ✅ PR.DS-01 | ✅ A.8.24 | — | ✅ CC6.7 | — | ✅ §164.312(a) | ✅ Req 3.7 | ✅ SC-12 |
| Approved algorithms only | — | ✅ A.8.24 | — | — | — | — | ✅ Req 4.2.1 | ✅ SC-13 |
| Certificate management | ✅ PR.PS-01 | ✅ A.8.24 | — | ✅ CC6.7 | — | — | ✅ Req 4.2.1 | ✅ SC-12 |

**Overlap efficiency:** Encryption controls are among the highest-overlap areas. **PCI-DSS** adds the most specificity: prohibits specific weak algorithms (SSL, early TLS), requires network-level segmentation for cardholder data environments, and mandates specific key length requirements. **FIPS 140-2 validated modules** are required for FedRAMP — a significant technical distinction.

---

### Domain: Logging and Monitoring

| Requirement | CSF 2.0 | ISO 27001 | CIS v8 | SOC 2 | GDPR | HIPAA | PCI-DSS | FedRAMP |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Enable logging on all systems | ✅ PR.PS-04 | ✅ A.8.15 | ✅ CIS 8.2 | ✅ CC7.2 | ✅ Art.30 | ✅ §164.312(b) | ✅ Req 10.2 | ✅ AU-2 |
| Centralize logs / SIEM | ✅ DE.CM-01 | ✅ A.8.16 | ✅ CIS 8.9 | ✅ CC7.2 | — | ✅ §164.312(b) | ✅ Req 10.5 | ✅ AU-9 |
| Log retention — 90 days hot | ✅ DE.CM-01 | ✅ A.8.15 | ✅ CIS 8.3 | ✅ CC7.2 | ✅ Art.30 | ✅ §164.312(b) | ✅ Req 10.7 (12 months) | ✅ AU-11 |
| Log retention — 1 year total | — | ✅ A.8.15 | ✅ CIS 8.10 | — | ✅ Art.30 | ✅ §164.312(b) | ✅ Req 10.7.1 | ✅ AU-11 |
| Log integrity protection | ✅ PR.PS-04 | ✅ A.8.15 | ✅ CIS 8.10 | ✅ CC7.2 | — | — | ✅ Req 10.3.3 | ✅ AU-9 |
| Privileged activity logging | ✅ DE.CM-03 | ✅ A.8.15 | ✅ CIS 8.5 | ✅ CC7.2 | — | ✅ §164.312(b) | ✅ Req 10.2.1.5 | ✅ AU-2 |
| Failed access attempt logging | ✅ DE.CM-01 | ✅ A.8.15 | ✅ CIS 8.5 | ✅ CC7.2 | — | ✅ §164.312(b) | ✅ Req 10.2.1.4 | ✅ AU-2 |
| Automated alerting | ✅ DE.AE-06 | ✅ A.8.16 | ✅ CIS 8.11 | ✅ CC7.2 | — | — | ✅ Req 10.6 | ✅ SI-4 |
| Security monitoring review | ✅ DE.AE-02 | ✅ A.8.16 | ✅ CIS 8.11 | ✅ CC7.2 | — | ✅ §164.308(a)(1) | ✅ Req 10.6 | ✅ SI-4 |

**Key differentiators:** PCI-DSS requires **12 months** log retention (most other frameworks specify 90 days + archival) and specifies exactly **which events must be logged** in Req 10.2.1. FedRAMP requires logs to be protected with AU-9 and accessible by the agency ISSO.

---

### Domain: Incident Response

| Requirement | CSF 2.0 | ISO 27001 | CIS v8 | SOC 2 | GDPR | HIPAA | PCI-DSS | FedRAMP |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Documented IRP | ✅ RS.MA-01 | ✅ A.5.24 | ✅ CIS 17.1 | ✅ CC7.3 | ✅ Art.33 | ✅ §164.308(a)(6) | ✅ Req 12.10 | ✅ IR-8 |
| IRP testing (tabletop) | ✅ RS.MA-04 | ✅ A.5.24 | ✅ CIS 17.3 | ✅ CC7.3 | — | ✅ §164.308(a)(6) | ✅ Req 12.10.2 | ✅ IR-3 |
| Incident classification | ✅ RS.MA-03 | ✅ A.5.25 | ✅ CIS 17.2 | ✅ CC7.3 | — | — | ✅ Req 12.10.3 | ✅ IR-4 |
| Regulatory breach notification | ✅ RS.CO-02 | ✅ A.5.26 | — | ✅ CC7.4 | ✅ **72 hours** (Art.33) | ✅ **60 days** (§164.404) | ✅ Per card brands | ✅ US-CERT 1 hr |
| Customer notification | ✅ RS.CO-02 | ✅ A.5.26 | — | ✅ CC9.2 | ✅ **Without delay** (Art.34) | ✅ **60 days** | ✅ Per card brands | — |
| Forensics / evidence handling | ✅ RS.AN-06 | ✅ A.5.28 | ✅ CIS 17.8 | ✅ CC7.4 | — | ✅ §164.308(a)(1) | ✅ Req 12.10.5 | ✅ IR-4 |
| Post-incident review | ✅ ID.IM-04 | ✅ A.5.27 | ✅ CIS 17.7 | ✅ CC7.5 | — | — | ✅ Req 12.10.6 | ✅ IR-4 |

**Key differentiators:** **Breach notification timelines vary significantly** — this is the most important framework differentiation in incident response:
- GDPR: 72 hours to supervisory authority; notification to data subjects "without undue delay"
- HIPAA: 60 days (Breach Notification Rule); HHS and media notification required for breaches >500 individuals
- PCI-DSS: Immediately to payment card brands; timelines per brand rules
- FedRAMP: 1 hour for Critical/High; 24 hours for Moderate; CISA and agency notification

---

### Domain: Vulnerability Management

| Requirement | CSF 2.0 | ISO 27001 | CIS v8 | SOC 2 | GDPR | HIPAA | PCI-DSS | FedRAMP |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Regular vulnerability scanning | ✅ ID.RA-01 | ✅ A.8.8 | ✅ CIS 7.5 | ✅ CC7.1 | — | ✅ §164.308(a)(1) | ✅ Req 11.3 | ✅ RA-5 |
| External scanning | ✅ ID.RA-01 | ✅ A.8.8 | ✅ CIS 7.6 | ✅ CC7.1 | — | — | ✅ Req 11.3.2 (quarterly) | ✅ RA-5 |
| Penetration testing | — | ✅ A.5.35 | ✅ CIS 18 | ✅ CC7.1 | — | — | ✅ Req 11.4 (annual) | ✅ CA-8 |
| Patch SLA — Critical | ✅ ID.RA-06 | ✅ A.8.8 | ✅ CIS 7.3 | — | — | — | ✅ **30 days** (Req 6.3.3) | ✅ **15 days** |
| Patch SLA — High | ✅ ID.RA-06 | ✅ A.8.8 | ✅ CIS 7.3 | — | — | — | ✅ Req 6.3.3 | ✅ **30 days** |
| Authenticated scanning | — | — | ✅ CIS 7.5 | — | — | — | ✅ Req 11.3.1 | ✅ RA-5 |
| Scanning by approved ASV | — | — | — | — | — | — | ✅ Req 11.3.2 (ASV required) | — |

**Key differentiator:** PCI-DSS requires **Approved Scanning Vendor (ASV)** for external scans — internal scanning tools are insufficient for external vulnerability scan requirements. FedRAMP has **tighter patch SLAs** (15 days for Critical) than most other frameworks.

---

## Part 3 — Net-New Requirements by Framework

If you have **ISO 27001** as your baseline, here are the **net-new requirements** each additional framework adds:

### Adding SOC 2 to ISO 27001 Baseline

**Net-new requirements (estimated): ~10–15**

| Area | Net-New SOC 2 Requirement |
|:---|:---|
| Availability | SLA monitoring; uptime commitments; capacity management evidence |
| Change management | Software development SDLC evidence specific to SOC 2 CC8 |
| Vendor management | Subservice organization monitoring with Type II reports (CC9.2) |
| Risk assessment | Must be connected to SOC 2 criteria specifically |
| Monitoring | Annual SOC 2 audit with independent auditor (not just internal) |

**Verdict:** ISO 27001 + SOC 2 is a very efficient combination. ~80–85% overlap. The primary addition is the **independent auditor** and the **Type I/II report** format.

---

### Adding GDPR to ISO 27001 Baseline

**Net-new requirements (estimated): ~15–20**

| Area | Net-New GDPR Requirement |
|:---|:---|
| Data subject rights | Right of access, rectification, erasure, portability — requires specific processes |
| Records of Processing Activities (RoPA) | Mandatory documentation of all processing activities (Art. 30) |
| Data Protection Impact Assessment (DPIA) | Required for high-risk processing; specific format and approval |
| Data Protection by Design | Privacy engineering requirements embedded in product development |
| Data Protection Officer (DPO) | Required for certain organizations; independent role with specific duties |
| Lawful basis for processing | Must identify and document legal basis for each processing activity |
| Cross-border data transfers | Standard Contractual Clauses (SCCs) or adequacy decisions for non-EU transfers |
| Breach notification timeline | 72-hour notification requirement is more specific than ISO 27001 |
| Children's data | Additional protections and parental consent requirements |

**Verdict:** ISO 27001 provides strong technical controls but GDPR adds significant **privacy program requirements** that go beyond information security. A dedicated privacy team or DPO is typically needed.

---

### Adding HIPAA to ISO 27001 Baseline

**Net-new requirements (estimated): ~20–25**

| Area | Net-New HIPAA Requirement |
|:---|:---|
| Business Associate Agreements (BAAs) | Required with all entities handling PHI; specific contract terms |
| Workforce training on HIPAA | Annual HIPAA-specific training (not just general security awareness) |
| Sanctions policy | Must discipline workforce for policy violations |
| Workstation use controls | Specific physical controls for workstations accessing PHI |
| PHI access logs | Detailed access logging for all PHI access |
| Minimum necessary standard | Access to PHI limited to minimum necessary for the role |
| Accounting of disclosures | Individuals can request a list of PHI disclosures |
| Breach assessment (4-factor test) | Specific breach risk assessment methodology required |
| 60-day breach notification | More prescriptive than ISO 27001; includes HHS reporting |
| Unique user identification | PHI access must be logged per individual; no shared IDs |

**Verdict:** HIPAA's **Privacy Rule** adds substantial requirements beyond what ISO 27001 covers. The security controls themselves overlap well, but the administrative and privacy-specific requirements are substantial additions.

---

### Adding PCI-DSS v4 to ISO 27001 Baseline

**Net-new requirements (estimated): ~35–45**

| Area | Net-New PCI-DSS Requirement |
|:---|:---|
| Cardholder data environment (CDE) scoping | Formal CDE scoping exercise; segmentation testing |
| ASV external scanning | Quarterly scans by Approved Scanning Vendor |
| Internal scanning frequency | Quarterly internal vulnerability scans |
| Annual penetration test | Required with specific methodology and scope |
| Annual segmentation test | If relying on segmentation to reduce CDE scope |
| Payment application security | PA-DSS / PCI SSF requirements for payment applications |
| Card data discovery scanning | Regular scanning for CHD outside the defined CDE |
| Specific authentication requirements | Password length, complexity, lockout values precisely defined |
| Requirement for PAN masking | First 6 and last 4 digits maximum for display |
| Cryptographic algorithm specifics | Prohibits SSL, TLS 1.0, early TLS 1.1 explicitly |
| Qualified Security Assessor (QSA) | Required for Level 1 merchants/service providers |
| Report on Compliance (ROC) | Level 1 requirement; specific format |

**Verdict:** PCI-DSS is the **most prescriptive** of all frameworks. Even a fully ISO 27001 certified organization will have significant additional work to achieve PCI-DSS compliance, primarily around CDE scoping, specific technical controls, and the mandatory third-party assessment processes.

---

### Adding FedRAMP to ISO 27001 Baseline

**Net-new requirements (estimated): ~30–40 (primarily documentation)**

| Area | Net-New FedRAMP Requirement |
|:---|:---|
| FIPS 140-2 validated cryptography | All cryptography must use FIPS-validated modules — not just strong algorithms |
| System Security Plan (SSP) format | Specific SSP format per FedRAMP template (often 200+ pages) |
| FIPS 199 categorization | Formal impact level categorization (Low/Moderate/High) |
| 3PAO assessment | Third Party Assessment Organization required (not just any auditor) |
| Continuous monitoring reporting | Monthly POA&M updates; ConMon reports to agency |
| FedRAMP-specific controls | Additional controls and parameters beyond NIST 800-53 |
| Incident notification timelines | 1-hour notification for critical; 24-hour for high |
| US data residency | Data must reside in US-controlled territory |
| Background check specifics | NACI or equivalent for all personnel |
| Penetration testing frequency | Annual red team assessment required at High baseline |
| JAB or Agency Authorization | Formal Authorization to Operate (ATO) from Agency or JAB |

**Verdict:** FedRAMP is primarily a **documentation and evidence burden** on top of NIST 800-53 controls (which map well to ISO 27001). Organizations with mature ISO 27001 programs are well-positioned for FedRAMP but must invest heavily in documentation, the 3PAO engagement, and the ongoing ConMon program.

---

## Part 4 — Multi-Framework Implementation Strategy

### Option A: ISO 27001 as the Foundation (Recommended for Commercial Organizations)

```
ISO 27001 (Core ISMS)
    │
    ├── + SOC 2 Type II (add ~6 months; strong evidence reuse)
    │
    ├── + GDPR (add privacy program; DPO if required)
    │
    ├── + HIPAA (if handling PHI — add BAAs and privacy rule compliance)
    │
    └── + PCI-DSS (if handling payment cards — significant additional effort)
```

**Timeline estimate:** ISO 27001 certification in 12–18 months → SOC 2 Type II in following 6–12 months → GDPR ongoing program → HIPAA/PCI as applicable.

---

### Option B: NIST CSF as the Foundation (Recommended for US-Centric Organizations)

```
NIST CSF 2.0 (Risk Framework)
    │
    ├── + CIS Controls IG2 (technical implementation layer)
    │
    ├── + SOC 2 Type II (customer assurance)
    │
    └── + FedRAMP (if targeting federal market)
```

---

### Option C: FedRAMP First (Recommended for GovTech Companies)

```
FedRAMP Moderate or High
    │
    ├── Inherits: NIST 800-53 controls (maps to CSF and ISO 27001)
    │
    ├── + ISO 27001 (international market expansion — ~30% net-new documentation)
    │
    └── + SOC 2 (commercial customers — ~20% net-new)
```

---

## Part 5 — Evidence Reuse Opportunities

### Single Evidence Set Satisfying Multiple Frameworks

| Evidence Artifact | ISO 27001 | SOC 2 | GDPR | HIPAA | PCI-DSS | FedRAMP |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|
| MFA configuration screenshot | A.5.17 | CC6.1 | Art.32 | §164.312(d) | Req 8.4 | IA-2 |
| Access review report | A.5.18 | CC6.2 | Art.5 | §164.312(a) | Req 7.3 | AC-2 |
| Vulnerability scan report | A.8.8 | CC7.1 | — | §164.308(a)(1) | Req 11.3 | RA-5 |
| SIEM alert configuration | A.8.16 | CC7.2 | — | §164.312(b) | Req 10.6 | SI-4 |
| IRP document | A.5.24 | CC7.3 | Art.33 | §164.308(a)(6) | Req 12.10 | IR-8 |
| Encryption policy + config | A.8.24 | CC6.7 | Art.32 | §164.312(a)(e) | Req 3.5, 4.2 | SC-8, SC-28 |
| Backup test report | A.8.13 | A1.2 | — | §164.308(a)(7) | Req 12.3.4 | CP-9 |
| Security awareness training records | A.6.3 | CC2.2 | — | §164.308(a)(5) | Req 12.6 | AT-2 |
| Penetration test report | A.5.35 | CC7.1 | — | §164.308(a)(1) | Req 11.4 | CA-8 |
| Vendor assessment questionnaire | A.5.22 | CC9.2 | Art.28 | §164.308(b) | Req 12.8 | SA-9 |

---

*Sources: NIST CSF 2.0 | ISO/IEC 27001:2022 | CIS Controls v8 | AICPA SOC 2 TSC 2017 | GDPR (EU 2016/679) | HIPAA Security Rule (45 CFR Part 164) | PCI-DSS v4.0 | FedRAMP Security Controls Baseline*
