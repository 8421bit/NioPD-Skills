---
name: niopd-pm-risk-analysis
description: Conducts systematic risk assessment and mitigation planning. Use for project planning, launch preparation, investment decisions, or proactive issue prevention.
---

# Risk Analysis Skill

This skill conducts systematic risk identification and mitigation planning using probability-impact assessment.

## Theoretical Foundation

### Risk Assessment Matrix

| | Low Impact | Medium Impact | High Impact |
|---|------------|---------------|-------------|
| **High Probability** | Medium | High | Critical |
| **Medium Probability** | Low | Medium | High |
| **Low Probability** | Low | Low | Medium |

### Risk Categories

| Category | Examples |
|----------|----------|
| **Technical** | Performance, integration, security |
| **Schedule** | Dependencies, estimation, resources |
| **Resource** | Skills, availability, budget |
| **External** | Vendors, regulations, market |
| **Business** | Strategy changes, stakeholder alignment |

### Risk Response Strategies
- **Avoid**: Change plan to eliminate risk
- **Mitigate**: Reduce probability or impact
- **Transfer**: Shift to third party (insurance, vendor)
- **Accept**: Acknowledge and monitor

### When to Use
- Project kickoff
- Sprint planning
- Launch preparation
- Quarterly reviews
- Major decisions

## Instructions

### Step 1: Identify Risks
For each category, brainstorm:
- "What could go wrong?"
- "What are we assuming will go well?"
- "What has caused problems before?"

### Step 2: Assess Each Risk
| Risk | Probability | Impact | Score | Category |
|------|-------------|--------|-------|----------|
| [Risk] | H/M/L | H/M/L | [P×I] | [Type] |

### Step 3: Prioritize
Focus on:
- High probability × High impact
- Issues with no current mitigation
- Risks outside our control

### Step 4: Develop Mitigations
For priority risks:
- **Mitigation Strategy**: [How to reduce]
- **Owner**: [Who is responsible]
- **Trigger**: [When to escalate]
- **Contingency**: [If risk materializes]

### Step 5: Create Monitoring Plan
- What indicators signal risk increase?
- How often to review?
- Who monitors each risk?

### Step 6: Generate Report
**File path**: `02-reports/[YYYYMMDD]-risk-analysis-v0.md`

| Risk | P | I | Mitigation | Owner | Status |
|------|---|---|------------|-------|--------|
| [Risk] | H/M/L | H/M/L | [Action] | [Who] | 🟢/🟡/🔴 |

## Output Specifications
- **File Naming**: `[YYYYMMDD]-risk-analysis-v0.md`
- **Location**: `02-reports/`
- **Template**: `references/risk-analysis-template.md`

## Related Skills
- `niopd-pm-dependencies`: Dependency risks
- `niopd-dt-scenarios`: Future scenarios
- `niopd-pm-release`: Release risks
- `niopd-pd-experiment`: Validation planning
