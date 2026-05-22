# Example — GenAI Use Case Intake and Review

> **Scenario:** A business operations team wants to deploy a GenAI tool to help staff draft internal reports and summarize meeting notes. The tool would be accessed via browser and requires no integration with internal systems.

---

## Context

| Field | Detail |
|-------|--------|
| **Organization** | Fictional enterprise (any industry) |
| **Use Case** | AI-assisted report drafting and meeting summarization |
| **AI Tool** | Hypothetical enterprise GenAI platform |
| **BRIDGE Domains** | B, G, I, D, E |

---

## Intake Form Summary

| Field | Response |
|-------|----------|
| **Use Case Name** | AI-Assisted Report Drafting and Meeting Summarization |
| **Business Owner** | Director of Business Operations |
| **Technology Owner** | IT Business Applications Manager |
| **AI Category** | Browser-Based GenAI / SaaS AI |
| **Data Classification** | Internal — meeting notes, draft documents, operational reports |
| **Autonomy Level** | Assisted — human reviews and approves all outputs |
| **Regulatory Scope** | No direct regulatory scope identified at intake |

---

## Risk Assessment Summary

| Threat | Likelihood | Impact | Risk | Notes |
|--------|-----------|--------|------|-------|
| Data leakage | Low | Medium | **Low** | No customer or regulated data in scope; internal meeting notes only |
| Prompt injection | Low | Low | **Low** | No external inputs; user-generated prompts only |
| Insecure output | Medium | Medium | **Medium** | Hallucinated content in reports could mislead decisions |
| Third-party exposure | Low | Medium | **Low** | Vendor has enterprise agreement with data processing terms; training opt-out confirmed |
| Weak monitoring | Low | Low | **Low** | Vendor provides audit logs; usage will be monitored |

**Overall Risk Rating: Low-Moderate**

---

## Conditions Applied at Approval

1. Users must complete the AI acceptable use awareness module before accessing the tool
2. The tool must not be used with customer data, financial records, or HR information
3. All AI-generated content must be reviewed and verified by the human author before distribution
4. Content generated with AI assistance must not be represented as unassisted human work in regulated contexts
5. The vendor's data retention and training opt-out settings must be verified and documented annually

---

## Controls Implemented

| Control | Description |
|---------|-------------|
| Acceptable use training | Mandatory module for all users before first access |
| Data scope restriction | Policy specifying internal operational data only; no customer, financial, or regulated data |
| Human review requirement | All AI-generated reports reviewed and signed off by the authoring employee |
| Vendor audit log configuration | Audit logs enabled and reviewed quarterly |
| Annual vendor review | SaaS AI review checklist to be completed annually |

---

## Governance Record

| Stage | Date | Outcome |
|-------|------|---------|
| Intake submitted | — | Received by governance team |
| Classification | — | Low-Moderate risk; standard review assigned |
| Review complete | — | Security and privacy review complete; no blocking issues |
| Approved with Conditions | — | 5 conditions documented |
| Deployment | — | Tool enabled; training completed by 94% of target users |
| First operational review | — | Scheduled for 6 months post-deployment |

---

## Lessons Learned

- Low-risk GenAI use cases can move through governance quickly when a structured intake process is in place
- Pre-approved tool catalogs reduce the burden — once the tool is approved for one team, expansion to others requires only a scope review, not a full re-assessment
- User awareness is the most effective control for output quality — users who understand AI limitations produce better-validated outputs

---

## Related Templates
- [AI Use Case Intake Template](../templates/ai-use-case-intake-template.md)
- [AI Risk Assessment Template](../templates/ai-risk-assessment-template.md)
