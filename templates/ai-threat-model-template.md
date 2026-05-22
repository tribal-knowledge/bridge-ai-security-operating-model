# AI Threat Model Template

> **Instructions:** Use this template to document a structured threat model for an AI use case. Apply STRIDE, OWASP Top 10 for LLM Applications, or MITRE ATLAS as appropriate. Complete after the AI Use Case Intake and before finalizing the Risk Assessment.

---

## Section 1 — System Description

| Field | Response |
|-------|----------|
| **Use Case ID** | |
| **Use Case Name** | |
| **AI Tool / Model** | |
| **Threat Model Author** | |
| **Date** | |
| **Threat Modeling Method(s)** | ☐ STRIDE ☐ OWASP LLM Top 10 ☐ MITRE ATLAS ☐ PASTA ☐ Abuse Case ☐ Other |

---

## Section 2 — System Overview

**2.1 What does this AI system do?**

> *(Describe the system's purpose, functionality, and user interaction model in 2–4 sentences.)*

**2.2 System Architecture (describe or attach diagram)**

> *(Describe data flows, components, integrations, and trust boundaries. Include: User → AI Interface → Model → Data Sources → Output.)*

**2.3 Trust Boundaries**

| Boundary | Description |
|----------|-------------|
| | |
| | |

**2.4 Key Assets to Protect**

| Asset | Description | Sensitivity |
|-------|-------------|-------------|
| | | |
| | | |
| | | |

---

## Section 3 — STRIDE Threat Analysis

For each STRIDE category, document applicable threats for this AI use case.

### S — Spoofing

| Threat | Attack Scenario | Component Affected | Mitigation |
|--------|----------------|-------------------|------------|
| | | | |

### T — Tampering

| Threat | Attack Scenario | Component Affected | Mitigation |
|--------|----------------|-------------------|------------|
| Prompt injection via uploaded document | Attacker embeds malicious instructions in a file that is fed to the AI | Input processing layer | Input validation, sandboxed file parsing |
| | | | |

### R — Repudiation

| Threat | Attack Scenario | Component Affected | Mitigation |
|--------|----------------|-------------------|------------|
| AI action with no audit trail | Agent takes a harmful action that cannot be attributed or reversed | Agent execution layer | Full audit logging, immutable log storage |
| | | | |

### I — Information Disclosure

| Threat | Attack Scenario | Component Affected | Mitigation |
|--------|----------------|-------------------|------------|
| AI exposes confidential data in output | User queries AI and receives data belonging to another user | Output layer / model | Access scoping, output filtering |
| | | | |

### D — Denial of Service

| Threat | Attack Scenario | Component Affected | Mitigation |
|--------|----------------|-------------------|------------|
| | | | |

### E — Elevation of Privilege

| Threat | Attack Scenario | Component Affected | Mitigation |
|--------|----------------|-------------------|------------|
| Agent exceeds permitted scope | AI agent uses a misconfigured integration to access admin-level functions | Agent permission layer | Least privilege, permission boundary testing |
| | | | |

---

## Section 4 — OWASP Top 10 for LLM Applications Mapping

| # | Vulnerability | Applicable? | Risk Level | Notes / Mitigations |
|---|--------------|-------------|-----------|---------------------|
| LLM01 | Prompt Injection | | | |
| LLM02 | Insecure Output Handling | | | |
| LLM03 | Training Data Poisoning | | | |
| LLM04 | Model Denial of Service | | | |
| LLM05 | Supply Chain Vulnerabilities | | | |
| LLM06 | Sensitive Information Disclosure | | | |
| LLM07 | Insecure Plugin Design | | | |
| LLM08 | Excessive Agency | | | |
| LLM09 | Overreliance | | | |
| LLM10 | Model Theft | | | |

---

## Section 5 — Abuse Cases

Document specific misuse scenarios relevant to this AI use case.

| # | Actor | Abuse Scenario | Motivation | Impact | Likelihood | Mitigation |
|---|-------|---------------|-----------|--------|-----------|------------|
| 1 | Malicious insider | | | | | |
| 2 | External attacker | | | | | |
| 3 | Negligent user | | | | | |
| 4 | Compromised vendor | | | | | |
| 5 | AI system itself (hallucination / error) | | | | | |

---

## Section 6 — Data Flow Threat Analysis

Map threats to data flows:

| Data Flow | From | To | Data Involved | Threat | Control |
|-----------|------|----|---------------|--------|---------|
| User prompt submission | User | AI model | Potentially sensitive user input | Data leakage, prompt injection | DLP, input validation |
| AI output delivery | AI model | User | AI-generated content | Insecure output, information disclosure | Output filtering, human review |
| File upload | User | AI system | Documents, source code | Data leakage, malware | File scanning, DLP |
| API call | AI agent | External system | Business data | Excessive agency, unauthorized access | Permission controls, audit logging |

---

## Section 7 — Key Findings and Recommendations

**High Priority Threats**

| # | Threat | Risk Level | Recommended Action | Owner |
|---|--------|-----------|-------------------|-------|
| 1 | | Critical / High | | |
| 2 | | Critical / High | | |
| 3 | | Critical / High | | |

**Summary**

> *(Summarize the overall threat landscape for this use case in 3–5 sentences. Note the highest-priority risks and the most critical mitigations required before deployment.)*

---

## Section 8 — Sign-Off

| Role | Name | Date |
|------|------|------|
| **Security Reviewer** | | |
| **Architecture Reviewer** | | |
| **Risk Owner** | | |
