# CSF 2.0 to ISO 27001:2022 Control Mapping

> **Purpose:** Cross-walk between NIST CSF 2.0 subcategories and ISO 27001:2022 Annex A controls
> **Use Case:** Organizations pursuing ISO 27001 certification can use this mapping to identify which CSF subcategories satisfy which Annex A controls — avoiding duplicate work
> **Coverage:** All 6 CSF 2.0 functions mapped to relevant ISO 27001:2022 Annex A controls

---

## How to Use This Mapping

1. **ISO 27001 → CSF direction:** If you have existing CSF controls in place, use this table to determine which ISO Annex A controls they satisfy
2. **CSF → ISO direction:** If you're building to CSF, use this to know which ISO controls you'll need to document for certification
3. **Gap identification:** Cells marked `—` indicate no direct mapping; those controls require standalone implementation

> **Important caveat:** This is an alignment mapping, not a compliance mapping. Satisfying a CSF subcategory does not automatically satisfy an ISO control — ISO requires specific documentation, evidence, and audit-readiness artifacts.

---

## GOVERN Function Mappings

| CSF 2.0 Subcategory | CSF Description | ISO 27001:2022 Controls |
|:---|:---|:---|
| GV.OC-01 | Mission and stakeholders understood | Clause 4.1, 4.2 |
| GV.OC-02 | Legal/regulatory requirements understood | Clause 4.1, 4.2; A.5.31, A.5.32, A.5.33 |
| GV.OC-03 | Critical objectives and capabilities identified | Clause 4.1, 6.1 |
| GV.OC-04 | Relationships and dependencies understood | A.5.19, A.5.20, A.5.21, A.5.22 |
| GV.OC-05 | Cybersecurity integrated into strategy | Clause 5.1, 6.2 |
| GV.RM-01 | Risk management objectives established | Clause 6.1.1, 6.1.2 |
| GV.RM-02 | Risk appetite and tolerance determined | Clause 6.1.2 |
| GV.RM-03 | Cybersecurity risk integrated into ERM | Clause 6.1.1 |
| GV.RM-04 | Strategic direction communicated | Clause 5.1, 7.4 |
| GV.RM-05 | Threats fed into risk management | Clause 6.1.2; A.5.7 |
| GV.RM-06 | Policies establish risk oversight | Clause 5.2, 6.1.1 |
| GV.RM-07 | Strategic opportunities considered | Clause 6.1.1 |
| GV.RR-01 | Leadership accountable for cybersecurity | Clause 5.1, 5.3 |
| GV.RR-02 | Roles and responsibilities assigned | Clause 5.3; A.5.2 |
| GV.RR-03 | Adequate resources allocated | Clause 7.1 |
| GV.RR-04 | Cybersecurity communicated org-wide | Clause 7.3, 7.4 |
| GV.PO-01 | Cybersecurity policy established | Clause 5.2; A.5.1 |
| GV.PO-02 | Policy reviewed and updated | Clause 9.3; A.5.1 |
| GV.OV-01 | Cybersecurity review outcomes inform risk | Clause 9.3 |
| GV.OV-02 | Cybersecurity strategy reviewed | Clause 9.3, 10.1 |
| GV.OV-03 | Results communicated to stakeholders | Clause 9.3, 7.4 |
| GV.SC-01 | Supply chain risk management program | A.5.19, A.5.20 |
| GV.SC-02 | Suppliers identified and prioritized | A.5.19, A.5.21 |
| GV.SC-03 | Contracts require cybersecurity | A.5.20 |
| GV.SC-04 | Suppliers routinely assessed | A.5.22 |
| GV.SC-05 | Response plans for supply chain incidents | A.5.26, A.5.29 |
| GV.SC-06 | Software integrity verified | A.8.29, A.8.30 |
| GV.SC-07 | Risks of acquired components understood | A.5.21 |
| GV.SC-08 | Risks of managed services understood | A.5.23 |
| GV.SC-09 | Security requirements in contracts | A.5.20 |
| GV.SC-10 | Supply chain effectiveness reviewed | A.5.22; Clause 9.3 |

---

## IDENTIFY Function Mappings

