---
name: niopd-ur-satisfaction
description: Analyzes user satisfaction metrics (NPS, CSAT). Use for customer health monitoring, product quality assessment, or stakeholder reporting.
---

# User Satisfaction Analysis Skill

This skill analyzes satisfaction metrics to understand customer health.

## Theoretical Foundation

### Key Metrics
| Metric | Scale | Meaning |
|--------|-------|---------|
| **NPS** | -100 to +100 | "Would you recommend?" |
| **CSAT** | 1-5 or 1-10 | "How satisfied were you?" |
| **CES** | 1-7 | "How easy was this?" |

### NPS Categories
- **Promoters** (9-10): Loyal enthusiasts
- **Passives** (7-8): Satisfied but vulnerable
- **Detractors** (0-6): Unhappy customers

## Instructions

### Step 1: Gather Satisfaction Data
Collect from:
- NPS surveys
- CSAT responses
- Review scores
- Support ratings

### Step 2: Calculate Scores
| Metric | Score | Benchmark | Trend |
|--------|-------|-----------|-------|
| NPS | [X] | [Industry avg] | ↑/↓/→ |
| CSAT | [X%] | [Industry avg] | ↑/↓/→ |

### Step 3: Identify Drivers
What drives satisfaction/dissatisfaction?

### Step 4: Recommend Actions
Prioritize improvements by impact

### Step 5: Generate Report
**File path**: `02-reports/[YYYYMMDD]-satisfaction-v0.md`

## Output Specifications
- **File Naming**: `[YYYYMMDD]-satisfaction-v0.md`
- **Location**: `02-reports/`
- **Template**: `references/satisfaction-template.md`
