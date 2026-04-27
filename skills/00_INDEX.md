# Yao Skill Repository Index

This index is the routing map for reusable ChatGPT / Codex skills.

## Repository Structure

```text
skills/
├── 00_INDEX.md
├── 01_Tender_Intelligence/
├── 02_Competitor_Analysis/
├── 03_Product_Strategy/
├── 04_Slide_Output/
└── 99_Templates/
```

---

## Trigger Map

| Trigger | Skill | File | Use When |
|---|---|---|---|
| `TENDER-SKILL` | Tender Intelligence Extraction Skill v1.1 | `skills/01_Tender_Intelligence/tender_intelligence_extraction_skill_v1.1.md` | Analyze shared micromobility tenders, permits, concessions, bike-sharing / e-bike / e-scooter procurement documents. |
| `SCORING-SKILL` | Tender Scoring Breakdown Skill | TBD | Break down tender scoring rules, weights, thresholds, award logic, and supplier implications. |
| `TEARDOWN-SKILL` | Competitor Vehicle Teardown Skill | TBD | Analyze competitor e-bike / e-scooter vehicle architecture, BOM, modules, TCO impact, and product positioning. |
| `TCO-SKILL` | TCO 2.0 Product Strategy Skill | TBD | Analyze product value proposition through OPEX, CAPEX, lifecycle, serviceability, and operator economics. |
| `ONEPAGE-SKILL` | Executive One-page Skill | TBD | Convert analysis into executive-ready one-page summary. |
| `FRONTEND-SLIDE-SKILL` | Frontend Slide HTML Skill | TBD | Generate single-file HTML slides following Yao's frontend slide format. |

---

## Current Active Skills

### TENDER-SKILL

- **File:** `skills/01_Tender_Intelligence/tender_intelligence_extraction_skill_v1.1.md`
- **Purpose:** Extract structured information from shared micromobility tenders and assess hardware supplier opportunities.
- **Primary outputs:**
  1. Basic tender information
  2. Vehicle and fleet scale
  3. Scoring structure
  4. Top evaluation criteria
  5. Hardware and product requirements
  6. Business opportunity judgment
  7. Risks and constraints
  8. Executive conclusion and next actions

---

## Standard Calling Format

```text
[TRIGGER]

Task:
Input:
Output:
Constraints:
```

Example:

```text
TENDER-SKILL

Task: Analyze a city shared e-bike tender.
Input: [official tender URL or uploaded PDF]
Output: Full structured tender extraction + Segway hardware supplier opportunity.
Constraints: Use official sources first. Mark unknown fields as not disclosed.
```

---

## Maintenance Rules

1. GitHub `main` branch is the source of truth.
2. All reusable skills should be saved under `skills/`.
3. Each skill must include:
   - Version
   - Trigger
   - Purpose
   - Inputs
   - Source Priority
   - Search Rules
   - Execution Steps
   - Output Structure
   - Quality Bar
   - Failure Handling
   - Change Log
4. Update this index whenever a new skill is added or renamed.
5. Do not store one-off analysis outputs in this repository. Store only reusable workflows, templates, and routing rules.
