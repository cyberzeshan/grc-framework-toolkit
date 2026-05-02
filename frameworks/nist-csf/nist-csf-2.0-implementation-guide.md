# NIST Cybersecurity Framework 2.0 — Implementation Guide

> **Version:** NIST CSF 2.0 (February 2024)
> **Audience:** Security engineers, GRC professionals, program managers
> **Purpose:** Field-tested implementation roadmap from baseline to Tier 3+

---

## Table of Contents

1. [Overview](#overview)
2. [The Six Functions](#the-six-functions)
3. [Implementation Tiers](#implementation-tiers)
4. [CSF Profiles](#csf-profiles)
5. [Phase-by-Phase Implementation Roadmap](#phase-by-phase-implementation-roadmap)
6. [GOVERN Function (GV)](#govern-function-gv)
7. [IDENTIFY Function (ID)](#identify-function-id)
8. [PROTECT Function (PR)](#protect-function-pr)
9. [DETECT Function (DE)](#detect-function-de)
10. [RESPOND Function (RS)](#respond-function-rs)
11. [RECOVER Function (RC)](#recover-function-rc)
12. [Measurement and Metrics](#measurement-and-metrics)
13. [Common Pitfalls](#common-pitfalls)

---

## Overview

The NIST Cybersecurity Framework 2.0 is a voluntary framework consisting of standards, guidelines, and best practices for managing cybersecurity risk. CSF 2.0 introduces the **GOVERN** function as a sixth pillar, elevating governance and supply chain risk management to first-class concerns.

### What Changed from CSF 1.1 to 2.0

| Area | CSF 1.1 | CSF 2.0 |
|:---|:---|:---|
| Functions | 5 (Identify, Protect, Detect, Respond, Recover) | 6 (adds **Govern**) |
| Audience | Critical infrastructure | All organizations of any size/sector |
| Supply chain | Limited (ID.SC) | Expanded GOVERN subcategories (GV.SC) |
| Implementation guidance | Framework tiers only | Tiers + Quick Start Guides |
| Community profiles | Not included | Organization and sector profiles included |

---

## The Six Functions

| Function | Abbrev. | Core Question | Subcategory Count |
|:---|:---:|:---|:---:|
| **Govern** | GV | How are cybersecurity risks managed organizationally? | 6 categories |
| **Identify** | ID | What assets, risks, and vulnerabilities exist? | 6 categories |
| **Protect** | PR | What safeguards are in place? | 6 categories |
| **Detect** | DE | How are cybersecurity events identified? | 3 categories |
| **Respond** | RS | What actions are taken when an incident occurs? | 5 categories |
| **Recover** | RC | How is resilience restored after an incident? | 3 categories |

### Function Relationships

```
GOVERN (overarches all functions)
    │
    ├── IDENTIFY ──► PROTECT ──► DETECT
    │                               │
    └───────────── RESPOND ◄────────┘
                       │
                   RECOVER
```

---

## Implementation Tiers

Tiers describe the degree to which an organization's cybersecurity risk management practices exhibit characteristics defined in the framework. Tiers are **not maturity levels** — they reflect how cybersecurity risk management is integrated into business decisions.

| Tier | Name | Risk Process | Integrated Risk Program | External Participation |
|:---:|:---|:---|:---|:---|
| **1** | Partial | Ad hoc, reactive, undefined | Not integrated into business | Not aware of sector practices |
| **2** | Risk Informed | Approved but not organization-wide | Aware but not policy-driven | Receives threat intel but doesn't share |
| **3** | Repeatable | Formally approved, consistently applied | Integrated across business units | Actively participates in sharing |
| **4** | Adaptive | Continuously improved, threat-intel driven | Fully integrated, board-level visibility | Leads and contributes to community |

> **Practitioner Note:** Most mid-market organizations start at Tier 1–2. Target Tier 3 before pursuing ISO 27001 or FedRAMP certification. Tier 4 requires a dedicated threat intelligence function and executive-level cybersecurity governance.

---

## CSF Profiles

A **Current Profile** captures the cybersecurity outcomes currently being achieved. A **Target Profile** captures the desired outcomes. The gap between them drives your roadmap.

### Profile Development Steps

1. **Identify organizational requirements** — regulatory, contractual, sector-specific
2. **Assess current state** — which subcategories are fully, partially, or not addressed?
3. **Define target state** — based on risk tolerance, business objectives, and requirements
4. **Gap analysis** — compare current to target; prioritize by risk impact
5. **Implementation roadmap** — sequence gaps into workstreams with owners and timelines

Use the accompanying `csf-profile-template.xlsx` to document current and target profiles.

---

## Phase-by-Phase Implementation Roadmap

### Phase 1: Foundation (Weeks 1–8)
**Goal:** Establish governance structure and asset visibility

- [ ] Appoint CISO or security program owner (GV.OC-01)
- [ ] Document organizational cybersecurity policy (GV.PO-01)
- [ ] Complete hardware and software asset inventory (ID.AM-01, ID.AM-02)
- [ ] Map data flows and data classification (ID.AM-05, ID.AM-07)
- [ ] Identify regulatory and contractual requirements (GV.OC-03)
- [ ] Conduct initial risk assessment (ID.RA-01 through ID.RA-08)
- [ ] Assign roles and responsibilities (GV.RR-01 through GV.RR-04)

**Exit Criteria:** Asset inventory >80% complete; governance policy approved by leadership; initial risk register established.

---

### Phase 2: Risk Management (Weeks 9–16)
**Goal:** Formalize risk management process and prioritize controls

- [ ] Establish risk management strategy (GV.RM-01 through GV.RM-07)
- [ ] Implement access control and identity management (PR.AA-01 through PR.AA-06)
- [ ] Deploy vulnerability management program (ID.RA-01, DE.CM-08)
- [ ] Establish supplier risk management baseline (GV.SC-01 through GV.SC-10)
- [ ] Implement data protection controls (PR.DS-01 through PR.DS-11)
- [ ] Deploy security awareness training (PR.AT-01, PR.AT-02)
- [ ] Establish logging and monitoring baseline (DE.CM-01 through DE.CM-09)

**Exit Criteria:** Risk register with treatment decisions; critical vendor assessments complete; MFA deployed for all privileged access.

---

### Phase 3: Detection & Response (Weeks 17–28)
**Goal:** Build detection capability and formalize incident response

- [ ] Implement SIEM or centralized log management (DE.CM-01, DE.AE-02)
- [ ] Define and test Incident Response Plan (RS.MA-01 through RS.MA-05)
- [ ] Establish incident analysis procedures (RS.AN-01 through RS.AN-08)
- [ ] Implement threat intelligence feeds (ID.RA-04, DE.AE-06)
- [ ] Conduct tabletop exercises (RS.MA-04)
- [ ] Establish business continuity and recovery plans (RC.RP-01, RC.RP-02)
- [ ] Test recovery procedures (RC.RP-03 through RC.RP-06)

**Exit Criteria:** IRP tested and approved; detection coverage for all critical assets; recovery time objectives defined and tested.

---

### Phase 4: Optimization (Ongoing)
**Goal:** Continuous improvement and program maturity

- [ ] Establish cybersecurity metrics and KPIs (GV.OC-05, PR.PS-03)
- [ ] Implement continuous monitoring program
- [ ] Integrate threat intelligence into risk management (GV.RM-05, ID.RA-04)
- [ ] Conduct annual program review with leadership (GV.OV-01 through GV.OV-03)
- [ ] Perform external benchmarking against sector peers
- [ ] Target Tier 3 across all functions

---

## GOVERN Function (GV)

The GOVERN function is new in CSF 2.0. It establishes context for cybersecurity risk decisions across the organization.

### GV.OC — Organizational Context

| Subcategory | Description | Implementation Guidance |
|:---|:---|:---|
| GV.OC-01 | Mission, stakeholders understood | Document org mission; identify internal/external stakeholders |
| GV.OC-02 | Legal/regulatory requirements understood | Map all applicable regulations (GDPR, HIPAA, PCI-DSS, etc.) |
| GV.OC-03 | Critical objectives and capabilities identified | Business impact analysis covering critical services |
| GV.OC-04 | Relationships and dependencies understood | Third-party and supply chain dependency mapping |
| GV.OC-05 | Cybersecurity requirements integrated into strategy | Include cybersecurity in strategic planning cycles |

### GV.RM — Risk Management Strategy

| Subcategory | Description | Implementation Guidance |
|:---|:---|:---|
| GV.RM-01 | Risk management objectives established | Executive-approved risk appetite statement |
| GV.RM-02 | Risk appetite and tolerance determined | Quantified thresholds (e.g., max acceptable annual loss) |
| GV.RM-03 | Cybersecurity risk management integrated into ERM | Joint working group with enterprise risk team |
| GV.RM-04 | Strategic direction communicated | Quarterly briefings to business unit leaders |
| GV.RM-05 | Threats and vulnerabilities fed into risk management | Threat intel integration with risk register |
| GV.RM-06 | Policies establish risk oversight responsibilities | RACI matrix for cybersecurity risk decisions |
| GV.RM-07 | Strategic opportunities considered in risk decisions | Risk-benefit analysis for new technologies |

### GV.RR — Roles, Responsibilities, and Authorities

| Subcategory | Description | Key Artifact |
|:---|:---|:---|
| GV.RR-01 | Leadership accountable for cybersecurity risk | Board resolution or executive charter |
| GV.RR-02 | Roles and responsibilities assigned | RACI matrix, job descriptions |
| GV.RR-03 | Adequate resources allocated | Budget allocation, headcount plan |
| GV.RR-04 | Cybersecurity communicated across organization | Security newsletter, all-hands updates |

### GV.PO — Policy

| Subcategory | Description |
|:---|:---|
| GV.PO-01 | Policy for managing cybersecurity risks established, communicated, and enforced |
| GV.PO-02 | Policy reviewed, updated, communicated, and enforced |

### GV.OV — Oversight

| Subcategory | Description |
|:---|:---|
| GV.OV-01 | Cybersecurity review outcomes inform risk management |
| GV.OV-02 | Cybersecurity strategy reviewed and adjusted |
| GV.OV-03 | Organizational cybersecurity results communicated to stakeholders |

### GV.SC — Cybersecurity Supply Chain Risk Management

| Subcategory | Description | Implementation Guidance |
|:---|:---|:---|
| GV.SC-01 | Supply chain risk management program established | Formal C-SCRM policy and program |
| GV.SC-02 | Suppliers identified, prioritized, and assessed | Vendor tier classification (critical/major/standard) |
| GV.SC-03 | Contracts require cybersecurity requirements | Standard security addendum in all contracts |
| GV.SC-04 | Suppliers routinely assessed | Annual questionnaires + continuous monitoring for critical vendors |
| GV.SC-05 | Response plans for supply chain incidents | Vendor incident notification SLAs in contracts |
| GV.SC-06 | Software integrity verified | SBOM collection and verification for critical software |
| GV.SC-07 | Risks of acquired components understood | Pre-acquisition security assessment |
| GV.SC-08 | Risks of managed services understood | Cloud/SaaS vendor risk assessments |
| GV.SC-09 | Supply chain security requirements in acquisition contracts | RFP security questionnaire template |
| GV.SC-10 | Effectiveness of supply chain risk management reviewed | Annual C-SCRM program review |

---

## IDENTIFY Function (ID)

### ID.AM — Asset Management

| Subcategory | Description | Tool/Method |
|:---|:---|:---|
| ID.AM-01 | Inventories of hardware maintained | CMDB, network discovery (Nmap, Lansweeper) |
| ID.AM-02 | Inventories of software maintained | Software asset management, endpoint agents |
| ID.AM-03 | Inventories of networks and network flows | Network diagrams, flow monitoring |
| ID.AM-04 | Inventories of services maintained | Service catalog, DNS, load balancer configs |
| ID.AM-05 | Assets prioritized by criticality | BIA-based asset criticality tiers |
| ID.AM-07 | Inventories of data and data types maintained | Data classification and data flow mapping |
| ID.AM-08 | Systems, hardware, software, services managed through their life cycle | Asset lifecycle policy from procurement to disposal |

### ID.RA — Risk Assessment

| Subcategory | Description |
|:---|:---|
| ID.RA-01 | Vulnerabilities in assets identified, validated, and recorded |
| ID.RA-02 | Threat intelligence received from forums and sources |
| ID.RA-03 | Internal and external threats identified and recorded |
| ID.RA-04 | Potential impacts and likelihoods of threats considered |
| ID.RA-05 | Threats, vulnerabilities, likelihoods, and impacts used to understand risk |
| ID.RA-06 | Risk responses chosen, prioritized, planned, tracked, and communicated |
| ID.RA-07 | Changes and exceptions are managed |
| ID.RA-08 | Processes for receiving, analyzing, and responding to disclosure are established |
| ID.RA-09 | Software and hardware authenticity verified before use |
| ID.RA-10 | Critical suppliers assessed before contracts signed |

### ID.IM — Improvement

| Subcategory | Description |
|:---|:---|
| ID.IM-01 | Improvements identified from evaluations |
| ID.IM-02 | Improvements identified from security tests and exercises |
| ID.IM-03 | Improvements identified from execution of operational processes |
| ID.IM-04 | Incident response and other responses evaluated and documented |

---

## PROTECT Function (PR)

### PR.AA — Identity Management, Authentication, and Access Control

| Subcategory | Description | Implementation |
|:---|:---|:---|
| PR.AA-01 | User, service, and hardware identities managed | Centralized IAM (Azure AD, Okta, etc.) |
| PR.AA-02 | Identities proofed and bound to credentials appropriately | Identity proofing at onboarding; hardware tokens for privileged accounts |
| PR.AA-03 | Users, services, and hardware authenticated | MFA enforced org-wide; phishing-resistant for critical systems |
| PR.AA-04 | Identity assertions protected | Federation standards (SAML, OIDC); token validation |
| PR.AA-05 | Access permissions and authorizations managed | RBAC; quarterly access reviews; PAM for admin accounts |
| PR.AA-06 | Physical access controlled | Badge access systems; visitor management; data center controls |

### PR.AT — Awareness and Training

| Subcategory | Description |
|:---|:---|
| PR.AT-01 | Personnel are provided with awareness and training so they are responsible for cybersecurity risks |
| PR.AT-02 | Individuals in specialized roles are provided with awareness and training specific to their responsibilities |

### PR.DS — Data Security

| Subcategory | Description |
|:---|:---|
| PR.DS-01 | Data-at-rest are protected |
| PR.DS-02 | Data-in-transit are protected |
| PR.DS-10 | Data-in-use are protected |
| PR.DS-11 | Backups are created, protected, maintained, and tested |

### PR.PS — Platform Security

| Subcategory | Description |
|:---|:---|
| PR.PS-01 | Configuration management practices are established and applied |
| PR.PS-02 | Software is maintained, replaced, and removed commensurate with risk |
| PR.PS-03 | Hardware is maintained, replaced, and removed commensurate with risk |
| PR.PS-04 | Log records are generated and made available for continuous monitoring |
| PR.PS-05 | Installation and execution of unauthorized software is prevented |
| PR.PS-06 | Secure software development practices are integrated |

### PR.IR — Technology Infrastructure Resilience

| Subcategory | Description |
|:---|:---|
| PR.IR-01 | Networks and environments are protected from unauthorized logical access |
| PR.IR-02 | The organization's technology assets are protected from environmental threats |
| PR.IR-03 | Mechanisms are implemented to achieve resilience requirements in normal and adverse situations |
| PR.IR-04 | Adequate resource capacity is ensured |

---

## DETECT Function (DE)

### DE.CM — Continuous Monitoring

| Subcategory | Description | Tool Examples |
|:---|:---|:---|
| DE.CM-01 | Networks and network services monitored | SIEM, IDS/IPS, NDR |
| DE.CM-02 | Physical environment monitored | CCTV, badge access logs, environmental sensors |
| DE.CM-03 | Personnel activity and technology usage monitored | DLP, UBA, endpoint agents |
| DE.CM-06 | External service provider activities monitored | Cloud access monitoring, CASB |
| DE.CM-09 | Computing hardware and software monitored | EDR, patch compliance dashboards |

### DE.AE — Adverse Event Analysis

| Subcategory | Description |
|:---|:---|
| DE.AE-02 | Potentially adverse events are analyzed to better characterize them |
| DE.AE-03 | Information is correlated from multiple sources |
| DE.AE-04 | Estimated impact and scope of adverse events are understood |
| DE.AE-06 | Information on adverse events is provided to authorized staff and tools |
| DE.AE-07 | Cyber threat intelligence is integrated into the analysis |
| DE.AE-08 | Incidents are declared when adverse events meet defined criteria |

---

## RESPOND Function (RS)

### RS.MA — Incident Management

| Subcategory | Description |
|:---|:---|
| RS.MA-01 | Incident response plan exists and is executable |
| RS.MA-02 | Incident reports are triaged and validated |
| RS.MA-03 | Incidents are categorized and prioritized |
| RS.MA-04 | Incidents are escalated or elevated as needed |
| RS.MA-05 | Incidents are declared contained after adequate analysis |

### RS.AN — Incident Analysis

| Subcategory | Description |
|:---|:---|
| RS.AN-03 | Analysis is performed to establish what has taken place during an incident |
| RS.AN-06 | Actions performed during an investigation are recorded |
| RS.AN-07 | Incident data and metadata are collected |
| RS.AN-08 | An incident's magnitude is estimated and validated |

### RS.CO — Incident Response Reporting and Communication

| Subcategory | Description |
|:---|:---|
| RS.CO-02 | Internal and external stakeholders are notified of incidents |
| RS.CO-03 | Information is shared with designated internal and external stakeholders |

### RS.MI — Incident Mitigation

| Subcategory | Description |
|:---|:---|
| RS.MI-01 | Incidents are contained |
| RS.MI-02 | Incidents are eradicated |

---

## RECOVER Function (RC)

### RC.RP — Incident Recovery Plan Execution

| Subcategory | Description |
|:---|:---|
| RC.RP-01 | Recovery portion of incident response plan is executed |
| RC.RP-02 | Recovery actions are selected, scoped, prioritized, and performed |
| RC.RP-03 | Completeness of recovery is confirmed and documented |
| RC.RP-04 | Public relations and reputation strategies are applied |
| RC.RP-05 | Recovery activities end when criteria are met |
| RC.RP-06 | Lessons learned are incorporated into recovery planning |

### RC.CO — Incident Recovery Communication

| Subcategory | Description |
|:---|:---|
| RC.CO-03 | Recovery activities and progress are communicated to stakeholders |
| RC.CO-04 | Public updates on recovery are shared using approved methods |

---

## Measurement and Metrics

### Tier Progression Metrics

| Metric | Tier 1 → 2 | Tier 2 → 3 | Tier 3 → 4 |
|:---|:---|:---|:---|
| Asset inventory coverage | <50% → 75% | 75% → 95% | 95% → 100% + automated |
| Risk assessment frequency | Ad hoc → Annual | Annual → Quarterly | Quarterly → Continuous |
| Patch cadence (critical) | >90 days → 30 days | 30 days → 14 days | 14 days → <7 days |
| IRP test frequency | Never → Annual tabletop | Annual tabletop → Semi-annual | Semi-annual → Quarterly + red team |
| Security training completion | <50% → 80% | 80% → 95% | 95% + role-specific |
| Mean Time to Detect (MTTD) | Unknown → <30 days | <30 days → <72 hours | <72 hours → <1 hour |
| Vendor assessments | Ad hoc → Tier 1 only | Tier 1+2 → All critical | All vendors + continuous monitoring |

---

## Common Pitfalls

1. **Treating tiers as maturity levels.** Tiers measure integration of risk management into business decisions — not control completeness. An organization can be Tier 4 on Govern and Tier 1 on Detect.

2. **Starting with controls instead of risk.** The CSF is risk-driven. Start with ID.RA before implementing PR controls, or you'll spend money on controls that don't address your actual risks.

3. **Skipping the Profile exercise.** Without a documented Current and Target Profile, you have no baseline and no roadmap. The Profile is the work product — the framework is just the structure.

4. **Ignoring GV.SC (supply chain).** Third-party risk is the #1 attack vector for mid-market organizations. Don't defer supply chain risk management until "Phase 2."

5. **One-and-done assessments.** The framework expects continuous improvement. An annual point-in-time assessment is insufficient for Tier 3+.

6. **Confusing CSF with a compliance checklist.** CSF is a risk management framework, not a certification program. Organizations seeking certifications should use CSF alongside ISO 27001 or NIST 800-53 — see `csf-to-iso27001-mapping.md`.

---

## References

- [NIST CSF 2.0 Core](https://www.nist.gov/cyberframework)
- [NIST SP 800-53 Rev 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) — Control catalog aligned to CSF
- [NIST IR 8286](https://csrc.nist.gov/publications/detail/nistir/8286/final) — Integrating CSF with ERM
- [CSF 2.0 Quick Start Guides](https://www.nist.gov/cyberframework/getting-started) — Sector-specific guidance
- Cross-framework mapping: see `csf-to-iso27001-mapping.md` and `../cross-framework/master-control-mapping.md`
