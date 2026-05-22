# Agentic AI Control Checklist

> **Instructions:** Use this checklist for any AI system that can take autonomous actions — sending messages, writing or deleting data, calling APIs, executing code, or triggering workflows. Agentic AI requires the most rigorous security review in the BRIDGE model.

---

## Review Information

| Field | Response |
|-------|----------|
| **Agent Name / System** | |
| **Platform / Framework** | |
| **Vendor / Developer** | |
| **Review Date** | |
| **Reviewed By** | |
| **Business Owner** | |
| **Autonomy Level** | ☐ Assisted ☐ Automated ☐ Fully Autonomous |

---

## Section 1 — Scope and Permission Definition

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 1.1 | The agent's permitted actions are explicitly defined in a documented allowlist | ☐ Yes ☐ No ☐ Planned | |
| 1.2 | The agent operates on a least-privilege basis — only the permissions it needs to complete its task | ☐ Yes ☐ No ☐ Unknown | |
| 1.3 | The agent cannot access data beyond its defined scope | ☐ Yes ☐ No ☐ Unknown | |
| 1.4 | Read and write permissions are separated — the agent cannot write where it only needs to read | ☐ Yes ☐ No ☐ Unknown | |
| 1.5 | The agent's tool access is restricted to an approved allowlist | ☐ Yes ☐ No ☐ Unknown | |
| 1.6 | External API access is restricted to only required endpoints | ☐ Yes ☐ No ☐ Unknown | |
| 1.7 | The agent cannot escalate its own permissions or grant access to others | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 2 — Human Oversight and Approval Gates

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 2.1 | A list of high-risk action categories requiring human approval before execution is defined | ☐ Yes ☐ No ☐ Planned | |
| 2.2 | Human approval gates are technically enforced (not just policy-based) | ☐ Yes ☐ No ☐ Unknown | |
| 2.3 | The agent cannot bypass human approval requirements | ☐ Yes ☐ No ☐ Unknown | |
| 2.4 | Approval requests are routed to the correct person and cannot be auto-approved by the agent | ☐ Yes ☐ No ☐ Unknown | |
| 2.5 | An escalation path exists if the approver is unavailable | ☐ Yes ☐ No ☐ Planned | |
| 2.6 | The agent stops and waits rather than proceeding if it cannot obtain required approval | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 3 — Execution Controls

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 3.1 | The agent runs in an isolated execution environment (sandbox) where possible | ☐ Yes ☐ No ☐ N/A | |
| 3.2 | Transaction limits are in place (e.g., maximum records modified, maximum spend, maximum messages sent per session) | ☐ Yes ☐ No ☐ N/A | |
| 3.3 | Rate limits are applied to prevent runaway or looping agent behavior | ☐ Yes ☐ No ☐ Planned | |
| 3.4 | The agent has a maximum session duration or timeout | ☐ Yes ☐ No ☐ Planned | |
| 3.5 | Memory is restricted — the agent does not retain sensitive data beyond its authorized session | ☐ Yes ☐ No ☐ Unknown | |
| 3.6 | The agent cannot initiate external communications (email, messaging, API calls) without authorization | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 4 — Kill Switch and Rollback

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 4.1 | A kill switch exists to halt agent operation immediately | ☐ Yes ☐ No ☐ Planned | |
| 4.2 | The kill switch can be triggered by an authorized person without requiring agent cooperation | ☐ Yes ☐ No ☐ Unknown | |
| 4.3 | Rollback capability exists for agent actions where technically feasible | ☐ Yes ☐ No ☐ N/A | |
| 4.4 | A runbook exists for responding to an agent that is behaving unexpectedly | ☐ Yes ☐ No ☐ Planned | |
| 4.5 | The blast radius of agent failure or misuse has been assessed and documented | ☐ Yes ☐ No ☐ Planned | |

---

## Section 5 — Prompt Injection and Input Security

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 5.1 | The agent's exposure to external content (emails, documents, web pages, tickets) that could contain prompt injection has been assessed | ☐ Yes ☐ No ☐ Unknown | |
| 5.2 | Input validation or filtering is applied to external content before it influences the agent's behavior | ☐ Yes ☐ No ☐ Planned | |
| 5.3 | The agent has been tested against known prompt injection techniques | ☐ Yes ☐ No ☐ Planned | |
| 5.4 | The agent will not execute instructions embedded in external content without authorization | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 6 — Logging and Monitoring

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 6.1 | Every action taken by the agent is logged with full context (what, when, why, on whose behalf) | ☐ Yes ☐ No ☐ Planned | |
| 6.2 | Logs are stored in an immutable or tamper-evident location | ☐ Yes ☐ No ☐ Unknown | |
| 6.3 | Alerts are configured for anomalous or unexpected agent behavior | ☐ Yes ☐ No ☐ Planned | |
| 6.4 | Agent activity is reviewed periodically for drift from expected behavior | ☐ Yes ☐ No ☐ Planned | |
| 6.5 | Logs are retained for a period sufficient to support incident investigation | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 7 — Incident Response

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 7.1 | An incident response procedure exists specifically for agentic AI misuse or failure | ☐ Yes ☐ No ☐ Planned | |
| 7.2 | The incident response team knows how to halt, isolate, and investigate the agent | ☐ Yes ☐ No ☐ Planned | |
| 7.3 | Communication procedures for agent-related incidents are defined | ☐ Yes ☐ No ☐ Planned | |

---

## Section 8 — Risk Summary

**Blast Radius Assessment:**

> *(Describe the worst-case impact if this agent behaves unexpectedly or is manipulated.)*

**Overall Risk Rating:**
- [ ] Low
- [ ] Moderate
- [ ] High
- [ ] Critical — additional controls or architecture changes required before deployment

**Key Findings:**

| # | Finding | Severity | Recommendation |
|---|---------|----------|----------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## Section 9 — Decision

| Field | Response |
|-------|----------|
| **Decision** | ☐ Approved ☐ Approved with Conditions ☐ Restricted ☐ Rejected |
| **Required Conditions** | |
| **Decision Date** | |
| **Decision Made By** | |
| **Next Review Date** | |
