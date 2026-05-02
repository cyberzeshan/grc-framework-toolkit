# Security Policy Exception Request

> **Purpose:** Formally document, review, and approve temporary deviations from information security policies, standards, or controls
> **When to Use:** When operational necessity requires a temporary deviation from an established security policy and a permanent control change is not appropriate
> **Distinguish from Risk Acceptance:** Exception requests cover policy deviations (e.g., a system cannot meet the MFA requirement). Risk Acceptance forms cover broader risk posture decisions. Use the Risk Acceptance Form when accepting a risk without a specific policy violation.
> **Authority:** Exceptions require CISO approval. High-risk exceptions require additional executive sign-off. See Section 7.

---

## Document Control

| Field | Value |
|:---|:---|
| **Form ID** | EX-[YYYY]-[###] |
| **Policy / Standard Referenced** | |
| **Date Submitted** | |
| **Submitted By** | |
| **Business Unit** | |
| **Status** | Pending / Approved / Rejected / Expired |
| **Approved Expiry Date** | |
| **Classification** | Internal — Confidential |

---

## Section 1 — Requestor Information

| Field | Value |
|:---|:---|
| **Requestor Name** | |
| **Title** | |
| **Business Unit / Department** | |
| **Manager / Director** | |
| **Email** | |
| **Phone** | |
| **Date of Request** | |

---

## Section 2 — Exception Details

### 2.1 Policy / Standard Being Excepted

| Field | Value |
|:---|:---|
| **Policy Name** | [e.g., Access Control Policy, Password Policy, Patch Management Policy] |
| **Policy ID** | [e.g., ISMS-POL-002] |
| **Specific Policy Requirement** | [Quote the exact policy statement or standard being excepted] |
| **Policy Owner** | |

### 2.2 Exception Description

> *Clearly describe what deviation from the policy is being requested. Be specific — vague exception requests will be returned for clarification.*

**What the policy requires:**

[Enter the required control or standard here]

**What is actually in place (the deviation):**

[Describe the current state that does not meet the policy requirement]

**Specific exception requested:**

[Describe precisely what exception is being requested — i.e., what should be permitted despite the policy]

### 2.3 Systems and Assets Affected

| System / Asset | Owner | Classification | Production? |
|:---|:---|:---|:---:|
| | | Public / Internal / Confidential / Restricted | Yes / No |
| | | | |
| | | | |

### 2.4 Users / Roles Affected

| User / Role / Group | Count | Access Level |
|:---|:---:|:---|
| | | |
| | | |

---

## Section 3 — Business Justification

### 3.1 Reason for Exception

> *Explain why the policy requirement cannot be met. Acceptable reasons include technical infeasibility, vendor dependency, operational criticality, or a time-limited transition period. "It's inconvenient" or "it slows us down" are not acceptable justifications.*

**Primary Reason Category:**
- [ ] Technical infeasibility — the system or environment does not support the required control
- [ ] Vendor dependency — a third-party vendor's product does not support the requirement
- [ ] Operational continuity — implementing the control would disrupt critical operations
- [ ] Transition period — control is being implemented but requires additional time
- [ ] Cost / resource constraint — with executive acknowledgement of the risk
- [ ] Legacy system — end-of-life system pending decommission
- [ ] Other: _______________________________________________

**Detailed Justification:**

[Provide a thorough explanation of why the exception is needed. Include: what was tried, what the technical or operational constraint is, and why alternatives are not viable.]

### 3.2 Business Impact of Denial

> *What happens to the business if this exception is not granted?*

[Describe the operational, financial, or project impact if the exception is denied]

### 3.3 Exception Duration

| Field | Value |
|:---|:---|
| **Start Date** | |
| **Requested Expiry Date** | |
| **Duration (days)** | |
| **Maximum Permitted Duration** | 90 days (standard) / 180 days (with CISO approval) / 365 days (executive + CISO) |

> **All exceptions are temporary.** Exceptions do not modify the underlying policy. If a permanent policy deviation is required, submit a policy change request through the policy governance process.

### 3.4 Remediation Plan

> *Exceptions are granted on the expectation of a remediation path. Describe the plan to bring the system or process into compliance.*

| Milestone | Description | Target Date | Owner |
|:---|:---|:---|:---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| **Full Compliance Achieved** | | | |

---

## Section 4 — Risk Assessment

### 4.1 Security Risk of the Exception

> *Assess the security risk introduced by permitting this exception. What is the increased exposure?*

**Threat(s) enabled or increased by this exception:**

[Describe specific threats that this deviation exposes the organization to]

**Assets or data at increased risk:**

[List specific assets, data types, or systems whose risk posture worsens with this exception]

**Likelihood of exploitation during exception period:**
☐ Low &nbsp; ☐ Medium &nbsp; ☐ High

**Impact if exploited:**
☐ Low &nbsp; ☐ Medium &nbsp; ☐ High &nbsp; ☐ Critical

**Overall exception risk rating:**
☐ Low &nbsp; ☐ Medium &nbsp; ☐ High &nbsp; ☐ Critical

### 4.2 Regulatory and Compliance Impact

> *Does this exception create a compliance exposure? Check all that apply.*

| Framework / Regulation | Impacted? | Notes |
|:---|:---:|:---|
| ISO 27001:2022 | ☐ Yes ☐ No | |
| SOC 2 | ☐ Yes ☐ No | |
| GDPR | ☐ Yes ☐ No | |
| HIPAA | ☐ Yes ☐ No | |
| PCI-DSS | ☐ Yes ☐ No | |
| FedRAMP | ☐ Yes ☐ No | |
| [Other] | ☐ Yes ☐ No | |

> **If any compliance framework is impacted:** Legal review is required before approval. Tag the Legal / Compliance team in the review process.

---

## Section 5 — Compensating Controls

> *All exceptions with a Medium or higher risk rating require compensating controls. Document the specific controls that will reduce risk during the exception period.*

| # | Compensating Control | How It Reduces Risk | Implementation Date | Verified By |
|:---:|:---|:---|:---|:---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

**Compensating control adequacy assessment:**
> *Describe whether the compensating controls adequately reduce the risk introduced by the exception, and to what residual risk level.*

[Enter compensating control adequacy assessment here]

**Residual risk after compensating controls:**
☐ Low &nbsp; ☐ Medium &nbsp; ☐ High &nbsp; ☐ Critical

---

## Section 6 — Monitoring During Exception Period

| Monitoring Activity | Frequency | Responsible Party | Alert Threshold |
|:---|:---|:---|:---|
| | Weekly / Monthly | | |
| | | | |

**Exception review checkpoint:**

☐ Mid-point review scheduled: _______________

☐ Pre-expiry review scheduled: _______________

### Automatic Revocation Triggers

This exception is automatically revoked and must be immediately re-reviewed if:

- [ ] A security incident occurs that is directly related to the excepted control
- [ ] Threat intelligence indicates active exploitation of the vulnerability
- [ ] The system's data classification increases
- [ ] Regulatory requirements change in a way that makes the exception non-compliant
- [ ] Compensating controls fail or are removed

---

## Section 7 — Approval Authority Matrix

| Residual Risk Rating | Approval Required | Timeline |
|:---:|:---|:---|
| **Low** | CISO (or delegate) | 5 business days |
| **Medium** | CISO | 5 business days |
| **High** | CISO + Business Unit VP | 10 business days |
| **Critical** | CISO + CIO + CEO | 10 business days; legal review required |

---

## Section 8 — Manager / Director Endorsement

By signing, the requestor's manager confirms the business justification is accurate and endorses the exception request.

| Field | Value |
|:---|:---|
| **Manager Name** | |
| **Title** | |
| **Endorsement** | ☐ Endorsed &nbsp; ☐ Not Endorsed |
| **Notes** | |
| **Signature** | |
| **Date** | |

---

## Section 9 — Security Team Review

| Field | Value |
|:---|:---|
| **Reviewed By** | |
| **Review Date** | |
| **Risk Rating Confirmed** | ☐ Yes &nbsp; ☐ Adjusted to: ________ |
| **Compensating Controls Adequate** | ☐ Yes &nbsp; ☐ No — see notes |
| **Compliance Impact** | ☐ None &nbsp; ☐ Flagged for legal review |
| **Security Recommendation** | ☐ Approve &nbsp; ☐ Approve with conditions &nbsp; ☐ Reject |
| **Conditions (if any)** | |
| **Reviewer Notes** | |
| **Signature** | |

---

## Section 10 — CISO Decision

| Field | Value |
|:---|:---|
| **CISO Name** | |
| **Decision Date** | |
| **Decision** | ☐ **APPROVED** &nbsp; ☐ **APPROVED WITH CONDITIONS** &nbsp; ☐ **REJECTED** |
| **Approved Duration** | _____ days (from _______________ to _______________) |
| **Conditions of Approval** | |
| **Rejection Reason (if rejected)** | |
| **CISO Signature** | |
| **Date** | |

---

## Section 11 — Additional Executive Approval (High / Critical risks only)

| Role | Name | Decision | Signature | Date |
|:---|:---|:---|:---|:---|
| Business Unit VP | | ☐ Approved ☐ Rejected | | |
| CIO | | ☐ Approved ☐ Rejected | | |
| CEO | | ☐ Approved ☐ Rejected | | |

---

## Section 12 — Post-Approval Actions

Upon approval, the following actions must be completed:

| Action | Owner | Due Date | Completed |
|:---|:---|:---|:---:|
| Record exception in exception register | Security Team | Within 2 business days | ☐ |
| Notify affected system owners | Requestor | Within 2 business days | ☐ |
| Implement compensating controls | Requestor | Per Section 5 | ☐ |
| Schedule mid-point review | Security Team | Per Section 6 | ☐ |
| Set expiry reminder in ticketing system | Security Team | Upon approval | ☐ |
| Notify compliance team if applicable | Security Team | Within 2 business days | ☐ |

---

## Section 13 — Exception Closure

To be completed when the exception expires, is revoked, or compliance is achieved:

| Field | Value |
|:---|:---|
| **Closure Date** | |
| **Closure Reason** | ☐ Full compliance achieved &nbsp; ☐ Exception expired &nbsp; ☐ System decommissioned &nbsp; ☐ Revoked |
| **Compliance Verification** | ☐ Verified by security team &nbsp; ☐ Pending verification |
| **Verified By** | |
| **Closed By** | |
| **Lessons Learned** | |

---

## Section 14 — Revision History

| Version | Date | Author | Changes |
|:---:|:---|:---|:---|
| 1.0 | | | Initial submission |
| | | | |

---

## Appendix A — Common Exception Scenarios and Guidance

| Scenario | Typical Duration | Common Compensating Controls | Notes |
|:---|:---|:---|:---|
| Legacy system cannot support MFA | 90–180 days | Network isolation; jump host with MFA; enhanced monitoring | Requires decommission timeline |
| Vendor product does not support TLS 1.2+ | 30–90 days | Network segmentation; monitoring; vendor escalation in progress | Require written vendor commitment |
| Development system uses shared credentials | 30 days | Dev environment network isolation; no production data | Never acceptable in production |
| Patch cannot be applied — vendor testing required | 14–30 days | Virtual patching via WAF/IPS; enhanced monitoring | Must document vendor test timeline |
| Admin account shared during incident response | 24–72 hours | All actions logged; post-incident review required | Emergency exception; notify CISO immediately |
| System cannot meet password length requirement | 90 days | Enforce max permitted length; MFA required; monitor for compromise | Document technical constraint |

---

*Form Retention: 3 years from closure date | Owner: CISO | Classification: Internal — Confidential*
