# Coding Agent Security Checklist

> **Instructions:** Use this checklist when reviewing the security posture of AI coding assistants (GitHub Copilot, Cursor, Windsurf, CodeWhisperer, Replit, etc.) before approving organizational use. Also use for periodic security reviews of tools already in use.

---

## Review Information

| Field | Response |
|-------|----------|
| **Tool Name** | |
| **Version / Plan** | |
| **Vendor** | |
| **Review Date** | |
| **Reviewed By** | |
| **Target Users** | *(e.g., all developers, specific team, specific project)* |

---

## Section 1 — Data Exposure and Confidentiality

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 1.1 | Code submitted to the AI for suggestion is not shared with the vendor for training (opt-out confirmed) | ☐ Yes ☐ No ☐ Unknown | |
| 1.2 | The tool does not retain submitted code beyond the session (or retention is documented and acceptable) | ☐ Yes ☐ No ☐ Unknown | |
| 1.3 | Developers are aware that pasting secrets, credentials, or API keys into prompts creates exposure risk | ☐ Yes ☐ No ☐ Planned | |
| 1.4 | The tool has been configured to avoid suggesting previously seen secrets or credentials | ☐ Yes ☐ No ☐ Unknown | |
| 1.5 | Proprietary algorithms or architecture are assessed for exposure risk when used with this tool | ☐ Yes ☐ No ☐ Planned | |
| 1.6 | The tool's access to the codebase is scoped to only what is necessary | ☐ Yes ☐ No ☐ Unknown | |

---

## Section 2 — Repository and Permission Controls

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 2.1 | The coding assistant's access to repositories is restricted to the minimum required | ☐ Yes ☐ No ☐ Unknown | |
| 2.2 | The tool cannot access repositories outside its authorized scope | ☐ Yes ☐ No ☐ Unknown | |
| 2.3 | Repository access is granted at the repository level, not the entire organization | ☐ Yes ☐ No ☐ Unknown | |
| 2.4 | Third-party IDE plugins associated with the tool are reviewed for permissions | ☐ Yes ☐ No ☐ N/A | |
| 2.5 | Service accounts or tokens used by the tool follow least privilege principles | ☐ Yes ☐ No ☐ N/A | |

---

## Section 3 — Code Quality and Security

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 3.1 | All AI-generated code is subject to human code review before merging | ☐ Yes ☐ No ☐ Planned | |
| 3.2 | SAST (Static Application Security Testing) is applied to all code including AI-generated code | ☐ Yes ☐ No ☐ Planned | |
| 3.3 | Secrets scanning is applied in the CI/CD pipeline to catch any credentials in AI-generated code | ☐ Yes ☐ No ☐ Planned | |
| 3.4 | SCA (Software Composition Analysis) is applied to review AI-suggested open-source libraries | ☐ Yes ☐ No ☐ Planned | |
| 3.5 | DAST is applied to applications where AI-generated code is part of the codebase | ☐ Yes ☐ No ☐ Planned | |
| 3.6 | Developers are trained to critically review AI suggestions rather than accept them uncritically | ☐ Yes ☐ No ☐ Planned | |
| 3.7 | The tool has been assessed for the risk of suggesting vulnerable or deprecated libraries | ☐ Yes ☐ No ☐ Unknown | |
| 3.8 | The tool has been assessed for the risk of open-source license contamination in suggestions | ☐ Yes ☐ No ☐ Unknown | |
| 3.9 | Secure coding standards are applied equally to AI-generated and human-written code | ☐ Yes ☐ No ☐ Yes | |

---

## Section 4 — AI-Assisted Code Review and Testing

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 4.1 | If AI is used for code review, human review is still required before merge | ☐ Yes ☐ No ☐ N/A | |
| 4.2 | AI-generated tests are validated for coverage and correctness | ☐ Yes ☐ No ☐ N/A | |
| 4.3 | AI-generated test cases are reviewed to ensure they test the right behaviors | ☐ Yes ☐ No ☐ N/A | |

---

## Section 5 — Autonomous / Agentic Coding Agents

*Complete this section if the tool can autonomously execute code, make commits, open pull requests, or interact with external systems.*

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 5.1 | Agent actions (commits, PRs, deployments) require human approval before execution | ☐ Yes ☐ No ☐ N/A | |
| 5.2 | The agent cannot deploy to production without explicit human authorization | ☐ Yes ☐ No ☐ N/A | |
| 5.3 | The agent's access to external APIs or systems is restricted and logged | ☐ Yes ☐ No ☐ N/A | |
| 5.4 | A kill switch or pause mechanism exists to halt agent operation | ☐ Yes ☐ No ☐ N/A | |
| 5.5 | Agent actions are fully logged with context for audit purposes | ☐ Yes ☐ No ☐ N/A | |

---

## Section 6 — Policy and Awareness

| # | Check | Status | Notes |
|---|-------|--------|-------|
| 6.1 | A coding assistant acceptable use policy is in place | ☐ Yes ☐ No ☐ Planned | |
| 6.2 | Developers have received training on secure use of AI coding tools | ☐ Yes ☐ No ☐ Planned | |
| 6.3 | Guidance on what must not be pasted into coding assistants is documented and communicated | ☐ Yes ☐ No ☐ Planned | |

---

## Section 7 — Risk Summary

**Overall Risk Rating:**
- [ ] Low
- [ ] Moderate
- [ ] High
- [ ] Critical

**Key Findings:**

| # | Finding | Severity | Recommendation |
|---|---------|----------|----------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## Section 8 — Decision

| Field | Response |
|-------|----------|
| **Decision** | ☐ Approved ☐ Approved with Conditions ☐ Restricted ☐ Rejected |
| **Scope of Approval** | *(e.g., all developers / specific team / specific repositories only)* |
| **Conditions** | |
| **Decision Date** | |
| **Next Review Date** | |
