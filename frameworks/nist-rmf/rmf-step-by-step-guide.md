# NIST Risk Management Framework — Step-by-Step Guide

> **Framework:** NIST Risk Management Framework (RMF)
> **Key References:** NIST SP 800-37 Rev 2 | NIST SP 800-53 Rev 5 | NIST SP 800-53A Rev 5
> **Audience:** Security engineers, ISSOs, ISSMs, Authorization Officials, program managers building federal or federal-adjacent security programs
> **Purpose:** Practical implementation guide for all 7 RMF steps, with required artifacts for each

---

## Overview

The NIST Risk Management Framework (RMF) is a structured process for integrating security, privacy, and supply chain risk management activities into the system development life cycle. It is **mandatory** for federal information systems under FISMA and is widely adopted by federal contractors, DoD contractors, and organizations seeking FedRAMP authorization.

### The 7 RMF Steps

```
PREPARE → CATEGORIZE → SELECT → IMPLEMENT → ASSESS → AUTHORIZE → MONITOR
    ↑                                                                  │
    └──────────────────────────────────────────────────────────────────┘
                         (Continuous Monitoring Loop)
```

---

## RMF Roles Reference

| Role | Abbreviation | Responsibility |
|:---|:---:|:---|
| Authorizing Official | AO | Accepts risk; issues Authorization to Operate (ATO) |
| Senior Agency Information Security Officer | SAISO | Organization-wide security program oversight |
| Information System Security Officer | ISSO | Day-to-day security for a specific system |
| Information System Security Manager | ISSM | Oversight of ISSOs; program-level security |
| System Owner | SO | Accountability for system operation and security |
| Common Control Provider | CCP | Provides and maintains inherited controls |
| Security Control Assessor | SCA | Independent assessment of controls |
| Senior Agency Official for Privacy | SAOP | Privacy risk management oversight |

---

## Step 0: PREPARE

> **Purpose:** Establish organizational- and system-level context before beginning the RMF lifecycle
> **SP 800-37 Reference:** Chapter 2

The PREPARE step was added in RMF Rev 2 to address gaps in organizational readiness. Many organizations skip this step — that is a mistake.

### Organization-Level Prepare Tasks

| Task | Description | Key Output |
|:---|:---|:---|
| P-1 | Assign key RMF roles (AO, SAISO, ISSM, ISSO) | Role assignment memo |
| P-2 | Establish a risk management strategy | Risk management strategy document |
| P-3 | Conduct organization risk assessment | Organization-level risk assessment |
| P-4 | Establish organization-wide tailoring criteria | Tailoring guidance document |
| P-5 | Identify common controls and CSPs | Common control register |
| P-6 | Develop organization-wide monitoring strategy | Continuous monitoring strategy |

### System-Level Prepare Tasks

| Task | Description | Key Output |
|:---|:---|:---|
| P-7 | Identify key stakeholders for the system | Stakeholder identification memo |
| P-8 | Describe the system | System description (for SSP Section 1) |
| P-9 | Register the system with the organization | System registration in ISSO tracker |
| P-10 | Allocate security and privacy requirements | Requirements allocation table |
| P-11 | Establish information life cycle for the system | Data lifecycle documentation |
| P-12 | Select ISSO and authorize development | ISSO appointment letter |
| P-13 | Identify authorizing officials | AO designation letter |
| P-14 | Determine authorization boundary | Authorization boundary diagram |
| P-15 | Identify system elements within the boundary | System component inventory |
| P-16 | Determine authorization type | New ATO vs. reauthorization determination |
| P-17 | Identify stakeholders' security and privacy requirements | Requirements register |
| P-18 | Determine placement within enterprise architecture | EA placement memo |
| P-19 | Conduct system risk assessment | Initial system risk assessment |

---

## Step 1: CATEGORIZE

> **Purpose:** Categorize the system and information based on impact level
> **SP 800-37 Reference:** Chapter 3, Task C-1 through C-3
> **Key Standard:** FIPS 199 | NIST SP 800-60 Vol 1 & 2

### Impact Levels (FIPS 199)

| Impact Level | Description | Examples |
|:---:|:---|:---|
| **Low** | Limited adverse effect on operations, assets, or individuals | Internal administrative systems, low-sensitivity data |
| **Moderate** | Serious adverse effect | Most government systems; PII in limited scope |
| **High** | Severe or catastrophic adverse effect | National security systems; life-safety systems; large-scale PII |

