# CSF Tier Self-Assessment Tool

> **Framework:** NIST Cybersecurity Framework 2.0
> **Purpose:** Establish current-state tier rating across all six CSF functions
> **Instructions:** Score each statement 1–4 using the scale below. Average scores per function to determine function-level tier. The lowest function tier is your overall program tier.

---

## Scoring Scale

| Score | Tier | Label | Description |
|:---:|:---:|:---|:---|
| **1** | Tier 1 | Partial | Practice is ad hoc, reactive, or not formalized |
| **2** | Tier 2 | Risk Informed | Practice is defined but not consistently applied org-wide |
| **3** | Tier 3 | Repeatable | Practice is formally approved, documented, and consistently applied |
| **4** | Tier 4 | Adaptive | Practice is continuously improved based on lessons learned and threat intel |

---

## Assessment Worksheet

**Organization:** ___________________________________
**Assessment Date:** ___________________________________
**Assessed By:** ___________________________________
**Review Cycle:** ___________________________________

---

## Function 1: GOVERN (GV)

*Governance establishes organizational context for cybersecurity risk management decisions.*

| # | Assessment Statement | Score (1–4) | Evidence / Notes |
|:---:|:---|:---:|:---|
| GV-1 | We have a documented cybersecurity policy approved by leadership | | |
| GV-2 | Cybersecurity roles and responsibilities are formally assigned with a RACI or equivalent | | |
| GV-3 | We have a documented and board-approved risk appetite statement | | |
| GV-4 | Cybersecurity risk is integrated into enterprise risk management processes | | |
| GV-5 | Legal, regulatory, and contractual cybersecurity requirements are identified and tracked | | |
| GV-6 | We have a formal supply chain / third-party risk management program | | |
| GV-7 | Critical suppliers are assessed and monitored on a defined schedule | | |
| GV-8 | Leadership receives regular cybersecurity performance reporting | | |
| GV-9 | Cybersecurity improvements are identified, tracked, and acted upon | | |
| GV-10 | The cybersecurity program is reviewed and updated at least annually | | |

**GV Total Score:** _____ / 40 &nbsp;&nbsp; **GV Average (÷10):** _____ &nbsp;&nbsp; **GV Tier (round down):** _____

---

## Function 2: IDENTIFY (ID)

*Identify establishes understanding of assets, risks, and vulnerabilities.*

| # | Assessment Statement | Score (1–4) | Evidence / Notes |
|:---:|:---|:---:|:---|
| ID-1 | We maintain a current hardware asset inventory (>90% coverage) | | |
| ID-2 | We maintain a current software asset inventory (>90% coverage) | | |
| ID-3 | Data assets are inventoried and classified by sensitivity | | |
| ID-4 | Assets are prioritized by business criticality | | |
| ID-5 | Network topology and data flow diagrams are current | | |
| ID-6 | We conduct formal risk assessments on a defined schedule | | |
| ID-7 | A risk register is maintained with treatment decisions documented | | |
| ID-8 | We receive and act on threat intelligence from external sources | | |
| ID-9 | Vulnerabilities are identified, tracked, and prioritized (e.g., via CVE scoring) | | |
| ID-10 | Lessons from past incidents and assessments are fed back into risk management | | |

**ID Total Score:** _____ / 40 &nbsp;&nbsp; **ID Average (÷10):** _____ &nbsp;&nbsp; **ID Tier (round down):** _____

---

## Function 3: PROTECT (PR)

*Protect implements safeguards to support delivery of critical services.*

| # | Assessment Statement | Score (1–4) | Evidence / Notes |
|:---:|:---|:---:|:---|
| PR-1 | All users authenticate with MFA for access to organizational systems | | |
| PR-2 | Privileged access is managed with PAM tooling and access reviews | | |
| PR-3 | Access permissions are reviewed at least annually (user recertification) | | |
| PR-4 | Data at rest is encrypted for sensitive and confidential data | | |
| PR-5 | Data in transit is encrypted using approved protocols (TLS 1.2+) | | |
| PR-6 | Backups are performed, verified, and tested for recovery | | |
| PR-7 | Security awareness training is conducted annually for all staff | | |
| PR-8 | Role-specific security training is provided (developers, admins, IR team) | | |
| PR-9 | Configuration baselines exist for all system types and are enforced | | |
| PR-10 | Patch management covers >95% of systems within defined SLAs | | |
| PR-11 | Network segmentation separates sensitive systems from general corporate networks | | |
| PR-12 | Software development follows secure SDLC practices | | |

**PR Total Score:** _____ / 48 &nbsp;&nbsp; **PR Average (÷12):** _____ &nbsp;&nbsp; **PR Tier (round down):** _____

---

## Function 4: DETECT (DE)

*Detect enables timely discovery of cybersecurity events.*

| # | Assessment Statement | Score (1–4) | Evidence / Notes |
|:---:|:---|:---:|:---|
| DE-1 | Logs are collected from all critical systems and centralized (SIEM or equivalent) | | |
| DE-2 | Log retention meets regulatory and forensic requirements (≥90 days hot, 1 year cold) | | |
| DE-3 | Alerts are defined and tuned for high-priority threat scenarios | | |
| DE-4 | Anomalous network activity is detected and investigated | | |
| DE-5 | Endpoint detection and response (EDR) covers all managed endpoints | | |
| DE-6 | Security events are correlated across multiple data sources | | |
| DE-7 | Defined criteria exist for declaring a security incident | | |
| DE-8 | Mean Time to Detect (MTTD) is measured and tracked | | |

