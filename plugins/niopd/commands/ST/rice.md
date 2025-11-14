---
argument-hint: [--initiatives=<file_path>] [--timeframe=<time_period>]
description: Prioritizes initiatives using the RICE scoring framework (Reach, Impact, Confidence, Effort).
---

# Command: /niopd:ST:rice

This command prioritizes initiatives using the RICE scoring framework to help product teams make data-driven decisions.

## Theoretical Foundation

### Origin and Development
The RICE scoring model was developed by **Sean McBride** and the product team at **Intercom** in 2016 to solve the challenge of prioritizing hundreds of competing product ideas. It was shared publicly to help other product teams make more objective prioritization decisions.

### Core Principle
RICE provides a **quantitative scoring framework** that combines four factors into a single priority score, enabling objective comparison of initiatives. It forces teams to make explicit their assumptions about reach, impact, confidence, and effort.

### The RICE Formula

**RICE Score = (Reach × Impact × Confidence) / Effort**

Higher scores indicate higher priority initiatives.

### The Four Factors

**R - Reach** (Number of people/events per time period)
- **Question**: How many people will this impact within a time period?
- **Measurement**: Absolute number (e.g., "500 customers per quarter")
- **Time Period**: Usually per quarter or per month
- **Example**: "2,000 users per month will see this feature"

**I - Impact** (Multiplier per person)
- **Question**: How much will this impact each person?
- **Scale**: 
  - **3** = Massive impact
  - **2** = High impact
  - **1** = Medium impact
  - **0.5** = Low impact
  - **0.25** = Minimal impact
- **Focus**: Impact on the goal you're trying to achieve
- **Example**: "High impact (2) on conversion rate"

**C - Confidence** (Percentage)
- **Question**: How confident are we in our estimates?
- **Scale**: Percentage (0-100%)
  - **100%** = High confidence (strong data)
  - **80%** = Medium confidence (some data)
  - **50%** = Low confidence (little data)
- **Purpose**: Discount uncertain initiatives
- **Example**: "80% confident based on similar past features"

**E - Effort** (Person-months)
- **Question**: How much total team time is required?
- **Measurement**: Person-months (product, design, engineering)
- **Includes**: All disciplines across entire team
- **Minimum**: 0.5 person-months (anything less rounds to 0.5)
- **Example**: "3 person-months" (1 designer + 2 engineers for 1 month)

### Scoring Example

**Initiative**: Add social login feature
- **Reach**: 1,000 new users per quarter
- **Impact**: 2 (High - improves signup conversion)
- **Confidence**: 80% (0.8)
- **Effort**: 2 person-months

**RICE Score** = (1,000 × 2 × 0.8) / 2 = **800**

### When to Use
- Product backlog prioritization
- Roadmap planning
- Feature prioritization
- Resource allocation
- Quarterly planning
- Initiative comparison

### Strengths
- Objective and data-driven
- Forces explicit estimation
- Easy to understand and communicate
- Accounts for uncertainty (confidence)
- Prevents effort alone from driving priorities

### Limitations
- Requires estimation effort
- "Impact" can be subjective
- Doesn't account for strategic fit
- Not suitable for very early-stage ideas with no data
- Should be combined with qualitative judgment

### Best Practices
- Define "Impact" relative to current goals (e.g., revenue, engagement)
- Use consistent time periods for Reach
- Include all team effort (not just engineering)
- Be conservative with Confidence scores
- Review and calibrate scores as a team
- Combine with qualitative factors (strategic fit, dependencies)

### Related Prioritization Methods
- **MoSCoW**: Categorical prioritization
- **WSJF (Weighted Shortest Job First)**: SAFe's economic prioritization
- **ICE Score**: Impact, Confidence, Ease (simpler variant)
- **Value vs. Effort Matrix**: 2x2 visual prioritization
- **Kano Model**: Feature categorization

### Complementary NioPD Commands
- `/niopd:ST:moscow` - Categorical requirement prioritization
- `/niopd:UR:kano` - Feature importance classification
- `/niopd:PM:roadmap` - Roadmap creation from prioritized items