### Security Objectives

| Objective | Question | FIPS 199 Definition |
|:---|:---|:---|
| **Confidentiality** | What is the impact if unauthorized disclosure occurs? | Preserving authorized restrictions on information access |
| **Integrity** | What is the impact if information is modified or destroyed? | Guarding against improper modification or destruction |
| **Availability** | What is the impact if access or use is disrupted? | Ensuring timely and reliable access to and use of information |

### Categorization Formula

```
SC(system) = {(confidentiality, impact), (integrity, impact), (availability, impact)}

Overall System Categorization = HIGH WATER MARK of all three security objectives
```

**Example:**
```
SC(HR System) = {(confidentiality, Moderate), (integrity, Low), (availability, Moderate)}
Overall Categorization: MODERATE
```

### Step 1 Required Artifacts

| Artifact | Description | Template |
|:---|:---|:---|
| FIPS 199 Categorization | Formal categorization for C, I, A | SSP Section 2 |
| SP 800-60 mapping | Information type mapping to impact levels | NIST SP 800-60 Vol 2 appendices |
| System Security Plan (SSP) — Section 1–4 | System identification, categorization, boundary | `system-security-plan-template.md` |
| AO review of categorization | AO concurrence with categorization | Signed categorization review memo |

---

## Step 2: SELECT

> **Purpose:** Select an initial set of controls from NIST SP 800-53 Rev 5
> **SP 800-37 Reference:** Chapter 3, Task S-1 through S-5

### Control Baseline Selection

| System Impact Level | Initial Baseline |
|:---:|:---|
| Low | SP 800-53 Low Baseline (~125 controls) |
| Moderate | SP 800-53 Moderate Baseline (~325 controls) |
| High | SP 800-53 High Baseline (~420 controls) |

### Tailoring Process

Tailoring allows organizations to adjust the baseline to their specific environment. **Tailoring steps:**

1. **Scoping** — Apply scoping considerations to remove controls not applicable to the system environment (e.g., no physical media → remove MA-8 if fully cloud-hosted)
2. **Parameterization** — Set organization-defined values for control parameters (e.g., minimum password length = 15 characters)
3. **Compensating controls** — When a required control cannot be implemented, define compensating controls that provide equivalent protection
4. **Supplementation** — Add controls beyond the baseline to address specific risks

### Control Allocation

| Control Type | Description | Example |
|:---|:---|:---|
| **System-specific** | Implemented by the system owner for that system only | Application-specific encryption |
| **Hybrid** | Partially system-specific, partially common | Audit logging (system provides logs; SIEM is common) |
| **Common (Inherited)** | Provided by the organization; inherited by multiple systems | Physical security, HR policies, network perimeter |

### Step 2 Required Artifacts

| Artifact | Description |
|:---|:---|
| Control selection worksheet | SP 800-53 baseline with scoping decisions documented |
| Tailoring justification | Written rationale for each control removed or modified |
| Control allocation table | System-specific vs. hybrid vs. inherited designation per control |
| SSP control descriptions | SSP Sections 13–15: control implementation descriptions |

---

## Step 3: IMPLEMENT

> **Purpose:** Implement the security and privacy controls and document the implementation
> **SP 800-37 Reference:** Chapter 3, Task I-1 through I-2

### Implementation Guidance

- For each selected control, document **how** it is implemented (not just **that** it is implemented)
- Reference specific system components, configurations, or tools
- Document who is responsible for maintaining the control
- Include evidence artifacts that will support the assessment

### Control Implementation Documentation (for SSP)

Each control in the SSP should address:

1. **Control Statement** — The full NIST SP 800-53 Rev 5 control text
2. **Implementation Description** — How this control is implemented for this specific system
3. **Control Origin** — System-specific / hybrid / inherited
4. **Responsible Role** — Who owns this control implementation
5. **Evidence** — What artifacts exist to demonstrate implementation

