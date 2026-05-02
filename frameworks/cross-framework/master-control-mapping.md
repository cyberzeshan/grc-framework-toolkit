# Master Control Mapping — NIST CSF 2.0 ↔ ISO 27001:2022 ↔ CIS Controls v8 ↔ SOC 2 TSC

> **Purpose:** Single-pane cross-reference across the four most commonly implemented cybersecurity frameworks
> **Use Case:** Multi-framework compliance programs — identify which single control implementation satisfies requirements across multiple frameworks simultaneously
> **Last Updated:** See git history | Source standards: NIST CSF 2.0 (Feb 2024), ISO 27001:2022, CIS Controls v8 (May 2021), SOC 2 TSC 2017

---

## How to Use This Mapping

**Scenario 1 — New control selection:** You need to address a risk. Find the control domain below to see which specific controls from each framework apply. Implement once; satisfy many.

**Scenario 2 — Gap analysis:** You've assessed against one framework. Use this table to project your compliance posture against the others.

**Scenario 3 — Evidence reuse:** One body of evidence (e.g., MFA configuration screenshot) may satisfy requirements across all four frameworks. Use this table to identify evidence reuse opportunities.

> **Important:** This is an alignment mapping. Frameworks use different definitions of "implemented." A control satisfying one framework's requirements may not fully satisfy another's without additional documentation or process specificity.

---

## Domain 1 — Asset Management

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Hardware asset inventory | ID.AM-01 | A.5.9 | CIS 1.1, 1.2, 1.3 | CC6.1 |
| Software asset inventory | ID.AM-02 | A.5.9 | CIS 2.1, 2.2, 2.3 | CC6.1 |
| Network / data flow inventory | ID.AM-03 | A.5.9, A.8.20 | CIS 1.5 | CC6.1 |
| Service catalog | ID.AM-04 | A.5.9 | CIS 2.1 | CC6.1 |
| Asset criticality / prioritization | ID.AM-05 | A.5.10, A.5.12 | CIS 1.1, 2.1 | CC6.1 |
| Data classification and inventory | ID.AM-07 | A.5.10, A.5.12, A.5.13 | CIS 3.1, 3.2, 3.7 | CC6.1 |
| Asset lifecycle management | ID.AM-08 | A.5.9, A.8.10 | CIS 1.1, 2.2 | CC6.1 |

---

## Domain 2 — Identity and Access Management

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Identity management lifecycle | PR.AA-01 | A.5.15, A.5.16 | CIS 5.1, 5.5 | CC6.1, CC6.2 |
| Identity proofing and binding | PR.AA-02 | A.5.16, A.5.17 | CIS 5.2 | CC6.1 |
| Multi-factor authentication | PR.AA-03 | A.5.17, A.8.5 | CIS 6.3, 6.4, 6.5 | CC6.1, CC6.3 |
| Privileged access management | PR.AA-05 | A.5.15, A.5.18, A.8.2 | CIS 5.4, 6.5 | CC6.1, CC6.3 |
| Access rights / least privilege | PR.AA-05 | A.5.15, A.5.18, A.8.3 | CIS 6.1, 6.2 | CC6.1, CC6.3 |
| Access provisioning and review | PR.AA-05 | A.5.18 | CIS 6.1, 6.2 | CC6.1, CC6.2 |
| Account deprovisioning | PR.AA-05 | A.5.18, A.6.5 | CIS 5.3, 6.2 | CC6.2 |
| Centralized access control / SSO | PR.AA-03 | A.5.15, A.5.17 | CIS 6.7 | CC6.1 |
| Physical access control | PR.AA-06 | A.7.1, A.7.2, A.7.3 | CIS 10.3 (indirect) | CC6.4 |
| Service account management | PR.AA-01 | A.5.16 | CIS 5.5 | CC6.1 |

---

## Domain 3 — Vulnerability Management

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Vulnerability identification and scanning | ID.RA-01, DE.CM-08 | A.8.8 | CIS 7.5, 7.6 | CC7.1 |
| Patch management — OS | ID.RA-01 | A.8.8 | CIS 7.3 | CC7.1 |
| Patch management — applications | ID.RA-01 | A.8.8 | CIS 7.4 | CC7.1 |
| Vulnerability remediation tracking | ID.RA-06 | A.8.8 | CIS 7.2, 7.7 | CC7.1 |
| Threat intelligence integration | ID.RA-02, ID.RA-04 | A.5.7 | CIS 7.5, 7.6 | CC7.1 |
| Vulnerability disclosure process | ID.RA-08 | A.8.8 | CIS 16.8 (indirect) | CC7.1 |

