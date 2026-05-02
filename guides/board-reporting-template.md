# Board Cybersecurity Reporting Template

> **Purpose:** Communicate cybersecurity risk posture, program status, and key decisions to the Board of Directors or Audit/Risk Committee in a format designed for non-technical audiences
> **Frequency:** Quarterly (full report) | Annually (comprehensive program review) | Ad Hoc (material incident or significant risk change)
> **Audience:** Board of Directors, Audit Committee, Risk Committee, Executive Sponsors
> **Presenter:** CISO or Security Program Owner
> **Target Length:** 15–20 minute presentation | 8–12 slides or equivalent written report

---

## Document Control

| Field | Value |
|:---|:---|
| **Report Title** | Cybersecurity Program — Board Update |
| **Reporting Period** | Q[X] [Year] |
| **Prepared By** | [CISO Name] |
| **Prepared Date** | |
| **Presentation Date** | |
| **Board / Committee** | [Board of Directors / Audit Committee / Risk Committee] |
| **Classification** | Board Confidential |

---

## Report Structure Overview

| Section | Content | Recommended Time |
|:---:|:---|:---|
| 1 | Executive Summary — One-Page Dashboard | 2 min |
| 2 | Security Posture Summary | 3 min |
| 3 | Key Risks and Risk Decisions | 4 min |
| 4 | Incident Summary | 2 min |
| 5 | Compliance and Certification Status | 2 min |
| 6 | Program Metrics | 2 min |
| 7 | Roadmap and Investment Asks | 3 min |
| 8 | Appendix | Reference only |

---

## Section 1 — Executive Summary Dashboard

> *This one-page summary should stand alone. Board members who read nothing else should understand the organization's security posture and any required decisions from this page.*

### 1.1 Overall Security Posture

**Overall Program Health:** &nbsp; 🟢 Good &nbsp; / &nbsp; 🟡 Improving &nbsp; / &nbsp; 🟠 Needs Attention &nbsp; / &nbsp; 🔴 At Risk

**One-sentence status:**
> *[e.g., "Our cybersecurity program is on track toward SOC 2 Type II certification in Q3, with no material incidents this quarter and continued improvement in patch compliance and MFA coverage."]*

[Enter one-sentence status here]

---

### 1.2 Functional Posture Indicators

| Security Domain | Status | Change from Last Quarter | Key Metric |
|:---|:---:|:---:|:---|
| Identity & Access Management | 🟢 / 🟡 / 🔴 | ↑ ↓ → | MFA coverage: __% |
| Vulnerability Management | 🟢 / 🟡 / 🔴 | ↑ ↓ → | Critical vulns patched within SLA: __% |
| Threat Detection & Monitoring | 🟢 / 🟡 / 🔴 | ↑ ↓ → | SIEM coverage of critical systems: __% |
| Incident Response | 🟢 / 🟡 / 🔴 | ↑ ↓ → | IRP tested: [Month/Year] |
| Data Protection | 🟢 / 🟡 / 🔴 | ↑ ↓ → | Encryption coverage at rest: __% |
| Vendor Risk | 🟢 / 🟡 / 🔴 | ↑ ↓ → | Critical vendors assessed: __% |
| Security Awareness | 🟢 / 🟡 / 🔴 | ↑ ↓ → | Training completion: __% |
| Compliance | 🟢 / 🟡 / 🔴 | ↑ ↓ → | [Current certification status] |

**Status Legend:** 🟢 On target &nbsp;|&nbsp; 🟡 Minor gaps, improving &nbsp;|&nbsp; 🟠 Needs attention, remediation planned &nbsp;|&nbsp; 🔴 Significant gap or active issue

---

### 1.3 Decisions Required from the Board

> *Flag any items requiring Board awareness, endorsement, or a formal decision. Keep this list to the most material items only.*

| # | Item | Decision Required | Recommended Action |
|:---:|:---|:---|:---|
| 1 | | ☐ Approve &nbsp; ☐ Endorse &nbsp; ☐ Awareness only | |
| 2 | | ☐ Approve &nbsp; ☐ Endorse &nbsp; ☐ Awareness only | |

*If no Board decisions are required this quarter, state: "No Board decisions are required this period."*

---

## Section 2 — Security Posture Summary

### 2.1 NIST CSF Maturity — Current vs. Target

> *Non-technical boards respond best to simple visual representations. Use this table or a radar chart in presentation format.*

| CSF Function | Current Tier | Target Tier | Status |
|:---|:---:|:---:|:---:|
| Govern | | | 🟢 / 🟡 / 🔴 |
| Identify | | | 🟢 / 🟡 / 🔴 |
| Protect | | | 🟢 / 🟡 / 🔴 |
| Detect | | | 🟢 / 🟡 / 🔴 |
| Respond | | | 🟢 / 🟡 / 🔴 |
| Recover | | | 🟢 / 🟡 / 🔴 |
| **Overall Program Tier** | | | |