| CSF 2.0 Subcategory | CSF Description | ISO 27001:2022 Controls |
|:---|:---|:---|
| ID.AM-01 | Hardware asset inventory | A.5.9 |
| ID.AM-02 | Software asset inventory | A.5.9 |
| ID.AM-03 | Network inventory | A.5.9, A.8.20 |
| ID.AM-04 | Services inventory | A.5.9 |
| ID.AM-05 | Assets prioritized by criticality | A.5.10, A.5.12 |
| ID.AM-07 | Data and data types inventoried | A.5.10, A.5.12 |
| ID.AM-08 | Assets managed through lifecycle | A.5.9, A.8.10 |
| ID.RA-01 | Vulnerabilities identified | A.8.8 |
| ID.RA-02 | Threat intelligence received | A.5.7 |
| ID.RA-03 | Internal/external threats identified | Clause 6.1.2 |
| ID.RA-04 | Impacts and likelihoods considered | Clause 6.1.2 |
| ID.RA-05 | Risk understood from threats/vulns/likelihoods | Clause 6.1.2 |
| ID.RA-06 | Risk responses chosen and tracked | Clause 6.1.3 |
| ID.RA-07 | Changes and exceptions managed | Clause 6.1.3, 10.1 |
| ID.RA-08 | Vulnerability disclosure processes established | A.8.8 |
| ID.RA-09 | Software and hardware authenticity verified | A.5.21, A.8.29 |
| ID.RA-10 | Critical suppliers assessed pre-contract | A.5.19, A.5.20 |
| ID.IM-01 | Improvements identified from evaluations | Clause 9.3, 10.1 |
| ID.IM-02 | Improvements from security tests | Clause 10.1; A.8.8 |
| ID.IM-03 | Improvements from operational processes | Clause 10.1 |
| ID.IM-04 | Incident response evaluated | Clause 10.1; A.5.27 |

---

## PROTECT Function Mappings

| CSF 2.0 Subcategory | CSF Description | ISO 27001:2022 Controls |
|:---|:---|:---|
| PR.AA-01 | Identities managed | A.5.15, A.5.16, A.5.17 |
| PR.AA-02 | Identities proofed and bound to credentials | A.5.16, A.5.17 |
| PR.AA-03 | Authentication enforced | A.5.17, A.8.5 |
| PR.AA-04 | Identity assertions protected | A.5.17, A.8.5 |
| PR.AA-05 | Access permissions managed | A.5.15, A.5.18, A.8.2, A.8.3 |
| PR.AA-06 | Physical access controlled | A.7.1, A.7.2, A.7.3, A.7.4 |
| PR.AT-01 | Awareness and training provided | A.6.3 |
| PR.AT-02 | Specialized role training provided | A.6.3 |
| PR.DS-01 | Data at rest protected | A.8.24 |
| PR.DS-02 | Data in transit protected | A.8.24 |
| PR.DS-10 | Data in use protected | A.8.11 |
| PR.DS-11 | Backups created and tested | A.8.13 |
| PR.PS-01 | Configuration management applied | A.8.9 |
| PR.PS-02 | Software maintained and replaced | A.8.8 |
| PR.PS-03 | Hardware maintained and replaced | A.5.9, A.8.10 |
| PR.PS-04 | Logs generated for continuous monitoring | A.8.15, A.8.16 |
| PR.PS-05 | Unauthorized software prevented | A.8.19 |
| PR.PS-06 | Secure software development practices | A.8.25, A.8.26, A.8.27, A.8.28 |
| PR.IR-01 | Networks protected from unauthorized access | A.8.20, A.8.21, A.8.22 |
| PR.IR-02 | Technology assets protected from environmental threats | A.7.5, A.7.6, A.7.8 |
| PR.IR-03 | Resilience mechanisms implemented | A.8.14 |
| PR.IR-04 | Adequate resource capacity ensured | A.8.6 |

---

## DETECT Function Mappings

| CSF 2.0 Subcategory | CSF Description | ISO 27001:2022 Controls |
|:---|:---|:---|
| DE.CM-01 | Networks and services monitored | A.8.15, A.8.16 |
| DE.CM-02 | Physical environment monitored | A.7.4 |
| DE.CM-03 | Personnel activity monitored | A.8.16 |
| DE.CM-06 | External service provider activities monitored | A.5.22; A.8.15 |
| DE.CM-09 | Computing hardware and software monitored | A.8.15, A.8.16 |
| DE.AE-02 | Adverse events analyzed | A.5.25, A.5.26 |
| DE.AE-03 | Information correlated from multiple sources | A.8.16 |
| DE.AE-04 | Impact and scope understood | A.5.25 |
| DE.AE-06 | Information provided to authorized staff | A.5.26 |
| DE.AE-07 | Cyber threat intelligence integrated | A.5.7 |
| DE.AE-08 | Incidents declared when criteria met | A.5.25 |

