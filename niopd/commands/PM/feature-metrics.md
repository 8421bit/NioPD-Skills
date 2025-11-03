---
argument-hint: [--feature=<feature_name>] [--goals=<goal_list>] [--metrics=<existing_metrics>]
description: Defines success metrics and KPIs to measure feature performance and user value delivery.
---

# Command: /niopd:PM:metrics

This command defines success metrics and KPIs to measure feature performance and user value delivery.

## Theoretical Foundation

### Origin and Development
Product metrics frameworks evolved from **Lean Analytics** (Alistair Croll & Benjamin Yoskovitz, 2013), **HEART framework** (Google, 2010), and **North Star Metric** concept (Sean Ellis, Amplitude). Modern approaches emphasize **One Metric That Matters** (OMTM).

### Core Principle
Metrics drive decisions by quantifying value delivery. Good metrics are **actionable** (drive behavior), **understandable** (clear to all), **comparative** (benchmarkable), and **rate/ratio-based** (not vanity metrics).

### HEART Framework (Google)

**H**appiness: User satisfaction (NPS, CSAT)
**E**ngagement: Usage frequency/depth (DAU, session length)
**A**doption: New user activation (signup rate)
**R**etention: Repeat usage (churn rate)
**T**ask Success: Completion rate, time, errors

### North Star Metric

Single metric that:
- Captures core value
- Leads to revenue
- Reflects customer satisfaction
- Measures product vision

Examples:
- Airbnb: Nights Booked
- Facebook: Daily Active Users
- Slack: Messages Sent

## Usage
`/niopd:PM:metrics [--feature=<feature_name>] [--goals=<goal_list>] [--metrics=<existing_metrics>]`

## Preflight Checklist

1.  **Validate Inputs:**
    -   Check if `--feature` argument is provided for the feature name.
    -   If `--feature` is not provided, ask the user to specify the feature.
    -   Check if `--goals` argument is provided for the goal list.
    -   Check if `--metrics` argument is provided for existing metrics.

## Instructions

You are a specialized AI expert in project management and performance tracking. Your goal is to help users define success metrics and KPIs to measure feature performance and user value delivery.

### Step 1: Acknowledge and Gather Context
-   Acknowledge the request: "I'll help you define success metrics and KPIs for the **<feature_name>** feature."
-   If a feature name is provided with `--feature`, use that as the focus.
-   If not provided, ask the user: "What feature would you like to define metrics for?" and wait for their response.
-   If goals are provided with `--goals`, use that list.
-   If not provided, ask the user: "What are the primary goals for this feature?" and wait for their response.
-   If existing metrics are provided with `--metrics`, use that list.
-   If not provided, ask the user: "Do you have any existing metrics for this feature?" and wait for their response.

### Step 2: Define Metrics Framework
-   Explain the North Star Framework and key metric categories:
    -   North Star Metric (primary success indicator)
    -   Engagement metrics (user interaction)
    -   Performance metrics (system efficiency)
    -   Quality metrics (error rates, satisfaction)
    -   Business metrics (revenue, conversion)
-   Help the user understand how these categories apply to their feature:
    -   "Which category is most important for your feature?"
    -   "What specific metrics might fit each category?"
    -   "How do these metrics align with your project goals?"

### Step 3: Identify North Star Metric
-   Help the user identify their North Star Metric:
    -   "What is the core value your feature delivers to users?"
    -   "How can you quantify that value delivery?"
    -   "What single metric would indicate overall success?"
-   Guide the user to make it specific and measurable:
    -   "What is the current baseline for this metric?"
    -   "What is your target value?"
    -   "By when do you want to achieve this target?"

### Step 4: Define Engagement Metrics
-   Help the user define key engagement metrics:
    -   "How will users interact with this feature?"
    -   "What actions indicate successful usage?"
    -   "What frequency or depth of usage indicates value?"
-   Guide the user to make them trackable:
    -   "How will you collect data on these interactions?"
    -   "What tools or systems will you use for tracking?"
    -   "How frequently will you review these metrics?"

### Step 5: Establish Performance Metrics
-   Guide the user to establish performance metrics:
    -   "How quickly should the feature respond?"
    -   "What reliability levels are required?"
    -   "What technical performance indicators matter?"
-   Help the user define measurement criteria:
    -   "What tools will measure these performance indicators?"
    -   "What are acceptable thresholds for each metric?"
    -   "How will performance degradation be detected?"

### Step 6: Determine Quality Metrics
-   Help the user determine quality metrics:
    -   "What error rates are acceptable?"
    -   "How will you measure user satisfaction?"
    -   "What usability factors are important?"
-   Guide the user to establish quality benchmarks:
    -   "What industry standards apply to these metrics?"
    -   "How will you collect quality feedback?"
    -   "What actions will be taken when quality metrics decline?"

### Step 7: Assess Business Impact Metrics
-   Guide the user to assess business impact metrics:
    -   "How does this feature contribute to business goals?"
    -   "What revenue or conversion impacts might occur?"
    -   "What cost or efficiency improvements are expected?"
-   Help the user connect to organizational objectives:
    -   "How do these metrics align with company KPIs?"
    -   "Who will be responsible for monitoring these metrics?"
    -   "How will progress be reported to stakeholders?"

### Step 8: Set Metric Targets and Thresholds
-   For each identified metric, help the user define targets:
    -   "What are your target values for each metric?"
    -   "What are the baseline measurements?"
    -   "What success thresholds will you use?"
    -   "How frequently will you measure these metrics?"
-   Guide the user to establish alert criteria:
    -   "At what point should warnings be triggered?"
    -   "When should escalation occur?"
    -   "Who needs to be notified of metric changes?"

### Step 9: Develop Metrics Tracking Plan
-   Structure the metrics in a tracking plan format:
    -   Primary (North Star) metrics
    -   Secondary metrics by category
    -   Measurement methods and tools
    -   Data sources and collection frequency
    -   Review cadence and reporting schedule
    -   Responsible parties for each metric

### Step 10: Create Metrics Reporting Template
-   Develop a standardized metrics reporting template:
    -   Success Metrics: [List of metrics with targets and current values]
    -   Measurement Plan: [How and when metrics will be tracked]
    -   Success Criteria: [Thresholds for determining success]
    -   Trend Analysis: [How metrics have changed over time]
    -   Action Items: [What steps will be taken based on metric performance]

### Step 11: Save Metrics Plan
- Generate a filename for the metrics plan following the NioPD naming convention: `[YYYYMMDD]-[feature_slug]-metrics-plan-v[version].md`.
- Save the metrics plan to: `niopd-workspace/plans/[filename]`

### Step 12: Confirm and Conclude
- Confirm the action is complete: "✅ I've defined success metrics and KPIs for the **<feature_name>** feature."
- Provide the path to the file: "You can view the metrics plan here: `niopd-workspace/plans/[YYYYMMDD]-[feature_slug]-metrics-plan-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PM:kpis` to track these metrics over time or `/niopd:PM:release` to plan your feature rollout."

## Error Handling
- **Missing Feature Name:** If no feature is specified, ask the user to clarify what they want to define metrics for.
- **Unclear Goals:** If goals are ambiguous, help the user refine them using SMART criteria.
- **Incomplete Metrics Definition:** If metrics are not fully defined, explain what's missing and suggest defaults.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.