# Statement of Applicability (SoA)

> **Standard:** ISO/IEC 27001:2022 — Clause 6.1.3(d)
> **Purpose:** Document which Annex A controls are applicable, the justification for inclusion or exclusion, and implementation status
> **Requirement:** The SoA is mandatory for ISO 27001 certification. It must reference risk treatment decisions and be approved by leadership.

---

## Document Control

| Field | Value |
|:---|:---|
| **Document Title** | Statement of Applicability |
| **Document ID** | ISMS-SOA-001 |
| **Version** | 1.0 |
| **Status** | Draft / Approved |
| **Owner** | [CISO / Security Program Owner] |
| **Approved By** | [CEO / Executive Sponsor] |
| **Approval Date** | |
| **Risk Assessment Reference** | [ISMS-RA-001 vX.X, dated DD/MM/YYYY] |
| **Review Frequency** | Annual or after risk reassessment |
| **Next Review Date** | |
| **Classification** | Internal — Confidential |

---

## Purpose and Scope

This Statement of Applicability (SoA) documents the information security controls selected by **[Organization Name]** following the completion of its information security risk assessment and risk treatment process, in accordance with ISO/IEC 27001:2022 Clause 6.1.3.

For each control in ISO 27001:2022 Annex A, this document records:
- Whether the control is **applicable** or **excluded**
- The **justification** (risk assessment finding, legal/contractual requirement, or business decision)
- The **implementation status**
- Reference to the **policy, procedure, or evidence** that implements the control

---

## Inclusion / Exclusion Legend

| Symbol | Applicable? | Meaning |
|:---:|:---|:---|
| ✅ | Yes | Control is in scope and implemented (or being implemented) |
| ❌ | No (Excluded) | Control is excluded; written justification required |

### Implementation Status

| Code | Status |
|:---:|:---|
| **F** | Fully Implemented — evidence available; audit-ready |
| **P** | Partially Implemented — in progress; gaps remain |
| **N** | Not Yet Implemented — planned; remediation in progress |
| **NA** | Not Applicable — formally excluded |

---

## Annex A Controls — Statement of Applicability

### A.5 — Organizational Controls (37 controls)

