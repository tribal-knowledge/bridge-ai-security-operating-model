# Example — Browser AI Access Control

> **Scenario:** A mid-sized financial services organization discovers that employees across multiple departments are using public GenAI tools through their browsers. The security team has no visibility into what tools are being used, by whom, or what data is being shared.

---

## Context

| Field | Detail |
|-------|--------|
| **Organization** | Fictional mid-sized financial services firm |
| **Challenge** | Shadow AI usage through browsers — no visibility or controls |
| **BRIDGE Domain** | B (Baseline), R (Regulate), E (Evidence) |
| **AI Category** | Browser-Based GenAI |

---

## What Was Discovered (Baseline Phase)

Through SWG and CASB log analysis, the security team identified:

- **47 distinct AI-related domains** accessed by employees in a 30-day period
- **Top tools used:** ChatGPT, Gemini, Claude.ai, Perplexity, Grammarly, Notion AI
- **Departments most active:** Operations, Marketing, Legal, Finance, and Technology
- **High-risk behaviors identified:**
  - Finance analysts uploading spreadsheets to public AI tools for data analysis
  - Legal team pasting contract language into GenAI tools for summarization
  - Developers submitting code snippets (including configuration files) to ChatGPT for debugging
  - HR team using an unapproved AI document tool to process employee records

**None of these tools were formally approved. None had been through a security or data review.**

---

## Risk Assessment Summary

| Risk | Rating | Finding |
|------|--------|---------|
| Data leakage | **High** | Financial data, contract text, employee records, and source code observed in AI sessions |
| Third-party exposure | **High** | No data processing agreements in place for any of the 47 tools identified |
| Access control failure | **Medium** | No controls preventing upload of classified data to AI tools |
| Weak monitoring | **High** | No logging of AI tool usage prior to this assessment |

---

## Controls Implemented (Regulate Phase)

### Step 1 — Tool Categorization
The 47 identified AI tools were classified:

| Tier | Tools | Count |
|------|-------|-------|
| Approved | Claude (Enterprise), Microsoft Copilot (licensed), Grammarly Business | 3 |
| Restricted | Notion AI (with conditions) | 1 |
| Tolerated (temporary) | ChatGPT (personal accounts) | 1 |
| Prohibited | All others, including unknown/unreviewed tools | 42 |

### Step 2 — Browser Controls Deployed
- **SWG:** URL categorization applied. Prohibited AI sites blocked with policy message.
- **CASB:** API-mode controls deployed for Microsoft 365 and Salesforce.
- **DLP rules added:** File upload block for `.xlsx`, `.pdf`, `.docx`, `.py`, `.js`, `.env` to uncategorized AI sites.
- **User coaching banners:** Warning message displayed when accessing Tolerated-tier AI tools.

### Step 3 — Approved Tool Guidance Published
- Approved AI tool catalog published on intranet
- Safe prompting guide distributed to all staff
- Department-specific guidance issued for Finance, Legal, and HR on what data must not be used with AI tools

---

## Evidence Collected (Evidence Phase)

| Evidence Type | Description |
|---------------|-------------|
| AI site access log (pre-controls) | Baseline 30-day access report — 47 tools, user breakdown, data uploaded |
| DLP rule configuration | Documentation of DLP rules implemented |
| Tool categorization registry | Full list of 47 tools with tier classification |
| Block confirmation report | 30-day post-implementation report showing blocked access attempts |
| User coaching touchpoints | Count of warning banners displayed and user acknowledgments |
| Approved tool catalog | Published list with guidance |

---

## Outcome

Within 60 days of implementation:

- Prohibited AI site access reduced by **78%**
- DLP blocked **34 file upload attempts** to uncategorized AI tools
- **6 departments** completed AI awareness briefings
- Security team moved from zero visibility to a structured AI access program

---

## Lessons Learned

1. Shadow AI adoption is pervasive — discovery before controls is essential
2. Users are not acting maliciously — they are using the tools they know. Education matters as much as enforcement
3. DLP rules must be tuned — initial rules generated false positives for legitimate tools
4. Approved tool availability reduces shadow AI — when approved tools were made available and easy to access, unapproved tool usage dropped significantly

---

## Related Templates
- [AI Use Case Intake Template](../templates/ai-use-case-intake-template.md)
- [AI Risk Assessment Template](../templates/ai-risk-assessment-template.md)
