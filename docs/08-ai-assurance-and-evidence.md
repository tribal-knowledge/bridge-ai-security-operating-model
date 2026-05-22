# 08 — AI Assurance and Evidence

## Purpose

The **E — Evidence, Assurance & Enablement** component of BRIDGE focuses on proving that AI controls are working and enabling the organization to use AI safely and confidently.

AI security programs must be able to demonstrate control effectiveness to executives, auditors, regulators, customers, and internal stakeholders. Assurance is not a one-time exercise — it is a continuous process.

---

## Assurance Activities

### Control Testing

| Test | Description |
|------|-------------|
| DLP rule testing for AI uploads | Verify that DLP policies correctly detect and block sensitive data uploads to AI tools |
| Blocked AI site testing | Confirm that prohibited AI tools are blocked across all user devices and browsers |
| Prompt injection testing | Test AI systems against known prompt injection techniques |
| Agent permission boundary testing | Verify that agents cannot exceed their defined permission scope |
| AI-generated code quality review | Sample and assess AI-generated code for security flaws |
| SaaS AI access control testing | Confirm role-based access inheritance is correctly applied in SaaS AI features |
| Audit log validation | Verify that AI system actions are logged completely and accurately |
| Tabletop exercises | Simulate AI-related incident scenarios to test response readiness |
| AI red team exercises | Conduct adversarial testing of AI systems to identify manipulation risks |

---

## Evidence Collection

A mature AI security program maintains an evidence library that supports audit, compliance, and executive reporting.

| Evidence Type | Description |
|---------------|-------------|
| AI inventory | Current list of all AI use cases with classification and status |
| Approved use case register | Record of approved AI use cases with decision documentation |
| Risk assessments | Completed risk assessments for each AI use case |
| Threat models | Documented threat models for high-risk AI use cases |
| Vendor reviews | Completed SaaS AI vendor review checklists and findings |
| Security test results | Outcomes from DLP tests, red team exercises, and control validation |
| DLP reports | Logs of AI-related DLP events and actions taken |
| Browser access logs | AI site access logs showing approved vs unapproved tool usage |
| SaaS configuration exports | Evidence of SaaS AI configuration settings and access controls |
| Training completion records | Evidence that employees completed AI awareness training |
| Executive risk reports | AI risk posture reports presented to leadership |

---

## Metrics and Reporting

### Program Metrics

| Metric | Description |
|--------|-------------|
| Approved AI use cases | Number of formally reviewed and approved AI use cases |
| Shadow AI tools discovered | Number of unapproved AI tools identified through monitoring |
| High-risk AI tools blocked | Number of prohibited AI tools blocked per period |
| Sensitive data upload attempts prevented | DLP events where AI uploads were blocked |
| AI risk assessments completed | Assessments completed vs total use cases requiring assessment |
| AI vendor reviews completed | Vendor assessments completed vs total SaaS AI platforms in use |
| Employees trained on AI policy | Percentage of target population completing AI awareness training |
| Agentic AI use cases reviewed | Number of autonomous agent use cases formally assessed |
| AI-related incidents or near misses | Security events attributed to AI use |
| Control maturity by BRIDGE domain | Self-assessed or independently assessed maturity score per domain |

### Reporting Cadence

| Audience | Frequency | Content |
|----------|-----------|---------|
| Executive leadership | Quarterly | AI risk posture, key metrics, material incidents, maturity progress |
| Security and risk committee | Monthly | Program metrics, control testing results, emerging threats |
| Audit and compliance | As required | Evidence library, control documentation, policy alignment |
| Board (if applicable) | Annually | AI governance maturity, strategic risk, regulatory position |

---

## AI Assurance Dashboard

An AI assurance dashboard should provide at-a-glance visibility into:

- Total AI use cases (approved / under review / restricted / prohibited / retired)
- Shadow AI discovery trend
- DLP events — AI upload attempts (blocked vs allowed)
- AI risk assessment completion rate
- Control testing coverage
- Training completion rate
- AI-related incidents (open / resolved)
- Maturity score by BRIDGE domain

---

## Enablement

Assurance is paired with enablement — helping the business adopt AI safely rather than simply blocking it.

| Enablement Asset | Description |
|-----------------|-------------|
| Approved AI tool catalog | Current list of approved AI tools with guidance on appropriate use |
| Safe prompting guidance | How to use AI tools effectively without exposing sensitive data |
| Secure coding assistant guidance | How developers should use AI coding tools securely |
| AI use case templates | Standardized forms for proposing and documenting AI use cases |
| Developer guardrails | Technical controls and coding standards for AI-assisted development |
| Business user training | AI literacy and responsible use training for non-technical staff |
| Security patterns for AI adoption | Reference architecture for common AI use case types |
| FAQs and decision trees | Self-service guidance for common questions about AI use |

---

## Key Outputs

- AI assurance dashboard
- AI control testing report
- AI evidence library
- AI executive reporting pack
- AI adoption enablement guide
- AI security maturity scorecard

---

## Related Documents

- [02 — The BRIDGE Model](02-bridge-model.md)
- [07 — AI Governance Lifecycle](07-ai-governance-lifecycle.md)
- [09 — Maturity Model](09-maturity-model.md)
