---
argument-hint: [--product=<product_name>] [--features=<feature_list>] [--survey=<survey_data>]
description: Analyzes customer satisfaction using the Kano model to classify product features into five categories.
---

# Command: /niopd:UR:kano

This command analyzes customer satisfaction using the Kano model to classify product features into five categories: Must-be, One-dimensional, Attractive, Indifferent, and Reverse.

## Theoretical Foundation

### Origin and Development
The Kano Model was developed by **Professor Noriaki Kano** at Tokyo University of Science in the 1980s. It provides a framework for understanding the relationship between product features and customer satisfaction.

### Core Principle
Not all features contribute to customer satisfaction equally. The Kano Model recognizes that the **relationship between feature presence and satisfaction is non-linear**: some features cause dissatisfaction when absent but don't increase satisfaction when present (must-haves), while others delight when present but don't cause dissatisfaction when absent (delighters).

### The Five Kano Categories

1. **Must-be Quality (Basic Needs)**:
   - **Absence**: Strong dissatisfaction
   - **Presence**: Neutral (expected)
   - **Example**: Security, reliability, core functionality
   - **Action**: Must implement, but don't over-invest

2. **One-dimensional Quality (Performance Needs)**:
   - **Linear relationship**: More = more satisfied
   - **Example**: Speed, capacity, efficiency
   - **Action**: Invest proportionally to competitive position

3. **Attractive Quality (Excitement Needs)**:
   - **Absence**: Neutral (not expected)
   - **Presence**: High satisfaction (delighters)
   - **Example**: Innovative features, unexpected benefits
   - **Action**: Source of differentiation

4. **Indifferent Quality**:
   - **Presence or absence**: No impact on satisfaction
   - **Action**: Deprioritize or remove

5. **Reverse Quality**:
   - **Presence**: Causes dissatisfaction
   - **Example**: Unwanted complexity
   - **Action**: Eliminate

### Kano Questionnaire
For each feature, ask two questions:
1. **Functional**: "How do you feel if this feature IS present?"
2. **Dysfunctional**: "How do you feel if this feature is NOT present?"

Responses: I like it | I expect it | I'm neutral | I can tolerate it | I dislike it

### Feature Evolution
Features evolve over time:
- **Attractive** → **One-dimensional** → **Must-be** (due to competition and expectations)
- Example: GPS in cars: Delighter (1990s) → Expected (today)

### When to Use
- Feature prioritization and roadmap planning
- Understanding customer expectations
- Identifying differentiation opportunities
- Avoiding over-investment in commoditized features
- New product planning

### Related Methodologies
- **RICE Scoring**: Complementary prioritization framework
- **MoSCoW Method**: Must-have, Should-have, Could-have, Won't-have
- **Value vs. Effort Matrix**: Combining Kano with implementation cost

