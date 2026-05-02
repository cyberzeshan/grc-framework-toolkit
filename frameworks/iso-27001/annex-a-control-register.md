# ISO 27001:2022 Annex A Control Register

> **Standard:** ISO/IEC 27001:2022
> **Purpose:** Complete register of all 93 Annex A controls with descriptions, implementation guidance, and cross-references
> **Use:** Reference alongside the Statement of Applicability (SoA) and gap analysis

---

## Overview

ISO 27001:2022 Annex A contains **93 controls** organized into **4 themes**:

| Theme | Controls | Count |
|:---|:---|:---:|
| A.5 | Organizational Controls | 37 |
| A.6 | People Controls | 8 |
| A.7 | Physical Controls | 14 |
| A.8 | Technological Controls | 34 |
| **Total** | | **93** |

**New in 2022 (not in 2013 edition):** 11 new controls marked with 🆕

---

## A.5 — Organizational Controls

### A.5.1 — Policies for Information Security
**Description:** Information security policies and topic-specific policies shall be defined, approved by management, published, communicated to and acknowledged by relevant personnel and relevant interested parties, and reviewed at planned intervals and if significant changes occur.

**Implementation Guidance:**
- Establish a top-level Information Security Policy signed by the CEO/Board
- Develop topic-specific policies (access control, cryptography, incident response, etc.)
- Review all policies at least annually or after major incidents
- Maintain documented evidence of policy acknowledgement by all staff

**Evidence Required:** Signed policy document, distribution records, acknowledgement log, review minutes

---

### A.5.2 — Information Security Roles and Responsibilities
**Description:** Information security roles and responsibilities shall be defined and allocated according to the needs of the organization.

**Implementation Guidance:**
- Create a RACI matrix for information security responsibilities
- Define roles: CISO, Data Owner, Data Custodian, System Owner, End User
- Include security responsibilities in all relevant job descriptions
- Ensure segregation of duties for conflicting roles

**Evidence Required:** RACI matrix, job descriptions with security responsibilities, org chart

---

### A.5.3 — Segregation of Duties
**Description:** Conflicting duties and conflicting areas of responsibility shall be segregated.

**Implementation Guidance:**
- Map all critical processes and identify conflicting duties
- Implement compensating controls where full SoD is not feasible (e.g., logging, supervisory review)
- Audit segregation quarterly for privileged system roles
- Document compensating controls where SoD is not achievable

**Evidence Required:** SoD matrix, access control configuration, compensating control documentation

---

### A.5.4 — Management Responsibilities
**Description:** Management shall require all personnel to apply information security in accordance with the established information security policy, topic-specific policies and procedures of the organization.

**Implementation Guidance:**
- Include security obligations in all employment contracts
- Conduct regular all-hands security communications from leadership
- Hold managers accountable for their teams' policy compliance
- Include security in performance reviews

**Evidence Required:** Employment contracts, management communications, HR policy

---

### A.5.5 — Contact with Authorities
**Description:** The organization shall establish and maintain contact with relevant authorities.

**Implementation Guidance:**
- Identify relevant authorities: law enforcement (FBI/CISA), data protection regulators (ICO, GDPR supervisory authorities), sector regulators
- Document contact information and escalation procedures
- Establish relationships before incidents occur
- Include authority contacts in the Incident Response Plan

**Evidence Required:** Authority contact register, IRP with escalation paths

---

### A.5.6 — Contact with Special Interest Groups
**Description:** The organization shall establish and maintain contact with special interest groups or other specialist security forums and professional associations.

**Implementation Guidance:**
- Join sector-specific ISAC (Information Sharing and Analysis Center)
- Subscribe to threat intelligence feeds (CISA alerts, vendor advisories)
- Participate in peer group forums (BSides, ISACA, (ISC)²)

**Evidence Required:** ISAC membership records, threat intel subscription receipts, participation logs

---

### A.5.7 🆕 — Threat Intelligence
**Description:** Information relating to information security threats shall be collected and analysed to produce threat intelligence.

**Implementation Guidance:**
- Subscribe to threat intelligence feeds (commercial or free: CISA, OTX, FS-ISAC)
- Integrate threat intelligence into risk assessments
- Distribute relevant intel to security operations and leadership
- Track TTPs (Tactics, Techniques, and Procedures) relevant to your sector

