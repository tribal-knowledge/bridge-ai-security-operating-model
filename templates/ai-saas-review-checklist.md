# SaaS AI Security Review Checklist

> **Instructions:** Complete this checklist when reviewing an AI feature embedded in a SaaS platform. Use this to assess vendor controls, data handling practices, access controls, and compliance posture before approving SaaS AI feature enablement.

---

## Review Information

| Field | Response |
|-------|----------|
| **SaaS Platform** | |
| **AI Feature Name** | |
| **Vendor / Provider** | |
| **Review Date** | |
| **Reviewed By** | |
| **Business Requestor** | |

---

## Section 1 — Vendor and Contract Review

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 1.1 | Vendor has a signed enterprise agreement with data processing terms | ☐ Yes ☐ No ☐ In Progress | |
| 1.2 | AI-specific data handling terms are documented in the contract or addendum | ☐ Yes ☐ No ☐ Unknown | |
| 1.3 | Vendor has published a privacy policy that covers AI feature data usage | ☐ Yes ☐ No ☐ Unknown | |
| 1.4 | Vendor confirms enterprise data is not used to train AI models (opt-out confirmed) | ☐ Yes ☐ No ☐ Unknown | |
| 1.5 | Data retention periods for AI prompts and outputs are defined and acceptable | ☐ Yes ☐ No ☐ Unknown | |
| 1.6 | Vendor provides evidence of relevant certifications (SOC 2, ISO 27001, etc.) | ☐ Yes ☐ No ☐ Unknown | |
| 1.7 | Breach notification obligations cover AI-processed data | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 2 — Data Handling and Residency

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 2.1 | Data residency region for AI-processed data is known and acceptable | ☐ Yes ☐ No ☐ Unknown | |
| 2.2 | AI feature does not transfer data to jurisdictions restricted by company policy | ☐ Yes ☐ No ☐ Unknown | |
| 2.3 | Enterprise data is logically separated from other tenants | ☐ Yes ☐ No ☐ Unknown | |
| 2.4 | Data classification has been assessed for all data the AI feature can access | ☐ Yes ☐ No ☐ Unknown | |
| 2.5 | Regulated data (PCI, HIPAA, GDPR, PIPEDA, etc.) is identified and appropriate controls are in place | ☐ Yes ☐ No ☐ N/A | |
| 2.6 | Customer data exposure through AI outputs has been assessed | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 3 — Access Control

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 3.1 | The AI feature respects existing user role-based access controls (RBAC) | ☐ Yes ☐ No ☐ Unknown | |
| 3.2 | The AI feature does not surface data that users should not have access to | ☐ Yes ☐ No ☐ Unknown | |
| 3.3 | Admin controls are available to limit AI feature scope (data sources, user groups) | ☐ Yes ☐ No ☐ Unknown | |
| 3.4 | The AI feature can be disabled or restricted at the tenant / org level | ☐ Yes ☐ No ☐ Unknown | |
| 3.5 | Users cannot enable AI features individually without IT / admin approval | ☐ Yes ☐ No ☐ Unknown | |
| 3.6 | Third-party plugins or extensions connected to the AI feature are reviewed | ☐ Yes ☐ No ☐ N/A | |

---

## Section 4 — Logging and Auditability

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 4.1 | Audit logs are available for AI-assisted user actions | ☐ Yes ☐ No ☐ Unknown | |
| 4.2 | Logs are retained for a sufficient period to support incident investigation | ☐ Yes ☐ No ☐ Unknown | |
| 4.3 | Logs are exportable or accessible via API for SIEM integration | ☐ Yes ☐ No ☐ Unknown | |
| 4.4 | AI feature activity is attributable to individual users | ☐ Yes ☐ No ☐ Unknown | |
| 4.5 | Prompt and output logging is available (where required for compliance) | ☐ Yes ☐ No ☐ N/A | |

---

## Section 5 — Feature Enablement and Change Management

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 5.1 | IT / security is notified before new AI features are enabled by default | ☐ Yes ☐ No ☐ Unknown | |
| 5.2 | A process exists to review and approve vendor-initiated AI feature updates | ☐ Yes ☐ No ☐ No | |
| 5.3 | AI feature scope and permissions can be reviewed after vendor updates | ☐ Yes ☐ No ☐ Unknown | |
| 5.4 | The vendor provides release notes or advance notice for AI feature changes | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 6 — Acceptable Use and End User Controls

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 6.1 | Acceptable use guidance for this AI feature has been communicated to users | ☐ Yes ☐ No ☐ Planned | |
| 6.2 | Users understand what data they should and should not use with the AI feature | ☐ Yes ☐ No ☐ Planned | |
| 6.3 | A process exists for users to report incorrect or harmful AI outputs | ☐ Yes ☐ No ☐ Planned | |

---

## Section 7 — Risk Summary

**Overall Risk Rating:**
- [ ] Low — no significant gaps identified
- [ ] Moderate — some gaps; conditions required before enabling
- [ ] High — significant gaps; feature should not be enabled until remediated
- [ ] Critical — feature should not be enabled; escalate to risk owner

**Key Findings:**

| # | Finding | Severity | Recommendation |
|---|---------|----------|----------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

**Conditions for Approval (if applicable):**

> *(List any conditions that must be met before this AI feature can be enabled.)*

---

## Section 8 — Decision

| Field | Response |
|-------|----------|
| **Decision** | ☐ Approved ☐ Approved with Conditions ☐ Deferred ☐ Rejected |
| **Decision Date** | |
| **Decision Made By** | |
| **Next Review Date** | |
| **Notes** | |