**Example — AC-2 Account Management:**
```
Implementation: User accounts for [System Name] are managed through Active Directory.
Account creation requires approval from the System Owner and is processed by the IT
Help Desk within 24 hours of request. Accounts are reviewed quarterly by the ISSO
using the AD user report. Accounts are disabled within 4 hours of termination notice
from HR. Service accounts are approved by the ISSO and reviewed annually.

Control Origin: Hybrid (AD managed centrally; application-level roles are system-specific)
Responsible Role: ISSO / Help Desk
Evidence: AD account audit report, quarterly review records, HR-IT offboarding SLA
```

### Step 3 Required Artifacts

| Artifact | Description |
|:---|:---|
| Completed SSP | All control descriptions populated with implementation details |
| Configuration baselines | System-specific hardening guides and configuration documentation |
| Plan of Action & Milestones (POA&M) — draft | Initial list of controls not yet fully implemented |
| Supporting policies and procedures | Referenced policies must exist and be current |

---

## Step 4: ASSESS

> **Purpose:** Determine if the controls are implemented correctly, operating as intended, and producing the desired outcome
> **SP 800-37 Reference:** Chapter 3, Task A-1 through A-5
> **Key Reference:** NIST SP 800-53A Rev 5 — Assessment Procedures

### Assessment Methods

| Method | Description | When Used |
|:---|:---|:---|
| **Examine** | Review, inspect, and analyze documents, mechanisms, configurations | All controls |
| **Interview** | Discuss implementation with system owners, administrators, users | Process controls, policy compliance |
| **Test** | Exercise control and observe behavior | Technical controls, automated mechanisms |

### Security Assessment Plan (SAP)

The SAP documents what will be assessed, how, and by whom. Required before assessment begins.

See `security-assessment-plan-template.md` for the full template.

**SAP must include:**
- System name, categorization, and ATO boundary
- Assessment scope and objectives
- Assessment team composition and independence
- Schedule and assessment procedures for each control
- Rules of engagement for any testing

### Security Assessment Report (SAR)

The SAR documents assessment findings and is the primary input to the authorization decision.

**SAR structure:**
1. Executive Summary
2. Assessment Methodology
3. Control Assessment Results (per-control findings)
4. Summary of Findings
5. Risks and Recommendations
6. Assessor Certification

### Finding Classifications

| Classification | Description | SSP/POA&M Action |
|:---|:---|:---|
| **Satisfied** | Control implemented correctly and operating as intended | No action required |
| **Other than Satisfied** | Control not implemented or implemented with deficiencies | POA&M entry required |

### Step 4 Required Artifacts

| Artifact | Description |
|:---|:---|
| Security Assessment Plan (SAP) | Approved before assessment begins |
| Security Assessment Report (SAR) | Assessment findings, per-control results |
| Updated POA&M | All OtS findings documented with remediation plan |
| Evidence packages | Supporting evidence for each assessed control |

---

## Step 5: AUTHORIZE

> **Purpose:** Provide organizational accountability by requiring a senior official to determine if the risk of operating the system is acceptable
> **SP 800-37 Reference:** Chapter 3, Task R-1 through R-5

### Authorization Decision Types

| Decision | Description |
|:---|:---|
| **Authorization to Operate (ATO)** | System is authorized to operate; risk accepted by AO |
| **Common Control Authorization (CCA)** | Common controls are authorized; available for inheritance |
| **Authorization to Use (ATU)** | System authorized to use external service (e.g., FedRAMP CSP) |
| **Denial of Authorization to Operate (DATO)** | AO determines risk is unacceptable; operation denied |

### Authorization Package

The AO reviews the authorization package and makes the risk acceptance decision.

**Authorization Package contents:**
1. System Security Plan (SSP) — final, approved
2. Security Assessment Report (SAR)
3. Plan of Action & Milestones (POA&M)
4. Executive Summary (Risk Executive Summary)

### Authorization Decision Factors

The AO considers:
- Security categorization
- Overall control effectiveness (from SAR)
- Residual risk (unmitigated risks remaining)
- POA&M completeness and remediation timeline
- Mission/business impact of not operating the system

### ATO Term

- Standard ATO: **3 years** (subject to continuous monitoring)
- ATO may be revoked at any time if significant risk is introduced

### Step 5 Required Artifacts

| Artifact | Description |
|:---|:---|
| Authorization package | SSP + SAR + POA&M compiled for AO review |
| Risk Executive Summary | 1–2 page summary of residual risk for AO |
| ATO letter | Signed by AO; specifies authorization boundary and term |
| POA&M with milestones | Approved plan to remediate outstanding findings |

