# 06 — AI Security Controls

## Purpose

The **D — Design** component of BRIDGE focuses on implementing security controls that reduce AI-specific risks while enabling responsible adoption. This document provides control guidance organized by AI use case type, extending existing cybersecurity practices into AI-enabled environments.

---

## Secure AI Development

For organizations building or customizing AI systems internally.

| Control | Description |
|---------|-------------|
| Secure architecture review | Review AI system design for security risks before build |
| Secure SDLC integration | Embed AI security requirements into development lifecycle |
| Data classification | Classify data used for training, fine-tuning, and inference |
| Model access control | Restrict who can query, retrain, or deploy models |
| Input validation | Validate and sanitize all inputs before passing to AI models |
| Output validation | Review and filter AI outputs before presenting to users or systems |
| Logging and monitoring | Log all inference requests, outputs, and model actions |
| Abuse case testing | Test the AI system against known misuse and manipulation scenarios |
| Red teaming | Conduct adversarial testing to identify prompt injection and bypass risks |
| Deployment controls | Control who can deploy AI models and into which environments |
| Incident response planning | Define response procedures for AI-specific incidents |

---

## Coding Agent Security

For organizations using AI coding assistants (GitHub Copilot, Cursor, Windsurf, CodeWhisperer, Replit, etc.).

| Control | Description |
|---------|-------------|
| Require human code review | All AI-generated code must be reviewed before merging |
| Scan AI-generated code | Apply SAST to all AI-generated code contributions |
| Run SAST, DAST, SCA, secrets scanning | Include in CI/CD pipeline regardless of code origin |
| Restrict repository access | Limit coding assistant scope to only necessary repositories |
| Control extension/plugin permissions | Review and restrict IDE plugin permissions |
| Monitor for insecure patterns | Flag AI suggestions that include known-insecure code patterns |
| Validate open-source license risk | Review AI-suggested libraries for license compatibility |
| Require secure coding standards | Apply the same standards to AI-generated code as human-written code |
| Block secret suggestions | Configure tools to prevent AI from suggesting credentials or keys |
| Log coding assistant usage | Maintain audit trail of AI-assisted contributions |

---

## SaaS AI Security

For AI features embedded in enterprise SaaS platforms (Microsoft 365 Copilot, Salesforce Einstein, Slack AI, etc.).

| Control | Description |
|---------|-------------|
| Review vendor AI terms | Understand data usage, training, retention, and sharing policies |
| Validate data retention settings | Ensure AI features do not retain data longer than required |
| Confirm model training opt-out | Verify enterprise data is not used to train vendor models |
| Review admin controls | Assess what controls exist to limit AI feature access and scope |
| Validate role-based access inheritance | Confirm AI features respect existing access controls |
| Review audit logs | Ensure AI-assisted actions are logged and attributable |
| Assess data residency | Confirm data processed by AI stays within required regions |
| Monitor AI feature enablement | Alert when new AI features are enabled by vendor update |
| Require contractual and compliance evidence | Obtain written commitments on data handling from vendors |
| Apply least-privilege scoping | Limit AI features to only the data and functions required |

---

## Business Tool AI Security

For AI features in business applications used for reporting, analytics, HR, finance, or customer interaction.

| Control | Description |
|---------|-------------|
| Define acceptable use | Specify which data and decisions AI can assist with |
| Require human review for material decisions | High-impact AI outputs require human validation before action |
| Validate output accuracy | Establish processes to verify AI-generated content before use |
| Prevent sensitive data exposure | Restrict which data fields AI features can access and include in outputs |
| Maintain audit trail | Log AI-assisted decisions with context and timestamp |
| Define escalation paths | Establish process when AI output is incorrect or disputed |
| Monitor business impact | Track outcomes of AI-assisted decisions over time |

---

## Security Tool AI Security

For AI capabilities within SIEM, SOAR, EDR, IAM, GRC, DLP, and vulnerability management platforms.

| Control | Description |
|---------|-------------|
| Validate detection logic | Review how AI generates or influences security alerts |
| Review alert enrichment accuracy | Assess false positive and false negative rates of AI enrichment |
| Maintain analyst oversight | Require human review before AI-driven response actions |
| Prevent automated over-response | Set boundaries on what AI can automatically take action on |
| Monitor false positive/negative rates | Track AI detection quality over time |
| Log AI-assisted decisions | Attribute decisions to AI vs human for post-incident review |
| Validate integration permissions | Ensure AI security tools have least-privilege access to data sources |

---

## Agentic AI Controls

For autonomous agents that can take actions, call APIs, send messages, or execute workflows.

| Control | Description |
|---------|-------------|
| Define allowed actions | Explicitly list what the agent is permitted to do |
| Limit tool access | Restrict which tools and APIs the agent can call |
| Require approval for high-risk actions | Define action categories that require human approval before execution |
| Sandbox execution | Run agents in isolated environments where possible |
| Restrict memory | Limit what the agent can retain across sessions |
| Monitor agent behavior | Log and alert on unexpected or anomalous agent actions |
| Apply rate limits | Limit the volume of actions an agent can perform in a given period |
| Maintain rollback capability | Ensure agent actions can be reversed or remediated |
| Implement kill switches | Provide mechanism to halt agent operation immediately |
| Full audit logging | Log every action taken by the agent with full context |

---

## Control Baseline Summary

| AI Type | Top 3 Controls |
|---------|---------------|
| Browser-Based GenAI | DLP at upload, URL categorization, user coaching |
| SaaS AI | Vendor review, access control validation, audit log review |
| Coding Agents | Human code review, SAST/secrets scanning, repo access restriction |
| Business Tool AI | Human review for material decisions, audit trail, output accuracy validation |
| Security Tool AI | Analyst oversight, detection logic validation, false positive monitoring |
| Agentic AI | Permission boundaries, human approval gates, kill switch |

---

## Related Documents

- [03 — Browser as AI Gateway](03-browser-as-ai-gateway.md)
- [05 — AI Risk and Threat Modeling](05-ai-risk-and-threat-modeling.md)
- [07 — AI Governance Lifecycle](07-ai-governance-lifecycle.md)
- [Templates — SaaS AI Review Checklist](../templates/ai-saas-review-checklist.md)
- [Templates — Coding Agent Security Checklist](../templates/coding-agent-security-checklist.md)
- [Templates — Agentic AI Control Checklist](../templates/agentic-ai-control-checklist.md)
