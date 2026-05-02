# Risk Acceptance Form

> **Purpose:** Formally document an executive decision to accept an identified information security risk rather than mitigate, transfer, or avoid it
> **When to Use:** When a risk treatment option (mitigation, insurance, avoidance) is not implemented and the organization chooses to accept the residual risk
> **Authority:** Risk acceptance requires sign-off from an executive with appropriate authority based on risk rating (see Section 6)
> **Retention:** Completed forms must be retained for a minimum of 3 years and referenced in the risk register

---

## Document Control

| Field | Value |
|:---|:---|
| **Form ID** | RA-[YYYY]-[###] |
| **Risk Register Reference** | RISK-[###] |
| **Date Submitted** | |
| **Submitted By** | |
| **Status** | Pending Review / Approved / Rejected / Expired |
| **Expiry Date** | |
| **Review Date** | |
| **Classification** | Internal — Confidential |

---

## Section 1 — Risk Identification

### 1.1 Risk Title

> *[A clear, concise title for the risk — e.g., "Unpatched critical vulnerability in legacy billing application"]*

**Risk Title:** _______________________________________________

### 1.2 Risk Description

> *Describe the risk in full. Include: what the threat is, what vulnerability or weakness it exploits, what assets are affected, and what could happen if the risk were realized.*

**Risk Description:**

[Enter detailed risk description here]

### 1.3 Affected Systems and Assets

| Asset / System | Asset Owner | Classification | Business Criticality |
|:---|:---|:---|:---|
| | | Public / Internal / Confidential / Restricted | Critical / High / Medium / Low |
| | | | |
| | | | |

### 1.4 Risk Category

Select all that apply:

- [ ] Confidentiality — unauthorized disclosure of information
- [ ] Integrity — unauthorized modification or destruction of information
- [ ] Availability — disruption of access to systems or data
- [ ] Compliance — regulatory or contractual non-compliance
- [ ] Reputational — damage to organizational reputation
- [ ] Financial — direct financial loss or liability
- [ ] Safety — risk to physical safety of personnel or public

### 1.5 Threat Source

- [ ] External threat actor (cybercriminal, nation-state, hacktivist)
- [ ] Insider threat (malicious employee)
- [ ] Insider threat (negligent employee / human error)
- [ ] Third-party / supply chain
- [ ] Natural disaster / environmental
- [ ] System failure / technical error
- [ ] Other: _______________________________________________

---

## Section 2 — Risk Assessment

### 2.1 Likelihood

| Rating | Label | Description |
|:---:|:---|:---|
| 1 | Rare | May occur only in exceptional circumstances (< once in 5 years) |
| 2 | Unlikely | Could occur at some time (once every 2–5 years) |
| 3 | Possible | Might occur at some time (once per year) |
| 4 | Likely | Will probably occur in most circumstances (multiple times per year) |
| 5 | Almost Certain | Expected to occur frequently (monthly or more) |

**Likelihood Rating:** _____ &nbsp;&nbsp; **Label:** _____________________

**Likelihood Justification:**
> *[Explain why this likelihood rating was assigned. Reference threat intelligence, historical incidents, or environmental factors.]*

[Enter justification here]

### 2.2 Impact

| Rating | Label | Description |
|:---:|:---|:---|
| 1 | Negligible | Minimal or no operational impact; no regulatory exposure; <$10K financial loss |
| 2 | Minor | Limited impact; contained to a single system or team; $10K–$100K loss |
| 3 | Moderate | Significant operational disruption; regulatory notification may be required; $100K–$1M loss |
| 4 | Major | Severe impact on operations or reputation; regulatory fines likely; $1M–$10M loss |
| 5 | Catastrophic | Organization-threatening; critical systems offline; regulatory sanctions; >$10M loss |

**Impact Rating:** _____ &nbsp;&nbsp; **Label:** _____________________

**Impact Justification:**
> *[Explain why this impact rating was assigned. Reference potential data exposure, regulatory consequences, business continuity impact, and reputational damage.]*

[Enter justification here]

### 2.3 Inherent Risk Score

| | **Impact 1** | **Impact 2** | **Impact 3** | **Impact 4** | **Impact 5** |
|:---:|:---:|:---:|:---:|:---:|:---:|
| **Likelihood 5** | Medium | High | High | Critical | Critical |
| **Likelihood 4** | Low | Medium | High | High | Critical |
| **Likelihood 3** | Low | Medium | Medium | High | High |
| **Likelihood 2** | Low | Low | Medium | Medium | High |
| **Likelihood 1** | Low | Low | Low | Low | Medium |

**Inherent Risk Score (L × I):** _____ / 25

**Inherent Risk Rating:** ☐ Low &nbsp; ☐ Medium &nbsp; ☐ High &nbsp; ☐ Critical

### 2.4 Existing Controls

> *List any controls already in place that partially mitigate this risk. Be specific.*

| Existing Control | Control Type | Effectiveness |
|:---|:---|:---|
| | Preventive / Detective / Corrective | High / Medium / Low |
| | | |
| | | |

### 2.5 Residual Risk Score

After applying existing controls:

**Residual Likelihood:** _____ &nbsp;&nbsp; **Residual Impact:** _____ &nbsp;&nbsp; **Residual Risk Score:** _____ / 25

**Residual Risk Rating:** ☐ Low &nbsp; ☐ Medium &nbsp; ☐ High &nbsp; ☐ Critical

> **This is the risk being accepted.** The Accepting Executive is accepting the residual risk described above.

---

## Section 3 — Risk Treatment Options Considered

> *Document the treatment options that were evaluated before acceptance was chosen. Risk acceptance should only be selected after other treatments have been genuinely considered.*

### 3.1 Mitigation (Reduce)

**Option considered:** [Describe what mitigation would involve]

**Estimated cost:** $_______________

**Estimated implementation time:** _______________

**Reason not selected:** [e.g., cost exceeds risk exposure; technical infeasibility; vendor dependency; resource constraints]

---

### 3.2 Transfer (Insurance / Contract)

**Option considered:** [Describe what risk transfer would involve — e.g., cyber insurance, contractual liability shift]

**Estimated cost:** $_______________

**Reason not selected:** [e.g., coverage not available; premium prohibitive; risk not transferable]

---

### 3.3 Avoidance (Eliminate)

**Option considered:** [Describe what avoidance would involve — e.g., decommissioning the system, discontinuing the activity]

**Business impact of avoidance:** [Describe operational impact of eliminating the risk source]

**Reason not selected:** [e.g., system is business-critical; alternative not available; avoidance creates greater risk elsewhere]

---

### 3.4 Acceptance (This Form)

**Rationale for acceptance:**

> *[Provide a clear business justification for accepting this risk. Reference: the cost-benefit analysis, the operational necessity, the compensating controls in place, and why the risk is tolerable at its current rating.]*

[Enter acceptance rationale here]

---

## Section 4 — Compensating Controls

> *List any compensating controls that will be implemented to limit exposure during the acceptance period. These are not full mitigations but reduce the likelihood or impact of the risk materializing.*

| Compensating Control | Responsible Party | Implementation Date | Effectiveness |
|:---|:---|:---|:---|
| | | | |
| | | | |
| | | | |

---

## Section 5 — Acceptance Conditions

### 5.1 Acceptance Period

**Start Date:** _______________

**Expiry Date:** _______________ (maximum 12 months; Critical risks maximum 90 days)

> Risk acceptance is **not permanent**. This form expires on the date above. The risk must be reassessed before expiry and a new acceptance form submitted if continued acceptance is warranted.

### 5.2 Monitoring During Acceptance Period

> *Define how this risk will be monitored during the acceptance period to detect if conditions change.*

| Monitoring Activity | Frequency | Responsible Party | Escalation Trigger |
|:---|:---|:---|:---|
| | Monthly / Quarterly | | |
| | | | |

### 5.3 Escalation Triggers

This risk acceptance must be immediately reviewed and potentially revoked if any of the following occur:

- [ ] A security incident occurs that is directly related to this risk
- [ ] Threat intelligence indicates active exploitation of the vulnerability in question
- [ ] Regulatory guidance changes the compliance exposure of this risk
- [ ] Business context changes materially (e.g., M&A, new product launch, change in data classification)
- [ ] A new control becomes available that significantly reduces remediation cost or effort
- [ ] The risk rating increases from its current level

---

## Section 6 — Acceptance Authority Matrix

> Risk acceptance must be approved by an executive with appropriate authority for the residual risk rating.

| Risk Rating | Acceptance Authority | Additional Notification |
|:---:|:---|:---|
| **Low** | CISO | None required |
| **Medium** | CISO + CIO | Notify affected Business Unit Leader |
| **High** | CISO + CIO + CEO | Notify Board Risk/Audit Committee at next meeting |
| **Critical** | CISO + CEO + Board | Immediate Board notification; legal review required |

---

## Section 7 — Risk Submitter Declaration

I certify that the information provided in this form is accurate and complete. I have reviewed the available risk treatment options and recommend acceptance of this risk for the reasons stated above.

| Field | Value |
|:---|:---|
| **Submitted By (Name)** | |
| **Title** | |
| **Business Unit / Team** | |
| **Email** | |
| **Date** | |
| **Signature** | |

---

## Section 8 — CISO Review

| Field | Value |
|:---|:---|
| **CISO Review Date** | |
| **CISO Assessment** | ☐ Concur with risk rating &nbsp; ☐ Risk rating adjusted (see notes) |
| **Adjusted Risk Rating (if changed)** | |
| **CISO Recommendation** | ☐ Approve acceptance &nbsp; ☐ Reject — require mitigation &nbsp; ☐ Escalate |
| **CISO Notes** | |
| **CISO Signature** | |
| **Date** | |

---

## Section 9 — Executive Acceptance Decision

### Primary Accepting Executive

| Field | Value |
|:---|:---|
| **Name** | |
| **Title** | |
| **Decision** | ☐ **ACCEPTED** — I accept this residual risk on behalf of the organization &nbsp;&nbsp; ☐ **REJECTED** — Risk must be mitigated |
| **Conditions (if any)** | |
| **Signature** | |
| **Date** | |

### Additional Acceptance (required for High and Critical risks)

| Field | Value |
|:---|:---|
| **Name** | |
| **Title** | |
| **Decision** | ☐ **ACCEPTED** &nbsp;&nbsp; ☐ **REJECTED** |
| **Signature** | |
| **Date** | |

---

## Section 10 — Risk Register Update

Upon approval, this risk acceptance must be recorded in the organizational risk register.

| Field | Value |
|:---|:---|
| **Risk Register ID** | RISK-[###] |
| **Date Added to Register** | |
| **Added By** | |
| **Next Review Date** | |
| **Reminder Set In** | [Ticketing system / calendar / GRC tool] |

---

## Section 11 — Revision History

| Version | Date | Author | Changes |
|:---:|:---|:---|:---|
| 1.0 | | | Initial submission |
| | | | |

---

*Form Retention: 3 years from expiry date | Owner: CISO | Classification: Internal — Confidential*