**DE Total Score:** _____ / 32 &nbsp;&nbsp; **DE Average (÷8):** _____ &nbsp;&nbsp; **DE Tier (round down):** _____

---

## Function 5: RESPOND (RS)

*Respond supports ability to contain the impact of cybersecurity incidents.*

| # | Assessment Statement | Score (1–4) | Evidence / Notes |
|:---:|:---|:---:|:---|
| RS-1 | A documented Incident Response Plan (IRP) exists and is accessible to responders | | |
| RS-2 | The IRP has been tested (tabletop exercise) in the past 12 months | | |
| RS-3 | Incident severity classification criteria are defined and understood by responders | | |
| RS-4 | Escalation paths and contact trees are documented and current | | |
| RS-5 | Incidents are contained using defined playbooks | | |
| RS-6 | Digital forensics and evidence preservation procedures are documented | | |
| RS-7 | Internal stakeholders are notified within defined timeframes | | |
| RS-8 | Regulatory breach notification requirements are understood and can be met | | |
| RS-9 | Post-incident reviews (PIRs) are conducted and documented | | |
| RS-10 | Lessons learned are incorporated into plan updates | | |

**RS Total Score:** _____ / 40 &nbsp;&nbsp; **RS Average (÷10):** _____ &nbsp;&nbsp; **RS Tier (round down):** _____

---

## Function 6: RECOVER (RC)

*Recover supports timely restoration of capabilities after a cybersecurity incident.*

| # | Assessment Statement | Score (1–4) | Evidence / Notes |
|:---:|:---|:---:|:---|
| RC-1 | Recovery plans exist for all critical systems (BCP/DRP documentation) | | |
| RC-2 | Recovery Time Objectives (RTOs) are defined for all critical systems | | |
| RC-3 | Recovery Point Objectives (RPOs) are defined and backup schedules align | | |
| RC-4 | Recovery procedures are tested at least annually | | |
| RC-5 | Recovery from a ransomware event is specifically planned and tested | | |
| RC-6 | Communications templates exist for public/customer notification post-incident | | |
| RC-7 | Lessons from recovery exercises are incorporated into plan updates | | |

**RC Total Score:** _____ / 28 &nbsp;&nbsp; **RC Average (÷7):** _____ &nbsp;&nbsp; **RC Tier (round down):** _____

---

## Summary Scorecard

| Function | Raw Score | Max Score | Average | **Tier** |
|:---|:---:|:---:|:---:|:---:|
| **GV** — Govern | | 40 | | |
| **ID** — Identify | | 40 | | |
| **PR** — Protect | | 48 | | |
| **DE** — Detect | | 32 | | |
| **RS** — Respond | | 40 | | |
| **RC** — Recover | | 28 | | |
| **Overall Program Tier** (lowest function) | | | | |

---

## Tier Interpretation

### Overall Tier 1 — Partial
**Risk:** High. Cybersecurity practices are ad hoc. The organization is likely unaware of the full extent of its risk exposure.

**Recommended Actions:**
- Immediate: Appoint a security owner; establish basic asset inventory
- 90 Days: Complete risk assessment; implement MFA and patch management
- 6 Months: Build and test an Incident Response Plan
- 12 Months: Target Tier 2 across all functions

---

### Overall Tier 2 — Risk Informed
**Risk:** Moderate. Risk management exists but is siloed and inconsistently applied.

**Recommended Actions:**
- Immediate: Formalize risk management process with documented risk register
- 90 Days: Extend controls coverage to all business units; close IAM gaps
- 6 Months: Implement SIEM or centralized logging; run first tabletop exercise
- 12 Months: Target Tier 3 across highest-risk functions

---

### Overall Tier 3 — Repeatable
**Risk:** Managed. Risk practices are formalized and consistently applied.

**Recommended Actions:**
- Focus: Threat intelligence integration; supply chain risk maturation
- Continuous: Quarterly risk reviews; annual program assessment
- Certification readiness: ISO 27001 or FedRAMP Authorization now achievable
- Target: Tier 4 in highest-risk functions (Identify, Detect)

---

### Overall Tier 4 — Adaptive
**Risk:** Low-to-Moderate. The organization continuously improves based on lessons learned and emerging threats.

**Recommended Actions:**
- Focus: External threat intelligence sharing; sector collaboration
- Innovation: Evaluate AI/ML-enhanced detection; automate response playbooks
- Leadership: Contribute to sector ISAC; publish threat intel
- Maintenance: Maintain Tier 4 through quarterly program reviews

---

## Gap Prioritization Matrix

After completing the assessment, use this matrix to prioritize remediation:

| Priority | Criteria | Action |
|:---|:---|:---|
| **Critical** | Any function at Tier 1 with regulatory exposure | Immediate remediation — assign owner, fund in current budget |
| **High** | Any function at Tier 1 without regulatory exposure; Tier 2 functions with active threat actors | Remediate within 90 days |
| **Medium** | Any function at Tier 2 in stable threat environment | Remediate within 6 months |
| **Low** | Tier 3 functions seeking Tier 4 | Ongoing improvement; include in next planning cycle |

---

## Next Steps

1. **Document current tier:** Enter scores into `csf-profile-template.xlsx` as the Current Profile
2. **Define target tier:** Work with leadership to define Target Profile (typically +1 tier per function)
3. **Build remediation roadmap:** Gap list from this assessment → prioritized project plan
4. **Schedule reassessment:** Tier assessments should be conducted annually or after major changes
5. **Cross-map to controls:** Use `../cross-framework/master-control-mapping.md` to map gaps to specific controls

---

*Last Updated: See git history | Framework Version: NIST CSF 2.0 (Feb 2024)*
