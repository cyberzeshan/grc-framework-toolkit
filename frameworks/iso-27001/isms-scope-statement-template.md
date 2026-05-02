# ISMS Scope Statement Template

> **Standard:** ISO/IEC 27001:2022 — Clause 4.3
> **Purpose:** Define the boundaries and applicability of the Information Security Management System
> **Output:** Approved scope statement referenced in Stage 1 audit and all ISMS documentation
> **Critical:** The scope statement is the first document auditors review. Vague scope = audit finding.

---

## Document Control

| Field | Value |
|:---|:---|
| **Document Title** | ISMS Scope Statement |
| **Document ID** | ISMS-SCOPE-001 |
| **Version** | 1.0 |
| **Status** | Draft / Under Review / Approved |
| **Owner** | [CISO / Security Program Owner] |
| **Approved By** | [CEO / Executive Sponsor] |
| **Approval Date** | |
| **Review Frequency** | Annual or upon material change |
| **Next Review Date** | |
| **Classification** | Internal |

---

## 1. Organization Overview

**Legal Name:** [Full legal name of the organization]

**Operating Name:** [Trade name, if different]

**Industry / Sector:** [e.g., Financial Services, Healthcare, SaaS, Government contractor]

**Headquarters:** [City, State/Province, Country]

**Number of Employees:** [Total headcount in scope]

**Applicable Regulations:** [List: e.g., GDPR, HIPAA, PCI-DSS, SOX, CCPA, FedRAMP]

---

## 2. ISMS Scope Statement

> **Instructions:** Write a clear, precise statement that defines what is included within the ISMS. The statement must be specific enough to support audit testing but comprehensive enough to cover all relevant information security risks.

### 2.1 Scope Narrative

The Information Security Management System (ISMS) of **[Organization Name]** encompasses:

**Business Functions / Departments:**
_[List the organizational units included. Be explicit. "All departments" is acceptable only if truly all-inclusive and can be evidenced.]_

- [ ] Executive / Leadership
- [ ] Engineering / Technology
- [ ] Product
- [ ] Sales & Marketing
- [ ] Customer Success / Support
- [ ] Finance
- [ ] Legal & Compliance
- [ ] Human Resources
- [ ] Operations / IT

**Products and Services in Scope:**
_[Describe the specific products, services, or service lines covered. This drives which data assets, systems, and processes fall under the ISMS.]_

> Example: "The development, delivery, and support of [Product Name], a SaaS platform providing [description], including all supporting infrastructure, data processing activities, and customer-facing services."

[Enter your products/services scope here]

**Information Types in Scope:**
- Customer Personally Identifiable Information (PII)
- Employee Personal Data
- Financial Records and Transactional Data
- Intellectual Property and Source Code
- System Credentials and Cryptographic Keys
- Audit Logs and Security Event Data
- [Other — specify]

---

### 2.2 Physical Scope

| Location | Address | Type | In Scope? | Notes |
|:---|:---|:---|:---:|:---|
| Headquarters | | Office | ✅ Yes | Primary location |
| Data Center / Co-Lo | | Data Center | ✅ Yes | Production infrastructure |
| Remote / Home Offices | | Distributed | ✅ Yes | Covered under remote work policy |
| [Additional office] | | | | |

**Cloud Environments:**

| Provider | Accounts / Projects | Region(s) | In Scope? |
|:---|:---|:---|:---:|
| AWS | [Account IDs] | us-east-1, eu-west-1 | ✅ Yes |
| Azure | [Subscription IDs] | | |
| GCP | [Project IDs] | | |
| [Other SaaS/PaaS] | | | |

---

### 2.3 Technical Scope

**In-scope systems and infrastructure:**

| System Category | Examples | Included? |
|:---|:---|:---:|
| Production application servers | [App name, API servers] | ✅ |
| Production databases | [PostgreSQL, RDS, MongoDB] | ✅ |
| Corporate IT systems | Email, HR, Finance systems | ✅ |
| Developer workstations | Managed laptops | ✅ |
| CI/CD pipeline | GitHub, Jenkins, CircleCI | ✅ |
| Source code repositories | GitHub / GitLab | ✅ |
| Cloud infrastructure | AWS VPCs, subnets, S3 | ✅ |
| Network infrastructure | Firewalls, VPN, switches | ✅ |
| Physical security systems | CCTV, badge readers | ✅ |

---

## 3. Explicit Exclusions

> **ISO 27001 Requirement:** All exclusions must be documented with justification. Auditors will scrutinize exclusions that appear to reduce scope artificially.

| Excluded Area | Justification | Risk Assessment Reference |
|:---|:---|:---|
| [e.g., Subsidiary XYZ] | Separate legal entity with its own ISMS; not operationally integrated | Risk Assessment v1.0, §3.2 |
| [e.g., Legacy system ABC] | System scheduled for decommission within 90 days; no customer data | Decommission plan dated [date] |
| [e.g., Office location DEF] | No information processing activities; administrative only | Site assessment [date] |

