# 04 — AI Use Case Taxonomy

## Why Taxonomy Matters

Not all AI use cases carry the same risk. A grammar-checking tool and an autonomous agent with access to financial systems require very different security approaches.

Classifying AI use cases across consistent dimensions allows security, risk, and governance teams to:
- Apply proportionate controls based on actual risk
- Prioritize review effort on high-impact use cases
- Build a structured AI inventory that supports compliance and audit
- Identify patterns of high-risk adoption early

---

## Primary Use Case Categories

### 1. Browser-Based GenAI Tools
Users accessing public or third-party AI tools through a web browser.

| Attribute | Notes |
|-----------|-------|
| Access method | Browser |
| Data exposure risk | High — user-controlled |
| Control point | Browser layer (SWG, CASB, DLP) |
| Examples | ChatGPT, Claude, Gemini, Perplexity |
| Key concern | Sensitive data uploaded or pasted |

---

### 2. AI Embedded in SaaS Platforms
AI features within enterprise SaaS tools that operate on existing business data.

| Attribute | Notes |
|-----------|-------|
| Access method | SaaS platform (approved) |
| Data exposure risk | Medium to High — inherits platform data access |
| Control point | SaaS admin controls, vendor review |
| Examples | Microsoft 365 Copilot, Salesforce Einstein, Slack AI |
| Key concern | AI feature accessing data beyond user's intended scope |

---

### 3. Coding Assistants and Developer AI
AI tools used by developers to generate, review, test, or refactor code.

| Attribute | Notes |
|-----------|-------|
| Access method | IDE plugin, browser, CLI |
| Data exposure risk | High — source code, secrets, architecture |
| Control point | Developer policy, code scanning, repo access controls |
| Examples | GitHub Copilot, Cursor, Windsurf, CodeWhisperer |
| Key concern | Insecure code generation, secret leakage, IP exposure |

---

### 4. Autonomous Agents and Agentic AI
AI systems that can take actions, call APIs, execute workflows, or operate with minimal human oversight.

| Attribute | Notes |
|-----------|-------|
| Access method | API, platform, orchestration layer |
| Data exposure risk | Very High — agents may access and modify data |
| Control point | Agent permission model, human approval gates |
| Examples | AI workflow automation, autonomous coding agents |
| Key concern | Excessive agency, unreviewed actions, cascading failures |

---

### 5. AI in Business Applications
AI features embedded in business tools used for reporting, analytics, HR, finance, or customer interaction.

| Attribute | Notes |
|-----------|-------|
| Access method | Business application |
| Data exposure risk | Medium to High — depends on data classification |
| Control point | Application-level controls, human review requirements |
| Examples | AI-generated reports, AI-assisted customer support |
| Key concern | Decision impact, regulatory relevance, audit trail |

---

### 6. AI in Security Tools
AI capabilities within security platforms (SIEM, SOAR, EDR, IAM, GRC, DLP, vulnerability management).

| Attribute | Notes |
|-----------|-------|
| Access method | Security platform |
| Data exposure risk | High — security data is sensitive by nature |
| Control point | Detection logic validation, analyst oversight |
| Examples | AI-powered alert triage, automated response |
| Key concern | False positives, over-automation, unreviewed decisions |

---

## Risk Classification Dimensions

Use these dimensions to score each AI use case:

| Dimension | Low | Medium | High |
|-----------|-----|--------|------|
| **Data Sensitivity** | Public data | Internal data | Confidential, regulated, or PII |
| **Level of Autonomy** | Human-driven | AI-assisted | Fully autonomous |
| **Business Impact** | Low criticality | Moderate criticality | High criticality |
| **Access Scope** | Read-only, limited | Read internal systems | Read/write, broad access |
| **Regulatory Relevance** | No regulation | Moderate regulation | Highly regulated (HIPAA, PCI, SOX) |
| **Third-Party Involvement** | Internal only | Approved vendor | Unapproved or unknown vendor |

---

## Use Case Classification Matrix

| Risk Score | Classification | Review Requirement |
|-----------|----------------|-------------------|
| 1–2 dimensions High | Moderate Risk | Standard review |
| 3–4 dimensions High | High Risk | Full security, privacy, legal, compliance review |
| 5–6 dimensions High | Critical Risk | Executive sign-off, enhanced monitoring, formal approval |

---

## Use Case Register Fields

Each AI use case in the inventory should capture:

| Field | Description |
|-------|-------------|
| Use Case ID | Unique identifier |
| Name | Short descriptive name |
| Business Owner | Person accountable for the use case |
| Technology Owner | Person responsible for implementation |
| Category | Browser / SaaS / Coding / Agentic / Business / Security |
| AI Tool / Vendor | Name of AI platform or tool |
| Data Classification | Public / Internal / Confidential / Regulated |
| Autonomy Level | Assisted / Automated / Autonomous |
| Regulatory Scope | Applicable regulations or frameworks |
| Risk Rating | Low / Moderate / High / Critical |
| Status | Proposed / Under Review / Approved / Restricted / Prohibited / Retired |
| Review Date | Date of last review |
| Next Review | Scheduled reassessment date |

---

## Related Documents

- [02 — The BRIDGE Model](02-bridge-model.md)
- [05 — AI Risk and Threat Modeling](05-ai-risk-and-threat-modeling.md)
- [07 — AI Governance Lifecycle](07-ai-governance-lifecycle.md)
- [Templates — AI Use Case Intake](../templates/ai-use-case-intake-template.md)