**Evidence Required:** Threat intel feed subscriptions, distribution records, risk assessment integration

---

### A.5.8 — Information Security in Project Management
**Description:** Information security shall be integrated into project management.

**Implementation Guidance:**
- Add security review gate to project initiation (PMO process)
- Require Data Protection Impact Assessment (DPIA) for projects processing personal data
- Include security architect or security engineer in project teams for significant projects
- Track security requirements as project deliverables

**Evidence Required:** Project management template with security gate, DPIA records, project security sign-offs

---

### A.5.9 — Inventory of Information and Other Associated Assets
**Description:** An inventory of information and other associated assets, including owners, shall be developed and maintained.

**Implementation Guidance:**
- Maintain CMDB for hardware assets
- Maintain software asset management (SAM) inventory
- Create a data asset register including data types, location, classification, and owner
- Review and update inventory at least quarterly (or continuously via automated discovery)

**Evidence Required:** CMDB exports, software inventory reports, data register

---

### A.5.10 — Acceptable Use of Information and Other Assets
**Description:** Rules for the acceptable use and procedures for handling information and other associated assets shall be identified, documented, and implemented.

**Implementation Guidance:**
- Publish an Acceptable Use Policy covering: corporate devices, BYOD, internet, email, social media, cloud storage
- Require annual acknowledgement from all staff
- Update to address AI tool usage

**Evidence Required:** Acceptable Use Policy, annual acknowledgement records

---

### A.5.11 — Return of Assets
**Description:** Personnel and other interested party users shall return all the organization's assets upon change or termination of their employment, contract or agreement.

**Implementation Guidance:**
- Create an offboarding checklist that includes asset return
- Integrate with HR offboarding workflow
- Document asset return with signature or receipt

**Evidence Required:** Offboarding checklist, asset return receipts, HR offboarding records

---

### A.5.12 — Classification of Information
**Description:** Information shall be classified according to the information security needs of the organization based on confidentiality, integrity and availability requirements.

**Implementation Guidance:**
- Define classification levels (e.g., Public / Internal / Confidential / Restricted)
- Document classification criteria and examples
- Train staff on classification requirements
- Apply classification to all new information assets

**Evidence Required:** Data classification policy, training records, example-classified documents

---

### A.5.13 — Labelling of Information
**Description:** An appropriate set of procedures for information labelling shall be developed and implemented in accordance with the information classification scheme.

**Implementation Guidance:**
- Define labelling standards for each classification level (digital headers/footers, email subject tags, physical labels)
- Implement DLP rules that enforce classification labels
- Include labelling requirements in document templates

**Evidence Required:** Labelling policy, DLP configuration, document templates

---

### A.5.14 — Information Transfer
**Description:** Information transfer rules, procedures, or agreements shall be in place for all types of transfer facilities within the organization and between the organization and other parties.

**Implementation Guidance:**
- Establish acceptable file transfer methods (secure email, SFTP, approved file sharing tools)
- Prohibit unauthorized channels (personal email, consumer cloud for sensitive data)
- Include data transfer requirements in supplier agreements

**Evidence Required:** Transfer policy, DLP configuration, supplier agreement clauses

---

### A.5.15 — Access Control
**Description:** Rules to control physical and logical access to information and other associated assets shall be established and implemented based on business and information security requirements.

**Implementation Guidance:**
- Document an Access Control Policy
- Implement Role-Based Access Control (RBAC)
- Apply least privilege principle
- Require quarterly access reviews for privileged accounts

**Evidence Required:** Access control policy, RBAC documentation, access review records

---

### A.5.16 — Identity Management
**Description:** The full life cycle of identities shall be managed.

**Implementation Guidance:**
- Implement centralized identity management (Active Directory, Okta, etc.)
- Automate provisioning/deprovisioning via HR system integration
- Inventory all service accounts and non-human identities
- Disable accounts within 24 hours of termination

**Evidence Required:** IAM system configuration, provisioning workflow, service account register

---

### A.5.17 — Authentication Information
**Description:** Allocation and management of authentication information shall be controlled by a management process, including advising personnel on appropriate handling of authentication information.

**Implementation Guidance:**
- Enforce MFA for all user accounts (phishing-resistant MFA for admin and remote access)
- Implement password policy (minimum length 12+, complexity, no reuse)
- Deploy PAM for privileged account credential management
- Never share authentication credentials