---

## Step 6: MONITOR

> **Purpose:** Maintain ongoing situational awareness about security and privacy posture through continuous monitoring
> **SP 800-37 Reference:** Chapter 3, Task M-1 through M-7

### Continuous Monitoring Components

| Component | Description | Frequency |
|:---|:---|:---|
| Vulnerability scanning | Automated scanning of system components | Weekly (minimum) |
| Configuration compliance | Automated drift detection against baselines | Continuous or weekly |
| Security control assessments | Periodic review of selected controls | Annual or on change |
| Patch management | Track and apply patches per SLA | Monthly (critical: 15 days) |
| Incident tracking | Active incident monitoring and reporting | Continuous |
| POA&M tracking | Progress tracking on open findings | Monthly |
| AO reporting | Security status report to AO | Monthly |

### Significant Change Determination

A **significant change** may trigger partial or full reassessment. Common triggers:
- Adding new functionality that changes the threat surface
- Changing system interconnections
- Moving to a new hosting environment
- Change in categorization (information type changes)
- Major architectural changes
- Significant security incidents

### Annual Assessment Requirements

Not all controls need annual assessment. The monitoring strategy defines which controls are assessed and at what frequency:

| Control Group | Typical Frequency |
|:---|:---|
| High-impact controls (AC, IA, AU, SC) | Annual |
| Configuration controls (CM, SA) | Semi-annual or continuous |
| Personnel controls (PS, AT) | Annual |
| Physical controls (PE) | Annual or on facility change |
| Low-impact controls | Every 3 years |

### Step 6 Required Artifacts

| Artifact | Description | Frequency |
|:---|:---|:---|
| Continuous monitoring plan | Documents what is monitored, how, and how often | Established at ATO |
| Monthly status report | Security posture summary for AO | Monthly |
| POA&M updates | Progress on open items; new findings | Monthly |
| Annual assessment report | Updated SAR for controls assessed in the year | Annual |
| Significant change determination | Documented analysis of whether change triggers reassessment | Per change |
| ATO reauthorization package | Full authorization package every 3 years (or sooner if major changes) | Every 3 years |

---

## RMF Timeline Reference

| Phase | Typical Duration | Key Milestone |
|:---|:---|:---|
| Prepare | 2–4 weeks | Roles assigned, boundary defined |
| Categorize | 1–2 weeks | Categorization approved by AO |
| Select | 2–4 weeks | SSP control sections populated |
| Implement | 3–9 months | All controls implemented; SSP complete |
| Assess | 4–8 weeks | SAR delivered |
| Authorize | 2–4 weeks | ATO letter issued |
| Monitor | Ongoing (3-year cycle) | Monthly status reports |

> **Total time to initial ATO:** Typically 6–18 months depending on system complexity and ISSO experience

---

## Common RMF Failure Points

1. **Incomplete boundary definition** — Assessors will find orphaned system components. Define the boundary precisely before categorization.

2. **SSP written for compliance, not accuracy** — Generic copy-paste control descriptions fail assessment. Each control must describe the specific implementation.

3. **POA&M as a parking lot** — POA&Ms with items open for 2+ years without progress signal management inattention. AOs may rescind ATOs for stale POA&Ms.

4. **Skipping the Prepare step** — Starting at Categorize without the organizational preparation work causes role confusion and delays.

5. **Independence failures in assessment** — The SCA must be independent from the system development team. ISSO cannot assess their own controls.

6. **Treating ATO as the finish line** — Authorization is the beginning of a continuous monitoring obligation, not the end of the security journey.

---

## References

- [NIST SP 800-37 Rev 2 — RMF for Information Systems and Organizations](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final)
- [NIST SP 800-53 Rev 5 — Security and Privacy Controls](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
- [NIST SP 800-53A Rev 5 — Assessment Procedures](https://csrc.nist.gov/publications/detail/sp/800-53a/rev-5/final)
- [FIPS 199 — Standards for Security Categorization](https://csrc.nist.gov/publications/detail/fips/199/final)
- [NIST SP 800-60 — Guide for Mapping Types of Information to Security Categories](https://csrc.nist.gov/publications/detail/sp/800-60/vol-1-rev-1/final)
- Templates: `system-security-plan-template.md` | `security-assessment-plan-template.md`
