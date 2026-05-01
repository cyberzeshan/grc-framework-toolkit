# 🔧 GRC Framework Toolkit

<div align="center">

![NIST](https://img.shields.io/badge/NIST_CSF_2.0-003087?style=flat-square&logoColor=white)
![ISO27001](https://img.shields.io/badge/ISO_27001%3A2022-0066CC?style=flat-square&logoColor=white)
![FedRAMP](https://img.shields.io/badge/FedRAMP-003366?style=flat-square&logoColor=white)
![NIST RMF](https://img.shields.io/badge/NIST_RMF-003087?style=flat-square&logoColor=white)
![CIS](https://img.shields.io/badge/CIS_Controls_v8-00A86B?style=flat-square&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**A practitioner's implementation library for enterprise GRC frameworks — designed for security engineers, compliance professionals, and program managers building production-grade security programs.**

</div>

---

## 📖 Overview

The **GRC Framework Toolkit** provides opinionated, field-tested implementation resources for the most widely adopted cybersecurity governance frameworks. Every artifact in this repository has been developed from real-world implementation experience and is designed to be immediately usable — not theoretical.

This is not a summary of what frameworks say. This is **how to actually implement them.**

---

## 📂 Repository Structure

```
grc-framework-toolkit/
│
├── frameworks/
│   ├── nist-csf/
│   │   ├── nist-csf-2.0-implementation-guide.md       # Full implementation roadmap
│   │   ├── csf-profile-template.xlsx                   # Current & Target profile worksheet
│   │   ├── csf-tier-assessment.md                      # Tier 1–4 self-assessment tool
│   │   └── csf-to-iso27001-mapping.md                  # Cross-framework control mapping
│   │
│   ├── iso-27001/
│   │   ├── iso27001-gap-analysis-template.md           # Clause-by-clause gap analysis
│   │   ├── isms-scope-statement-template.md            # Scope & boundary definition
│   │   ├── statement-of-applicability-template.md      # SoA with justification fields
│   │   └── annex-a-control-register.md                 # All 93 Annex A controls mapped
│   │
│   ├── nist-rmf/
│   │   ├── rmf-step-by-step-guide.md                   # All 7 RMF steps with artifacts
│   │   ├── system-security-plan-template.md            # SSP template (NIST SP 800-18)
│   │   └── security-assessment-plan-template.md        # SAP template (NIST SP 800-53A)
│   │
│   ├── cis-controls/
│   │   ├── cis-v8-implementation-guide.md              # IG1/IG2/IG3 prioritization
│   │   └── cis-benchmark-checklist.md                  # Hardening verification checklist
│   │
│   └── cross-framework/
│       ├── master-control-mapping.md                   # NIST ↔ ISO ↔ CIS ↔ SOC 2 mapping
│       └── regulatory-overlap-analysis.md              # Efficiency matrix for multi-framework
│
├── templates/
│   ├── program-charter-template.md
│   ├── risk-acceptance-form.md
│   └── exception-request-template.md
│
└── guides/
    ├── grc-program-maturity-model.md
    └── board-reporting-template.md
```

---

## 🚀 Quick Start

### Starting a NIST CSF Implementation

1. **Assess Current State** — Run the [CSF Tier Assessment](frameworks/nist-csf/csf-tier-assessment.md) to establish your baseline maturity
2. **Define Target Profile** — Use the [CSF Profile Template](frameworks/nist-csf/csf-profile-template.xlsx) to set outcome priorities by function
3. **Identify Gaps** — Compare current vs. target profiles to produce a prioritized gap list
4. **Map to Controls** — Use the [Master Control Mapping](frameworks/cross-framework/master-control-mapping.md) to identify which controls address each gap
5. **Build Roadmap** — Sequence remediation by risk priority and implementation effort

### Starting an ISO 27001 Certification

1. **Define Scope** — Complete the [ISMS Scope Statement](frameworks/iso-27001/isms-scope-statement-template.md)
2. **Perform Gap Analysis** — Run the [Clause-by-Clause Gap Analysis](frameworks/iso-27001/iso27001-gap-analysis-template.md)
3. **Complete the SoA** — Populate the [Statement of Applicability](frameworks/iso-27001/statement-of-applicability-template.md) with all 93 Annex A controls
4. **Address Mandatory Clauses** — Clauses 4–10 are non-negotiable for certification
5. **Engage a Certification Body** — Prepare documentation for Stage 1 (document review) and Stage 2 (implementation audit)

---

## 📋 NIST CSF 2.0 — Implementation Guide (Excerpt)

### The Six Functions

| Function | Abbreviation | Core Question |
|:---|:---:|:---|
| **Govern** | GV | How are cybersecurity risks managed organizationally? |
| **Identify** | ID | What assets, risks, and vulnerabilities exist? |
| **Protect** | PR | What safeguards are in place? |
| **Detect** | DE | How are cybersecurity events identified? |
| **Respond** | RS | What actions are taken when an incident occurs? |
| **Recover** | RC | How is resilience restored after an incident? |

### Implementation Tiers

| Tier | Name | Description |
|:---:|:---|:---|
| 1 | **Partial** | Risk practices are ad hoc, reactive, and not formalized |
| 2 | **Risk Informed** | Risk awareness exists but is not organization-wide |
| 3 | **Repeatable** | Risk practices are formally approved and consistently applied |
| 4 | **Adaptive** | Risk practices are continuously improved based on lessons learned and threat intelligence |

> **Practitioner Note:** Most mid-market enterprises begin at Tier 1–2. Target Tier 3 before pursuing certifications. Tier 4 is the domain of mature security programs with dedicated threat intelligence functions.

---

## 📋 ISO 27001:2022 — Gap Analysis Template (Excerpt)

### Mandatory Clauses Assessment

| Clause | Requirement | Status | Evidence | Gap | Priority |
|:---|:---|:---:|:---|:---|:---:|
| 4.1 | Understanding the organization and its context | 🔴 Not Started | — | Context not documented | High |
| 4.2 | Understanding needs and expectations of interested parties | 🔴 Not Started | — | Stakeholder register missing | High |
| 4.3 | Determining the scope of the ISMS | 🟡 In Progress | Draft scope doc | Needs formal approval | High |
| 5.1 | Leadership and commitment | 🔴 Not Started | — | No ISMS policy signed by top management | Critical |
| 5.2 | Policy | 🔴 Not Started | — | ISMS policy not established | Critical |
| 5.3 | Organizational roles, responsibilities and authorities | 🟡 In Progress | Org chart | ISMS roles not formally assigned | High |
| 6.1 | Actions to address risks and opportunities | 🔴 Not Started | — | Risk treatment plan not established | Critical |
| 6.2 | Information security objectives | 🔴 Not Started | — | No measurable security objectives | High |
| 7.1 | Resources | 🟢 Compliant | Budget allocated | — | — |
| 7.2 | Competence | 🟡 In Progress | Training records partial | Competence framework needed | Medium |
| 9.1 | Monitoring, measurement, analysis and evaluation | 🔴 Not Started | — | No KPIs or metrics program | High |
| 9.2 | Internal audit | 🔴 Not Started | — | Internal audit program not established | Critical |
| 9.3 | Management review | 🔴 Not Started | — | No review cycle defined | High |
| 10.1 | Continual improvement | 🔴 Not Started | — | No improvement process | Medium |

**Status Legend:** 🔴 Not Started &nbsp;|&nbsp; 🟡 In Progress &nbsp;|&nbsp; 🟢 Compliant &nbsp;|&nbsp; ⚫ Not Applicable

---

## 🗺️ Cross-Framework Control Mapping (Sample)

| Control Domain | NIST CSF 2.0 | ISO 27001:2022 | CIS Controls v8 | SOC 2 TSC |
|:---|:---|:---|:---|:---|
| Asset Inventory | ID.AM-01, ID.AM-02 | A.5.9, A.5.10 | CIS 1.1, 1.2 | CC6.1 |
| Access Control | PR.AA-01 to PR.AA-06 | A.5.15–A.5.18 | CIS 5, 6 | CC6.1, CC6.2, CC6.3 |
| Vulnerability Management | ID.RA-01, DE.CM-08 | A.8.8 | CIS 7 | CC7.1 |
| Incident Response | RS.MA-01 to RS.MA-05 | A.5.24–A.5.28 | CIS 17 | CC7.3, CC7.4, CC7.5 |
| Encryption | PR.DS-01, PR.DS-02 | A.8.24 | CIS 3.11 | CC6.7 |
| Security Awareness | PR.AT-01, PR.AT-02 | A.6.3 | CIS 14 | CC2.2 |
| Logging & Monitoring | DE.CM-01 to DE.CM-09 | A.8.15, A.8.16 | CIS 8 | CC7.2 |
| Supplier Risk | GV.SC-01 to GV.SC-10 | A.5.19–A.5.22 | CIS 15 | CC9.2 |

---

## 📚 References

- [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework)
- [NIST SP 800-53 Rev 5 — Security and Privacy Controls](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
- [ISO/IEC 27001:2022](https://www.iso.org/standard/82875.html)
- [CIS Controls v8](https://www.cisecurity.org/controls/v8)
- [NIST Risk Management Framework](https://csrc.nist.gov/projects/risk-management)

---

## 📄 License

MIT License — free to use, adapt, and distribute with attribution.

---

<div align="center">
<i>Built by <a href="https://github.com/cyberzeshan">Zeshan Ahmad</a> · GRC Engineer & Cybersecurity SME</i>
</div>