| Control | Title | Applicable | Justification | Status | Policy / Evidence Reference |
|:---|:---|:---:|:---|:---:|:---|
| A.5.1 | Policies for information security | ✅ | Risk assessment: all risk treatments require governing policy | N | ISMS-POL-001 (in draft) |
| A.5.2 | Information security roles and responsibilities | ✅ | Required to establish accountability for risk treatment | P | ISMS-RACI-001 |
| A.5.3 | Segregation of duties | ✅ | Required to reduce fraud and error risk in critical processes | P | IT-POL-006 |
| A.5.4 | Management responsibilities | ✅ | Clause 5.1 obligation; management accountability required | N | ISMS-POL-001 |
| A.5.5 | Contact with authorities | ✅ | Legal obligation for breach notification; regulatory relationships | N | ISMS-IRP-001 |
| A.5.6 | Contact with special interest groups | ✅ | Threat intelligence requirement from risk assessment | N | — |
| A.5.7 | Threat intelligence | ✅ | Risk assessment: threat landscape awareness required | N | — |
| A.5.8 | Information security in project management | ✅ | Risk assessment: insecure SDLC identified as risk | N | SDLC-POL-001 |
| A.5.9 | Inventory of information and other associated assets | ✅ | Clause 8 operation; foundational for all other controls | P | CMDB-001, DATA-REG-001 |
| A.5.10 | Acceptable use of information and other assets | ✅ | Required to set behavioural expectations for all personnel | P | IT-POL-001 |
| A.5.11 | Return of assets | ✅ | Required upon termination; offboarding risk | F | HR-OFF-001 |
| A.5.12 | Classification of information | ✅ | Risk assessment: data handling inconsistency identified | N | DATA-CLASS-001 (in draft) |
| A.5.13 | Labelling of information | ✅ | Required to implement classification scheme | N | DATA-CLASS-001 |
| A.5.14 | Information transfer | ✅ | Risk assessment: data exfiltration risk identified | P | IT-POL-003 |
| A.5.15 | Access control | ✅ | Risk assessment: unauthorized access identified as top risk | P | IAM-POL-001 |
| A.5.16 | Identity management | ✅ | Required to implement access control | P | IAM-POL-001 |
| A.5.17 | Authentication information | ✅ | Risk assessment: credential compromise identified as top risk | P | IAM-POL-002 |
| A.5.18 | Access rights | ✅ | Required by access control policy; Clause 8 operation | N | IAM-POL-001 |
| A.5.19 | Information security in supplier relationships | ✅ | Risk assessment: supply chain risk identified | N | VRM-POL-001 (in draft) |
| A.5.20 | Addressing IS within supplier agreements | ✅ | Contractual obligation to protect customer data | N | VRM-TMPL-001 |
| A.5.21 | Managing IS in the ICT supply chain | ✅ | Risk assessment: software supply chain risk identified | N | VRM-POL-001 |
| A.5.22 | Monitoring, review and change management of suppliers | ✅ | Required to maintain ongoing supplier risk management | N | VRM-POL-001 |
| A.5.23 | IS for use of cloud services | ✅ | Risk assessment: cloud misconfigurations identified | N | CLOUD-POL-001 (in draft) |
| A.5.24 | IS incident management planning | ✅ | Legal breach notification obligations; risk treatment | N | IRP-001 (in draft) |
| A.5.25 | Assessment and decision on IS events | ✅ | Required to triage and respond to incidents | N | IRP-001 |
| A.5.26 | Response to IS incidents | ✅ | Risk treatment: incident containment required | N | IRP-001 |
| A.5.27 | Learning from IS incidents | ✅ | Clause 10.1 continual improvement requirement | N | IRP-001 |
| A.5.28 | Collection of evidence | ✅ | Legal obligation; regulatory investigation support | N | FORENSICS-001 (in draft) |
| A.5.29 | IS during disruption | ✅ | Risk assessment: availability risk to critical services | N | BCP-001 (in draft) |
| A.5.30 | ICT readiness for business continuity | ✅ | Required to ensure recovery from disruption | N | DRP-001 (in draft) |
| A.5.31 | Legal, statutory, regulatory and contractual requirements | ✅ | Mandatory compliance obligation | P | LEGAL-REG-001 |
| A.5.32 | Intellectual property rights | ✅ | Legal obligation; IP protection | F | LEGAL-POL-001 |
| A.5.33 | Protection of records | ✅ | Legal and regulatory retention requirements | P | REC-POL-001 |
| A.5.34 | Privacy and protection of PII | ✅ | GDPR / applicable privacy law obligation | N | PRIV-POL-001 (in draft) |
| A.5.35 | Independent review of IS | ✅ | ISO 27001 certification requirement (Clause 9.2) | N | AUDIT-PROG-001 |
| A.5.36 | Compliance with policies and procedures | ✅ | Required to demonstrate conformance | N | AUDIT-PROG-001 |
| A.5.37 | Documented operating procedures | ✅ | Required for consistent control operation | P | Various IT runbooks |

---

### A.6 — People Controls (8 controls)

| Control | Title | Applicable | Justification | Status | Policy / Evidence Reference |
|:---|:---|:---:|:---|:---|:---:|
| A.6.1 | Screening | ✅ | HR risk; insider threat mitigation | F | HR-POL-002 |
| A.6.2 | Terms and conditions of employment | ✅ | Required to assign security responsibilities to staff | P | HR-CONTRACT-001 |
| A.6.3 | IS awareness, education and training | ✅ | Risk assessment: human error identified as top risk | P | TRAIN-001 |
| A.6.4 | Disciplinary process | ✅ | Required to enforce security policy compliance | F | HR-POL-003 |
| A.6.5 | Responsibilities after termination | ✅ | Risk assessment: data exfiltration at termination | P | HR-OFF-001 |
| A.6.6 | Confidentiality or NDA agreements | ✅ | Contractual obligation to protect confidential information | F | HR-NDA-001 |
| A.6.7 | Remote working | ✅ | Risk assessment: remote work security gaps identified | P | IT-POL-005 |
| A.6.8 | IS event reporting | ✅ | Required to enable incident management (A.5.24) | N | IRP-001 |

