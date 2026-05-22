# 09 — BRIDGE Maturity Model

## Overview

The BRIDGE Maturity Model provides a structured way to assess the current state of an organization's AI security program and define a path toward continuous improvement.

Maturity is assessed across all six BRIDGE domains. Organizations can be at different maturity levels across different domains — for example, strong in governance but early in assurance.

---

## Five Maturity Levels

| Level | Name | Description |
|-------|------|-------------|
| **1** | Ad Hoc | AI use is unmanaged, visibility is limited, and controls are inconsistent |
| **2** | Aware | AI risks are recognized, basic policies exist, and some tools are monitored |
| **3** | Defined | AI inventory, intake, risk assessment, and control baselines are established |
| **4** | Managed | AI controls are integrated into browser, SaaS, SDLC, vendor, and risk processes |
| **5** | Optimized | AI security is continuously monitored, tested, measured, and improved |

---

## Maturity by BRIDGE Domain

### B — Baseline AI Usage

| Level | Indicators |
|-------|-----------|
| 1 | No AI inventory. No visibility into what AI tools are in use. AI discovery is reactive. |
| 2 | Some AI tools are known. Basic awareness of browser-based AI usage. No structured inventory. |
| 3 | Formal AI inventory exists. Use case register is maintained. Shadow AI discovery is in progress. |
| 4 | Continuous AI discovery is automated. Inventory is complete and current. Department-level views are maintained. |
| 5 | AI inventory is integrated with procurement, architecture review, and risk systems. Real-time discovery is operational. |

---

### R — Regulate Access & Data Flow

| Level | Indicators |
|-------|-----------|
| 1 | No AI-specific access controls. No DLP for AI tools. No site categorization. |
| 2 | Some AI sites are categorized. Basic URL filtering is in place. No formal tiering. |
| 3 | AI tool access tiers are defined. DLP rules for AI uploads are implemented. Browser controls are in place. |
| 4 | Browser, CASB, SWG, and DLP controls are integrated and consistently enforced. Agent permission model is defined. |
| 5 | Access controls are dynamically adjusted based on risk. DLP rules are tested and tuned continuously. |

---

### I — Identify AI Risk & Threats

| Level | Indicators |
|-------|-----------|
| 1 | No AI risk assessments. Threats are not formally identified. No threat modeling for AI. |
| 2 | Some awareness of AI risks. Informal risk conversations occur. No structured assessment process. |
| 3 | AI risk assessment template is in use. Threat modeling is performed for high-risk use cases. Misuse case library exists. |
| 4 | Risk assessments are completed for all AI use cases. Threat models are maintained and updated. |
| 5 | Continuous threat intelligence is applied to AI risk. Risk scenarios are updated as AI capabilities evolve. |

---

### D — Design Secure AI Controls

| Level | Indicators |
|-------|-----------|
| 1 | No AI-specific security controls. Existing controls are not adapted for AI. |
| 2 | Some controls are applied to known AI tools. No formal control baseline. |
| 3 | AI security control baseline is defined. Control guidance exists for GenAI, SaaS AI, coding agents, and agentic AI. |
| 4 | Controls are implemented and verified across all AI use case types. Control effectiveness is tested. |
| 5 | Controls are continuously improved based on testing results, threat intelligence, and incident learning. |

---

### G — Govern AI Lifecycle

| Level | Indicators |
|-------|-----------|
| 1 | No AI governance process. AI use cases are not formally reviewed or approved. No AI policy. |
| 2 | Basic AI acceptable use policy exists. Some AI tools are reviewed informally before use. |
| 3 | Formal AI intake process is operational. Governance roles are defined. AI lifecycle stages are documented. |
| 4 | AI governance is integrated into procurement, architecture review, and vendor management. Lifecycle reassessment is systematic. |
| 5 | AI governance is automated where possible. Policy is continuously updated. Governance metrics are tracked and reported. |

---

### E — Evidence, Assurance & Enablement

| Level | Indicators |
|-------|-----------|
| 1 | No AI assurance activities. No AI-related metrics or reporting. No enablement resources. |
| 2 | Some AI-related logging exists. Basic reporting to leadership is informal. |
| 3 | AI assurance dashboard is operational. Key metrics are tracked. Enablement resources exist (approved tool catalog, safe prompting guide). |
| 4 | Control testing is systematic. Evidence library is maintained. Executive reporting is formalized. |
| 5 | Continuous assurance is operational. AI security maturity is independently assessed. Enablement program is measured for effectiveness. |

---

## How to Use This Model

### Step 1 — Self-Assessment
For each BRIDGE domain, identify which level best describes your current state. Use the indicators above as a guide. Be honest — Level 3 is a strong position for most organizations.

### Step 2 — Gap Analysis
For each domain, identify the gap between your current level and your target level. What capabilities, processes, or controls need to be in place to move to the next level?

### Step 3 — Roadmap
Build a roadmap that prioritizes the most impactful improvements. Focus first on domains where your maturity is lowest relative to your risk exposure.

### Step 4 — Track Progress
Reassess maturity annually (or after significant program changes). Track progress over time and report to leadership.

---

## Maturity Assessment Template

| BRIDGE Domain | Current Level | Target Level | Key Gap | Priority Action | Owner | Target Date |
|---------------|--------------|-------------|---------|----------------|-------|-------------|
| B — Baseline AI Usage | | | | | | |
| R — Regulate Access & Data Flow | | | | | | |
| I — Identify AI Risk & Threats | | | | | | |
| D — Design Secure AI Controls | | | | | | |
| G — Govern AI Lifecycle | | | | | | |
| E — Evidence, Assurance & Enablement | | | | | | |

---

## Implementation Roadmap Reference

### First 30 Days (Level 1 → Level 2)
- Create AI governance working group
- Draft AI acceptable use policy
- Start AI tool inventory
- Identify browser-based AI usage
- Classify approved, restricted, and prohibited AI tools
- Build initial AI use case intake form

### Days 31–60 (Level 2 → Level 3)
- Implement browser and DLP controls for AI access
- Review major SaaS AI features
- Create AI risk assessment template
- Build coding assistant security guidance
- Identify high-risk AI use cases
- Start employee awareness campaign

### Days 61–90 (Level 3 → Level 4)
- Establish formal AI governance process
- Integrate AI review into procurement and architecture review
- Perform threat modeling for high-risk AI use cases
- Define agentic AI security controls
- Create AI assurance dashboard
- Report AI risk posture to leadership

---

## Related Documents

- [01 — Overview](01-overview.md)
- [02 — The BRIDGE Model](02-bridge-model.md)
- [08 — AI Assurance and Evidence](08-ai-assurance-and-evidence.md)
