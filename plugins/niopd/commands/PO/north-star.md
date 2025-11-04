---
argument-hint: [--product=<product_name>] [--metric=<proposed_metric>] [--vision=<product_vision>]
description: Identifies and aligns around a single North Star metric that captures the core value delivered to customers.
---

# Command: /niopd:PO:north-star

This command identifies and aligns around a single North Star metric that captures the core value delivered to customers, ensuring all teams work toward a common goal.

## Theoretical Foundation

### Origin and Development
The North Star Metric concept was popularized by **Sean Ellis** (growth hacking pioneer) and **Amplitude**'s product team in the 2010s. It evolved from the "**One Metric That Matters**" (OMTM) concept from **Lean Analytics** (Croll & Yoskovitz, 2013).

### Core Principle
The North Star Metric is the **single metric** that best captures the **core value** delivered to customers. It serves as a company's **true north** - the leading indicator of sustainable growth that aligns all teams toward a common goal.

### North Star Criteria

A good North Star metric must be:

**1. Captures Value** - Represents customer benefit
- Not vanity metric
- Reflects real value delivery
- Customer-centric

**2. Actionable** - Guides decisions
- Teams can influence it
- Clear improvement strategies
- Drives prioritization

**3. Universal** - Applies company-wide
- All teams contribute
- Cross-functional alignment
- Shared ownership

**4. Predictive** - Leads business outcomes
- Correlates with revenue
- Indicates future success
- Early warning system

**5. Measurable** - Quantifiable and trackable
- Clear definition
- Reliable data
- Real-time tracking

### Examples of North Star Metrics

- **Airbnb**: Nights Booked
- **Facebook**: Daily Active Users (DAU)
- **Slack**: Messages Sent by Teams
- **Spotify**: Time Spent Listening
- **Amazon**: Purchases per Month
- **Netflix**: Hours Watched
- **Uber**: Rides per Week

### North Star vs. Other Metrics

**North Star** (Leading):
- Predicts future success
- Captures customer value
- Drives daily decisions

**Revenue** (Lagging):
- Confirms past success
- Financial outcome
- Board/investor focus

**Growth Rate** (Secondary):
- Rate of change
- Momentum indicator
- Marketing focus

### Supporting Metrics Framework

**Input Metrics** (Drivers):
- Actions that increase North Star
- Team-specific metrics
- Tactical focus areas

**North Star Metric** (Core):
- Single unifying metric
- Strategic focus
- Company-wide alignment

**Output Metrics** (Outcomes):
- Revenue, retention, etc.
- Business results
- Executive/board focus

## Usage
`/niopd:PO:north-star [--product=<product_name>] [--metric=<proposed_metric>] [--vision=<product_vision>]`

## Preflight Checklist

1.  **Validate Product Name:**
    -   If the `--product` argument is not provided, prompt the user to specify the product name.
    -   Confirm that the product name is valid and meaningful.