**Tier Reference:**
- Tier 1 — Partial: Ad hoc, reactive
- Tier 2 — Risk Informed: Defined but not org-wide
- Tier 3 — Repeatable: Formal, consistent, documented
- Tier 4 — Adaptive: Continuously improving

**Narrative:**
> *[2–3 sentences describing what has improved this quarter and what remains the primary gap. Example: "We achieved Tier 3 in Protect this quarter following completion of our MFA rollout. Our primary gap remains in the Detect function where SIEM implementation is 60% complete and on track for Q[X]."]*

[Enter narrative here]

---

### 2.2 Threat Environment Context

> *Brief boards on the external threat environment relevant to your organization. Connect threats to your posture — show you are aware of what's happening and that your defenses address it.*

**Threat Landscape Summary — [Quarter Year]:**

| Threat | Relevance to [Org] | Our Defense |
|:---|:---|:---|
| [e.g., Ransomware targeting [sector]] | High — we operate in this sector | Immutable backups; EDR coverage 98%; IR tested Q[X] |
| [e.g., Supply chain attacks via software dependencies] | Medium — we use open source in product | SBOM implemented; SCA scanning in CI/CD pipeline |
| [e.g., Business email compromise (BEC)] | High — finance team is a target | DMARC enforced; finance-specific BEC training quarterly |
| [e.g., MFA bypass / session hijacking] | Medium | Phishing-resistant MFA (FIDO2) for admin accounts |

**Key threat intelligence source(s):** [CISA, sector ISAC, threat intel vendor]

---

## Section 3 — Key Risks and Risk Decisions

### 3.1 Top Risk Register Summary

> *Present 3–5 top risks. Boards should understand the nature of the risk, current exposure, and treatment status. Avoid technical jargon.*

| Risk | Business Impact | Likelihood | Rating | Treatment | Status |
|:---|:---|:---:|:---:|:---|:---:|
| [Risk title in plain English] | [What could happen to the business] | Low/Med/High | Critical/High/Med/Low | Mitigating / Accepted / Transferring | On track / Overdue |
| | | | | | |
| | | | | | |
| | | | | | |
| | | | | | |

### 3.2 Risk Decisions Requiring Board Awareness

> *Board-level risk awareness or endorsement for accepted or escalated risks.*

#### Risk Decision [1]: [Risk Title]

**Plain-English Description:**
> *[One paragraph explaining the risk in terms a business leader understands — what is the threat, what is at risk, and what could happen]*

**Current Exposure:**
> Likelihood: [Low / Medium / High] &nbsp;|&nbsp; Impact: [Low / Medium / High / Critical] &nbsp;|&nbsp; Overall Rating: [Low / Medium / High / Critical]

**Treatment Decision:**
> ☐ Mitigating — [Brief description of mitigating controls and timeline]
> ☐ Accepting — [Business justification; acceptance signed by [role] on [date]; expiry [date]]
> ☐ Transferring — [Insurance / contractual]

**Board Action Required:**
> ☐ Awareness only &nbsp; ☐ Endorsement of risk acceptance &nbsp; ☐ Budget approval for mitigation

---

### 3.3 Risk Trend

| Quarter | Risk Register Size | Critical | High | Medium | Low |
|:---:|:---:|:---:|:---:|:---:|:---:|
| Q[X-3] | | | | | |
| Q[X-2] | | | | | |
| Q[X-1] | | | | | |
| **Q[X] (Current)** | | | | | |

**Trend Narrative:**
> *[Brief explanation of why the risk register has grown/shrunk, what new risks were added, and what was remediated.]*

---

## Section 4 — Incident Summary

### 4.1 Incident Overview — [Quarter]

| Severity | Count | Notable Events | Resolution Status |
|:---:|:---:|:---|:---:|
| Critical (P1) | | | All resolved / [X] open |
| High (P2) | | | All resolved / [X] open |
| Medium (P3) | | | All resolved / [X] open |
| Low (P4) | | | All resolved / [X] open |

**Total incidents this quarter:** _____ &nbsp;&nbsp; **vs. last quarter:** _____ &nbsp;&nbsp; **Trend:** ↑ ↓ →

### 4.2 Material Incident Detail

> *For any P1 or significant P2 incident, provide a brief post-incident summary for the Board.*

#### Incident: [Title / Reference ID]

