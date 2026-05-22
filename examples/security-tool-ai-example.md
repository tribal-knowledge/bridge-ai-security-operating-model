# Example — AI in Security Tools

> **Scenario:** A security operations team is evaluating AI-assisted alert triage and automated response capabilities in their SIEM/SOAR platform. The AI feature can enrich alerts, recommend response actions, and — in some configurations — automatically close or escalate alerts.

---

## Context

| Field | Detail |
|-------|--------|
| **Organization** | Fictional enterprise |
| **Security Tool** | SIEM / SOAR platform with AI alert enrichment and response capability |
| **AI Feature** | AI-assisted alert triage, enrichment, and optional automated response |
| **BRIDGE Domains** | I, D, G, E |
| **Risk Level** | High — AI influences security decisions; potential for over-automation |

---

## Why AI in Security Tools Requires Careful Review

Security tools with AI capabilities sit at a critical intersection:

- They process highly sensitive security data (threat intelligence, logs, vulnerability data, incident details)
- Their outputs influence real security decisions — which alerts are investigated, which are dismissed, what actions are taken
- Over-automation can suppress legitimate alerts (false negatives) or trigger unnecessary response actions (false positives)
- AI-assisted decisions may be difficult to audit if logging is insufficient

The goal is to enable AI to increase analyst efficiency while maintaining human oversight over consequential decisions.

---

## Risk Assessment Summary

| Threat | Likelihood | Impact | Risk | Notes |
|--------|-----------|--------|------|-------|
| Automated over-response | **Medium** | **High** | **High** | AI auto-closing alerts or triggering containment actions without human review could suppress real incidents or cause operational disruption |
| False negative rate increase | **Medium** | **High** | **High** | If AI enrichment incorrectly classifies malicious alerts as benign, real incidents could be missed |
| Insecure output (AI enrichment errors) | **Medium** | **Medium** | **Medium** | Incorrect AI enrichment could misdirect analyst investigation |
| Data exposure to AI model | **Low** | **High** | **Medium** | Security log data and threat intelligence submitted to AI model — vendor data handling must be confirmed |
| Weak monitoring of AI decisions | **Medium** | **High** | **High** | If AI-assisted decisions are not logged separately from human decisions, audit trail quality degrades |
| Third-party model exposure | **Low** | **Medium** | **Low** | If AI uses a third-party LLM, security data may be processed externally |

**Overall Risk Rating: High**

---

## Controls Required

### Analyst Oversight (Required)
- AI may enrich and recommend; it may not auto-close, auto-escalate, or auto-respond without analyst confirmation
- An analyst must review and confirm all AI-recommended response actions before execution
- This requirement must be technically enforced in the SOAR playbook configuration — not just policy

### Logging and Attribution (Required)
- All AI-assisted triage decisions must be logged separately from human decisions
- Log entries must indicate: alert ID, AI recommendation, AI confidence score, human decision, analyst ID, timestamp
- Logs must be retained for the same period as other security event records (minimum 12 months)

### False Positive / False Negative Monitoring (Required)
- A process must exist to track the quality of AI enrichment over time
- Monthly review of AI alert triage accuracy — false positives and false negatives
- Threshold defined: if false negative rate exceeds X%, AI triage is suspended pending review

### Vendor Data Handling (Required)
- Vendor must confirm that security log data submitted for AI processing is not used for model training
- Data residency for AI-processed security data must be confirmed and documented
- Vendor must provide evidence of SOC 2 Type II or equivalent

### Detection Logic Transparency (Required)
- The security team must have access to documentation of how the AI enrichment model generates recommendations
- Black-box AI recommendations without explanation are not acceptable for high-severity alert triage

---

## What the Team Got Right

This team approached AI in security tools thoughtfully:

1. They started with AI in **read-only mode** — enrichment and recommendations only, no automated actions
2. They ran a **90-day pilot** comparing AI-recommended triage decisions against analyst decisions before enabling any automation
3. They published **analyst guidance** on how to interpret AI confidence scores
4. They built **feedback loops** — analysts could flag incorrect AI recommendations directly in the tool, feeding a quality improvement process

---

## Phased Implementation

| Phase | Capability Enabled | Human Requirement |
|-------|-------------------|-------------------|
| Phase 1 (Months 1–3) | AI enrichment and recommendations only — read-only | Analyst makes all triage and response decisions |
| Phase 2 (Months 4–6) | AI auto-close for confirmed low-severity noise (predefined category only) | Analyst reviews AI auto-close decisions in daily report |
| Phase 3 (Month 7+) | Expand AI auto-close categories based on Phase 2 accuracy data | Ongoing monitoring; threshold-based suspension policy in place |

---

## Metrics Tracked

| Metric | Frequency | Threshold for Action |
|--------|-----------|---------------------|
| AI recommendation accuracy | Monthly | <85% accuracy triggers review |
| False negative rate | Monthly | Any confirmed missed incident triggers review |
| Analyst override rate | Monthly | >30% override rate triggers model review |
| AI-assisted vs human decision breakdown | Monthly | Reported to Security leadership |
| Auto-close accuracy (Phase 2+) | Weekly | <95% accuracy suspends auto-close |

---

## Lessons Learned

1. AI in security tools is most valuable as an analyst force-multiplier, not as a replacement for analyst judgment on high-severity alerts
2. False negative risk is more dangerous than false positive risk in a security context — tune for recall, not just precision
3. Logging AI decisions separately from human decisions is essential for post-incident review and audit
4. Starting in read-only enrichment mode and earning trust through demonstrated accuracy before enabling automation is the right approach

---

## Related Templates
- [AI Risk Assessment Template](../templates/ai-risk-assessment-template.md)
- [AI Threat Model Template](../templates/ai-threat-model-template.md)
- [Agentic AI Control Checklist](../templates/agentic-ai-control-checklist.md)
