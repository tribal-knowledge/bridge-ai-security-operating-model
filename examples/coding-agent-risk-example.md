# Example — Coding Agent Risk Review

> **Scenario:** A technology team requests approval to use an AI coding assistant across all software development squads. The tool integrates directly with GitHub and provides inline code suggestions within the IDE.

---

## Context

| Field | Detail |
|-------|--------|
| **Organization** | Fictional technology company |
| **Use Case** | AI-assisted code generation and review across all development squads |
| **AI Tool** | Hypothetical AI coding assistant (IDE plugin + GitHub integration) |
| **BRIDGE Domains** | B, I, D, G |

---

## Risk Assessment Summary

| Threat | Likelihood | Impact | Risk | Notes |
|--------|-----------|--------|------|-------|
| Secret leakage | **High** | **High** | **Critical** | Developers routinely work in repositories with .env files, config files, and hardcoded credentials in test branches |
| Insecure code generation | **High** | **High** | **Critical** | Coding assistants have known history of suggesting insecure patterns (SQL injection, path traversal, insecure crypto) |
| IP / source code exposure | **Medium** | **High** | **High** | Source code submitted to cloud-based AI model; need to confirm training opt-out |
| License contamination | **Medium** | **Medium** | **Medium** | AI suggestions may include copyleft code that conflicts with proprietary licensing |
| Excessive repository access | **Medium** | **High** | **High** | Tool has GitHub org-level access by default; needs scoping to specific repos |
| Unreviewed AI-generated PRs | **Medium** | **High** | **High** | Risk that AI-generated code is merged without sufficient human review |

**Overall Risk Rating: High**

---

## Conditions Applied at Approval

1. **Secrets scanning is mandatory** — secrets scanning must be enabled in all repositories before the coding assistant is activated; any repository without secrets scanning is excluded from AI assistant access
2. **Human code review is required** — all AI-generated code must be reviewed by a qualified developer before merging; code review requirements cannot be waived for AI-generated pull requests
3. **Repository scope must be restricted** — the tool's GitHub access must be scoped to specific approved repositories, not the entire organization
4. **Training opt-out must be confirmed** — the vendor must confirm in writing that source code submitted for suggestions is not used for model training
5. **SAST must be applied** — SAST scanning must be included in the CI/CD pipeline for all repositories where the coding assistant is used
6. **Developer training is required** — all developers must complete the secure coding assistant guidance before using the tool
7. **License review process required** — a process for reviewing AI-suggested open-source libraries for license compatibility must be in place

---

## Controls Implemented

| Control | Owner | Status |
|---------|-------|--------|
| Secrets scanning enabled in all in-scope repositories | Platform / DevSecOps | Required before activation |
| SAST added to CI/CD pipeline | DevSecOps | Required before activation |
| SCA (Software Composition Analysis) configured | DevSecOps | Required before activation |
| Repository access scoped to approved list | Platform team | Required before activation |
| Vendor training opt-out confirmed in writing | Vendor management | Complete |
| Secure coding assistant developer guide published | Security team | Complete |
| Developer training completion tracked | L&D / Security | Ongoing |
| Quarterly code quality review of AI-assisted repositories | Security / Engineering | Ongoing |

---

## Key Finding: The Secret Leakage Risk

During the review, the security team identified that 14 of 31 active repositories contained credentials, API keys, or configuration secrets in non-production branches — not in `.gitignore` exclusions.

**Remediation required before go-live:**
1. Secret scanning sweep across all 31 repositories
2. Revocation and rotation of any exposed credentials
3. `.gitignore` and pre-commit hook standards applied to all repositories
4. Developer awareness on not pasting secrets into coding assistant prompts

This finding was escalated to the CISO as a pre-existing risk that the coding assistant review had surfaced.

---

## Governance Record

| Stage | Outcome |
|-------|---------|
| Intake submitted | Received; classified as High risk |
| Full review conducted | Security, architecture, and legal |
| Initial approval withheld | Secret leakage finding required remediation |
| Remediation completed | Secrets remediated; conditions documented |
| Approved with Conditions | 7 conditions; phased rollout approved |
| Phase 1 deployment | 2 pilot squads; 30-day review before broader rollout |

---

## Lessons Learned

- Coding assistant reviews frequently surface pre-existing risks (secret leakage, insecure patterns) that are not AI-specific but are exposed by the review process
- Least-privilege scoping of repository access is consistently underimplemented by default — vendor defaults must be reviewed and restricted
- Developer education on what not to paste into coding assistants is as important as technical controls

---

## Related Templates
- [Coding Agent Security Checklist](../templates/coding-agent-security-checklist.md)
- [AI Risk Assessment Template](../templates/ai-risk-assessment-template.md)
- [AI Threat Model Template](../templates/ai-threat-model-template.md)
