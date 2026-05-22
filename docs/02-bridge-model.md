# 02 — The BRIDGE Model

## Full Model Reference

| Letter | Capability | Objective |
|--------|-----------|-----------|
| **B** | Baseline AI Usage | Discover where and how AI is being used |
| **R** | Regulate Access & Data Flow | Control AI access, prompts, uploads, outputs, and agent permissions |
| **I** | Identify AI Risk & Threats | Assess AI-specific risks using threat modeling and risk analysis |
| **D** | Design Secure AI Controls | Extend security controls to AI systems, SaaS AI, coding agents, and embedded AI |
| **G** | Govern AI Lifecycle | Define policy, ownership, approvals, education, and compliance |
| **E** | Evidence, Assurance & Enablement | Prove controls work and enable safe AI adoption |

---

## B — Baseline AI Usage

Establish visibility into AI usage across the enterprise. Before securing AI, the organization must understand where AI is being used, who is using it, what data is involved, and what business outcomes are expected.

### What to Discover

**Browser-Based AI**
- Which AI sites are being accessed
- Which users and departments are accessing them
- Whether access is approved, tolerated, or prohibited
- Whether sensitive data is being uploaded or pasted
- Whether files, source code, credentials, or customer data are involved

**SaaS Platform AI**
- Which SaaS platforms have AI features enabled
- What enterprise data the AI feature can access
- Whether access controls are inherited correctly
- Whether prompts and outputs are logged
- Whether customer data is used for model training

**Coding Agents and Developer AI**
- Which AI coding tools are in use
- Whether insecure code is being generated
- Whether secrets or credentials are at risk
- Whether AI-generated code is reviewed before merge

**Business and Security Tool AI**
- Data sensitivity of AI-assisted workflows
- Level of autonomy in AI-driven decisions
- Regulatory relevance of AI-processed data

### Key Outputs
- AI inventory
- AI use case register
- AI access map
- AI tool classification
- Shadow AI visibility report
- Department-level AI usage view

---

## R — Regulate Access & Data Flow

Control how users, devices, browsers, SaaS platforms, applications, and agents interact with AI.

### AI Tool Access Tiers

| Tier | Description | Treatment |
|------|-------------|-----------|
| Approved | Reviewed and authorized | Allow with monitoring |
| Restricted | Allowed for limited use cases | Allow with warning and DLP |
| Tolerated | Not formally approved but not blocked | Monitor and educate |
| Prohibited | High-risk or non-compliant | Block |
| Unknown | Newly discovered | Investigate |

### Key Control Areas
- Browser-layer controls (SWG, CASB, enterprise browser, DLP)
- Data flow controls by data classification
- Agent permission controls (least privilege, human approval gates, kill switches)
- SaaS AI feature access management

### Key Outputs
- AI access policy
- Browser control policy
- AI DLP rule set
- AI site categorization
- Agent permission model
- SaaS AI access control baseline

---

## I — Identify AI Risk & Threats

Identify which AI threats apply to each use case through risk analysis and threat modeling.

### Key Threat Categories

| Risk Area | Description |
|-----------|-------------|
| Data leakage | Sensitive data entered into AI tools or exposed through AI outputs |
| Prompt injection | Malicious instructions hidden in documents, websites, emails, tickets, or code |
| Insecure output | AI-generated content that is wrong, unsafe, biased, or misleading |
| Excessive agency | AI agents performing unauthorized or harmful actions |
| Insecure code generation | AI-generated code introducing vulnerabilities |
| Third-party exposure | AI vendors, APIs, plugins, and SaaS integrations introducing supply chain risk |
| Access control failure | AI surfacing data users should not be able to access |
| Model misuse | AI used for prohibited, unethical, or non-compliant activities |
| Lack of transparency | Inability to explain AI behavior, data usage, or decision logic |
| Weak monitoring | Lack of logs, alerts, or evidence for AI activity |

### Key Outputs
- AI risk assessment
- AI threat model
- AI misuse case library
- Agent risk profile
- SaaS AI risk assessment
- Coding assistant risk review

---

## D — Design Secure AI Controls

Design and implement controls that reduce AI-specific risks while enabling responsible adoption.

### Control Categories
- Secure AI development (architecture, SDLC, input/output validation)
- Coding agent security (code review, SAST/DAST, secrets scanning)
- SaaS AI security (vendor terms, data retention, audit logs)
- Business tool AI security (human review, audit trail, escalation paths)
- Security tool AI security (detection logic validation, analyst oversight)
- Agentic AI controls (permission boundaries, sandboxing, kill switches)

### Key Outputs
- AI security control baseline
- Secure AI architecture checklist
- Coding agent security standard
- SaaS AI review checklist
- Agentic AI control framework
- AI testing and validation plan

---

## G — Govern AI Lifecycle

Create governance structures that manage AI from idea to retirement.

### Lifecycle Stages

| Stage | Governance Activity |
|-------|---------------------|
| Intake | Capture proposed AI use case |
| Classification | Assess business purpose, data, risk, and autonomy |
| Review | Security, privacy, legal, compliance, architecture, and business review |
| Approval | Approve, reject, restrict, or request remediation |
| Deployment | Implement controls and monitoring |
| Operation | Monitor usage, risk, performance, and incidents |
| Change | Reassess when data, model, vendor, or autonomy changes |
| Retirement | Remove access, revoke integrations, archive evidence |

### Key Outputs
- AI governance policy
- AI acceptable use standard
- AI intake workflow
- AI risk acceptance process
- AI impact assessment
- AI roles and responsibilities matrix
- AI education and awareness plan

---

## E — Evidence, Assurance & Enablement

Demonstrate that AI controls are working and enable the organization to use AI safely.

### Assurance Activities
- Control testing (DLP, blocked sites, prompt injection, agent permissions)
- Evidence collection (inventory, assessments, logs, test results)
- Metrics and reporting (approved use cases, shadow AI, incidents, training completion)

### Enablement
- Approved AI tool catalog
- Safe prompting guidance
- Secure coding assistant guidance
- Developer guardrails
- Business user training
- AI security maturity scorecard

### Key Outputs
- AI assurance dashboard
- AI control testing report
- AI evidence library
- AI executive reporting pack
- AI adoption enablement guide
- AI security maturity scorecard
