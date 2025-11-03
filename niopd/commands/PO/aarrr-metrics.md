---
argument-hint: [--product=<product_name>] [--period=<time_period>] [--cohort=<cohort_definition>]
description: Analyzes growth metrics using the AARRR Pirate Framework (Acquisition, Activation, Retention, Referral, Revenue).
---

# Command: /niopd:PO:aarrr-metrics

This command analyzes growth metrics using the AARRR Pirate Framework to identify growth bottlenecks and optimization opportunities throughout the customer lifecycle.

## Theoretical Foundation

### Origin and Development
The AARRR (Pirate Metrics) framework was created by **Dave McClure** (500 Startups) in 2007. It provides a **funnel-based approach** to growth metrics, focusing on the complete customer lifecycle rather than isolated metrics.

### Core Principle
AARRR measures the **end-to-end customer journey** through five sequential stages. By analyzing conversion between stages, teams identify **growth bottlenecks** and prioritize optimization efforts where they'll have maximum impact.

### The Five Pirate Metrics

**1. Acquisition** - How do users find you?
- **Metrics**: Traffic, visitors, sources
- **Question**: Which channels drive users?
- **Goal**: Cost-effective user acquisition

**2. Activation** - Do users have a great first experience?
- **Metrics**: Signups, first actions, "aha moment"
- **Question**: Do users experience value?
- **Goal**: Convert visitors to active users

**3. Retention** - Do users come back?
- **Metrics**: DAU/MAU, churn rate, cohort retention
- **Question**: Is the product sticky?
- **Goal**: Build habit-forming experiences

**4. Referral** - Do users tell others?
- **Metrics**: Viral coefficient, referral rate, NPS
- **Question**: Does product drive word-of-mouth?
- **Goal**: Organic growth through advocacy

**5. Revenue** - How do you monetize?
- **Metrics**: LTV, ARPU, conversion to paid
- **Question**: Does product generate sustainable revenue?
- **Goal**: Profitable growth

### Funnel Analysis

AARRR is a **sequential funnel**:
- Optimize from bottom-up (Retention before Acquisition)
- Fix leaks before adding more water
- **Retention** is foundation (no point acquiring users who churn)
- **Referral** amplifies good retention
- **Revenue** validates product-market fit

### Related Frameworks

- **HEART** (Google): Happiness, Engagement, Adoption, Retention, Task Success
- **AARRR+** (Croll & Yoskovitz): Added Awareness stage
- **North Star Metric**: Single metric capturing core value

## Usage
`/niopd:PO:aarrr-metrics [--product=<product_name>] [--period=<time_period>] [--cohort=<cohort_definition>]`

## Preflight Checklist

1.  **Validate Product Name:**
    -   If the `--product` argument is not provided, prompt the user to specify the product name.
    -   Confirm that the product name is valid and meaningful.

