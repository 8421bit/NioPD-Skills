---
name: niopd-pm-kpis
description: Defines and tracks Key Performance Indicators for product features and initiatives. Use for metrics planning, success measurement, stakeholder reporting, or OKR alignment.
---

# KPI Definition and Tracking Skill

This skill helps define, structure, and track Key Performance Indicators that measure product success.

## Theoretical Foundation

### What Makes a Good KPI
**SMART Criteria:**
- **S**pecific: Precise definition
- **M**easurable: Quantifiable
- **A**chievable: Realistic target
- **R**elevant: Aligned to goals
- **T**ime-bound: Clear deadline

### KPI Hierarchy

| Level | Example | Owner |
|-------|---------|-------|
| **North Star** | Monthly Active Users | CEO/CPO |
| **Input Metrics** | Daily Signups, Retention | Product |
| **Feature Metrics** | Feature Adoption Rate | PM |
| **Health Metrics** | Error Rate, Latency | Engineering |

### Common Product KPIs
- **Acquisition**: CAC, Conversion Rate
- **Activation**: Time to Value, Completion Rate
- **Retention**: D7/D30 Retention, Churn
- **Revenue**: ARPU, LTV
- **Referral**: NPS, Viral Coefficient

### When to Use
- Feature launch planning
- Product review preparation
- OKR setting
- Stakeholder alignment
- Success evaluation

## Instructions

### Step 1: Identify Objectives
- "What are we trying to achieve with this feature/product?"
- "What behavior change do we want?"
- "What business impact do we expect?"

### Step 2: Define KPIs
For each objective:

```markdown
### KPI: [Name]

**Definition**: [Precise definition]
**Formula**: [How calculated]
**Data Source**: [Where data comes from]
**Owner**: [Who is responsible]

**Baseline**: [Current value]
**Target**: [Goal value]
**Timeline**: [By when]

**Leading Indicators**: [Early signals]
**Lagging Indicators**: [Outcome measures]
```

### Step 3: Set Targets
- Review historical data
- Benchmark against industry
- Consider resource constraints
- Set stretch but achievable goals

### Step 4: Define Tracking Cadence
- Daily: Health metrics
- Weekly: Feature metrics
- Monthly: Product metrics
- Quarterly: Business metrics

### Step 5: Create Dashboard View
| KPI | Baseline | Target | Current | Status | Trend |
|-----|----------|--------|---------|--------|-------|
| [KPI] | [X] | [Y] | [Z] | 🟢/🟡/🔴 | ↑/↓/→ |

### Step 6: Generate Report
**File path**: `02-reports/[YYYYMMDD]-kpi-report-v0.md`

## Output Specifications
- **File Naming**: `[YYYYMMDD]-kpi-report-v0.md`
- **Location**: `02-reports/`
- **Template**: `references/kpi-report-template.md`

## Related Skills
- `niopd-st-okr`: OKR framework
- `niopd-po-aarrr-metrics`: AARRR funnel
- `niopd-po-north-star`: North Star Metric
- `niopd-pm-feature-metrics`: Feature-specific metrics