**Evidence Required:** MFA configuration, password policy, PAM deployment records

---

### A.5.18 — Access Rights
**Description:** Access rights to information and other associated assets shall be provisioned, reviewed, modified and removed in accordance with the organization's topic-specific policy on and rules for access control.

**Implementation Guidance:**
- Implement access request and approval workflow
- Conduct quarterly access reviews / user recertification
- Revoke access immediately upon role change or termination
- Log all access rights changes

**Evidence Required:** Access review reports, provisioning workflow, termination audit log

---

### A.5.19 — Information Security in Supplier Relationships
**Description:** Processes and procedures shall be defined and implemented to manage the information security risks associated with the use of supplier's products or services.

**Implementation Guidance:**
- Develop a vendor risk management program
- Tier vendors by criticality (critical/major/standard)
- Complete security assessments before onboarding new critical vendors
- Maintain a vendor register

**Evidence Required:** VRM policy, vendor register, assessment questionnaires

---

### A.5.20 — Addressing IS Within Supplier Agreements
**Description:** Relevant information security requirements shall be established and agreed with each supplier based on the type of supplier relationship.

**Implementation Guidance:**
- Develop a standard security addendum for all supplier contracts
- Include: data handling requirements, incident notification SLAs, right-to-audit, subprocessor disclosure
- Ensure DPAs (Data Processing Agreements) in place for all data processors

**Evidence Required:** Contract security addendum template, signed supplier agreements, DPAs

---

### A.5.21 — Managing IS in the ICT Supply Chain
**Description:** Processes and procedures shall be defined and implemented to manage the information security risks associated with the ICT products and services supply chain.

**Implementation Guidance:**
- Maintain a software bill of materials (SBOM) for critical applications
- Assess open source components for known vulnerabilities
- Evaluate ICT vendors' security practices before acquisition

**Evidence Required:** SBOM, ICT vendor assessment records, procurement security checklist

---

### A.5.22 — Monitoring, Review and Change Management of Supplier Services
**Description:** The organization shall regularly monitor, review, evaluate and manage change in supplier information security practices and service delivery.

**Implementation Guidance:**
- Conduct annual security assessments of critical vendors
- Monitor vendor security posture continuously (e.g., via SecurityScorecard, BitSight)
- Review supplier contracts at renewal for updated security requirements

**Evidence Required:** Annual assessment reports, monitoring platform records, contract renewal notes

---

### A.5.23 🆕 — Information Security for Use of Cloud Services
**Description:** Processes for acquisition, use, management and exit from cloud services shall be defined, in accordance with the organization's information security requirements.

**Implementation Guidance:**
- Establish a Cloud Security Policy
- Assess cloud providers against shared responsibility model
- Implement cloud security posture management (CSPM)
- Define cloud exit procedures to avoid lock-in risk

**Evidence Required:** Cloud security policy, CSPM tool reports, provider assessments

---

### A.5.24 — Information Security Incident Management Planning and Preparation
**Description:** The organization shall plan and prepare for managing information security incidents by defining, establishing and communicating information security incident management processes, roles and responsibilities.

**Implementation Guidance:**
- Develop and approve an Incident Response Plan (IRP)
- Define severity classification criteria
- Establish an incident response team with clear roles
- Test the IRP at least annually via tabletop exercise

**Evidence Required:** IRP document, roles assignment, tabletop exercise report

---

### A.5.25 — Assessment and Decision on Information Security Events
**Description:** The organization shall assess information security events and decide if they are to be categorized as information security incidents.

**Implementation Guidance:**
- Define incident classification criteria (P1/P2/P3/P4)
- Train SOC/help desk on triage procedures
- Document escalation thresholds
- Maintain incident log

**Evidence Required:** Classification criteria, triage procedure, incident log

---

### A.5.26 — Response to Information Security Incidents
**Description:** Information security incidents shall be responded to in accordance with the documented procedures.

**Implementation Guidance:**
- Develop playbooks for common incident types (ransomware, phishing, data breach, DDoS)
- Define containment, eradication, and recovery steps per playbook
- Include legal and communications in the response team

**Evidence Required:** Incident playbooks, response team roster, incident records

---

### A.5.27 — Learning from Information Security Incidents
**Description:** Knowledge gained from information security incidents shall be used to strengthen and improve the information security controls.