## Usage
`/niopd:ST:rice [--initiatives=<file_path>] [--timeframe=<time_period>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Inputs:**
    -   Check if `--initiatives` argument is provided for the initiatives file.
    -   Check if `--timeframe` argument is provided for the time period.

## Instructions

You are Nio, an AI Product Assistant. Your task is to help users prioritize initiatives using the RICE scoring framework.

### Core Principle
Always ensure that your analysis is grounded in the RICE framework's core principle: providing a quantitative scoring framework that combines four factors (Reach, Impact, Confidence, Effort) into a single priority score, enabling objective comparison of initiatives.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you prioritize initiatives using the RICE scoring framework."
-   If the `--initiatives` argument wasn't provided, ask the user: "What initiatives would you like to prioritize?" and wait for their response.
-   If the `--timeframe` argument wasn't provided, ask the user: "What is the time period for this analysis?" and wait for their response.
-   If configuration file exists and contains initiatives or timeframe settings, use those values as defaults
-   If language setting in configuration is Chinese, respond in Chinese; otherwise, respond in English

### Step 2: Explain RICE Framework
-   Briefly explain the RICE scoring framework:
    -   Reach - How many people will be impacted within a time period?
    -   Impact - What's the impact per person?
    -   Confidence - How confident are we in our estimates?
    -   Effort - How much work is required?
    -   Formula: RICE Score = (Reach × Impact × Confidence) / Effort
-   Ask the user: "Do you understand the RICE framework, or would you like me to elaborate?" and wait for their response.

### Step 3: Score Each Initiative
-   Guide the user through scoring each initiative:
    -   "What is the Reach for [initiative]? (Number of people impacted)"
    -   "What is the Impact for [initiative]? (Scale: 3=Massive, 2=High, 1=Medium, 0.5=Low, 0.25=Minimal)"
    -   "What is your Confidence level for [initiative]? (Percentage)"
    -   "What is the Effort for [initiative]? (Person-months required)"
-   Wait for the user's responses for each initiative.

### Step 4: Calculate RICE Scores
-   Help the user calculate scores:
    -   "Based on the formula, the RICE Score for [initiative] is: (Reach × Impact × Confidence) / Effort"
    -   Calculate and present the score for each initiative
-   Wait for the user's confirmation.

### Step 5: Rank Initiatives
-   Guide the user to rank initiatives by RICE score:
    -   "Based on the scores, how would you rank these initiatives?"
    -   "Which initiatives should be prioritized for implementation?"
-   Wait for the user's responses.

### Step 6: Create Resource Allocation Plan
-   Help the user plan resource allocation:
    -   "What resources are required for the top initiatives?"
    -   "What is the timeline for implementation?"
    -   "What dependencies exist between initiatives?"
-   Wait for the user's responses.

### Step 7: Create Comprehensive RICE Scoring Analysis Document

Generate a detailed RICE scoring report with the following structure:

---
# RICE Score Prioritization: [Product/Project Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Product/Team:** [name]  
**Time Period:** [Quarter/Month]  
**Total Initiatives Scored:** [number]  
**Goal Focus:** [Primary goal - e.g., "Increase monthly active users"]

---

## Executive Summary

**Top 3 Priorities (by RICE Score):**
1. **[Initiative]** - Score: [XXX]
2. **[Initiative]** - Score: [XXX]
3. **[Initiative]** - Score: [XXX]

**Resource Allocation Recommendation:**
- Commit to: Top [X] initiatives (Score > [threshold])
- Consider: [X] initiatives (Score [range])
- Defer: [X] initiatives (Score < [threshold])

**Total Effort Required (Top 5):** [XX] person-months

---

## RICE Scoring Framework

### Formula
**RICE Score = (Reach × Impact × Confidence) / Effort**

### Factor Definitions (For This Analysis)

**Reach:** Number of [users/customers/events] per [quarter/month]

**Impact:** Contribution to [primary goal]
- **3.0** = Massive impact
- **2.0** = High impact  
- **1.0** = Medium impact
- **0.5** = Low impact
- **0.25** = Minimal impact

**Confidence:** How certain are we?
- **100%** = High (strong data, validated hypothesis)
- **80%** = Medium (some data, reasonable assumptions)
- **50%** = Low (speculation, uncertain)

**Effort:** Total person-months (all disciplines)
- Minimum unit: 0.5 person-months

---

## Scored Initiatives (Ranked by RICE Score)

### #1: [Initiative Name] - RICE Score: [XXX]

**Description:**  
[Brief description of what this initiative accomplishes]

#### RICE Breakdown

**Reach: [X,XXX]** [users/customers] per [quarter/month]
- **Calculation**: [How reach was estimated]
- **Assumptions**: [Key assumptions about reach]
- **Data Source**: [Customer data/Analytics/Estimate]

**Impact: [X.X]** ([Massive/High/Medium/Low/Minimal])
- **Impact on**: [Primary metric affected - e.g., "conversion rate"]
- **Expected change**: [e.g., "+15% conversion improvement"]
- **Rationale**: [Why this impact level]

**Confidence: [XX]%** ([High/Medium/Low] confidence)
- **Based on**: [Data/Similar features/Assumptions]
- **Risk factors**: [Uncertainties that reduce confidence]
- **Validation**: [How this will be/has been validated]

**Effort: [X.X]** person-months
- **Product**: [X.X pm]
- **Design**: [X.X pm]
- **Engineering**: [X.X pm]
- **Other**: [X.X pm]
- **Total**: [X.X pm]

#### Calculation
**RICE Score = ([Reach] × [Impact] × [Confidence]) / [Effort]**  
**RICE Score = ([X] × [X] × [X]) / [X] = [XXX]**

#### Additional Context

**Strategic Alignment:** [How this supports company strategy]

**Dependencies:**
- Requires: [Prerequisites]
- Enables: [Future initiatives this unlocks]

**Timeline:** [Estimated start - end dates]

**Owner:** [PM/Team responsible]

**Status:** [Committed/Under consideration/Deferred]

---

### #2: [Initiative Name] - RICE Score: [XXX]
[Repeat full structure]

### #3: [Initiative Name] - RICE Score: [XXX]
[Repeat full structure]

### #4: [Initiative Name] - RICE Score: [XXX]
[Repeat structure for all initiatives]

---

## RICE Comparison Matrix

| Rank | Initiative | Reach | Impact | Confidence | Effort | RICE Score | Priority |
|------|------------|-------|--------|------------|--------|------------|----------|
| 1 | [Name] | [X,XXX] | [X.X] | [XX]% | [X.X] | **[XXX]** | P0 |
| 2 | [Name] | [X,XXX] | [X.X] | [XX]% | [X.X] | **[XXX]** | P0 |
| 3 | [Name] | [X,XXX] | [X.X] | [XX]% | [X.X] | **[XXX]** | P1 |
| 4 | [Name] | [X,XXX] | [X.X] | [XX]% | [X.X] | [XXX] | P1 |
| 5 | [Name] | [X,XXX] | [X.X] | [XX]% | [X.X] | [XXX] | P2 |
| 6 | [Name] | [X,XXX] | [X.X] | [XX]% | [X.X] | [XX] | P2 |
| 7 | [Name] | [X,XXX] | [X.X] | [XX]% | [X.X] | [XX] | Defer |

---

## Prioritization Tiers

### Tier 1: Commit (RICE > [threshold, e.g., 100])

**Initiatives:**
1. [Initiative] - Score: [XXX]
2. [Initiative] - Score: [XXX]
3. [Initiative] - Score: [XXX]

**Total Effort:** [XX] person-months  
**Expected Impact:** [Aggregate expected benefit]  
**Timeline:** [Start date] - [End date]  
**Resource Requirement:** [Team composition needed]

**Recommendation:** ✅ **COMMIT** - Greenlight for immediate execution

---

### Tier 2: Consider (RICE [range, e.g., 50-100])

**Initiatives:**
1. [Initiative] - Score: [XX]
2. [Initiative] - Score: [XX]

**Total Effort:** [XX] person-months  
**Decision Criteria:**
- Capacity after Tier 1 completion
- Strategic alignment
- Dependencies on Tier 1 initiatives

**Recommendation:** ⚠️ **EVALUATE** - Include if capacity allows or strategic value high

---

### Tier 3: Defer (RICE < [threshold, e.g., 50])

**Initiatives:**
1. [Initiative] - Score: [XX]
2. [Initiative] - Score: [XX]

**Deferral Rationale:**
- Low RICE score relative to other opportunities
- Insufficient capacity in current planning period
- Awaiting additional validation

**Recommendation:** 🔴 **DEFER** - Revisit in next planning cycle

---

## Sensitivity Analysis

### Impact Sensitivity

"What if we're wrong about Impact?"

| Initiative | Current Score | If Impact +1 | If Impact -0.5 | Rank Change |
|------------|---------------|--------------|----------------|-------------|
| [Name] | [XXX] | [XXX] | [XX] | ↑/↓/- |
| [Name] | [XXX] | [XXX] | [XX] | ↑/↓/- |

**Key Insight:** [Which initiatives are most sensitive to impact assumptions]

---

### Effort Sensitivity

"What if initiatives take longer than estimated?"

| Initiative | Current Score | If Effort +50% | If Effort +100% | Rank Change |
|------------|---------------|----------------|-----------------|-------------|
| [Name] | [XXX] | [XX] | [XX] | ↑/↓/- |
| [Name] | [XXX] | [XX] | [XX] | ↑/↓/- |

**Key Insight:** [Which initiatives remain high priority even if effort doubles]

---

### Confidence Sensitivity

"What if we're less confident?"

| Initiative | Current Score | At 50% Confidence | Rank Change |
|------------|---------------|-------------------|-------------|
| [Name] | [XXX] | [XX] | ↑/↓/- |
| [Name] | [XXX] | [XX] | ↑/↓/- |

**Key Insight:** [Which initiatives need validation before commitment]

---

## Resource Allocation Plan

### Team Capacity

**Available Capacity:** [Total person-months per quarter/month]  
**Breakdown:**
- Product: [X] person-months
- Design: [X] person-months
- Engineering: [X] person-months

**Committed (Tier 1):** [X] person-months ([XX]% of capacity)  
**Buffer:** [X] person-months ([XX]% for unknowns)

---

### Allocation by Initiative

| Initiative | Product | Design | Engineering | Total | Start | End |
|------------|---------|--------|-------------|-------|-------|-----|
| [Name] | [X.X pm] | [X.X pm] | [X.X pm] | [X.X pm] | [Date] | [Date] |
| [Name] | [X.X pm] | [X.X pm] | [X.X pm] | [X.X pm] | [Date] | [Date] |
| [Name] | [X.X pm] | [X.X pm] | [X.X pm] | [X.X pm] | [Date] | [Date] |
| **Total** | **[X]** | **[X]** | **[X]** | **[X]** | | |

---

### Timeline (Gantt View)

```
            Q1                Q2                Q3                Q4
            |----|----|----|----|----|----|----|----|----|----|----|----|