| Field | Detail |
|:---|:---|
| **Date** | |
| **Classification** | Critical / High |
| **Type** | Ransomware / Phishing / Data breach / Unauthorized access / Other |
| **Systems Affected** | |
| **Data Involved** | |
| **Business Impact** | |
| **Detection Method** | Internal detection / Customer report / Third party / Other |
| **Time to Detect** | |
| **Time to Contain** | |
| **Regulatory Notification Required?** | Yes / No |
| **Regulatory Notification Made?** | Yes — [Date] / No — Not required |
| **Root Cause** | |
| **Remediation Completed** | Yes / In progress — [Date] |
| **Lessons Learned** | |

### 4.3 Incident Trend (12-month view)

| Month | Total Incidents | P1/P2 | Phishing-Related | Insider Threat |
|:---:|:---:|:---:|:---:|:---:|
| [Month 1] | | | | |
| [Month 2] | | | | |
| [Month 3] | | | | |
| … | | | | |

---

## Section 5 — Compliance and Certification Status

### 5.1 Certification Dashboard

| Framework / Certification | Status | Last Audit | Next Audit / Renewal | Auditor |
|:---|:---:|:---:|:---:|:---|
| ISO 27001:2022 | ✅ Certified / 🟡 In progress / ⚪ Planned / ❌ Gap | | | |
| SOC 2 Type II | ✅ Certified / 🟡 In progress / ⚪ Planned / ❌ Gap | | | |
| PCI-DSS v4 | ✅ Compliant / 🟡 In progress / ⚪ Planned / N/A | | | |
| FedRAMP | ✅ Authorized / 🟡 In progress / ⚪ Planned / N/A | | | |
| HIPAA | ✅ Compliant / 🟡 In progress / N/A | | | |
| GDPR | 🟢 Program active / 🟡 Gaps identified | | | |
| [Other] | | | | |

### 5.2 Regulatory Obligations

> *Brief the Board on material regulatory developments relevant to the organization.*

| Obligation | Jurisdiction | Status | Risk if Non-Compliant |
|:---|:---|:---|:---|
| [e.g., GDPR breach notification readiness] | EU | 🟢 Ready | Fines up to 4% of global revenue |
| [e.g., SEC cybersecurity disclosure rule] | US | 🟡 Implementing | SEC enforcement action |
| [e.g., NIS2 Directive compliance] | EU | ⚪ Assessing impact | Regulatory sanctions |
| [Other] | | | |

### 5.3 Audit Findings Summary

| Audit | Date | Finding Count | Critical/High | Remediated | In Progress | Open |
|:---|:---|:---:|:---:|:---:|:---:|:---:|
| Internal audit — [scope] | | | | | | |
| External audit — [auditor] | | | | | | |
| Customer security assessment | | | | | | |

---

## Section 6 — Program Metrics

### 6.1 Key Performance Indicators — Quarterly Snapshot

| KPI | Current Quarter | Last Quarter | Target | Status |
|:---|:---:|:---:|:---:|:---:|
| MFA enrollment — all users | % | % | 100% | 🟢 / 🟡 / 🔴 |
| Critical vulnerabilities patched within 15 days | % | % | ≥98% | |
| High vulnerabilities patched within 30 days | % | % | ≥95% | |
| Security training completion | % | % | ≥95% | |
| Mean Time to Detect — security events (hours) | hrs | hrs | Trending ↓ | |
| Mean Time to Respond — P1 incidents (hours) | hrs | hrs | <4 hrs | |
| Open critical/high POA&M items overdue | count | count | 0 | |
| Critical vendors with current assessments | % | % | 100% | |
| Backup restore success rate | % | % | 100% | |
| Phishing simulation click rate | % | % | <5% | |

### 6.2 Security Investment Efficiency

| Metric | Value | Notes |
|:---|:---:|:---|
| Security budget as % of IT budget | % | Industry benchmark: 8–15% |
| Security budget per employee ($) | $ | |
| Security FTEs per 1,000 employees | | Industry benchmark: ~2–5 per 1,000 |
| Cost per confirmed security incident | $ | |

---

## Section 7 — Roadmap and Investment

### 7.1 Current Quarter Achievements

> *Summarize the 3–5 most significant security accomplishments this quarter. Frame as risk reduction or business value.*

| Achievement | Business Value / Risk Reduced |
|:---|:---|
| [e.g., Completed MFA rollout for all 847 employees] | Eliminates credential-based attacks for 100% of user accounts |
| [e.g., Passed SOC 2 Type II audit with zero exceptions] | Unlocks enterprise sales pipeline; customer trust demonstrated |
| [e.g., Reduced critical vulnerability backlog by 78%] | Reduced attack surface on 34 internet-facing systems |
| | |
| | |

### 7.2 Next Quarter Priorities

| Priority | Initiative | Risk Addressed | Investment | Timeline |
|:---:|:---|:---|:---|:---|
| 1 | | | $[X] | Q[X] |
| 2 | | | $[X] | Q[X] |
| 3 | | | $[X] | Q[X] |