---

### A.7 — Physical Controls (14 controls)

| Control | Title | Applicable | Justification | Status | Policy / Evidence Reference |
|:---|:---|:---:|:---|:---|:---:|
| A.7.1 | Physical security perimeters | ✅ | Risk assessment: unauthorized physical access risk | F | PHYS-POL-001 |
| A.7.2 | Physical entry | ✅ | Required to control access to secure areas | F | PHYS-POL-001 |
| A.7.3 | Securing offices, rooms and facilities | ✅ | Required to protect information assets | F | PHYS-POL-001 |
| A.7.4 | Physical security monitoring | ✅ | Required to detect unauthorized access | P | PHYS-POL-001 |
| A.7.5 | Protecting against physical and environmental threats | ✅ | Risk assessment: availability risk from physical threats | F | PHYS-POL-002 |
| A.7.6 | Working in secure areas | ✅ | Required to control behavior in security zones | P | PHYS-POL-001 |
| A.7.7 | Clear desk and clear screen | ✅ | Risk assessment: information exposure risk | P | IT-POL-001 |
| A.7.8 | Equipment siting and protection | ✅ | Required to protect hardware from unauthorized access | F | PHYS-POL-002 |
| A.7.9 | Security of assets off-premises | ✅ | Risk assessment: laptop loss/theft identified | P | IT-POL-005 |
| A.7.10 | Storage media | ✅ | Risk assessment: data on removable media | P | IT-POL-004 |
| A.7.11 | Supporting utilities | ✅ | Risk assessment: power/utility failure risk | F | PHYS-POL-002 |
| A.7.12 | Cabling security | ✅ | Required to prevent eavesdropping or sabotage | F | PHYS-POL-002 |
| A.7.13 | Equipment maintenance | ✅ | Required to maintain availability | F | IT-MAINT-001 |
| A.7.14 | Secure disposal or reuse of equipment | ✅ | Risk assessment: data exposure from decommissioned hardware | P | IT-POL-004 |

---

### A.8 — Technological Controls (34 controls)