---

## Domain 4 — Data Protection

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Encryption at rest | PR.DS-01 | A.8.24 | CIS 3.11 | CC6.1, CC6.7 |
| Encryption in transit | PR.DS-02 | A.8.24 | CIS 3.10 | CC6.1, CC6.7 |
| Encryption on endpoints (full-disk) | PR.DS-01 | A.8.24 | CIS 3.6 | CC6.7 |
| Data loss prevention (DLP) | PR.DS-01, PR.DS-02 | A.8.12, A.5.14 | CIS 3.13 | CC6.7 |
| Data masking / de-identification | PR.DS-10 | A.8.11 | CIS 3.12 | CC6.7 |
| Backup and recovery | PR.DS-11 | A.8.13 | CIS 11.1, 11.2, 11.3, 11.4 | A1.2 |
| Secure media disposal | ID.AM-08 | A.7.14 | CIS 3.5 | CC6.5 |
| Data retention and deletion | ID.AM-07 | A.5.33, A.8.10 | CIS 3.4 | CC6.5 |
| Data flow documentation | ID.AM-03, ID.AM-07 | A.5.14 | CIS 3.8 | CC6.1 |

---

## Domain 5 — Security Configuration Management

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Configuration baseline and hardening | PR.PS-01 | A.8.9 | CIS 4.1, 4.2 | CC6.1, CC7.1 |
| Network device configuration | PR.PS-01 | A.8.9, A.8.20 | CIS 4.2, 12.1 | CC6.1 |
| Default account/credential management | PR.PS-01 | A.8.9 | CIS 4.7 | CC6.1 |
| Unnecessary services disabled | PR.PS-01 | A.8.19 | CIS 4.8 | CC6.1 |
| Session lock / auto-lock | PR.PS-01 | A.8.9 | CIS 4.3 | CC6.1 |
| Change management | PR.PS-02 | A.8.32 | CIS 4.1, 4.2 | CC8.1 |
| Secure SDLC | PR.PS-06 | A.8.25, A.8.26, A.8.27 | CIS 16.1, 16.2 | CC8.1 |
| Secure coding standards | PR.PS-06 | A.8.28 | CIS 16.7 | CC8.1 |
| Application security testing | PR.PS-06 | A.8.29 | CIS 16.5, 16.6 | CC8.1 |

---

## Domain 6 — Logging, Monitoring, and Detection

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Log collection and centralization | PR.PS-04, DE.CM-01 | A.8.15 | CIS 8.1, 8.2, 8.9 | CC7.2 |
| Log retention | PR.PS-04 | A.8.15 | CIS 8.3, 8.10 | CC7.2 |
| Log integrity and protection | PR.PS-04 | A.8.15 | CIS 8.10 | CC7.2 |
| Security event monitoring / SIEM | DE.CM-01 | A.8.15, A.8.16 | CIS 8.11, 13.1 | CC7.2 |
| Network traffic monitoring | DE.CM-01, DE.CM-03 | A.8.16 | CIS 13.2, 13.3 | CC7.2 |
| Endpoint monitoring (EDR) | DE.CM-09 | A.8.7, A.8.16 | CIS 10.7, 13.4 | CC7.2 |
| Anomaly detection | DE.AE-02, DE.AE-03 | A.8.16 | CIS 13.6 | CC7.2 |
| Security alerting and tuning | DE.AE-06 | A.8.16 | CIS 8.11, 13.1 | CC7.2 |
| DNS query logging | DE.CM-01 | A.8.15 | CIS 8.6 | CC7.2 |
| Command-line audit logging | DE.CM-03 | A.8.15 | CIS 8.8 | CC7.2 |

---