2.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/docs` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in growth metrics and the AARRR Pirate Framework. Your goal is to analyze customer lifecycle metrics to identify growth bottlenecks and optimization opportunities.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you analyze growth metrics using the AARRR framework for the **<product_name>** product."
-   If the `--product` argument wasn't provided, ask the user: "What product would you like to analyze with AARRR metrics?" and wait for their response.
-   If the `--period` argument wasn't provided, ask the user: "What time period should I analyze? (e.g., last month, Q1 2024, last 90 days)" and wait for their response.
-   If the `--cohort` argument wasn't provided, ask the user: "Do you want to analyze a specific user cohort? (e.g., mobile users, premium users, or all users)" and wait for their response.

### Step 2: Product Context Analysis
-   Help the user define the product context:
    -   "What type of product is **<product_name>**? (e.g., SaaS, marketplace, mobile app, e-commerce)"
    -   "What is the primary business model?"
    -   "Who are the target users?"
    -   "What is the core value proposition?"
-   Wait for the user's responses.

### Step 3: Current Metrics Baseline
-   Guide the user through gathering current metrics:
    -   "What data sources do you have available? (e.g., Google Analytics, Mixpanel, internal database)"
    -   "Do you have access to the following metrics for the **<period>** period?"
        -   "Acquisition: Total visitors, new signups, traffic sources?"
        -   "Activation: First actions completed, onboarding completion rate?"
        -   "Retention: DAU/MAU, churn rate, cohort retention data?"
        -   "Referral: Referral rate, viral coefficient, NPS score?"
        -   "Revenue: MRR/ARR, ARPU, conversion rates?"
-   Wait for the user's responses.

### Step 4: Acquisition Analysis
-   Analyze acquisition metrics with the user:
    -   "What are your top acquisition channels and their performance?"
    -   "What is your Cost Per Acquisition (CPA) for each channel?"
    -   "What is the conversion rate from visitor to signup?"
    -   "Are there any seasonal patterns or trends?"
    -   "What is your current acquisition strategy?"
-   Wait for the user's responses.

### Step 5: Activation Analysis
-   Analyze activation metrics with the user:
    -   "How do you define an 'activated' user for **<product_name>**?"
    -   "What is the activation rate (% of signups who become activated)?"
    -   "What is the time to activation (how long until users reach their 'aha moment')?"
    -   "What are the biggest drop-off points in your onboarding funnel?"
    -   "What onboarding features or flows do you currently have?"
-   Wait for the user's responses.

### Step 6: Retention Analysis
-   Analyze retention metrics with the user:
    -   "What are your Day 1, Day 7, Day 30, and Day 90 retention rates?"
    -   "What is your monthly churn rate?"
    -   "What is your DAU/MAU ratio (stickiness metric)?"
    -   "Which features do retained users use most frequently?"
    -   "Have you identified what differentiates retained users from churned users?"
-   Wait for the user's responses.

### Step 7: Referral Analysis
-   Analyze referral metrics with the user:
    -   "What percentage of users refer others?"
    -   "What is your viral coefficient (K factor)?"
    -   "What is your Net Promoter Score (NPS)?"
    -   "Do you have a formal referral program?"
    -   "What referral channels are most effective?"
-   Wait for the user's responses.

### Step 8: Revenue Analysis
-   Analyze revenue metrics with the user:
    -   "What is your current MRR/ARR?"
    -   "What is your conversion rate from free to paid?"
    -   "What is your Average Revenue Per User (ARPU)?"
    -   "What is your Customer Lifetime Value (CLV)?"
    -   "What are your revenue growth trends?"
-   Wait for the user's responses.

### Step 9: Funnel Analysis
-   Guide the user through overall funnel analysis:
    -   "Looking at the complete AARRR funnel, where is the biggest drop-off?"
    -   "Which stage has the most room for improvement?"
    -   "How does your funnel performance compare to industry benchmarks?"
    -   "What is the cumulative conversion rate from visitor to paying customer?"
-   Wait for the user's responses.

### Step 10: Bottleneck Identification
-   Help the user identify growth bottlenecks:
    -   "Based on the data, what are the top 3 bottlenecks limiting growth?"
    -   "For each bottleneck, what is the estimated impact if solved?"
    -   "What is the estimated effort required to address each bottleneck?"
    -   "Are there any quick wins (high impact, low effort)?"
-   Wait for the user's responses.

### Step 11: Benchmarking
-   Guide the user in understanding industry benchmarks:
    -   "Let me share typical AARRR benchmarks for your industry:"
        -   For SaaS: Activation ~25-40%, Retention D30 ~20-40%, Viral K ~0.5-0.7
        -   For Mobile Apps: Activation ~20-30%, Retention D30 ~15-25%, Viral K ~0.3-0.5
        -   For Marketplaces: Activation ~30-50%, Retention D30 ~25-45%, Viral K ~0.6-1.0
    -   "How do your metrics compare to these benchmarks?"
    -   "Which metrics are above/below industry standards?"
-   Wait for the user's responses.

### Step 12: Optimization Recommendations
-   Develop actionable recommendations:
    -   "Based on the analysis, let's prioritize optimization opportunities:"
    -   For each AARRR stage with issues, ask:
        -   "What specific actions could improve this metric?"
        -   "What resources would be needed?"
        -   "What is a realistic improvement target?"
        -   "What is the timeline for implementation?"
-   Wait for the user's responses.

### Step 13: Implementation Roadmap
-   Help the user develop an implementation plan:
    -   "Let's create a phased roadmap:"
        -   "Month 1: Quick wins and critical bottlenecks"
        -   "Month 2-3: Medium priority improvements"
        -   "Month 4-6: Strategic long-term initiatives"
    -   "Who will be responsible for each initiative?"
    -   "How will you measure success?"
-   Wait for the user's responses.

### Step 14: Monitoring Plan
-   Guide the user in establishing ongoing monitoring:
    -   "How frequently should you review AARRR metrics?"
    -   "What alert thresholds should trigger immediate action?"
    -   "What dashboards or tools will you use for monitoring?"
    -   "Who needs to be included in metric reviews?"
-   Wait for the user's responses.

### Step 15: Create AARRR Metrics Analysis Report

Produce a markdown report with the following structure:

---
# AARRR Pirate Metrics Analysis: [Product Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Analysis Period:** [period]  
**Product:** [product_name]  
**Cohort:** [cohort_definition if specified]

---

## Executive Summary
*2-3 paragraph overview of key findings, critical bottlenecks, and top recommendations*

---

## Product Context

### Product Overview
- **Product Type:** [SaaS/Marketplace/Mobile App/E-commerce]
- **Business Model:** [Subscription/Freemium/Transaction/Advertising]
- **Target Users:** [User segments]
- **Core Value Proposition:** [Value delivered]

### Analysis Scope
- **Time Period:** [Analysis period]
- **Cohort Definition:** [If applicable]
- **Data Sources:** [Analytics platforms used]
- **Report Generated:** [Current date]

---

## 1. Acquisition Metrics Analysis

### Traffic Sources Performance
| Source | Visitors | % of Total | Conversion Rate | Cost per Acquisition | ROI |
|--------|----------|------------|-----------------|---------------------|-----|
| [Channel 1] | [Number] | [%] | [%] | [$Amount] | [Ratio] |
| [Channel 2] | [Number] | [%] | [%] | [$Amount] | [Ratio] |
| [Channel 3] | [Number] | [%] | [%] | [$Amount] | [Ratio] |
| **Total** | [Total] | 100% | [Avg %] | [Avg $] | [Avg Ratio] |

### Key Acquisition Metrics
- **Total Visitors:** [Number]
- **New Signups:** [Number]
- **Overall Conversion Rate:** [%]
- **Average CPA:** [$Amount]
- **Traffic Growth Rate:** [% MoM/YoY]

### Acquisition Insights
**Top Performing Channels:**  
[Analysis of best channels with rationale]

**Underperforming Channels:**  
[Analysis of weak channels with root causes]

**Seasonal Patterns:**  
[Identified trends and patterns]

**Opportunities:**  
[Untapped or underutilized acquisition channels]

---

## 2. Activation Metrics Analysis

### Activation Definition
**Activated User Criteria:**  
[Specific actions/events that define activation]

### Activation Funnel
| Funnel Step | Users | Drop-off | Conversion Rate |
|-------------|-------|----------|----------------|
| Signup Completed | [Number] | - | 100% |
| Email Verified | [Number] | [Number] | [%] |
| Profile Completed | [Number] | [Number] | [%] |
| First Key Action | [Number] | [Number] | [%] |
| **Activated Users** | [Number] | - | [%] |

### Key Activation Metrics
- **Activation Rate:** [% of signups]
- **Time to Activation:** [Average time]
- **Onboarding Completion:** [%]
- **Day 1 Activation:** [%]
- **Day 7 Activation:** [%]

### Activation Insights
**Activation Barriers:**  
[Key obstacles preventing activation]

**"Aha Moment" Analysis:**  
[When and how users realize value]

**Onboarding Effectiveness:**  
[Strengths and weaknesses of current onboarding]

**Optimization Opportunities:**  
[Specific improvements to increase activation]

---

## 3. Retention Metrics Analysis

### Retention Curves
| Period | Retention Rate | Active Users | Churn Rate |
|--------|----------------|--------------|------------|
| Day 1 | [%] | [Number] | [%] |
| Day 7 | [%] | [Number] | [%] |
| Day 30 | [%] | [Number] | [%] |
| Day 90 | [%] | [Number] | [%] |
| Day 180 | [%] | [Number] | [%] |

### Engagement Metrics
- **Daily Active Users (DAU):** [Number]
- **Monthly Active Users (MAU):** [Number]
- **DAU/MAU Ratio:** [% - stickiness]
- **Session Frequency:** [Sessions/user/week]
- **Session Duration:** [Average minutes]
- **Monthly Churn Rate:** [%]

### Cohort Retention Analysis
[Cohort retention table or analysis if applicable]

### Retention Insights
**Churn Patterns:**  
[When and why users typically leave]

**Retention Drivers:**  
[Features/behaviors that predict retention]

**Power User Characteristics:**  
[Traits of highly engaged users]

**Retention Gaps:**  
[Opportunities to reduce churn]

---

## 4. Referral Metrics Analysis

### Viral Metrics
- **Referral Rate:** [% of users who refer]
- **Average Referrals per User:** [Number]
- **Referred User Conversion Rate:** [%]
- **Viral Coefficient (K):** [Value]
- **Viral Cycle Time:** [Days/hours]

### Word of Mouth Metrics
- **Net Promoter Score (NPS):** [Score]
- **Customer Satisfaction (CSAT):** [%]
- **Social Mentions:** [Volume]
- **Referral Program Participation:** [%]

### Referral Channel Performance
| Channel | Referrals | Conversion | Quality Score |
|---------|-----------|------------|---------------|
| [Channel 1] | [Number] | [%] | [Score] |
| [Channel 2] | [Number] | [%] | [Score] |
| [Channel 3] | [Number] | [%] | [Score] |

### Referral Insights
**Most Effective Channels:**  
[Best performing referral methods]

**Advocate Profile:**  
[Characteristics of users who refer]

**Referral Barriers:**  
[Obstacles preventing more referrals]

**Viral Growth Potential:**  
[Assessment of viral growth opportunity]

---

## 5. Revenue Metrics Analysis

### Revenue Funnel
| Stage | Users | Conversion | Revenue |
|-------|-------|------------|----------|
| Active Users | [Number] | - | - |
| Trial Users | [Number] | [%] | - |
| Paying Customers | [Number] | [%] | [$Amount] |
| Upgraded Users | [Number] | [%] | [$Amount] |

### Key Revenue Metrics
- **Monthly Recurring Revenue (MRR):** [$Amount]
- **Annual Recurring Revenue (ARR):** [$Amount]
- **Free to Paid Conversion:** [%]
- **Average Revenue Per User (ARPU):** [$Amount]
- **Customer Lifetime Value (CLV):** [$Amount]
- **Revenue Churn Rate:** [%]
- **Revenue Growth Rate:** [% MoM]

### Monetization Analysis
**Pricing Tier Adoption:**  
[Distribution across pricing plans]

**Upgrade Patterns:**  
[When/why users upgrade]

**Revenue Expansion:**  
[Upsell/cross-sell performance]

**Monetization Efficiency:**  
[CLV:CAC ratio and payback period]

---

## AARRR Funnel Overview

### Complete Funnel Analysis
| Stage | Key Metric | Current | Industry Benchmark | Gap |
|-------|------------|---------|-------------------|-----|
| **Acquisition** | Signup Rate | [%] | [%] | [+/- %] |
| **Activation** | Activation Rate | [%] | [%] | [+/- %] |
| **Retention** | Day 30 Retention | [%] | [%] | [+/- %] |
| **Referral** | Viral Coefficient | [K] | [K] | [+/- K] |
| **Revenue** | Free to Paid | [%] | [%] | [+/- %] |

### Cumulative Conversion Rate
**Visitor → Paying Customer:** [Overall % conversion]

### Biggest Leaks in the Funnel
1. **[Stage Name]:** [% drop-off] - [Root cause]
2. **[Stage Name]:** [% drop-off] - [Root cause]
3. **[Stage Name]:** [% drop-off] - [Root cause]

---

## Growth Bottleneck Analysis

### Critical Bottlenecks

#### Bottleneck #1: [Name]
- **Stage Affected:** [AARRR stage]
- **Current Performance:** [Metric value]
- **Impact:** [Business impact description]
- **Root Cause:** [Analysis of why this is happening]
- **Estimated Improvement Potential:** [Quantified opportunity]

#### Bottleneck #2: [Name]
- **Stage Affected:** [AARRR stage]
- **Current Performance:** [Metric value]
- **Impact:** [Business impact description]
- **Root Cause:** [Analysis of why this is happening]
- **Estimated Improvement Potential:** [Quantified opportunity]

#### Bottleneck #3: [Name]
- **Stage Affected:** [AARRR stage]
- **Current Performance:** [Metric value]
- **Impact:** [Business impact description]
- **Root Cause:** [Analysis of why this is happening]
- **Estimated Improvement Potential:** [Quantified opportunity]

### Priority Matrix
| Issue | Impact (1-5) | Effort (1-5) | Score | Priority |
|-------|--------------|--------------|-------|----------|
| [Issue 1] | [N] | [N] | [Impact/Effort] | High/Medium/Low |
| [Issue 2] | [N] | [N] | [Impact/Effort] | High/Medium/Low |
| [Issue 3] | [N] | [N] | [Impact/Effort] | High/Medium/Low |

---

## Actionable Recommendations

### High Priority Actions (Month 1)

#### Recommendation #1: [Title]
- **Description:** [What to do]
- **Expected Impact:** [Quantified improvement]
- **Resources Required:** [Team, budget, tools]
- **Timeline:** [Implementation timeframe]
- **Success Metrics:** [How to measure success]

#### Recommendation #2: [Title]
- **Description:** [What to do]
- **Expected Impact:** [Quantified improvement]
- **Resources Required:** [Team, budget, tools]
- **Timeline:** [Implementation timeframe]
- **Success Metrics:** [How to measure success]

### Medium Priority Actions (Month 2-3)

#### Recommendation #3: [Title]
- **Description:** [What to do]
- **Expected Impact:** [Quantified improvement]
- **Resources Required:** [Team, budget, tools]
- **Timeline:** [Implementation timeframe]
- **Success Metrics:** [How to measure success]

### Long-term Strategic Initiatives (Month 4-6)

#### Initiative #1: [Title]
- **Description:** [What to do]
- **Strategic Rationale:** [Why this matters]
- **Investment Required:** [Resources needed]
- **Timeline:** [Implementation timeframe]
- **Success Metrics:** [How to measure success]

---

## Implementation Roadmap

### Month 1: Critical Bottlenecks
- **Week 1:** [Specific actions]
- **Week 2:** [Specific actions]
- **Week 3:** [Specific actions]
- **Week 4:** [Specific actions]
- **Success Criteria:** [Month 1 goals]

### Month 2-3: Medium Priority Improvements
- **Month 2 Focus:** [Key initiatives]
- **Month 3 Focus:** [Key initiatives]
- **Success Criteria:** [Q1 goals]

### Month 4-6: Strategic Long-term Moves
- **Q2 Focus:** [Strategic initiatives]
- **Success Criteria:** [6-month goals]

---

## Monitoring & Review Plan

### Metrics Dashboard
**Primary KPIs to Track:**
- Acquisition: [Key metrics]
- Activation: [Key metrics]
- Retention: [Key metrics]
- Referral: [Key metrics]
- Revenue: [Key metrics]

### Review Cadence
- **Weekly:** [Quick metrics review]
- **Monthly:** [Comprehensive AARRR analysis]
- **Quarterly:** [Strategic deep dive]

### Alert Thresholds
| Metric | Warning Threshold | Critical Threshold | Action Required |
|--------|------------------|-------------------|------------------|
| [Metric 1] | [Value] | [Value] | [Action] |
| [Metric 2] | [Value] | [Value] | [Action] |
| [Metric 3] | [Value] | [Value] | [Action] |

### Stakeholder Reporting
- **Audience:** [Who needs updates]
- **Format:** [Dashboard/Report/Presentation]
- **Frequency:** [How often]

---

## Appendix

### Data Sources
[List of analytics platforms and data sources used]

### Methodology Notes
[Any important methodological considerations]

### Industry Benchmarks References
[Sources for benchmark data]

---

*Report generated by NioPD AARRR Metrics Analysis*

---

### Step 16: Save the Report
- Generate a filename for the AARRR metrics report following the NioPD naming convention: `[YYYYMMDD]-[product_slug]-aarrr-metrics-v[version].md`.
- Save the AARRR metrics report to: `niopd-workspace/docs/[filename]`

### Step 17: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the AARRR Pirate Metrics analysis for **<product_name>**."
- Provide the path to the file: "You can view the detailed AARRR analysis report at: `niopd-workspace/docs/[YYYYMMDD]-[product_slug]-aarrr-metrics-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PO:north-star` to identify your North Star metric based on this analysis, or `/niopd:PM:kpis` to track key performance indicators over time."

## Error Handling
- **Missing Product Name:** If no product name is specified, explain that a product name is required and ask for one.
- **Insufficient Data:** If the user doesn't have access to key metrics, explain what data is needed and offer to proceed with partial analysis.
- **Unclear Definitions:** If activation or other definitions are unclear, help the user define them based on best practices for their product type.
- **File Save Errors:** If there are issues saving the report, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial analysis can still provide value.