Initiative 1  =================
Initiative 2       ================
Initiative 3                  ======================
Initiative 4                         ===========
```

---

## Qualitative Factors (Non-RICE Considerations)

### Strategic Fit

| Initiative | Strategic Alignment | Notes |
|------------|---------------------|-------|
| [Name] | ⭐⭐⭐⭐⭐ (Critical) | [Aligns with company OKR #1] |
| [Name] | ⭐⭐⭐ (Moderate) | [Supports but not core to strategy] |
| [Name] | ⭐ (Low) | [Nice-to-have, not strategic] |

**Adjustment:** Consider promoting strategically critical initiatives even with lower RICE scores

---

### Technical Debt / Foundation

| Initiative | Reduces Tech Debt? | Platform Value? |
|------------|-------------------|------------------|
| [Name] | ✅ High | ✅ Enables future work |
| [Name] | ❌ No | ❌ Standalone |
| [Name] | ⚠️ Medium | ⚠️ Some reusability |

**Adjustment:** Platform investments may warrant higher priority than RICE alone suggests

---

### Risk & Learning

| Initiative | Validation Needed | Learning Value |
|------------|------------------|----------------|
| [Name] | ✅ Run experiment first | ⚠️ Tests key hypothesis |
| [Name] | ❌ Well-understood | ❌ Known solution |

**Adjustment:** High-learning initiatives may warrant pilot/MVP before full commitment

---

## Recommendations & Next Steps

### Immediate Actions (Next 2 Weeks)

1. **Greenlight Tier 1 Initiatives:**
   - [Initiative 1]: Assign team, kick off
   - [Initiative 2]: Begin discovery
   - [Initiative 3]: Allocate resources

2. **Validate High-Uncertainty Items:**
   - [Initiative with low confidence]: Run experiment to increase confidence
   - [Initiative with uncertain effort]: Spike to refine estimate

3. **Communicate Deferrals:**
   - Inform stakeholders of Tier 3 deferrals
   - Set expectations for next review cycle

---

### Short-term (This Quarter)

- [ ] Execute all Tier 1 initiatives
- [ ] Monitor progress against effort estimates
- [ ] Measure actual impact vs. predicted
- [ ] Reassess Tier 2 based on capacity

---

### Medium-term (Next Quarter)

- [ ] Retrospective on RICE accuracy
- [ ] Calibrate scoring based on learnings
- [ ] Re-score deferred initiatives
- [ ] Incorporate new opportunities

---

## Scoring Calibration Notes

### For Future Scoring Sessions

**Impact Calibration:**
- **3.0 Massive** = [Concrete example from your domain]
- **2.0 High** = [Concrete example]
- **1.0 Medium** = [Concrete example]
- **0.5 Low** = [Concrete example]

**Reach Calibration:**
- Our monthly active users: [X]
- Average feature adoption rate: [X]%
- Benchmark "high reach": [X]+ per quarter

**Effort Calibration:**
- Small feature: [X] pm (e.g., [past example])
- Medium feature: [X] pm (e.g., [past example])
- Large feature: [X]+ pm (e.g., [past example])

---

## Appendix

### A. Estimation Assumptions

**Reach Calculations:**
[Document how reach was estimated for key initiatives]

**Impact Justifications:**
[Detail why impact scores were assigned]

**Effort Breakdowns:**
[Show detailed effort estimation methodology]

### B. Data Sources

- User analytics: [Tool/Dashboard]
- Customer feedback: [Sources]
- Market research: [Reports]
- Historical data: [Past initiatives performance]

### C. Stakeholder Input

**Reviewed by:**
- [Stakeholder 1] - [Role]
- [Stakeholder 2] - [Role]

**Feedback incorporated:**
- [Key feedback item 1]
- [Key feedback item 2]

---

**Prepared By:** [PM/Team]  
**Scoring Session Date:** [Date]  
**Participants:** [Names]  
**Last Updated:** [YYYYMMDD]  
**Next Review:** [Date - typically quarterly]

---

**Filename:** `[YYYYMMDD]-[product_slug]-rice-prioritization-v[version].md`  
**Save to:** `niopd-workspace/reports/[filename]`

### Step 8: Confirm and Conclude
-   Confirm the completion: "✅ I've created a comprehensive RICE prioritization analysis for **[product]**."
-   Show file path: `niopd-workspace/reports/[filename]`
-   Suggest next steps:
    -   "Validate with MoSCoW categorization: `/niopd:ST:moscow`"
    -   "Create user stories for top initiatives: `/niopd:PD:stories`"
    -   "Build roadmap from priorities: `/niopd:PM:roadmap`"
    -   "Plan release schedule: `/niopd:PM:release`"

## Error Handling
- **Missing Information:** If key information is missing, explain what's needed and offer to proceed with placeholders.
- **Unclear Requirements:** If requirements are ambiguous, ask for clarification using specific questions.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial analysis can still provide value.
