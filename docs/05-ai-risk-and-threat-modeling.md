# 05 — AI Risk and Threat Modeling

## Purpose

Threat modeling and risk analysis are the foundation of the **I — Identify** component of BRIDGE. Before designing controls, teams must understand what can go wrong for each AI use case — what threats apply, what the impact would be, and how likely they are given the context.

AI risks vary significantly based on the use case, data involved, model type, access level, degree of autonomy, and business impact. A one-size-fits-all approach is not sufficient.

---

## Key AI Threat Categories

| Risk Area | Description | Example |
|-----------|-------------|---------|
| **Data leakage** | Sensitive data entered into AI tools or exposed through AI outputs | Employee pastes client contract into a public GenAI tool |
| **Prompt injection** | Malicious instructions hidden in documents, websites, emails, tickets, or code | A document fed to an AI agent contains instructions to exfiltrate data |
| **Insecure output** | AI-generated content that is wrong, unsafe, biased, or misleading | AI produces incorrect legal guidance presented as fact |
| **Excessive agency** | AI agents performing unauthorized or harmful actions | Agent deletes records or sends unapproved communications |
| **Insecure code generation** | AI-generated code introducing vulnerabilities | Coding assistant generates SQL with injection flaws |
| **Third-party exposure** | AI vendors, APIs, plugins, and SaaS integrations introducing supply chain risk | AI vendor uses customer data to train models without consent |
| **Access control failure** | AI surfacing data users should not be able to access | AI tool exposes documents from other departments |
| **Model misuse** | AI used for prohibited, unethical, or non-compliant activities | AI used to generate misleading communications or bypass controls |
| **Lack of transparency** | Inability to explain AI behavior, data usage, or decision logic | Unable to audit AI-assisted hiring decision |
| **Weak monitoring** | Lack of logs, alerts, or evidence for AI activity | AI agent actions not recorded in any audit trail |

---

## Threat Modeling Methods Applicable to AI

| Method | Best For |
|--------|----------|
| **STRIDE** | Systematic threat identification across Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege |
| **PASTA** | Risk-centric threat modeling aligned to business objectives |
| **OWASP Top 10 for LLM Applications** | LLM-specific vulnerability taxonomy (prompt injection, insecure output, training data poisoning, etc.) |
| **MITRE ATLAS** | Adversarial threat landscape for AI systems — attacker tactics and techniques |
| **NIST AI RMF** | Governance-aligned risk management for AI systems |
| **Abuse Case Modeling** | Identifying how AI systems could be misused by insiders, adversaries, or the AI itself |
| **Data Flow Diagrams (DFD)** | Mapping data movement into, through, and out of AI systems to identify exposure points |
| **AI System Cards** | Documenting model behavior, limitations, intended use, and known failure modes |

---

## STRIDE Applied to AI Use Cases

| STRIDE Category | AI Context | Example Threat |
|----------------|------------|----------------|
| **Spoofing** | Impersonating a trusted user or system to manipulate AI | Attacker uses stolen credentials to interact with an enterprise AI agent |
| **Tampering** | Modifying inputs to manipulate AI behavior | Prompt injection through a document uploaded by an external user |
| **Repudiation** | AI actions that cannot be attributed or audited | Agent performs an action with no log trail |
| **Information Disclosure** | AI exposing data to unauthorized parties | AI tool returns confidential data in response to an unrelated query |
| **Denial of Service** | Disrupting AI availability or degrading performance | Flooding an AI endpoint with requests |
| **Elevation of Privilege** | AI operating with permissions beyond what was intended | Agent inherits admin-level permissions through misconfigured integration |

---

## Risk Assessment Questions by Use Case Type

### For All AI Use Cases
- What data does the AI use case process?
- What is the data classification?
- Can users upload files or paste data?
- Are prompts and outputs logged?
- Can the system explain how results were generated?
- What happens if the AI is wrong?
- What happens if the AI is manipulated?

### For Agentic AI Use Cases (Additional)
- Can the AI access internal systems?
- Can the AI take action (write, delete, send, execute)?
- Can the AI call external APIs?
- Can external content influence prompts (prompt injection risk)?
- Is there human review before important decisions?
- Are there rate limits, transaction limits, or kill switches?
- What is the blast radius if the agent behaves unexpectedly?

### For SaaS AI Features (Additional)
- What enterprise data does the AI feature have access to?
- Does the AI feature use customer data for model training?
- Can the feature be enabled by end users without IT review?
- Are audit logs available for AI-assisted actions?
- Does the vendor provide data residency and retention controls?

### For Coding Assistants (Additional)
- Does the coding assistant have access to private repositories?
- Can it see secrets, API keys, or credentials in code?
- Is AI-generated code reviewed before merging?
- Does the tool suggest vulnerable or deprecated libraries?

---

## Risk Scoring Approach

For each identified threat, assess:

| Factor | Options |
|--------|---------|
| **Likelihood** | Low / Medium / High |
| **Impact** | Low / Medium / High |
| **Existing Controls** | None / Partial / Sufficient |
| **Residual Risk** | Low / Moderate / High / Critical |

A simple risk matrix:

| | **Low Impact** | **Medium Impact** | **High Impact** |
|-|---------------|------------------|----------------|
| **High Likelihood** | Moderate | High | Critical |
| **Medium Likelihood** | Low | Moderate | High |
| **Low Likelihood** | Low | Low | Moderate |

---

## Misuse Case Examples

| Actor | Misuse Scenario | Risk |
|-------|----------------|------|
| Malicious insider | Uses AI to exfiltrate confidential data in an authorized session | Data breach |
| External attacker | Crafts a prompt injection via a customer email to manipulate an AI agent | Unauthorized action |
| Negligent employee | Pastes regulated customer data into a public AI tool | Compliance violation |
| Compromised vendor | AI vendor exposes enterprise data through a security breach | Third-party risk |
| AI system itself | Hallucinates and produces inaccurate output that drives a bad business decision | Decision integrity failure |

---

## Key Outputs

- AI risk assessment (per use case)
- AI threat model (STRIDE, OWASP, MITRE ATLAS mapping)
- AI misuse case library
- Agent risk profile (for agentic use cases)
- SaaS AI risk assessment (per platform)
- Coding assistant risk review

---

## Related Documents

- [02 — The BRIDGE Model](02-bridge-model.md)
- [04 — AI Use Case Taxonomy](04-ai-use-case-taxonomy.md)
- [06 — AI Security Controls](06-ai-security-controls.md)
- [Templates — AI Threat Model](../templates/ai-threat-model-template.md)
- [Templates — AI Risk Assessment](../templates/ai-risk-assessment-template.md)