> **Practitioner Note:** If you are excluding a system that processes personal data or is internet-facing, expect significant auditor scrutiny. Prepare a detailed written justification.

---

## 4. Interested Parties and Their Requirements

> **Clause 4.2 requirement:** Identify interested parties relevant to the ISMS and their information security requirements.

| Interested Party | Type | Key Information Security Requirements |
|:---|:---|:---|
| Customers | External | Data protection, availability, breach notification within [X hours] |
| Regulators | External | [GDPR Art. 32, HIPAA Security Rule, PCI-DSS, etc.] |
| Employees | Internal | Privacy of personal data; secure tools and systems |
| Shareholders / Board | Internal | Risk visibility, material breach disclosure |
| Suppliers / Vendors | External | Secure data handling; access controls; NDA compliance |
| Cloud Service Providers | External | Shared responsibility model compliance |
| Certification Body | External | ISO 27001:2022 conformance |
| [Cyber Insurer] | External | Security controls baseline per policy requirements |
| Legal Counsel | Internal | Regulatory and contractual obligation tracking |

---

## 5. Internal and External Issues

> **Clause 4.1 requirement:** Identify internal and external issues relevant to the ISMS.

### External Issues

| Category | Issue | ISMS Impact |
|:---|:---|:---|
| Threat landscape | Ransomware targeting our sector | Increases risk to data availability and confidentiality |
| Regulatory | GDPR enforcement increasing; new AI Act obligations | Compliance scope may expand |
| Supply chain | SaaS vendor concentration risk | Third-party incident could affect service delivery |
| Market | Customer security questionnaires increasingly stringent | Certification required to win enterprise contracts |
| Geopolitical | Operations in [country] with conflicting data laws | Data residency controls required |

### Internal Issues

| Category | Issue | ISMS Impact |
|:---|:---|:---|
| People | Security team understaffed; 2 open FTE | Slower remediation; coverage gaps |
| Technology | Legacy application with known technical debt | Higher vulnerability surface |
| Process | Change management process immature | Increased risk of unauthorized changes |
| Culture | Developer velocity prioritized over security | Risk of insecure code being deployed |
| Financial | Security budget constrained | Limits tooling investments |

---

## 6. Interface and Dependencies

> Identify where the ISMS interfaces with other management systems or organizational processes.

| Interface | System / Framework | How It Integrates |
|:---|:---|:---|
| Enterprise Risk Management | [ERM platform / process] | Information security risks reported to ERM quarterly |
| Business Continuity Management | BCP/DRP | ISMS covers information security aspects of BCM |
| HR Onboarding / Offboarding | [HRIS system] | Security controls triggered by employment status changes |
| Change Management | [ITSM tool] | Security review gate in change approval workflow |
| Vendor Management | [Procurement system] | Security assessment required before vendor approval |
| Legal / Compliance | [Compliance program] | Regulatory requirements feeding into ISMS scope |
| Software Development (SDLC) | [Agile/DevOps process] | Secure SDLC requirements integrated into dev workflow |

---

## 7. Scope Boundary Diagram

> Insert or reference a diagram illustrating the ISMS boundary. The diagram should show:
> - In-scope systems, locations, and people
> - Explicit exclusions (clearly labeled "Out of Scope")
> - Key interfaces with external parties (customers, vendors, regulators)
> - Data flows crossing the ISMS boundary

```
[INSERT ARCHITECTURE / BOUNDARY DIAGRAM HERE]

Suggested tool: draw.io, Lucidchart, or Mermaid diagram
Reference: architecture/isms-boundary-diagram.png
```

---

## 8. Approval and Sign-Off

| Role | Name | Signature | Date |
|:---|:---|:---|:---|
| ISMS Owner / CISO | | | |
| Executive Sponsor / CEO | | | |
| Legal Counsel | | | |
| IT Director | | | |

---

## 9. Revision History

| Version | Date | Author | Changes |
|:---:|:---|:---|:---|
| 1.0 | | | Initial draft |
| | | | |

---

## Appendix A: Scope Checklist

Use before submitting for executive approval:

- [ ] Scope narrative clearly identifies what services/products are covered
- [ ] All physical locations are listed with in/out-of-scope designation
- [ ] Cloud accounts and regions are explicitly listed
- [ ] All exclusions are documented with written justification
- [ ] Interested parties and their requirements are documented
- [ ] Internal and external issues are identified
- [ ] Interfaces with other management systems are noted
- [ ] Boundary diagram exists and is current
- [ ] Executive sponsorship obtained and signed

---

*Template Version: ISO/IEC 27001:2022 (Clause 4.3) | See git history for revision dates*