## Domain 7 — Incident Response

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Incident response plan | RS.MA-01 | A.5.24 | CIS 17.1, 17.4 | CC7.3 |
| Incident classification / triage | RS.MA-02, RS.MA-03 | A.5.25 | CIS 17.2 | CC7.3 |
| Incident escalation | RS.MA-04 | A.5.25, A.5.26 | CIS 17.5 | CC7.4 |
| Incident containment | RS.MI-01 | A.5.26 | CIS 17.7 | CC7.4 |
| Incident eradication | RS.MI-02 | A.5.26 | CIS 17.7 | CC7.4 |
| Forensics / evidence collection | RS.AN-06, RS.AN-07 | A.5.28 | CIS 17.8 | CC7.4 |
| Internal incident notification | RS.CO-02 | A.5.26, A.6.8 | CIS 17.5 | CC7.3, CC7.4 |
| External / regulatory notification | RS.CO-02 | A.5.26, A.5.5 | CIS 17.6 | CC7.4, CC9.2 |
| Post-incident review | ID.IM-04 | A.5.27 | CIS 17.7 | CC7.5 |
| Incident response testing (tabletop) | RS.MA-04 | A.5.24 | CIS 17.3 | CC7.3 |

---

## Domain 8 — Business Continuity and Recovery

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Business continuity planning | RC.RP-01 | A.5.29, A.5.30 | CIS 11.1 | A1.2, A1.3 |
| Recovery time and point objectives | RC.RP-01 | A.5.30 | CIS 11.1 | A1.2 |
| Backup and recovery testing | RC.RP-03 | A.8.13 | CIS 11.5 | A1.2, A1.3 |
| Disaster recovery plan | RC.RP-01 | A.5.29, A.5.30 | CIS 11.1 | A1.2, A1.3 |
| Redundant infrastructure | PR.IR-03, PR.IR-04 | A.8.14 | CIS 11.3 | A1.1, A1.2 |
| Recovery communications | RC.CO-03, RC.CO-04 | A.5.26 | — | CC9.2 |

---

## Domain 9 — Third-Party / Supply Chain Risk

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Vendor inventory / classification | GV.SC-02 | A.5.19 | CIS 15.1 | CC9.2 |
| Vendor security assessments | GV.SC-04, GV.SC-10 | A.5.22 | CIS 15.2 | CC9.2 |
| Security in vendor contracts | GV.SC-03, GV.SC-09 | A.5.20 | CIS 15.3 | CC9.2 |
| Software supply chain security | GV.SC-06, GV.SC-07 | A.5.21, A.8.29 | CIS 16.4, 16.5 | CC9.2 |
| Cloud service provider security | GV.SC-08 | A.5.23 | CIS 15.1 | CC9.2 |
| Subprocessor and fourth-party risk | GV.SC-04 | A.5.22 | CIS 15.2 | CC9.2 |

---

## Domain 10 — Security Awareness and Human Risk

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Security awareness training | PR.AT-01 | A.6.3 | CIS 14.1, 14.2 | CC2.2 |
| Role-based security training | PR.AT-02 | A.6.3 | CIS 14.3, 14.4 | CC2.2 |
| Phishing simulation | PR.AT-01 | A.6.3 | CIS 14.7 | CC2.2 |
| Developer secure coding training | PR.PS-06 | A.6.3 | CIS 14.5 | CC2.2 |
| Security culture measurement | GV.OV-01 | A.6.3 | CIS 14.9 | CC2.2 |
| Acceptable use policy | GV.PO-01 | A.5.10 | CIS 4.1 (indirect) | CC2.2 |
| Background checks | GV.RR-02 | A.6.1 | — | CC6.1 |
| NDA / confidentiality agreements | GV.RR-02 | A.6.6 | — | CC6.1 |

---

## Domain 11 — Network Security

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Network segmentation | PR.IR-01 | A.8.22 | CIS 12.2 | CC6.1, CC6.6 |
| Firewall and perimeter controls | PR.IR-01 | A.8.20, A.8.21 | CIS 4.4, 4.5, 12.3 | CC6.1, CC6.6 |
| Remote access security (VPN) | PR.AA-03, PR.IR-01 | A.6.7, A.8.20 | CIS 6.3, 6.4 | CC6.1, CC6.6 |
| Email security (DMARC/DKIM/SPF) | PR.PS-01 | A.8.23 | CIS 9.5 | CC6.1 |
| Web filtering and DNS security | PR.PS-01, DE.CM-01 | A.8.23 | CIS 9.2, 9.3 | CC6.1 |
| Wireless network security | PR.IR-01 | A.8.20 | CIS 12.6 | CC6.6 |
| IDS/IPS | DE.CM-01 | A.8.16 | CIS 13.3 | CC7.2 |
| DDoS protection | PR.IR-03 | A.8.6 (indirect) | CIS 13.5 | A1.1 |

---

