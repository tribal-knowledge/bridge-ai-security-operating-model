# AI Risk Assessment Template

> **Instructions:** Complete this template for each AI use case requiring a formal risk assessment. This template supports the **I — Identify** component of the BRIDGE model. Reference the completed AI Use Case Intake form before starting.

---

## Section 1 — Use Case Reference

| Field | Response |
|-------|----------|
| **Use Case ID** | |
| **Use Case Name** | |
| **AI Tool / Platform** | |
| **Vendor / Provider** | |
| **AI Category** | ☐ Browser GenAI ☐ SaaS AI Feature ☐ Coding Assistant ☐ Agentic AI ☐ Business Tool AI ☐ Security Tool AI |
| **Assessment Date** | |
| **Assessed By** | |
| **Review Cycle** | ☐ Initial ☐ Periodic ☐ Change-triggered |

---

## Section 2 — Risk Context

**2.1 Data Sensitivity**

| Data Type Involved | Classification | Volume / Sensitivity |
|-------------------|---------------|---------------------|
| | | |
| | | |
| | | |

**2.2 Level of Autonomy**
- [ ] Assisted (human decides)
- [ ] Automated (human oversight)
- [ ] Autonomous (AI acts independently)

**2.3 Business Impact if AI Fails or is Compromised**
- [ ] Low — minimal operational impact
- [ ] Medium — moderate operational or reputational impact
- [ ] High — significant financial, regulatory, or reputational impact
- [ ] Critical — severe or enterprise-wide impact

**2.4 Regulatory Scope**

> *(List applicable regulations or frameworks)*

---

## Section 3 — Threat Assessment

Rate each threat category for likelihood and impact, then calculate residual risk.

**Likelihood:** 1 = Low, 2 = Medium, 3 = High  
**Impact:** 1 = Low, 2 = Medium, 3 = High  
**Risk Score:** Likelihood × Impact (1–3 = Low, 4–6 = Medium, 7–9 = High)

| # | Threat Category | Applicable? | Likelihood (1–3) | Impact (1–3) | Risk Score | Notes |
|---|----------------|-------------|-----------------|-------------|-----------|-------|
| 1 | Data leakage — sensitive data enters an AI tool or AI outputs expose sensitive data | | | | | |
| 2 | Prompt injection — malicious instructions manipulate AI behavior via inputs | | | | | |
| 3 | Insecure output — AI produces incorrect, unsafe, biased, or misleading content | | | | | |
| 4 | Excessive agency — AI agent takes unauthorized or harmful actions | | | | | |
| 5 | Insecure code generation — AI-generated code introduces vulnerabilities | | | | | |
| 6 | Third-party exposure — vendor, API, or plugin introduces supply chain risk | | | | | |
| 7 | Access control failure — AI surfaces data users should not access | | | | | |
| 8 | Model misuse — AI used for prohibited, unethical, or non-compliant purposes | | | | | |
| 9 | Lack of transparency — AI behavior, data use, or decisions cannot be explained | | | | | |
| 10 | Weak monitoring — AI activity is not logged, alerted, or auditable | | | | | |

---

## Section 4 — Control Assessment

For each applicable threat, assess whether adequate controls exist.

| Threat | Control(s) in Place | Control Adequacy | Gap / Recommendation |
|--------|--------------------|-----------------|-----------------------|
| Data leakage | | ☐ None ☐ Partial ☐ Sufficient | |
| Prompt injection | | ☐ None ☐ Partial ☐ Sufficient | |
| Insecure output | | ☐ None ☐ Partial ☐ Sufficient | |
| Excessive agency | | ☐ None ☐ Partial ☐ Sufficient | |
| Insecure code generation | | ☐ None ☐ Partial ☐ Sufficient | |
| Third-party exposure | | ☐ None ☐ Partial ☐ Sufficient | |
| Access control failure | | ☐ None ☐ Partial ☐ Sufficient | |
| Model misuse | | ☐ None ☐ Partial ☐ Sufficient | |
| Lack of transparency | | ☐ None ☐ Partial ☐ Sufficient | |
| Weak monitoring | | ☐ None ☐ Partial ☐ Sufficient | |

---

## Section 5 — Residual Risk Summary

| Threat | Inherent Risk | Control Adequacy | Residual Risk |
|--------|--------------|-----------------|---------------|
| Data leakage | | | |
| Prompt injection | | | |
| Insecure output | | | |
| Excessive agency | | | |
| Insecure code generation | | | |
| Third-party exposure | | | |
| Access control failure | | | |
| Model misuse | | | |
| Lack of transparency | | | |
| Weak monitoring | | | |

**Overall Residual Risk Rating:**
- [ ] Low
- [ ] Moderate
- [ ] High
- [ ] Critical

---

## Section 6 — Risk Treatment

**6.1 Recommended Risk Treatment**
- [ ] Accept — residual risk is within tolerance
- [ ] Mitigate — implement additional controls (see Section 6.2)
- [ ] Transfer — contractual controls required from vendor
- [ ] Avoid — recommend not approving this use case

**6.2 Required Mitigating Actions**

| # | Action | Owner | Target Date | Status |
|---|--------|-------|------------|--------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |

---

## Section 7 — Special Considerations

**7.1 Vendor Risk Notes**

> *(Document any vendor-specific concerns identified during assessment — data retention, training opt-out, contractual gaps, etc.)*

**7.2 Regulatory or Privacy Concerns**

> *(Note any regulatory obligations, privacy impact assessment requirements, or compliance gaps.)*

**7.3 Human Oversight Requirements**

> *(Specify where human review is required before AI outputs are acted upon.)*

---

## Section 8 — Assessment Sign-Off

| Role | Name | Signature / Approval | Date |
|------|------|---------------------|------|
| **Security Owner** | | | |
| **Privacy Owner** | | | |
| **Risk Owner** | | | |
| **Compliance Owner** | | | |

---

## Section 9 — Next Review

| Field | Response |
|-------|----------|
| **Next Scheduled Review Date** | |
| **Review Trigger Conditions** | ☐ Data change ☐ Model/vendor change ☐ Autonomy increase ☐ Incident ☐ Regulatory change |
| **Linked Use Case ID** | |
