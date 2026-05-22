# Example — SaaS AI Feature Risk Review

> **Scenario:** An enterprise is preparing to enable Microsoft 365 Copilot across its organization. The IT and security teams must assess the security and data risk before rollout.

---

## Context

| Field | Detail |
|-------|--------|
| **Organization** | Fictional enterprise (healthcare-adjacent, not a covered entity) |
| **SaaS Platform** | Microsoft 365 |
| **AI Feature** | Microsoft 365 Copilot |
| **BRIDGE Domains** | B, I, D, G, E |
| **Risk Level** | High — AI feature has broad access to enterprise data |

---

## What Makes This Use Case High Risk

Microsoft 365 Copilot connects to a broad range of data sources within the Microsoft 365 ecosystem — emails, Teams messages, SharePoint documents, OneDrive files, calendar data, and more. The AI feature generates responses based on data the user has access to, which can include:

- Documents shared broadly across the organization
- Emails and messages sent to distribution lists
- Files on SharePoint sites with permissive access controls
- Historical data the user may not actively be aware they can access

**The risk is not that Copilot introduces new access — it is that Copilot makes existing access much more visible and actionable.** A user can ask Copilot to summarize everything related to a topic and receive a response drawn from documents they technically have access to but would never have found manually.

---

## Pre-Deployment Assessment Findings

### Finding 1 — Overly Permissive SharePoint Access Controls (Critical)
A significant portion of SharePoint sites were configured with "Everyone" or "All staff" access. This means Copilot could surface documents from HR, Legal, Finance, and Executive teams to any user who asked the right question.

**Remediation required:** SharePoint access control remediation before Copilot is enabled. Sites containing sensitive data must be restricted to named groups.

### Finding 2 — Sensitive Data in Shared Locations (High)
The data classification sweep identified salary information, draft contracts, and M&A-related documents in broadly accessible SharePoint locations.

**Remediation required:** Sensitive documents must be moved to restricted libraries before go-live.

### Finding 3 — Microsoft Purview Not Fully Deployed (Medium)
Microsoft Purview (sensitivity labels and DLP) was partially deployed. Without full label coverage, Copilot could be used to extract or summarize unlabeled sensitive documents.

**Remediation required:** Sensitivity label coverage must reach a minimum threshold before Copilot rollout. DLP policies must be extended to cover Copilot interactions.

### Finding 4 — Training Opt-Out Confirmed (No Action Required)
Microsoft confirmed through enterprise agreement that Microsoft 365 Copilot does not use customer data for model training. Documented in vendor review record.

### Finding 5 — Audit Logging Available (No Action Required)
Microsoft 365 Copilot activity is logged in the Microsoft Purview audit log. Retention configured for 90 days (extended to 180 days as a condition of approval).

---

## Controls Required Before Go-Live

| # | Control | Owner | Status |
|---|---------|-------|--------|
| 1 | SharePoint access control remediation | IT / Data Governance | Required before activation |
| 2 | Sensitive document relocation to restricted libraries | Data Owners | Required before activation |
| 3 | Microsoft Purview sensitivity label coverage ≥ 80% | IT / Compliance | Required before activation |
| 4 | DLP policies extended to cover Copilot interactions | Security / IT | Required before activation |
| 5 | Audit log retention extended to 180 days | IT | Required before activation |
| 6 | Copilot user training completed | L&D / Security | Required before go-live |
| 7 | Phased rollout — pilot group of 50 users first | IT | Agreed |

---

## Phased Rollout Plan

| Phase | Scope | Duration | Gate |
|-------|-------|----------|------|
| Phase 1 | 50 pilot users — IT and Operations | 30 days | Security review of access patterns; no incidents |
| Phase 2 | 500 users — Technology and Marketing | 30 days | DLP event review; user feedback |
| Phase 3 | Organization-wide | Ongoing | Ongoing monitoring |

---

## Post-Deployment Monitoring

| Metric | Frequency |
|--------|-----------|
| Audit log review for unusual query patterns | Monthly |
| DLP events triggered via Copilot interactions | Monthly |
| SharePoint permission drift review | Quarterly |
| Sensitivity label coverage rate | Quarterly |
| User awareness assessment | Annually |

---

## Governance Record

| Stage | Outcome |
|-------|---------|
| Intake submitted | Classified as High risk |
| Pre-deployment assessment | 5 findings; 4 requiring remediation |
| Remediation tracking | Critical and High findings resolved |
| Approved with Conditions | 7 conditions; phased rollout |
| Phase 1 complete | No incidents; Phase 2 approved |

---

## Lessons Learned

- SaaS AI features do not create new access — they amplify existing access. Access control hygiene is the most important prerequisite
- Organizations that invest in data governance and sensitivity labeling before enabling SaaS AI have significantly lower risk exposure
- Phased rollout allows security teams to monitor real-world usage patterns before broad deployment

---

## Related Templates
- [SaaS AI Security Review Checklist](../templates/ai-saas-review-checklist.md)
- [AI Risk Assessment Template](../templates/ai-risk-assessment-template.md)
