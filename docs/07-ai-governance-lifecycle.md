# 07 — AI Governance Lifecycle

## Purpose

The **G — Govern** component of BRIDGE establishes the structures, processes, and roles required to manage AI from initial proposal through to retirement.

AI governance should not be a one-time approval. It should be a **lifecycle process** — continuously reassessed as the AI system, its data, its vendor, or its level of autonomy changes.

---

## Lifecycle Stages

| Stage | Description | Governance Activity |
|-------|-------------|---------------------|
| **Intake** | A new AI use case is proposed | Capture use case details using the intake template |
| **Classification** | Assess the nature and risk of the use case | Classify by category, data sensitivity, autonomy, and business impact |
| **Review** | Multi-disciplinary review of the proposal | Security, privacy, legal, compliance, architecture, and business review |
| **Approval** | Decision on whether the use case can proceed | Approve, reject, restrict to specific conditions, or request remediation |
| **Deployment** | Use case is implemented in the environment | Implement required controls, confirm monitoring is in place |
| **Operation** | Use case is live and in active use | Monitor usage, risk indicators, performance, and incidents |
| **Change** | Something material changes about the use case | Trigger reassessment when data, model, vendor, autonomy, or scope changes |
| **Retirement** | Use case is discontinued | Remove access, revoke integrations, archive evidence and documentation |

---

## Governance Roles and Responsibilities

| Role | Responsibility |
|------|---------------|
| **Business Owner** | Defines the business purpose and expected outcome. Accountable for appropriate use. |
| **Technology Owner** | Responsible for implementation, operation, and technical controls. |
| **Data Owner** | Approves the use of specific data assets within the AI use case. |
| **Security Owner** | Reviews security risk, threat model, and control adequacy. |
| **Privacy Owner** | Assesses privacy impact and data protection compliance. |
| **Legal/Compliance Owner** | Reviews regulatory obligations, contractual requirements, and acceptable use boundaries. |
| **Risk Owner** | Accepts, remediates, or escalates residual risk. |
| **User Community** | Uses AI responsibly in accordance with policy and training. |

---

## AI Governance Policy Areas

The following policy areas should be addressed in an enterprise AI governance program:

| Policy Area | Key Questions to Address |
|-------------|--------------------------|
| **Acceptable AI use** | What AI use is permitted? For which purposes? |
| **Prohibited AI use** | What AI use is never permitted? |
| **Data handling** | What data can be used with AI? What cannot? |
| **Public AI tools** | What rules apply to browser-based GenAI tools? |
| **SaaS AI features** | How are AI features in SaaS platforms governed? |
| **Coding assistants** | What rules apply to AI-assisted code generation? |
| **Autonomous agents** | What controls are required for agentic AI? |
| **Human oversight** | When is human review required before AI-assisted actions? |
| **AI-generated content** | How must AI-generated content be labeled or reviewed? |
| **AI vendor risk** | How are AI vendors assessed and monitored? |
| **Audit and evidence** | What must be logged and retained for AI systems? |
| **Incident response** | How are AI-related incidents identified, escalated, and managed? |

---

## AI Intake Process

When a business or technology team proposes a new AI use case, the following process should be followed:

1. **Submission** — Business owner submits an intake form describing the use case, business purpose, data involved, AI tool or vendor, and intended users
2. **Initial Triage** — Governance team classifies the use case by category and initial risk level
3. **Review Assignment** — Relevant reviewers (security, privacy, legal, compliance, architecture) are assigned based on risk classification
4. **Assessment** — Each reviewer assesses the use case against their domain requirements
5. **Decision** — Governance authority makes an approval decision (Approve / Restrict / Reject / Remediate)
6. **Conditions** — Any conditions, controls, or monitoring requirements are documented
7. **Notification** — Business owner is informed of the decision and next steps
8. **Deployment Support** — Technology owner implements required controls before go-live
9. **Ongoing Review** — Use case is added to the AI inventory and scheduled for periodic reassessment

---

## Approval Decision Framework

| Decision | Meaning | Conditions |
|----------|---------|------------|
| **Approved** | Use case is authorized for deployment | Standard controls must be in place |
| **Approved with Conditions** | Use case is authorized with specific requirements | Conditions must be met and verified before go-live |
| **Restricted** | Use case is approved for limited scope or audience | Restrictions are formally documented |
| **Rejected** | Use case is not approved | Business owner may appeal with additional controls or scope changes |
| **Deferred** | Additional information is needed before a decision | Specific information requested before reassessment |
| **Remediate and Resubmit** | Use case can be approved if specific issues are resolved | Remediation requirements are documented |

---

## Change Triggers — When to Reassess

An approved AI use case should be reassessed whenever any of the following occur:

- The AI model or vendor changes
- The data classification or data types involved change
- The level of autonomy increases
- The user population or access scope expands significantly
- A security incident or near miss occurs
- The vendor changes their data handling, training, or retention practices
- New regulatory requirements apply to the use case
- Material changes occur in the business process the AI supports

---

## AI Education and Awareness

Governance only works if users understand the policies. An effective AI awareness program should cover:

| Audience | Content |
|----------|---------|
| All employees | Acceptable use policy, what data can and cannot be used with AI, how to report concerns |
| Developers | Coding assistant security, code review requirements, secret handling |
| Business users | Safe prompting, output verification, escalation when AI is wrong |
| Managers and leaders | AI risk posture, oversight responsibilities, incident escalation |
| Security and risk teams | BRIDGE model, threat modeling methods, assurance requirements |

---

## Key Outputs

- AI governance policy and acceptable use standard
- AI intake workflow and submission form
- AI risk acceptance process
- AI impact assessment template
- AI roles and responsibilities matrix
- AI education and awareness plan
- AI use case register (ongoing)

---

## Related Documents

- [02 — The BRIDGE Model](02-bridge-model.md)
- [04 — AI Use Case Taxonomy](04-ai-use-case-taxonomy.md)
- [08 — AI Assurance and Evidence](08-ai-assurance-and-evidence.md)
- [Templates — AI Use Case Intake](../templates/ai-use-case-intake-template.md)
- [Templates — AI Risk Assessment](../templates/ai-risk-assessment-template.md)
