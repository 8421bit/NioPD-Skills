---
argument-hint: [--for=<initiative_name>]
description: Generates a KPI status report for an initiative. Auto-detects initiative name from current directory if not specified.
---

# Command: /niopd:PM:kpis

This command generates a KPI status report for a specific initiative.

## Theoretical Foundation

### Origin and Development
Key Performance Indicators (KPIs) emerged from **Management by Objectives (MBO)** by **Peter Drucker** (1954) and **Balanced Scorecard** by **Kaplan & Norton** (1992). Modern KPI frameworks emphasize **leading vs. lagging indicators** and **actionable metrics** over vanity metrics.

### Core Principle
KPIs are **quantifiable measurements** that evaluate success in achieving objectives. They answer "How do we know if we're succeeding?" by translating strategy into measurable outcomes. Good KPIs drive decisions and actions.

### KPI Types

**Leading Indicators** (Predictive):
- **Predict** future performance
- **Example**: Website visits → predicts sales
- **Action**: Change inputs to affect outcomes

**Lagging Indicators** (Historical):
- **Measure** past performance
- **Example**: Revenue, customer churn
- **Action**: Learn from results

### SMART KPIs

- **S**pecific: Clear definition
- **M**easurable: Quantifiable
- **A**chievable**: Realistic targets
- **R**elevant**: Aligned to objectives
- **T**ime-bound**: Defined timeframe

### Related Frameworks
- **OKRs**: Objectives and Key Results (Google)
- **North Star Metric**: Single focus metric
- **HEART**: Happiness, Engagement, Adoption, Retention, Task Success
- **AARRR**: Acquisition, Activation, Retention, Revenue, Referral

## Usage
`/niopd:PM:kpis [--for=<initiative_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative name.

**Examples:**
```bash
# Explicit initiative name
/niopd:PM:kpis --for=dark-mode-feature

# Auto-detect from current directory
cd dark-mode-feature
/niopd:PM:kpis  # Uses "dark-mode-feature"
```

## Preflight Checklist

1.  **Determine Initiative Name:**
    -   If `--for=<initiative_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative name from current directory: `<directory_name>`"
    -   Store the determined name as `<initiative_name>` for use in all subsequent steps

2.  **Validate Initiative:**
    -   Check that the initiative file `niopd-workspace/docs/*<initiative_slug>*.md` exists. If not, inform the user.

## Instructions

You are a specialized AI expert in tracking Key Performance Indicators (KPIs). Your goal is to provide comprehensive KPI monitoring and analysis for product initiatives.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request: "You got it. I'll check the latest KPI status for the **<initiative_name>** initiative."
-   Read the initiative file from `niopd-workspace/docs/`.

### Step 2: File Location & Validation
- Locate the initiative file in `niopd-workspace/docs/`.
- Verify that the file exists and is readable.
- Check that the file contains the required KPI tracking sections.

### Step 3: KPI Identification & Extraction
- Identify all defined KPIs in the initiative file.
- Extract KPI names, targets, current values, and measurement methods.
- Note any KPIs that are leading indicators vs. lagging indicators.
- Identify KPIs that are quantitative vs. qualitative.

### Step 4: Data Collection & Verification
- Collect current values for each KPI from available sources.
- Verify data accuracy and consistency across sources.
- Identify any missing or incomplete KPI data.
- Note the frequency and recency of KPI measurements.

### Step 5: Status Assessment & Calculation
- Calculate progress percentages for each KPI.
- Determine status indicators (✅ Achieved, 🟢 On Track, 🟡 At Risk, 🔴 Off Track, 🔵 Not Started).
- Compare current values to targets and baselines.
- Identify any KPIs that have improved, declined, or remained stable.

### Step 6: Trend Analysis
- Analyze performance trajectories over time.
- Identify patterns, cycles, or anomalies in KPI performance.
- Compare current performance to historical trends.
- Project future performance based on current trajectories.

### Step 7: Risk Assessment
- Identify KPIs that are at risk or off track.
- Assess the potential impact of underperforming KPIs.
- Identify root causes of KPI issues.
- Note any external factors affecting KPI performance.

### Step 8: Opportunity Analysis
- Identify KPIs that are exceeding targets.
- Assess opportunities for leveraging overperformance.
- Note any positive trends or emerging strengths.
- Identify areas for acceleration or expansion.

### Step 9: Recommendation Development
- Develop specific, actionable recommendations for at-risk KPIs.
- Suggest strategies for maintaining or improving on-track KPIs.
- Identify resource needs or support requests.
- Prioritize recommendations based on impact and urgency.

### Step 10: Context & External Factors
- Identify market conditions affecting KPI performance.
- Note resource constraints or support needs.
- Consider seasonal or temporal factors.
- Assess the impact of external events or changes.

### Step 11: KPI Status Report Generation
Produce a markdown report with the following structure:

```
---
# KPI Status Report: [Initiative Name]

## Executive Summary
*A high-level overview of overall KPI performance and key insights*

## Overall Initiative Status
- **Overall Health:** [Overall status with color indicator]
- **KPIs Tracked:** [Number] metrics monitored
- **On Target:** [Number] metrics performing well
- **At Risk:** [Number] metrics requiring attention
- **Off Track:** [Number] metrics with significant concerns

## KPI Performance Dashboard

### ✅ Achieved Metrics
#### KPI 1: [Name of KPI]
- **Target:** [Target Value]
- **Current:** [Current Value]
- **Progress:** [Percentage] complete
- **Status:** ✅ Achieved
- **Achievement Date:** [Date if available]
- **Impact:** [Business impact of achievement]

### 🟢 On Track Metrics
#### KPI 2: [Name of KPI]
- **Target:** [Target Value]
- **Current:** [Current Value]
- **Baseline:** [Starting Value]
- **Progress:** [Percentage] complete
- **Trend:** [Improving/Stable/Declining]
- **Projection:** [Estimated completion date]
- **Status:** 🟢 On Track
- **Insight:** [Key insight about performance]

### 🟡 At Risk Metrics
#### KPI 3: [Name of KPI]
- **Target:** [Target Value]
- **Current:** [Current Value]
- **Baseline:** [Starting Value]
- **Progress:** [Percentage] complete
- **Gap to Target:** [Absolute and percentage gap]
- **Trend:** [Improving/Stable/Declining]
- **Status:** 🟡 At Risk
- **Concerns:** [Key issues or risks]
- **Recommended Actions:** [Suggested interventions]

### 🔴 Off Track Metrics
#### KPI 4: [Name of KPI]
- **Target:** [Target Value]
- **Current:** [Current Value]
- **Baseline:** [Starting Value]
- **Progress:** [Percentage] complete
- **Gap to Target:** [Absolute and percentage gap]
- **Trend:** [Improving/Stable/Declining]
- **Projection:** [Estimated outcome if current trend continues]
- **Status:** 🔴 Off Track
- **Critical Issues:** [Major problems or blockers]
- **Urgent Actions Needed:** [Immediate interventions required]

### 🔵 Not Started/Inactive Metrics
#### KPI 5: [Name of KPI]
- **Target:** [Target Value]
- **Current:** [Current Value or "Not Measured"]
- **Status:** 🔵 Not Started
- **Planned Start:** [Date if available]
- **Dependencies:** [What needs to happen first]

## Trend Analysis

### Performance Trajectory
- **Overall Trend:** [Improving/Stable/Declining]
- **Rate of Change:** [Quantified improvement or decline]
- **Key Drivers:** [Main factors affecting performance]

### Milestone Progress
- **Completed Milestones:** [List of achieved interim goals]
- **Upcoming Milestones:** [List of next targets]
- **Missed Milestones:** [List of any unmet interim goals]

## Risk Assessment

### High Priority Risks
1. **[Risk]:** [Description and potential impact]
2. **[Risk]:** [Description and potential impact]

### Moderate Concerns
1. **[Concern]:** [Description and potential impact]
2. **[Concern]:** [Description and potential impact]

## Opportunity Analysis

### Exceeding Expectations
- **[KPI/Aspect]:** [How performance exceeds targets and potential for further improvement]

### Acceleration Opportunities
- **[Opportunity]:** [How to leverage current success for greater results]

## Recommendations

### Immediate Actions (0-30 days)
1. **[Action]:** [Specific, time-bound recommendation]
2. **[Action]:** [Specific, time-bound recommendation]

### Strategic Adjustments (1-3 months)
1. **[Adjustment]:** [Suggested changes to approach or targets]
2. **[Adjustment]:** [Suggested changes to approach or targets]

### Long-term Considerations (3+ months)
1. **[Consideration]:** [Strategic implications for future planning]
2. **[Consideration]:** [Strategic implications for future planning]

## Context & External Factors

### Market Conditions
- **[Factor]:** [How external conditions affect KPIs]
- **[Factor]:** [How external conditions affect KPIs]

### Resource Considerations
- **[Constraint/Support]:** [How resource availability impacts performance]
- **[Constraint/Support]:** [How resource availability impacts performance]

## Appendix

### Detailed KPI Definitions
#### [KPI Name]
- **Definition:** [Precise definition of what is measured]
- **Calculation Method:** [How the metric is computed]
- **Data Source:** [Where the data comes from]
- **Frequency:** [How often it's measured]

### Historical Performance (if available)
[Data table or summary of historical KPI performance]

### Measurement Notes
[Any important details about how KPIs are tracked or limitations in measurement]

---
*Report generated on [Date]*
*Initiative: [Initiative Name]*

### Step 10: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_slug]-kpis-v[version].md`.
- Save the report to: `niopd-workspace/plans/[filename]`

### Step 11: Confirm and Conclude
- Confirm the action is complete: "✅ The KPI status report is ready."
- Provide the path to the file: "You can view it here: `niopd-workspace/plans/[YYYYMMDD]-[initiative-name]-kpi-report-v1.md`"

## Error Handling
- **Missing KPI Information:** If KPI sections are incomplete or missing, note which information is unavailable and explain how this affects analysis.
- **Invalid Data Formats:** If KPI values are in unclear formats, explain the issue and suggest standard formats (percentages, counts, time periods).
- **Unrealistic Targets:** If targets appear unrealistic based on baselines or current progress, note this and suggest review.
- **Insufficient Data:** If too few KPIs are defined to provide meaningful analysis, suggest expanding metric definition.
- **Inconsistent Status Information:** If status indicators in the initiative file conflict with calculated values, highlight discrepancies and use calculated values as primary.

In all error cases, provide clear explanations, suggest improvements, and focus on extracting maximum value from available information.