**Implementation Guidance:**
- Conduct post-incident reviews (PIRs) for all P1 and P2 incidents
- Track action items from PIRs to completion
- Share lessons learned with relevant teams
- Feed findings back into risk register and training program

**Evidence Required:** PIR reports, action item tracker, updated risk register

---

### A.5.28 — Collection of Evidence
**Description:** The organization shall establish and implement procedures for the identification, collection, acquisition and preservation of evidence related to information security events.

**Implementation Guidance:**
- Document a digital forensics procedure
- Train incident responders on evidence preservation
- Ensure log integrity (tamper-evident logging)
- Maintain chain of custody documentation

**Evidence Required:** Forensics procedure, training records, chain of custody templates

---

### A.5.29 — Information Security During Disruption
**Description:** The organization shall plan how to maintain information security at an appropriate level during disruption.

**Implementation Guidance:**
- Integrate information security requirements into Business Continuity Plans
- Define security controls that must remain active during disruption
- Test security controls in continuity scenarios

**Evidence Required:** BCP with IS requirements, BCM test records

---

### A.5.30 🆕 — ICT Readiness for Business Continuity
**Description:** ICT readiness shall be planned, implemented, maintained and tested based on business continuity objectives and ICT continuity requirements.

**Implementation Guidance:**
- Define RTOs and RPOs for all critical systems
- Implement backup and replication according to RPOs
- Test recovery procedures at least annually
- Document ICT recovery runbooks

**Evidence Required:** RTO/RPO documentation, backup test records, DRP runbooks

---

### A.5.31 — Legal, Statutory, Regulatory and Contractual Requirements
**Description:** Legal, statutory, regulatory and contractual requirements relevant to information security and the organization's approach to meet these requirements shall be identified, documented and kept up to date.

**Implementation Guidance:**
- Maintain a regulatory requirements register
- Map each requirement to ISMS controls
- Assign owners for each regulatory obligation
- Review register semi-annually or on regulatory changes

**Evidence Required:** Regulatory register, control mapping, review records

---

### A.5.32 — Intellectual Property Rights
**Description:** The organization shall implement appropriate procedures to protect intellectual property rights.

**Implementation Guidance:**
- Establish IP policy covering patents, copyrights, and trade secrets
- Enforce software license management
- Include IP clauses in employment and contractor agreements

**Evidence Required:** IP policy, license management records, contract IP clauses

---

### A.5.33 — Protection of Records
**Description:** Records shall be protected from loss, destruction, falsification, unauthorized access and unauthorized release.

**Implementation Guidance:**
- Define retention periods for all record types (consider legal minimums)
- Implement access controls on record repositories
- Ensure backups cover critical records
- Include ISMS records in the retention schedule

**Evidence Required:** Retention policy, access control configuration, backup coverage

---

### A.5.34 — Privacy and Protection of PII
**Description:** The organization shall identify and meet the requirements regarding the preservation of privacy and protection of PII according to applicable laws and regulations.

**Implementation Guidance:**
- Conduct a data protection impact assessment (DPIA) for high-risk processing activities
- Implement privacy by design in product development
- Maintain records of processing activities (RoPA) as required by GDPR
- Appoint a Data Protection Officer (DPO) if required

**Evidence Required:** Privacy policy, RoPA, DPIA records, DPO appointment (if applicable)

---

### A.5.35 — Independent Review of Information Security
**Description:** The organization's approach to managing information security and its implementation shall be reviewed independently at planned intervals or when significant changes occur.

**Implementation Guidance:**
- Establish an internal audit program
- Conduct at least one full ISMS internal audit per year
- Engage external auditor or consultant for independent assessment
- Report findings to management and track to closure

**Evidence Required:** Internal audit program, audit reports, management review minutes

---

### A.5.36 — Compliance with Policies and Procedures
**Description:** Compliance with the organization's information security policy, topic-specific policies and standards shall be regularly reviewed.

**Implementation Guidance:**
- Implement technical compliance monitoring (configuration scanning, policy enforcement)
- Conduct periodic management reviews of compliance status
- Track and remediate non-conformities

**Evidence Required:** Compliance scan reports, management review records, corrective action log

---

### A.5.37 — Documented Operating Procedures
**Description:** Operating procedures for information processing facilities shall be documented and made available to personnel who need them.

**Implementation Guidance:**
- Document runbooks for all critical IT operations
- Store procedures in accessible, version-controlled repository
- Review procedures at least annually and after changes