## Usage
`/niopd:UR:kano [--product=<product_name>] [--features=<feature_list>] [--survey=<survey_data>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Inputs:**
    -   Check if `--product` argument is provided to specify the product.
    -   If `--product` is not provided, ask the user to specify which product they're analyzing.
    -   Check if `--features` argument is provided for the feature list.
    -   Check if `--survey` argument is provided for survey data.

## Instructions

You are Nio, an AI Product Assistant. Your task is to help users analyze customer satisfaction using the Kano model to classify product features.

### Core Principle
Always ensure that your analysis is grounded in the Kano Model core principle: not all features contribute to customer satisfaction equally. The relationship between feature presence and satisfaction is non-linear - some features cause dissatisfaction when absent but don't increase satisfaction when present (must-haves), while others delight when present but don't cause dissatisfaction when absent (delighters).

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you analyze customer satisfaction using the Kano model to classify product features."
-   If the `--product` argument wasn't provided, ask the user: "Which product would you like to analyze?" and wait for their response.
-   If the `--features` argument wasn't provided, ask the user: "What features are you considering for this product?" and wait for their response.
-   If the `--survey` argument wasn't provided, ask the user: "Do you have survey data available? If so, please provide it." and wait for their response.
-   If configuration file exists and contains product, features, or survey data settings, use those values as defaults
-   If language setting in configuration is Chinese, respond in Chinese; otherwise, respond in English

### Step 2: Explain Kano Model Framework
-   Briefly explain the Kano model categories:
    -   Must-be Quality - Basic expectations that cause dissatisfaction when absent
    -   One-dimensional Quality - Features with linear relationship to satisfaction
    -   Attractive Quality - Delighters that cause satisfaction when present
    -   Indifferent Quality - Features that don't affect satisfaction
    -   Reverse Quality - Features that cause dissatisfaction when present
-   Ask the user: "Do you understand these categories, or would you like me to elaborate?" and wait for their response.

### Step 3: Design Kano Survey
-   Guide the user through survey design:
    -   "For each feature, we need to ask two questions:"
    -   "1. How would you feel if this feature WERE present?"
    -   "2. How would you feel if this feature WERE NOT present?"
    -   "The response options are: I like it, I expect it, I don't care, I can tolerate it, I dislike it"
-   Wait for the user's confirmation.

### Step 4: Collect Feature Classifications
-   For each feature, guide the user through classification:
    -   "What was the functional response for [feature]?"
    -   "What was the dysfunctional response for [feature]?"
    -   "Based on the Kano matrix, what category does this feature belong to?"
-   Wait for the user's responses for each feature.

### Step 5: Calculate Better-Worse Coefficients
-   Help the user calculate coefficients:
    -   "Better Coefficient (B) = (L + E) / Total Responses"
    -   "Worse Coefficient (W) = (D + T) / Total Responses"
    -   "Satisfaction Coefficient (S) = B - W"
    -   "Importance Coefficient (I) = B + W"
-   Ask the user to provide the response data for calculation.

### Step 6: Prioritize Features
-   Guide the user to prioritize features based on categories:
    -   "Which features are Must-be (high priority)?"
    -   "Which features are One-dimensional (medium priority)?"
    -   "Which features are Attractive (differentiation opportunities)?"
-   Wait for the user's responses.

### Step 7: Create Implementation Roadmap
-   Help the user create a roadmap:
    -   "Which Must-be features should be implemented first?"
    -   "What's the timeline for One-dimensional features?"
    -   "When should Attractive features be introduced?"
-   Wait for the user's responses.

### Step 8: Create Comprehensive Kano Model Analysis Document

Generate a detailed Kano analysis report with the following comprehensive structure:

---
# Kano Model Analysis: [Product Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Product:** [product_name]  
**Survey Period:** [Start date] - [End date]  
**Survey Respondents:** [Number of participants]  
**Response Rate:** [Percentage]

---

## Executive Summary

**Total Features Analyzed:** [Number]

**Category Distribution:**
- Must-be Quality: [Number of features] ([Percentage]%)
- One-dimensional Quality: [Number] ([Percentage]%)
- Attractive Quality: [Number] ([Percentage]%)
- Indifferent Quality: [Number] ([Percentage]%)
- Reverse Quality: [Number] ([Percentage]%)

**Key Findings:**
1. [Most important finding - e.g., "3 critical must-be features are missing"]
2. [Differentiation opportunity - e.g., "5 attractive features identified for competitive advantage"]
3. [Efficiency finding - e.g., "7 indifferent features consuming development resources"]

**Strategic Recommendations:**
- **Immediate action:** [Must-be features to implement]
- **Differentiation focus:** [Attractive features for competitive edge]
- **Resource optimization:** [Indifferent/Reverse features to deprioritize]

---

## Kano Model Overview

### Understanding the Categories

**Must-be Quality (Basic Needs):**
> Features customers expect as baseline. Absence causes dissatisfaction, but presence doesn't increase satisfaction.

**One-dimensional Quality (Performance Needs):**
> Features with linear relationship - more is better. Directly correlate with satisfaction.

**Attractive Quality (Excitement Needs):**
> Unexpected delighters. Presence creates high satisfaction, absence doesn't cause dissatisfaction.

**Indifferent Quality:**
> Features that don't affect satisfaction either way. Candidates for deprioritization.

**Reverse Quality:**
> Features that actually reduce satisfaction when present. Should be eliminated.

---

## Survey Methodology

### Survey Design

**Functional Question:**  
*"How would you feel if [feature] WERE present?"*

**Dysfunctional Question:**  
*"How would you feel if [feature] WERE NOT present?"*

**Response Options:**
1. I like it
2. I expect it
3. I'm neutral
4. I can tolerate it
5. I dislike it

### Kano Evaluation Table

| Customer Requirements | Dysfunctional → | Like | Must-be | Neutral | Live with | Dislike |
|----------------------|-----------------|------|---------|---------|-----------|----------|
| **Functional ↓** | | | | | | |
| **Like** | | Q | A | A | A | O |
| **Must-be** | | R | I | I | I | M |
| **Neutral** | | R | I | I | I | M |
| **Live with** | | R | I | I | I | M |
| **Dislike** | | R | R | R | R | Q |

A = Attractive | M = Must-be | O = One-dimensional | I = Indifferent | R = Reverse | Q = Questionable

### Survey Demographics

**Respondent Breakdown:**
| Segment | Count | Percentage |
|---------|-------|------------|
| [Segment 1: e.g., "Enterprise users"] | [Count] | [%] |
| [Segment 2: e.g., "SMB users"] | [Count] | [%] |
| [Segment 3: e.g., "Individual users"] | [Count] | [%] |

**Response Quality:**
- Valid responses: [Number] ([Percentage]%)
- Questionable responses: [Number] ([Percentage]%)
- Excluded responses: [Number] ([Percentage]%)

---

## Feature Analysis Results

### Must-be Quality Features

**Feature 1: [Feature Name]**
- **Category:** Must-be
- **Functional Response:** [Distribution: Like X%, Expect Y%, etc.]
- **Dysfunctional Response:** [Distribution]
- **Better Coefficient (B):** [0.00 - 1.00]
- **Worse Coefficient (W):** [-1.00 - 0.00]
- **Satisfaction Coefficient (S = B + |W|):** [Score]
- **Impact:** High dissatisfaction if absent, neutral if present
- **Action Required:** ✅ **MUST IMPLEMENT** - Critical baseline requirement
- **Estimated Effort:** [High/Medium/Low]
- **Priority:** [P0 - Highest]

**Feature 2: [Feature Name]**
- [Same structure]

**Feature 3: [Feature Name]**
- [Same structure]

**Must-be Summary:**
- Total must-be features: [Number]
- Implemented: [Number]
- Missing (urgent): [Number]
- Investment required: [Estimated effort]

---

### One-dimensional Quality Features

**Feature 1: [Feature Name]**
- **Category:** One-dimensional (Performance)
- **Functional Response:** [Distribution]
- **Dysfunctional Response:** [Distribution]
- **Better Coefficient (B):** [0.00 - 1.00] (Higher = more satisfaction when present)
- **Worse Coefficient (W):** [-1.00 - 0.00] (Lower = more dissatisfaction when absent)
- **Satisfaction Coefficient (S):** [High value indicates strong linear relationship]
- **Impact:** Linear relationship - more performance = more satisfaction
- **Competitive Benchmark:** [How you compare to competitors]
- **Action Required:** ⚠️ **INVEST PROPORTIONALLY** - Match or exceed competition
- **Estimated Effort:** [High/Medium/Low]
- **Priority:** [P1-P2]

**Feature 2: [Feature Name]**
- [Same structure]

**One-dimensional Summary:**
- Total performance features: [Number]
- Competitive advantage: [Number where you lead]
- Competitive parity: [Number where you match]
- Competitive gap: [Number where you lag]
- Investment priority: [Which to focus on]

---

### Attractive Quality Features (Delighters)

**Feature 1: [Feature Name]**
- **Category:** Attractive (Delighter)
- **Functional Response:** [Distribution: High "Like it" percentage]
- **Dysfunctional Response:** [Distribution: High "Neutral" percentage]
- **Better Coefficient (B):** [High value: 0.5-1.0]
- **Worse Coefficient (W):** [Close to 0]
- **Satisfaction Coefficient (S):** [Very positive]
- **Impact:** Creates delight when present, no dissatisfaction when absent
- **Differentiation Potential:** ⭐ **HIGH** - Competitive advantage opportunity
- **Competitive Status:** [No competitor offers this / Few offer / Common]
- **Innovation Value:** [How innovative/unique]
- **Action Required:** 🚀 **DIFFERENTIATE** - Source of competitive advantage
- **Estimated Effort:** [High/Medium/Low]
- **Priority:** [P1-P2 for differentiation]

**Feature 2: [Feature Name]**
- [Same structure]

**Attractive Summary:**
- Total delighter features identified: [Number]
- High-impact delighters: [Number with B > 0.7]
- Feasible to implement: [Number with reasonable effort]
- Recommended for roadmap: [Number to prioritize]
- Expected competitive impact: [Assessment]

---

### Indifferent Quality Features

**Feature 1: [Feature Name]**
- **Category:** Indifferent
- **Functional Response:** [High "Neutral" and "Can tolerate" percentages]
- **Dysfunctional Response:** [High "Neutral" percentage]
- **Better Coefficient (B):** [Close to 0]
- **Worse Coefficient (W):** [Close to 0]
- **Satisfaction Coefficient (S):** [Near 0 - no impact]
- **Impact:** No effect on satisfaction either way
- **Current Investment:** [Effort being spent]
- **Action Required:** ⛔ **DEPRIORITIZE** - Redirect resources to higher-value features
- **Estimated Savings:** [Resources freed up]
- **Recommendation:** [Remove / Minimize / Maintain if no cost]

**Feature 2: [Feature Name]**
- [Same structure]

**Indifferent Summary:**
- Total indifferent features: [Number]
- Currently implemented: [Number wasting resources]
- Potential resource savings: [Estimated % of capacity]
- Recommended action: [Deprecation plan]

---

### Reverse Quality Features

**Feature 1: [Feature Name]**
- **Category:** Reverse
- **Functional Response:** [High "Dislike it" or "Can tolerate" percentages]
- **Dysfunctional Response:** [Preference for absence]
- **Better Coefficient (B):** [Negative or very low]
- **Worse Coefficient (W):** [Positive - opposite of normal]
- **Impact:** Presence causes dissatisfaction
- **Why Reverse:** [Reason: Too complex / Unwanted / Inappropriate for segment]
- **Action Required:** ❌ **REMOVE** - Actively reduces satisfaction
- **Priority:** [P0 - Immediate removal]
- **Deprecation Plan:** [How to phase out]

**Feature 2: [Feature Name]**
- [Same structure]

**Reverse Summary:**
- Total reverse features: [Number]
- Currently in product: [Number to remove]
- User segment affected: [Who dislikes it]
- Removal timeline: [Deprecation schedule]

---

## Coefficients & Prioritization

### Better-Worse Analysis

**Calculation Formulas:**
- **Better Coefficient (B)** = (Like + Expect) / Total Responses
  - Range: 0 to 1 (higher = more satisfaction when present)
- **Worse Coefficient (W)** = -1 × (Dislike + Expect) / Total Responses  
  - Range: -1 to 0 (lower = more dissatisfaction when absent)
- **Satisfaction Index (SI)** = B + |W|
  - Range: 0 to 2 (higher = stronger impact on satisfaction)

### Feature Prioritization Matrix

| Feature | Category | Better (B) | Worse (W) | SI | Implementation Effort | Priority Score | Rank |
|---------|----------|------------|-----------|-----|----------------------|----------------|------|
| [Feature 1] | [M/O/A/I/R] | [0.XX] | [-0.XX] | [X.XX] | [H/M/L] | [Calculated] | 1 |
| [Feature 2] | [M/O/A/I/R] | [0.XX] | [-0.XX] | [X.XX] | [H/M/L] | [Calculated] | 2 |
| [Feature 3] | [M/O/A/I/R] | [0.XX] | [-0.XX] | [X.XX] | [H/M/L] | [Calculated] | 3 |
| ... | | | | | | | |

**Priority Score Formula:**  
`Priority = (SI × Importance Weight) / (Effort × Effort Weight)`

Where:
- Must-be: Importance Weight = 3.0
- One-dimensional: Importance Weight = 2.0  
- Attractive: Importance Weight = 1.5
- Indifferent: Importance Weight = 0.2
- Reverse: Importance Weight = -1.0 (negative priority)

---

## Segment Analysis

### Category Distribution by Segment

| Feature | Overall | Segment 1 | Segment 2 | Segment 3 |
|---------|---------|-----------|-----------|------------|
| [Feature 1] | [Category] | [Category if different] | [Category if different] | [Category if different] |
| [Feature 2] | [Category] | [Category] | [Category] | [Category] |

**Segment-Specific Insights:**

**[Segment 1 Name]:**
- **Unique Must-be Features:** [Features this segment requires]
- **Unique Delighters:** [Features that excite this segment]
- **Strategy:** [How to serve this segment]

**[Segment 2 Name]:**
- [Same structure]

**[Segment 3 Name]:**
- [Same structure]

---

## Kano Model Evolution Over Time

### Feature Lifecycle

**Current State Analysis:**

| Feature | Current Category | Category 2 Years Ago | Predicted in 2 Years | Evolution Pattern |
|---------|-----------------|---------------------|---------------------|-------------------|
| [Feature 1] | Must-be | Attractive | Must-be | A → O → M (Typical) |
| [Feature 2] | One-dimensional | Attractive | Must-be | Moving toward commodity |
| [Feature 3] | Attractive | Not available | One-dimensional | Competitive response expected |

**Evolution Insights:**
- [Feature] is evolving from delighter to must-be - implement before it becomes expected
- [Feature] is becoming commoditized - don't over-invest
- [Feature] remains a delighter - opportunity to maintain differentiation

---

## Implementation Roadmap

### Phase 1: Foundation (Q1-Q2) - Must-be Features

**Critical Must-be Features:**
1. **[Feature]** - [Description]
   - Impact: Eliminates dissatisfaction
   - Effort: [Estimate]
   - Timeline: [Date]

2. **[Feature]** - [Description]
   - Impact: Table stakes for market
   - Effort: [Estimate]
   - Timeline: [Date]

**Success Criteria:**
- [ ] All critical must-be features implemented
- [ ] Customer complaints about missing basics reduced by [X]%
- [ ] Feature parity with competition achieved

---

### Phase 2: Competitive Positioning (Q3-Q4) - One-dimensional Features

**Performance Features:**
1. **[Feature]** - [Description]
   - Impact: Competitive advantage in [dimension]
   - Competitive gap: [Current vs. target]
   - Effort: [Estimate]
   - Timeline: [Date]

2. **[Feature]** - [Description]
   - [Same structure]

**Success Criteria:**
- [ ] Match or exceed competitor performance on key dimensions
- [ ] NPS improvement of [X] points
- [ ] Win rate improvement in competitive deals

---

### Phase 3: Differentiation (Next Year) - Attractive Features

**Delighter Features:**
1. **[Feature]** - [Description]
   - Impact: Market differentiation
   - Uniqueness: [No competitor / First to market]
   - Effort: [Estimate]
   - Timeline: [Date]

2. **[Feature]** - [Description]
   - [Same structure]

**Success Criteria:**
- [ ] Launch unique features competitors lack
- [ ] Generate buzz and word-of-mouth
- [ ] Premium pricing power established
- [ ] Win rate in feature-driven deals increased by [X]%

---

### Continuous: Resource Optimization

**Features to Deprecate/Deprioritize:**

| Feature | Category | Action | Timeline | Resources Freed |
|---------|----------|--------|----------|------------------|
| [Feature] | Indifferent | Deprecate | [Q] | [% capacity] |
| [Feature] | Reverse | Remove | [Q] | [% capacity] |
| [Feature] | Indifferent | Minimize maintenance | [Q] | [% capacity] |

**Resource Reallocation:**
- Resources freed: [Total %]
- Redirected to: [Must-be: X%, One-dimensional: Y%, Attractive: Z%]

---

## Strategic Recommendations

### For Product Strategy

**Short-term (0-6 months):**
1. **Complete Must-be Foundation:** [Specific features]
2. **Quick Win Delighters:** [Low-effort attractive features]
3. **Remove Reverse Features:** [Features causing dissatisfaction]

**Medium-term (6-12 months):**
1. **Performance Gap Closure:** [One-dimensional features lagging competition]
2. **Differentiation Bets:** [High-impact attractive features]
3. **Segment-Specific Features:** [Targeted must-haves for key segments]

**Long-term (12-24 months):**
1. **Platform Delighters:** [Attractive features requiring foundation]
2. **Future Must-haves:** [Features evolving from attractive to must-be]
3. **Innovation Pipeline:** [Next generation attractive features]

### For Marketing & Positioning

**Don't Market Must-be Features:**
- Customers expect these - marketing them signals you're behind
- Focus messaging on where you exceed expectations

**Highlight One-dimensional Advantages:**
- "50% faster", "2x more capacity" - quantify performance leads
- Competitive comparison charts

**Lead with Attractive Features:**
- These create buzz and word-of-mouth
- "Only product that...", "First to..."
- Case studies showing unexpected value

### For Sales Enablement

**Qualification:**
- Must-be: "Do you need [baseline capability]?" (Threshold question)
- One-dimensional: "How important is [performance] to you?" (Competitive win)
- Attractive: "Would [delighter] be valuable?" (Differentiation)

**Demo Strategy:**
- Assume must-be features (don't waste time)
- Demonstrate one-dimensional superiority (with metrics)
- Wow with attractive features (memorable moments)

### For Pricing Strategy

**Must-be Features:**
- Include in base pricing - can't charge premium for expected features

**One-dimensional Features:**
- Tier pricing based on performance levels
- "Basic", "Professional", "Enterprise" tiers

**Attractive Features:**
- Justify premium pricing
- Early access pricing
- Add-on packages

---

## Validation & Continuous Improvement

### Kano Survey Schedule

**Frequency:** [Quarterly / Bi-annually / Annually]

**Next Survey Date:** [Date]

**Survey Updates:**
- [ ] Add new features being considered
- [ ] Remove deprecated features
- [ ] Track category evolution of existing features
- [ ] Segment analysis for new customer types

### Monitoring Plan

**Leading Indicators:**
- Feature usage analytics
- Support ticket trends
- NPS by feature
- Churn analysis by feature absence

**Validation Methods:**
- User interviews to deep-dive on surprising results
- A/B testing to confirm category classifications
- Competitive win/loss analysis
- Customer advisory board feedback

---

## Appendix

### A. Raw Survey Data Summary

[Include summary statistics, response distributions, data quality notes]

### B. Statistical Significance

**Sample Size Calculation:**
- Population: [Total customer base]
- Sample: [Survey respondents]
- Confidence Level: [95%]
- Margin of Error: [±X%]

**Segment Sample Sizes:**
- [Segment 1]: [n=X, MoE=±Y%]
- [Segment 2]: [n=X, MoE=±Y%]

### C. Kano Questionnaire Used

[Include actual questions sent to customers]

---

**Prepared By:** [Name/Team]  
**Reviewed By:** [Stakeholders]  
**Last Updated:** [YYYYMMDD]  
**Next Review:** [Date]

---

**Filename:** `[YYYYMMDD]-[product_slug]-kano-analysis-v[version].md`  
**Save to:** `niopd-workspace/reports/[filename]`

### Step 9: Confirm and Conclude
-   Confirm the completion: "✅ I've created a comprehensive Kano Model analysis for **[product]**."
-   Show file path: `niopd-workspace/reports/[filename]`
-   Suggest next steps:
    -   "Prioritize features with RICE scoring: `/niopd:ST:rice`"
    -   "Create user stories for prioritized features: `/niopd:PD:stories`"
    -   "Build features into PRD: `/niopd:PD:draft-prd`"
    -   "Plan feature rollout: `/niopd:PM:release`"

## Error Handling
- **Missing Information:** If key information is missing, explain what's needed and offer to proceed with placeholders.
- **Unclear Requirements:** If requirements are ambiguous, ask for clarification using specific questions.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial analysis can still provide value.