## Domain 12 — Governance, Risk, and Compliance

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Information security policy | GV.PO-01, GV.PO-02 | A.5.1, Clause 5.2 | CIS 4.1 (indirect) | CC2.1 |
| Risk assessment | GV.RM-01, ID.RA-03 | Clause 6.1.2 | CIS 7.1 (indirect) | CC3.1, CC3.2 |
| Risk register and treatment | GV.RM-06, ID.RA-06 | Clause 6.1.3 | — | CC3.2, CC3.3 |
| Risk appetite statement | GV.RM-02 | Clause 6.1.2 | — | CC3.1 |
| Internal audit | GV.OV-01 | Clause 9.2 | — | CC4.1, CC4.2 |
| Management review | GV.OV-03 | Clause 9.3 | — | CC4.1 |
| Regulatory compliance tracking | GV.OC-02 | A.5.31, A.5.36 | — | CC2.1 |
| Privacy / PII protection | GV.OC-02 | A.5.34 | CIS 3.1, 3.2 | P1–P8 (Privacy TSC) |
| Board / executive reporting | GV.OV-03 | Clause 9.3 | — | CC1.4 |
| Security roles and responsibilities | GV.RR-01, GV.RR-02 | Clause 5.3, A.5.2 | — | CC1.3 |

---

## SOC 2 Trust Services Criteria — Framework Alignment Summary

| SOC 2 Category | Key Controls | Primary NIST CSF | Primary ISO 27001 | Primary CIS |
|:---|:---|:---|:---|:---|
| CC1 — Control Environment | Governance, roles, ethics | GV.RR, GV.PO | Clause 5, A.5.1, A.5.2 | — |
| CC2 — Communication | Policies, training | GV.PO, PR.AT | A.5.1, A.6.3, A.7.4 | CIS 14 |
| CC3 — Risk Assessment | Risk identification, treatment | ID.RA, GV.RM | Clause 6.1 | — |
| CC4 — Monitoring | Internal audit, management review | GV.OV | Clause 9 | — |
| CC5 — Control Activities | Logical access, change mgmt | PR.AA, PR.PS | A.5.15–A.5.18, A.8.32 | CIS 5, 6, 4 |
| CC6 — Logical and Physical Access | IAM, encryption, physical | PR.AA, PR.DS | A.5.15–A.5.18, A.7, A.8.24 | CIS 5, 6, 3 |
| CC7 — System Operations | Monitoring, incident response | DE.CM, RS | A.8.15, A.8.16, A.5.24–A.5.28 | CIS 8, 13, 17 |
| CC8 — Change Management | Change control, SDLC | PR.PS | A.8.25–A.8.32 | CIS 4, 16 |
| CC9 — Risk Mitigation | Vendor risk, insurance | GV.SC | A.5.19–A.5.23 | CIS 15 |
| A1 — Availability | BCP, redundancy, backups | RC, PR.IR | A.5.29, A.5.30, A.8.13, A.8.14 | CIS 11 |
| C1 — Confidentiality | Data classification, DLP | PR.DS, ID.AM | A.5.12, A.8.11, A.8.12, A.8.24 | CIS 3 |
| P1–P8 — Privacy | PII protection, consent | GV.OC-02 | A.5.34 | CIS 3.1, 3.2 |

---

## Framework Comparison at a Glance

| Dimension | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 |
|:---|:---|:---|:---|:---|
| **Type** | Risk framework | ISMS standard | Control set | Trust criteria |
| **Certification?** | No | Yes (third-party) | No | Yes (SOC 2 report) |
| **Mandatory?** | Voluntary (US) | Voluntary | Voluntary | Voluntary (customer-driven) |
| **Primary audience** | All organizations | All organizations | All organizations | Service organizations |
| **Prescriptiveness** | Low — outcome-based | Medium — control-based | High — specific safeguards | Medium — criteria-based |
| **Control count** | ~108 subcategories | 93 Annex A controls | 153 safeguards | ~60 criteria points |
| **Update frequency** | Major updates every 5–8 yrs | Every 5–10 yrs | Every 3–5 yrs | Periodic |
| **Compliance evidence** | Profiles and tiers | Audit trail and documentation | Safeguard implementation | Type I or Type II report |
| **Best used for** | Risk management strategy | Certification / regulatory | Technical implementation | Customer assurance |

---

*Sources: NIST CSF 2.0 (NIST, Feb 2024) | ISO/IEC 27001:2022 | CIS Controls v8 (CIS, 2021) | SOC 2 TSC (AICPA, 2017) | NIST IR 8477 | CIS Controls Cloud Companion Guide*