**Evidence Required:** Runbook library, version control history, review records

---

## A.6 — People Controls

*(See gap analysis and SoA for individual control details — A.6.1 through A.6.8)*

| Control | Title | New in 2022? |
|:---|:---|:---:|
| A.6.1 | Screening | |
| A.6.2 | Terms and conditions of employment | |
| A.6.3 | Information security awareness, education and training | |
| A.6.4 | Disciplinary process | |
| A.6.5 | Responsibilities after termination or change of employment | |
| A.6.6 | Confidentiality or non-disclosure agreements | |
| A.6.7 | Remote working | |
| A.6.8 | Information security event reporting | |

---

## A.7 — Physical Controls

| Control | Title | New in 2022? |
|:---|:---|:---:|
| A.7.1 | Physical security perimeters | |
| A.7.2 | Physical entry | |
| A.7.3 | Securing offices, rooms and facilities | |
| A.7.4 | Physical security monitoring | |
| A.7.5 | Protecting against physical and environmental threats | |
| A.7.6 | Working in secure areas | |
| A.7.7 | Clear desk and clear screen | |
| A.7.8 | Equipment siting and protection | |
| A.7.9 | Security of assets off-premises | |
| A.7.10 | Storage media | |
| A.7.11 | Supporting utilities | |
| A.7.12 | Cabling security | |
| A.7.13 | Equipment maintenance | |
| A.7.14 | Secure disposal or reuse of equipment | |

---

## A.8 — Technological Controls

| Control | Title | New in 2022? |
|:---|:---|:---:|
| A.8.1 | User endpoint devices | |
| A.8.2 | Privileged access rights | |
| A.8.3 | Information access restriction | |
| A.8.4 | Access to source code | |
| A.8.5 | Secure authentication | |
| A.8.6 | Capacity management | |
| A.8.7 | Protection against malware | |
| A.8.8 | Management of technical vulnerabilities | |
| A.8.9 | Configuration management | |
| A.8.10 | Information deletion | 🆕 |
| A.8.11 | Data masking | 🆕 |
| A.8.12 | Data leakage prevention | |
| A.8.13 | Information backup | |
| A.8.14 | Redundancy of information processing facilities | |
| A.8.15 | Logging | |
| A.8.16 | Monitoring activities | |
| A.8.17 | Clock synchronisation | |
| A.8.18 | Use of privileged utility programs | |
| A.8.19 | Installation of software on operational systems | |
| A.8.20 | Networks security | |
| A.8.21 | Security of network services | |
| A.8.22 | Segregation of networks | |
| A.8.23 | Web filtering | 🆕 |
| A.8.24 | Use of cryptography | |
| A.8.25 | Secure development life cycle | |
| A.8.26 | Application security requirements | |
| A.8.27 | Secure system architecture and engineering principles | 🆕 |
| A.8.28 | Secure coding | 🆕 |
| A.8.29 | Security testing in development and acceptance | |
| A.8.30 | Outsourced development | |
| A.8.31 | Separation of development, test and production environments | |
| A.8.32 | Change management | |
| A.8.33 | Test information | 🆕 |
| A.8.34 | Protection of information systems during audit testing | |

---

## New Controls in ISO 27001:2022 (11 total)

| Control | Title | Theme |
|:---|:---|:---:|
| A.5.7 | Threat intelligence | Organizational |
| A.5.23 | IS for use of cloud services | Organizational |
| A.5.30 | ICT readiness for business continuity | Organizational |
| A.7.4 | Physical security monitoring | Physical |
| A.8.9 | Configuration management | Technological |
| A.8.10 | Information deletion | Technological |
| A.8.11 | Data masking | Technological |
| A.8.12 | Data leakage prevention | Technological |
| A.8.16 | Monitoring activities | Technological |
| A.8.23 | Web filtering | Technological |
| A.8.28 | Secure coding | Technological |

---

## References

- ISO/IEC 27001:2022 — Information security, cybersecurity and privacy protection
- ISO/IEC 27002:2022 — Guidance for implementing Annex A controls
- See `statement-of-applicability-template.md` for inclusion/exclusion decisions
- See `iso27001-gap-analysis-template.md` for current implementation status

---

*Standard: ISO/IEC 27001:2022 | Control count: 93 across 4 themes*