| Control | Title | Applicable | Justification | Status | Policy / Evidence Reference |
|:---|:---|:---:|:---|:---|:---:|
| A.8.1 | User endpoint devices | ✅ | Risk assessment: endpoint compromise identified | P | IT-POL-002 |
| A.8.2 | Privileged access rights | ✅ | Risk assessment: admin account compromise is top risk | N | IAM-POL-002 (PAM program) |
| A.8.3 | Information access restriction | ✅ | Required to enforce least privilege | P | IAM-POL-001 |
| A.8.4 | Access to source code | ✅ | Risk assessment: IP theft risk | F | DEV-POL-001 |
| A.8.5 | Secure authentication | ✅ | Required by access control policy | P | IAM-POL-002 |
| A.8.6 | Capacity management | ✅ | Risk assessment: availability degradation risk | P | OPS-POL-001 |
| A.8.7 | Protection against malware | ✅ | Risk assessment: malware is top threat | F | SEC-POL-002 |
| A.8.8 | Management of technical vulnerabilities | ✅ | Risk assessment: unpatched systems identified | P | VULN-POL-001 |
| A.8.9 | Configuration management | ✅ | Risk assessment: misconfiguration is top vulnerability class | P | IT-POL-006 |
| A.8.10 | Information deletion | ✅ | Legal / GDPR data minimization obligation | N | DATA-CLASS-001 |
| A.8.11 | Data masking | ✅ | Risk assessment: PII in test environments identified | N | DATA-CLASS-001 |
| A.8.12 | Data leakage prevention | ✅ | Risk assessment: data exfiltration risk | P | DLP-POL-001 |
| A.8.13 | Information backup | ✅ | Risk assessment: data loss risk; availability requirement | P | BACKUP-POL-001 |
| A.8.14 | Redundancy of information processing facilities | ✅ | Risk assessment: availability risk to critical services | P | DRP-001 |
| A.8.15 | Logging | ✅ | Required for monitoring, audit, and incident response | P | LOG-POL-001 |
| A.8.16 | Monitoring activities | ✅ | Risk assessment: lack of detection capability identified | N | SOC-POL-001 (in draft) |
| A.8.17 | Clock synchronisation | ✅ | Required for log integrity and forensics | F | IT-POL-006 |
| A.8.18 | Use of privileged utility programs | ✅ | Required to control admin tool usage | P | IAM-POL-002 |
| A.8.19 | Installation of software on operational systems | ✅ | Risk assessment: unauthorized software risk | P | IT-POL-002 |
| A.8.20 | Networks security | ✅ | Risk assessment: network intrusion risk | P | NET-POL-001 |
| A.8.21 | Security of network services | ✅ | Required to govern use of external network services | P | NET-POL-001 |
| A.8.22 | Segregation of networks | ✅ | Risk assessment: flat network increases blast radius | N | NET-POL-001 |
| A.8.23 | Web filtering | ✅ | Risk assessment: malicious web content as attack vector | F | NET-POL-002 |
| A.8.24 | Use of cryptography | ✅ | Risk assessment: data in transit/at rest protection | P | CRYPTO-POL-001 |
| A.8.25 | Secure development life cycle | ✅ | Risk assessment: insecure code as vulnerability source | N | SDLC-POL-001 |
| A.8.26 | Application security requirements | ✅ | Required to define security in development | N | SDLC-POL-001 |
| A.8.27 | Secure system architecture and engineering | ✅ | Risk assessment: insecure design identified | N | SDLC-POL-001 |
| A.8.28 | Secure coding | ✅ | Risk assessment: application vulnerabilities identified | N | SDLC-POL-002 |
| A.8.29 | Security testing in development and acceptance | ✅ | Required to validate security before deployment | P | SDLC-POL-001 |
| A.8.30 | Outsourced development | ❌ | **EXCLUDED:** All software development is performed in-house; no outsourced development | NA | Risk Assessment §4.2, Exclusion documented |
| A.8.31 | Separation of dev, test and production environments | ✅ | Risk assessment: production data exposure risk | P | IT-POL-006 |
| A.8.32 | Change management | ✅ | Risk assessment: unauthorized changes as risk | P | CHG-POL-001 |
| A.8.33 | Test information | ✅ | Risk assessment: PII in test environments; GDPR obligation | N | DATA-CLASS-001 |
| A.8.34 | Protection of IS during audit testing | ✅ | Required to protect production during audit activity | N | AUDIT-PROG-001 |

---

## SoA Summary

| Section | Total Controls | Applicable (✅) | Excluded (❌) | Fully Implemented | Partially Implemented | Not Yet Implemented |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|
| A.5 Organizational | 37 | 37 | 0 | 3 | 12 | 22 |
| A.6 People | 8 | 8 | 0 | 3 | 4 | 1 |
| A.7 Physical | 14 | 14 | 0 | 8 | 5 | 1 |
| A.8 Technological | 34 | 33 | 1 | 3 | 15 | 15 |
| **Total** | **93** | **92** | **1** | **17** | **36** | **39** |
| **% of applicable controls** | | **99%** | **1%** | **18%** | **39%** | **42%** |

---

## Excluded Controls Log

> All excluded controls must be documented here with risk justification. Exclusion is only permitted when the control is irrelevant due to the nature of the organization.

| Control | Title | Reason for Exclusion | Risk Rationale | Approved By | Date |
|:---|:---|:---|:---|:---|:---|
| A.8.30 | Outsourced development | Organization performs all development in-house. No third-party developers are engaged. | Risk does not apply; no outsourced development relationships exist. | [CISO] | |
| | | | | | |

---

## Approval

| Role | Name | Signature | Date |
|:---|:---|:---|:---|
| ISMS Owner / CISO | | | |
| Executive Sponsor | | | |
| Internal Audit Lead | | | |

---

## Revision History

| Version | Date | Author | Changes |
|:---:|:---|:---|:---|
| 1.0 | | | Initial SoA based on risk assessment version [X.X] |
| | | | |

---

*Template Version: ISO/IEC 27001:2022 (Clause 6.1.3) | See git history for revision dates*