### 7.3 Investment Requests (if any)

> *This section is only used when a budget request requires Board awareness or approval.*

#### Investment Request: [Initiative Name]

**Business Case:**
> *[Explain in non-technical terms: what the investment addresses, what the risk is if we don't invest, and what the expected outcome is]*

| Field | Detail |
|:---|:---|
| **Investment Amount** | $[X] |
| **One-time / Recurring** | One-time / Annual / Both |
| **Risk Addressed** | |
| **Risk Rating Before Investment** | Critical / High / Medium |
| **Expected Risk Rating After** | High / Medium / Low |
| **Alternative Considered** | |
| **Recommendation** | Approve / Defer / Reject |
| **Board Action Required** | Approval / Endorsement / Awareness |

---

## Section 8 — Appendix

### 8A — Glossary of Key Terms

| Term | Plain-English Definition |
|:---|:---|
| **Attack Surface** | All the points where an attacker could try to enter or extract data from our systems |
| **CVE / Vulnerability** | A known security weakness in software that attackers can exploit; critical CVEs must be patched within 15 days |
| **MFA** | Multi-Factor Authentication — requires a second form of verification beyond a password (like a phone code) |
| **Phishing** | Deceptive emails designed to trick employees into revealing passwords or clicking malicious links |
| **Ransomware** | Malware that encrypts organizational data and demands payment for the decryption key |
| **SIEM** | Security Information and Event Management — software that collects and analyzes security logs from all systems |
| **SOC 2** | A third-party audit that confirms our security controls meet Trust Services Criteria — used by enterprise customers |
| **Zero-day** | A vulnerability that is unknown to the software vendor; no patch is yet available; highest risk category |
| **Threat Actor** | An individual or group that poses a cybersecurity threat — includes criminals, nation-states, and insiders |
| **MTTD / MTTR** | Mean Time to Detect / Mean Time to Respond — how quickly we find and contain security events |

### 8B — Regulatory Notification Obligations Reference

| Regulation | Trigger | Notification Timeline | Authority | Penalty Range |
|:---|:---|:---|:---|:---|
| GDPR | Personal data breach | 72 hours | Data protection supervisory authority | Up to 4% global revenue or €20M |
| HIPAA Breach Notification | PHI breach > 500 individuals | 60 days | HHS + media in affected state | Up to $1.9M per category per year |
| SEC Cybersecurity Rule | Material cybersecurity incident | 4 business days (Form 8-K) | SEC | Enforcement action |
| PCI-DSS | Cardholder data breach | Immediately | Card brands (Visa, Mastercard) | Fines + potential loss of card processing |
| [State breach notification] | [PII breach per state definition] | [30–90 days per state] | [State AG] | [Per-record fines] |

### 8C — Year-over-Year Program Comparison

| Metric | [Year N-2] | [Year N-1] | [Year N Q[X]] | Trend |
|:---|:---:|:---:|:---:|:---:|
| MFA coverage | % | % | % | ↑ |
| Patch compliance — critical | % | % | % | ↑ |
| Mean Time to Detect (hours) | | | | ↓ |
| Security training completion | % | % | % | ↑ |
| Total security incidents | | | | ↓ |
| Certifications held | | | | ↑ |
| Security budget ($) | $ | $ | $ | ↑ |
| Overall NIST CSF Tier | | | | ↑ |

---

## Presenter Notes

**Tone guidance for Board presentations:**

- **Lead with business impact** — translate every metric into dollars, customer risk, or regulatory exposure
- **Avoid jargon** — say "password theft" not "credential compromise"; "hacker group" not "APT"; "backup copies" not "immutable offline backups"
- **Be direct about gaps** — boards distrust sanitized reports; acknowledge what isn't working and what you're doing about it
- **Anticipate questions** — prepare for: "Are we doing enough?", "How do we compare to peers?", "What would a breach cost us?", "Is our cyber insurance adequate?"
- **The 3-question test** — at the end of your update, the Board should know: (1) How are we doing? (2) What's the biggest risk right now? (3) What do you need from us?

**Questions boards commonly ask:**
1. "If we were breached today, would we know?" → Point to MTTD metric and SIEM/EDR coverage
2. "What's our biggest vulnerability right now?" → Reference top risk from Section 3
3. "Are we spending enough on security?" → Reference security budget as % of IT and peer benchmarks
4. "Is our cyber insurance aligned with our actual risk?" → Address in risk transfer discussion
5. "What happens if our CEO's email is compromised?" → Reference BEC controls and incident response
6. "How long would it take us to recover from ransomware?" → Reference RTO/RPO and backup test results

---

*Template Version: 1.0 | Quarterly cadence | Owner: CISO | Classification: Board Confidential*
