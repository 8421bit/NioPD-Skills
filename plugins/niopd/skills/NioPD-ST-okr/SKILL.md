---
name: niopd-st-okr
description: Applies OKR (Objectives and Key Results) framework to define and track strategic goals. Use for quarterly planning, goal alignment, performance management, or team focus.
---

# OKR Framework Skill

This skill applies the OKR framework to set ambitious, measurable goals and track progress systematically.

## Theoretical Foundation

### Origin
OKRs were developed by **Andy Grove** at Intel and popularized by **John Doerr** at Google. They're now used by leading tech companies worldwide.

### OKR Structure

```
Objective (WHAT): Qualitative, inspirational goal
├── Key Result 1 (HOW): Quantitative measure
├── Key Result 2 (HOW): Quantitative measure
└── Key Result 3 (HOW): Quantitative measure
```

| Component | Characteristics |
|-----------|-----------------|
| **Objective** | Qualitative, memorable, ambitious |
| **Key Results** | Quantitative, measurable, time-bound |

### Good OKR Criteria
- **Objectives**: Ambitious but achievable, inspiring, directive
- **Key Results**: Specific, measurable, stretch (60-70% success = healthy)

### OKR Types
- **Company OKRs**: Organizational direction
- **Team OKRs**: Departmental contribution
- **Individual OKRs**: Personal contribution

### When to Use
- Quarterly planning
- Annual strategy cascade
- Team alignment
- Performance reviews
- Focus maintenance

## Instructions

### Step 1: Define Objectives
For each objective:
- "What do we want to achieve?"
- "Why does this matter?"
- "Is it inspirational and memorable?"

### Step 2: Define Key Results
For each objective, define 2-5 key results:
- "How will we know we achieved it?"
- "What number will change?"
- "Is it ambitious but achievable?"

### Step 3: Validate KRs
Each Key Result should be:
- [ ] Specific (clear definition)
- [ ] Measurable (has a number)
- [ ] Achievable (stretch but possible)
- [ ] Relevant (drives objective)
- [ ] Time-bound (deadline)

### Step 4: Score Baseline and Targets
| KR | Baseline | Target | Stretch |
|----|----------|--------|---------|
| [KR1] | [Current] | [70% success] | [100% success] |

### Step 5: Create Tracking Plan
- Weekly: Quick confidence check
- Monthly: Detailed progress review
- Quarterly: Scoring and retrospective

### Step 6: Generate OKR Document
**File path**: `04-plans/[YYYYMMDD]-okr-[quarter]-v0.md`

**Format:**
```markdown
## Objective 1: [Objective Statement]

| Key Result | Baseline | Target | Current | Score |
|------------|----------|--------|---------|-------|
| KR1.1: [Result] | [X] | [Y] | [Z] | [0-1.0] |
| KR1.2: [Result] | [X] | [Y] | [Z] | [0-1.0] |

**Overall Score**: [Average]
**Status**: 🟢 On Track / 🟡 At Risk / 🔴 Off Track
```

## Scoring Guide
- **0.0-0.3**: Failed to make progress
- **0.4-0.6**: Made progress but fell short
- **0.7-1.0**: Delivered (1.0 may mean not ambitious enough)

## Output Specifications
- **File Naming**: `[YYYYMMDD]-okr-[quarter]-v0.md`
- **Location**: `04-plans/`
- **Template**: `references/okr-template.md`

## Related Skills
- `niopd-pm-kpis`: KPI definition
- `niopd-po-north-star`: North Star alignment
- `niopd-pd-roadmap`: Execution planning
- `niopd-st-balanced-scorecard`: Multi-dimensional goals