2.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/reports` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in product strategy and North Star metrics. Your goal is to help identify and align around a single North Star metric that captures the core value delivered to customers.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you identify and align around a North Star metric for the **<product_name>** product."
-   If the `--product` argument wasn't provided, ask the user: "What product would you like to define a North Star metric for?" and wait for their response.
-   If the `--metric` argument wasn't provided, ask the user: "Do you have a proposed North Star metric in mind?" and wait for their response.
-   If the `--vision` argument wasn't provided, ask the user: "What is the product vision for **<product_name>**?" and wait for their response.

### Step 2: Product Foundation Analysis
-   Help the user define the product foundation:
    -   "What is the vision statement for **<product_name>**?"
    -   "Who is the target audience for this product?"
    -   "What is the core value proposition?"
    -   "What are the long-term aspirations for this product?"
-   Wait for the user's responses.

### Step 3: Current State Analysis
-   Guide the user through analyzing the current state:
    -   "What is the current product maturity stage?"
    -   "What is the market position and key differentiators?"
    -   "What is the business model?"
    -   "What growth stage is the product currently in?"
-   Wait for the user's responses.

### Step 4: Success Definition
-   Help the user define success metrics:
    -   "How do customers define success when using this product?"
    -   "What business outcomes does this product drive?"
    -   "Is there stakeholder alignment on success metrics?"
    -   "What is the time horizon for measuring success?"
-   Wait for the user's responses.

### Step 5: Customer Value Assessment
-   Guide the user through understanding customer value:
    -   "What are the core jobs customers hire this product to accomplish?"
    -   "How does the product create value for end users, paying customers, and beneficiaries?"
    -   "What customer success metrics are most important?"
-   Wait for the user's responses.

### Step 6: North Star Criteria Explanation
-   Explain the North Star criteria to the user:
    -   "A good North Star metric should capture value, be actionable, universal, predictive, and measurable."
    -   "Let me explain each criterion in detail:"
        -   "Capture Value: Represents the primary benefit customers receive"
        -   "Actionable: Guides clear product and business decisions"
        -   "Universal: Applies across all product areas and teams"
        -   "Predictive: Correlates with long-term business outcomes"
        -   "Measurable: Quantifiable and trackable over time"
-   Ask the user: "Do you understand these criteria, or would you like me to explain any in more detail?" and wait for their response.

### Step 7: Metric Candidate Generation
-   Help the user brainstorm North Star metric candidates:
    -   "Based on our discussion, what are some potential North Star metrics for **<product_name>**?"
    -   "Let's consider metrics that capture the core value delivered to customers."
-   Wait for the user's responses.

### Step 8: Metric Evaluation
-   Guide the user through evaluating each candidate metric against the North Star criteria:
    -   For each proposed metric, ask the user to rate it on a scale of 1-5 for each criterion:
        -   "How well does this metric capture value? (1-5)"
        -   "How actionable is this metric? (1-5)"
        -   "How universal is this metric? (1-5)"
        -   "How predictive is this metric? (1-5)"
        -   "How measurable is this metric? (1-5)"
    -   Calculate the total score for each metric.
-   Wait for the user's responses.

### Step 9: North Star Metric Selection
-   Help the user select the best North Star metric based on scores and discussion:
    -   "Based on our evaluation, which metric should be the North Star for **<product_name>**?"
    -   "Let's define this metric in detail:"
        -   "What is the precise definition of this metric?"
        -   "How will it be calculated?"
        -   "What data sources will we use?"
        -   "How frequently will we measure it?"
-   Wait for the user's responses.

### Step 10: Supporting Metrics
-   Help the user identify supporting metrics:
    -   "What leading indicators will help predict North Star performance?"
    -   "What lagging indicators will confirm North Star outcomes?"
    -   "What input metrics influence the North Star?"
    -   "What output metrics flow from the North Star?"
-   Wait for the user's responses.

### Step 11: Implementation Roadmap
-   Guide the user through planning the implementation:
    -   "What steps are needed to adopt this North Star metric?"
    -   "How will we educate the team about this metric?"
    -   "What tools and dashboards do we need to set up?"
    -   "How will we communicate this metric to stakeholders?"
-   Wait for the user's responses.

### Step 12: Team Alignment
-   Help the user consider cross-functional impact:
    -   "How will this North Star metric influence the product team's decisions?"
    -   "How will engineering align with this metric?"
    -   "How will design work connect to this North Star?"
    -   "How will marketing and sales drive this metric?"
-   Wait for the user's responses.

### Step 13: Measurement Framework
-   Guide the user in establishing measurement mechanisms:
    -   "What data infrastructure do we need to support this metric?"
    -   "What tracking mechanisms will we use?"
    -   "How often will we review performance?"
-   Wait for the user's responses.

### Step 14: Risk Management
-   Help the user identify potential risks:
    -   "What implementation risks do we need to consider?"
    -   "How might this metric be gamed or misinterpreted?"
    -   "What data quality issues might arise?"
-   Wait for the user's responses.

### Step 15: Success Metrics
-   Guide the user in defining success metrics for the North Star implementation:
    -   "How will we measure the success of our North Star implementation?"
    -   "What organizational impacts should we expect?"
    -   "What business outcomes will indicate success?"
-   Wait for the user's responses.

### Step 16: Create North Star Framework Report
Produce a markdown report with the following structure:

---
# North Star Framework Report: [Product Name]

## Executive Summary
*A brief overview of the selected North Star metric and key insights*

## Product Foundation
### Vision Statement
[Product vision identified in Step 2]

### Target Audience
[Target audience identified in Step 2]

### Core Value Proposition
[Value proposition identified in Step 2]

## Current State Analysis
[Current state analysis from Step 3]

## Customer Value Assessment
[Customer value insights from Step 5]

## Selected North Star Metric
### Metric Name
[Name of selected North Star metric]

### Definition
[Precise definition from Step 9]

### Calculation Method
[Calculation method from Step 9]

### Data Sources
[Data sources from Step 9]

### Frequency of Measurement
[Measurement frequency from Step 9]

## Supporting Metrics
[Supporting metrics identified in Step 10]

## Implementation Roadmap
[Roadmap developed in Step 11]

## Team Alignment
[Cross-functional alignment from Step 12]

## Measurement Framework
[Measurement framework from Step 13]

## Risk Management
[Risk management plan from Step 14]

## Success Metrics
[Success metrics from Step 15]

---

### Step 17: Save the Report
- Generate a filename for the North Star Framework report following the NioPD naming convention: `[YYYYMMDD]-[product_slug]-north-star-v[version].md`.
- Save the North Star Framework report to: `niopd-workspace/docs/[filename]`

### Step 18: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the North Star Framework analysis for the **<product_name>** product."
- Provide the path to the file: "You can view the detailed North Star Framework report at: `niopd-workspace/docs/[YYYYMMDD]-[product_slug]-north-star-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PO:north-star` to revisit and refine this analysis as your product evolves, or `/niopd:PM:kpis` to track progress against your North Star metric."

## Error Handling
- **Missing Product Name:** If no product name is specified, explain that a product name is required and ask for one.
- **Incomplete Metric Evaluation:** If the user doesn't provide sufficient information for metric evaluation, explain what's needed and offer to proceed with partial analysis.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial North Star analysis can still provide value.
```

This command generates a comprehensive North Star Framework report to identify and align around a single metric that captures the core value delivered to customers. The report includes customer value assessment, metric evaluation, implementation roadmap, and success metrics.