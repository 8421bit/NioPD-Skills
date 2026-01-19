---
name: niopd-st-rice
description: Applies RICE prioritization framework to score and rank features or initiatives. Use for feature prioritization, roadmap planning, resource allocation decisions, or stakeholder alignment on priorities.
---

# RICE Prioritization Skill

This skill applies the RICE framework (Reach, Impact, Confidence, Effort) to systematically prioritize features, initiatives, or projects.

## Theoretical Foundation

### Origin
RICE was developed by **Intercom** as a systematic way to prioritize features in a product backlog, combining quantitative assessment with structured effort estimation.

### The RICE Formula

```
RICE Score = (Reach × Impact × Confidence) ÷ Effort
```

| Factor | Definition | Scale |
|--------|------------|-------|
| **Reach** | How many customers affected in time period | Number (e.g., users/quarter) |
| **Impact** | How much will it improve outcomes | 0.25-3 (Minimal to Massive) |
| **Confidence** | How sure are we of estimates | 20%-100% |
| **Effort** | Person-months to complete | Number |

### Impact Scale
- **3** = Massive impact
- **2** = High impact
- **1** = Medium impact
- **0.5** = Low impact
- **0.25** = Minimal impact

### When to Use
- Roadmap planning sessions
- Sprint prioritization
- Feature request evaluation
- Resource allocation decisions
- Stakeholder alignment

## Instructions

### Step 1: Gather Items
List all features/initiatives to prioritize from:
- Backlog
- Feedback analysis
- Strategic initiatives
- Stakeholder requests

### Step 2: Score Reach
For each item:
- "How many customers will this affect in [quarter/month]?"
- Use actual data when available
- Estimate when necessary

### Step 3: Score Impact
For each item:
- "How much will this improve outcomes for affected users?"
- Use 0.25-3 scale
- Consider metrics movement

### Step 4: Score Confidence
For each item:
- "How confident are we in Reach and Impact estimates?"
- 100% = High certainty (data-backed)
- 80% = Medium (educated guess)
- 50% = Low (speculation)

### Step 5: Estimate Effort
For each item:
- "How many person-months to complete?"
- Include design, dev, QA, launch
- Use team input when possible

### Step 6: Calculate Scores
Apply formula:

| Feature | Reach | Impact | Confidence | Effort | **Score** |
|---------|-------|--------|------------|--------|-----------|
| [F1] | 10,000 | 2 | 80% | 3 | **5,333** |
| [F2] | 5,000 | 3 | 50% | 2 | **3,750** |

### Step 7: Rank and Discuss
- Sort by RICE score descending
- Discuss outliers and concerns
- Consider strategic alignment
- Make final priority decisions

### Step 8: Generate Report
**File path**: `02-reports/[YYYYMMDD]-rice-prioritization-v0.md`

**Contents:**
1. Prioritized list with scores
2. Methodology notes
3. Key decisions made
4. Next steps

## Output Specifications
- **File Naming**: `[YYYYMMDD]-rice-prioritization-v0.md`
- **Location**: `02-reports/`
- **Template**: `references/rice-template.md`

## Related Skills
- `niopd-st-moscow`: Alternative prioritization
- `niopd-ur-kano`: Satisfaction-based categorization
- `niopd-pd-roadmap`: Roadmap creation
- `niopd-bs-feature-planning`: Feature ideation