---

## RESPOND Function Mappings

| CSF 2.0 Subcategory | CSF Description | ISO 27001:2022 Controls |
|:---|:---|:---|
| RS.MA-01 | Incident response plan executable | A.5.24 |
| RS.MA-02 | Incident reports triaged and validated | A.5.25 |
| RS.MA-03 | Incidents categorized and prioritized | A.5.25 |
| RS.MA-04 | Incidents escalated as needed | A.5.25, A.5.26 |
| RS.MA-05 | Incidents declared contained | A.5.26 |
| RS.AN-03 | Analysis of what took place | A.5.26, A.5.27 |
| RS.AN-06 | Actions during investigation recorded | A.5.26; A.8.15 |
| RS.AN-07 | Incident data and metadata collected | A.8.15 |
| RS.AN-08 | Incident magnitude estimated | A.5.25, A.5.26 |
| RS.CO-02 | Stakeholders notified of incidents | A.5.26, A.6.8 |
| RS.CO-03 | Information shared with stakeholders | A.5.26 |
| RS.MI-01 | Incidents contained | A.5.26 |
| RS.MI-02 | Incidents eradicated | A.5.26 |

---

## RECOVER Function Mappings

| CSF 2.0 Subcategory | CSF Description | ISO 27001:2022 Controls |
|:---|:---|:---|
| RC.RP-01 | Recovery plan executed | A.5.29, A.5.30 |
| RC.RP-02 | Recovery actions selected and performed | A.5.26, A.5.29 |
| RC.RP-03 | Completeness of recovery confirmed | A.5.29 |
| RC.RP-04 | Reputation strategies applied | A.5.26 |
| RC.RP-05 | Recovery activities end when criteria met | A.5.29 |
| RC.RP-06 | Lessons learned incorporated | A.5.27; Clause 10.1 |
| RC.CO-03 | Recovery progress communicated to stakeholders | A.5.26 |
| RC.CO-04 | Public updates shared via approved methods | A.5.26 |

---

## ISO 27001 Controls Without Direct CSF Mapping

The following ISO 27001:2022 Annex A controls do not map directly to a CSF subcategory and require standalone implementation:

| ISO Control | Description | Notes |
|:---|:---|:---|
| A.6.1 | Screening | HR pre-employment screening — no CSF equivalent |
| A.6.2 | Terms and conditions of employment | HR policy — tangential to CSF |
| A.6.4 | Disciplinary process | HR domain |
| A.6.5 | Responsibilities after termination | HR/legal domain |
| A.6.6 | Confidentiality agreements | Legal/contractual |
| A.6.7 | Remote working | Operationally specific |
| A.7.9 | Security of assets off-premises | Physical security specific |
| A.7.10 | Storage media | Physical security specific |
| A.7.14 | Secure disposal or reuse | Physical security specific |
| A.5.34 | Privacy and protection of personal information (GDPR) | Requires separate privacy program |
| A.5.35 | Independent review of information security | Internal audit specific |
| A.5.36 | Compliance with policies and procedures | Compliance monitoring specific |

---

## Summary: Coverage Analysis

| CSF Function | Total Subcategories | Mapped to ISO Controls | Coverage |
|:---|:---:|:---:|:---:|
| Govern (GV) | 30 | 30 | 100% |
| Identify (ID) | 21 | 21 | 100% |
| Protect (PR) | 22 | 22 | 100% |
| Detect (DE) | 11 | 11 | 100% |
| Respond (RS) | 13 | 13 | 100% |
| Recover (RC) | 8 | 8 | 100% |
| **Total** | **105** | **105** | **100%** |

> **Note:** Coverage indicates that a mapping exists — not that implementing CSF subcategories alone satisfies ISO 27001 certification requirements. ISO 27001 requires documented evidence, defined processes, internal audit, and third-party certification body review.

---

## Related Resources

- Full implementation guidance: `nist-csf-2.0-implementation-guide.md`
- ISO 27001 gap analysis: `../iso-27001/iso27001-gap-analysis-template.md`
- All 93 Annex A controls: `../iso-27001/annex-a-control-register.md`
- Multi-framework mapping (adds CIS and SOC 2): `../cross-framework/master-control-mapping.md`

---

*Sources: NIST CSF 2.0 Core (Feb 2024) | ISO/IEC 27001:2022 | NIST IR 8477 (Mapping NIST CSF 2.0 to ISO/IEC 27001)*
