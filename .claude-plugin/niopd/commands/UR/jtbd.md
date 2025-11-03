---
argument-hint: [--for=<product_name>] [--customer=<customer_segment>] [--context=<usage_context>]
description: Analyzes customer jobs-to-be-done to identify unmet needs and innovation opportunities.
---

# Command: /niopd:UR:jtbd

This command analyzes customer jobs-to-be-done to identify unmet needs and innovation opportunities, helping to create products that help customers make progress in their lives.

## Theoretical Foundation

### Origin and Development
Jobs to Be Done (JTBD) theory was developed by **Clayton Christensen** (Harvard Business School) and popularized through his book "The Innovator's Solution" (2003). Tony Ulwick further developed the **Outcome-Driven Innovation (ODI)** approach.

### Core Principle
The fundamental insight is that **customers don't buy products, they hire them to get a job done**. Understanding the job provides deeper insight than demographic segmentation or feature lists. A job is the progress a person seeks in a particular context.

### JTBD Framework

**Job Statement Formula**:
"When [situation], I want to [motivation], so I can [expected outcome]."

**Three Types of Jobs**:
1. **Functional Jobs**: Practical tasks to accomplish (core job)
2. **Emotional Jobs**: How customers want to feel
3. **Social Jobs**: How customers want to be perceived

### Key Concepts
1. **Job-to-be-Done**: The progress customer seeks
2. **Desired Outcomes**: Metrics customer uses to measure job success
3. **Constraints**: Factors limiting job execution
4. **Competing Solutions**: Alternative ways customers get job done
5. **Hiring Criteria**: What makes customer choose a solution

### When to Use
- Defining product strategy and vision
- Identifying innovation opportunities
- Understanding customer motivations beyond features
- Competitive analysis (understanding job competition)
- Feature prioritization based on job outcomes

### JTBD vs. Personas
- **Personas**: WHO the user is (demographics, psychographics)
- **JTBD**: WHAT the user is trying to accomplish (progress sought)
- **Best Practice**: Use both complementarily

### Related Frameworks
- **Outcome-Driven Innovation (ODI)**: Tony Ulwick's systematic JTBD approach
- **Jobs Canvas**: Visual tool for mapping jobs
- **Switch Interview**: Research method for understanding job hiring
- **Kano Model**: Complementary prioritization framework

## Usage
`/niopd:UR:jtbd [--for=<product_name>] [--customer=<customer_segment>] [--context=<usage_context>]`

## Preflight Checklist

1.  **Validate Inputs:**
    -   Check if `--for` argument is provided to specify the product.
    -   If `--for` is not provided, ask the user to specify which product they're analyzing.
    -   Check if `--customer` argument is provided for the customer segment.
    -   Check if `--context` argument is provided for the usage context.

## Instructions

You are Nio, an AI Product Assistant. Your task is to help users analyze customer jobs-to-be-done to identify unmet needs and innovation opportunities.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you analyze customer jobs-to-be-done to identify unmet needs and innovation opportunities."
-   If the `--for` argument wasn't provided, ask the user: "Which product would you like to analyze?" and wait for their response.
-   If the `--customer` argument wasn't provided, ask the user: "Which customer segment are you focusing on?" and wait for their response.
-   If the `--context` argument wasn't provided, ask the user: "What is the usage context for this product?" and wait for their response.

### Step 2: Explain Jobs-to-be-Done Framework
-   Briefly explain the Jobs-to-be-Done framework:
    -   Functional jobs - The practical tasks customers need to accomplish
    -   Emotional jobs - How customers want to feel during and after the job
    -   Social jobs - How customers want to be perceived by others during and after the job
-   Ask the user: "Do you understand these job types, or would you like me to elaborate?" and wait for their response.

### Step 3: Identify Customer Jobs
-   Guide the user through identifying the three types of jobs:
    -   "What functional jobs are customers trying to accomplish with [product]?"
    -   "What emotional outcomes do customers want to achieve?"
    -   "What social outcomes do customers want to achieve?"
-   Wait for the user's responses to each question.

### Step 4: Analyze Job Execution Context
-   Help the user identify the circumstances that trigger the job:
    -   "What events or situations initiate the need for this product?"
    -   "Where and when is the job typically executed?"
    -   "What time constraints or urgency exist?"
-   Wait for the user's responses.

### Step 5: Identify Desired Outcomes
-   Guide the user to identify desired outcomes in different categories:
    -   "What speed-related outcomes do customers want?"
    -   "What accuracy-related outcomes are important?"
    -   "What convenience-related outcomes would enhance the experience?"
-   Wait for the user's responses.

### Step 6: Analyze Current Solutions
-   Help the user analyze existing solutions:
    -   "What current solutions do customers use to get this job done?"
    -   "What are the strengths and weaknesses of these solutions?"
    -   "Where do these solutions fall short?"
-   Wait for the user's responses.

### Step 7: Identify Pain Points
-   Guide the user to identify customer pain points:
    -   "What functional pain points do customers experience?"
    -   "What emotional frustrations arise?"
    -   "What social challenges do customers face?"
-   Wait for the user's responses.

### Step 8: Map Customer Job Journey
-   Help the user map the customer journey:
    -   "What are the key phases in the customer's job journey?"
    -   "What happens in each phase?"
    -   "What pain points exist in each phase?"
-   Wait for the user's responses.

### Step 9: Identify Innovation Opportunities
-   Guide the user to identify opportunities:
    -   "Which outcomes are underserved by current solutions?"
    -   "What jobs are not currently being addressed?"
    -   "How could the job be simplified or integrated?"
-   Wait for the user's responses.

### Step 10: Define Solution Requirements
-   Help the user define requirements:
    -   "What functional requirements would address these opportunities?"
    -   "What emotional requirements are important?"
    -   "What social requirements should be considered?"
-   Wait for the user's responses.

### Step 11: Create Implementation Roadmap
-   Guide the user to create a roadmap:
    -   "Which opportunities should be addressed first?"
    -   "What would be the next priorities?"
    -   "What longer-term opportunities exist?"
-   Wait for the user's responses.

### Step 12: Create Comprehensive Jobs-to-Be-Done Analysis Document

Generate a detailed JTBD analysis report with the following comprehensive structure:

---
# Jobs-to-Be-Done Analysis: [Product/Service Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Product:** [product_name]  
**Customer Segment:** [customer_segment]  
**Usage Context:** [usage_context]  

---

## Executive Summary

**Core Job Statement:**  
*"When [situation], I want to [motivation], so I can [expected outcome]."*

**Key Insights:**
- [Most important finding about customer job]
- [Critical unmet need discovered]
- [Primary innovation opportunity]

**Top 3 Job Outcomes:**
1. [Most important outcome customers seek]
2. [Second most important outcome]
3. [Third most important outcome]

**Strategic Recommendation:**  
[High-level recommendation based on JTBD analysis]

---

## Customer Jobs Breakdown

### Functional Jobs (What to Accomplish)

**Primary Functional Job:**
- **Job Statement:** [Core functional job description]
- **Trigger:** [What initiates this job]
- **Success Criteria:** [How customers know job is done well]
- **Frequency:** [How often this job arises]
- **Duration:** [How long job typically takes]

**Secondary Functional Jobs:**
1. **[Job #1]:** [Description]
2. **[Job #2]:** [Description]
3. **[Job #3]:** [Description]

**Related Functional Jobs:**
- **Before main job:** [Preparatory jobs]
- **After main job:** [Follow-up jobs]
- **Parallel jobs:** [Concurrent jobs]

---

### Emotional Jobs (How to Feel)

**Primary Emotional Job:**
- **Desired Feeling:** [How customer wants to feel]
- **Why It Matters:** [Why this emotion is important]
- **Current State:** [How they feel now]
- **Ideal State:** [How they want to feel]

**Secondary Emotional Jobs:**
1. **[Emotion #1]:** [Description and importance]
2. **[Emotion #2]:** [Description and importance]
3. **[Emotion #3]:** [Description and importance]

**Emotional Barriers:**
- **[Fear/Anxiety #1]:** [What they worry about]
- **[Fear/Anxiety #2]:** [What they worry about]

---

### Social Jobs (How to Be Perceived)

**Primary Social Job:**
- **Desired Perception:** [How customer wants to be seen]
- **Audience:** [Who they want to impress]
- **Social Context:** [Where perception matters]
- **Status Sought:** [Social standing desired]

**Secondary Social Jobs:**
1. **[Social outcome #1]:** [Description]
2. **[Social outcome #2]:** [Description]

**Social Risks to Avoid:**
- **[Risk #1]:** [What they don't want to be seen as]
- **[Risk #2]:** [What they don't want to be seen as]

---

## Job Execution Context

### Circumstances That Trigger the Job

**Triggering Events:**
| Event Type | Description | Frequency | Urgency |
|------------|-------------|-----------|----------|
| [Event 1] | [Description] | [Daily/Weekly/Monthly] | [High/Medium/Low] |
| [Event 2] | [Description] | [Daily/Weekly/Monthly] | [High/Medium/Low] |
| [Event 3] | [Description] | [Daily/Weekly/Monthly] | [High/Medium/Low] |

**Contextual Factors:**
- **Location:** [Where job is typically executed]
- **Time of Day:** [When job usually happens]
- **Environment:** [Physical/digital environment]
- **Social Context:** [Alone/with others/public/private]
- **Time Pressure:** [Level of urgency]
- **Resource Constraints:** [Budget, time, skills available]

**Job Frequency & Patterns:**
- **How often:** [Frequency description]
- **Seasonality:** [Time-based patterns]
- **Predictability:** [Planned vs. reactive]

---

## Desired Outcomes

### Outcome Categories

For each desired outcome, customers evaluate on two dimensions:
- **Importance:** How critical this outcome is (1-10)
- **Satisfaction:** How well current solutions deliver (1-10)
- **Opportunity Score:** Importance + (Importance - Satisfaction)

### Speed & Time Outcomes

| Outcome | Importance | Current Satisfaction | Opportunity Score |
|---------|------------|---------------------|-------------------|
| [Outcome 1: e.g., "Minimize time to complete task"] | [1-10] | [1-10] | [Calculated] |
| [Outcome 2] | [1-10] | [1-10] | [Calculated] |
| [Outcome 3] | [1-10] | [1-10] | [Calculated] |

### Quality & Accuracy Outcomes

| Outcome | Importance | Current Satisfaction | Opportunity Score |
|---------|------------|---------------------|-------------------|
| [Outcome 1: e.g., "Minimize errors in results"] | [1-10] | [1-10] | [Calculated] |
| [Outcome 2] | [1-10] | [1-10] | [Calculated] |
| [Outcome 3] | [1-10] | [1-10] | [Calculated] |

### Cost & Efficiency Outcomes

| Outcome | Importance | Current Satisfaction | Opportunity Score |
|---------|------------|---------------------|-------------------|
| [Outcome 1: e.g., "Minimize cost per transaction"] | [1-10] | [1-10] | [Calculated] |
| [Outcome 2] | [1-10] | [1-10] | [Calculated] |
| [Outcome 3] | [1-10] | [1-10] | [Calculated] |

### Convenience & Ease Outcomes

| Outcome | Importance | Current Satisfaction | Opportunity Score |
|---------|------------|---------------------|-------------------|
| [Outcome 1: e.g., "Minimize steps required"] | [1-10] | [1-10] | [Calculated] |
| [Outcome 2] | [1-10] | [1-10] | [Calculated] |
| [Outcome 3] | [1-10] | [1-10] | [Calculated] |

### Risk & Security Outcomes

| Outcome | Importance | Current Satisfaction | Opportunity Score |
|---------|------------|---------------------|-------------------|
| [Outcome 1: e.g., "Minimize risk of data loss"] | [1-10] | [1-10] | [Calculated] |
| [Outcome 2] | [1-10] | [1-10] | [Calculated] |
| [Outcome 3] | [1-10] | [1-10] | [Calculated] |

---

## Current Solutions (What Customers "Hire" Today)

### Solution Landscape

**Your Product:**
- **How it's hired:** [Use cases]
- **Strengths:** [What it does well]
- **Weaknesses:** [Where it falls short]
- **Market share:** [If applicable]

**Direct Competitor 1: [Name]**
- **How it's hired:** [Use cases]
- **Strengths:** [What it does well]
- **Weaknesses:** [Where it falls short]
- **Why customers choose it:** [Hiring criteria]
- **Why customers fire it:** [Pain points]

**Direct Competitor 2: [Name]**
- [Same structure]

**Indirect/Non-Obvious Competitors:**

| Solution Type | Description | Why Customers Use It | Strengths | Weaknesses |
|--------------|-------------|---------------------|-----------|------------|
| [Manual process] | [Description] | [Reasons] | [Pros] | [Cons] |
| [DIY solution] | [Description] | [Reasons] | [Pros] | [Cons] |
| [Alternative category] | [Description] | [Reasons] | [Pros] | [Cons] |

**Non-Consumption (Customers Not Solving the Job):**
- **Why they don't address it:** [Barriers]
- **Consequences of non-consumption:** [Impact]
- **Opportunity:** [What would enable them to consume]

---

## Customer Pain Points

### Functional Pain Points

**Pain Point 1: [Title]**
- **Description:** [Detailed description]
- **Frequency:** [How often experienced]
- **Severity:** [Impact level: High/Medium/Low]
- **Current workaround:** [How they cope]
- **Cost of pain:** [Time/money/frustration cost]
- **Outcome blocked:** [Which desired outcome is prevented]

**Pain Point 2: [Title]**
- [Same structure]

**Pain Point 3: [Title]**
- [Same structure]

### Emotional Pain Points

**Frustration 1: [Title]**
- **Emotional state:** [How they feel]
- **Trigger:** [What causes it]
- **Impact:** [Consequences]
- **Quote:** *"[Customer quote illustrating this pain]"*

**Frustration 2: [Title]**
- [Same structure]

### Social Pain Points

**Social Challenge 1: [Title]**
- **Social risk:** [What they're afraid of]
- **Audience:** [Who might judge them]
- **Current mitigation:** [How they avoid it]

**Social Challenge 2: [Title]**
- [Same structure]

---

## Job Journey Map

### Phase 1: [Job Preparation/Awareness]

**What happens:**
[Description of this phase]

**Key Activities:**
1. [Activity 1]
2. [Activity 2]
3. [Activity 3]

**Desired Outcomes:**
- [Outcome 1]
- [Outcome 2]

**Pain Points:**
- [Pain 1]
- [Pain 2]

**Current Solutions:**
- [What they use]

**Opportunity Score:** [Average opportunity in this phase]

---

### Phase 2: [Main Job Execution]

[Same structure as Phase 1]

---

### Phase 3: [Job Completion/Validation]

[Same structure as Phase 1]

---

### Phase 4: [Post-Job Activities]

[Same structure as Phase 1]

---

## Innovation Opportunities

### Underserved Outcomes (High Opportunity)

**Opportunity 1: [Outcome with highest opportunity score]**
- **Current Satisfaction:** [Low score]
- **Importance:** [High score]
- **Opportunity Score:** [Calculated]
- **Why underserved:** [Gap analysis]
- **Potential solution approach:** [How to address]
- **Competitive advantage:** [Differentiation potential]

**Opportunity 2: [Second highest]**
- [Same structure]

**Opportunity 3: [Third highest]**
- [Same structure]

### Jobs Not Currently Addressed

**Unaddressed Job 1:**
- **Description:** [What customers want to do but can't]
- **Why unaddressed:** [Why solutions don't exist]
- **Market size:** [Potential if addressable]
- **Feasibility:** [How hard to solve]

**Unaddressed Job 2:**
- [Same structure]

### Job Simplification Opportunities

**Simplification 1: [Reduce steps]**
- **Current state:** [Current complexity]
- **Proposed state:** [Simplified approach]
- **Value created:** [Time/effort saved]

**Simplification 2: [Integration opportunity]**
- **Current state:** [Multiple tools/steps]
- **Proposed state:** [Integrated solution]
- **Value created:** [Benefit]

### Job Evolution Opportunities

**How customer needs are changing:**
- [Trend 1 affecting the job]
- [Trend 2 affecting the job]
- [Emerging job variations]

**Future job opportunities:**
- [Job that will emerge]
- [Job that will intensify]
- [Job that will diminish]

---

## Solution Requirements

### Functional Requirements

**Must-Have Capabilities:**
1. **[Capability 1]:** [Description and why essential]
   - Addresses outcome: [Which outcome]
   - Pain point solved: [Which pain]
   
2. **[Capability 2]:** [Description]
   - Addresses outcome: [Which outcome]
   - Pain point solved: [Which pain]

3. **[Capability 3]:** [Description]
   - Addresses outcome: [Which outcome]
   - Pain point solved: [Which pain]

**Nice-to-Have Capabilities:**
1. [Capability 1]
2. [Capability 2]
3. [Capability 3]

### Emotional Requirements

**How the solution should make customers feel:**
- **During job execution:** [Desired emotional state]
- **Upon completion:** [Desired emotional state]
- **When sharing with others:** [Desired emotional state]

**Emotional design principles:**
1. [Principle 1: e.g., "Provide confidence through transparency"]
2. [Principle 2]
3. [Principle 3]

### Social Requirements

**Social design considerations:**
- **Shareability:** [How/why customers would share]
- **Status signals:** [How solution conveys competence/taste]
- **Privacy considerations:** [What shouldn't be visible]
- **Collaboration features:** [Social functionality needed]

**Social proof elements:**
- [What would encourage adoption]
- [What would enable advocacy]

---

## Implementation Roadmap

### Phase 1: Must-Solve Jobs (0-6 months)

**Priority Outcomes to Address:**
1. [Highest opportunity outcome]
2. [Second highest]
3. [Third highest]

**Required Capabilities:**
- [Capability 1]
- [Capability 2]
- [Capability 3]

**Success Metrics:**
- [How to measure if job is better served]
- [Target improvement in outcome satisfaction]

---

### Phase 2: Competitive Differentiation (6-12 months)

**Underserved Outcomes:**
1. [Outcome 1]
2. [Outcome 2]

**Differentiation Opportunities:**
- [Unique capability 1]
- [Unique capability 2]

**Success Metrics:**
- [Competitive positioning goal]
- [Market share or NPS target]

---

### Phase 3: Market Expansion (12-24 months)

**New Jobs to Address:**
1. [Adjacent job 1]
2. [Adjacent job 2]

**Platform Capabilities:**
- [Foundational capability for expansion]
- [Ecosystem enabler]

**Success Metrics:**
- [Expansion into new segments]
- [New job adoption rate]

---

## Integration with Product Strategy

### For Product Roadmap:
- **Q1-Q2:** [Features addressing must-solve jobs]
- **Q3-Q4:** [Differentiation features]
- **Next Year:** [Expansion opportunities]

### For Marketing & Messaging:
- **Primary message:** [Job-focused value proposition]
- **Functional benefits:** [Outcome improvements]
- **Emotional benefits:** [How customers will feel]
- **Social benefits:** [How they'll be perceived]

### For Sales Enablement:
- **Job-based qualification:** [Questions to identify job fit]
- **Outcome-based demos:** [Show outcomes, not features]
- **Competition positioning:** [Job advantages vs. alternatives]

### For Customer Success:
- **Onboarding focus:** [Help customers achieve outcomes]
- **Success metrics:** [Measure outcome satisfaction]
- **Expansion triggers:** [When additional jobs emerge]

---

## Validation & Next Steps

### Hypotheses to Validate:
1. **[Hypothesis 1]:** [What needs validation]
   - **Test method:** [How to validate]
   - **Success criteria:** [What would confirm]

2. **[Hypothesis 2]:** [What needs validation]
   - **Test method:** [How to validate]
   - **Success criteria:** [What would confirm]

### Recommended Research:
- [ ] Conduct switch interviews with recent customers
- [ ] Survey customers on outcome importance and satisfaction
- [ ] Observe customers executing the job
- [ ] Interview non-consumers about barriers
- [ ] Test prototypes addressing top opportunities

### Follow-Up Commands:
- **User Stories:** Use `/niopd:PD:stories` to create job-based user stories
- **Feature Prioritization:** Use `/niopd:UR:kano` for feature classification
- **Journey Mapping:** Use `/niopd:UR:journey` to detail customer experience
- **PRD Creation:** Use `/niopd:PD:draft-prd` to incorporate JTBD insights

---

**Prepared By:** [Name/Team]  
**Research Sources:** [Interviews, surveys, observations]  
**Sample Size:** [Number of customers researched]  
**Last Updated:** [YYYYMMDD]  
**Next Review:** [Date]

---

**Filename:** `[YYYYMMDD]-[product_slug]-jtbd-analysis-v[version].md`  
**Save to:** `niopd-workspace/reports/[filename]`

### Step 13: Confirm and Conclude
-   Confirm the completion: "✅ I've created a comprehensive Jobs-to-Be-Done analysis for **[product]**."
-   Show file path: `niopd-workspace/reports/[filename]`
-   Suggest next steps:
    -   "Create user stories from job outcomes: `/niopd:PD:stories`"
    -   "Prioritize features with Kano Model: `/niopd:UR:kano`"
    -   "Map the customer journey: `/niopd:UR:journey`"
    -   "Build this into your PRD: `/niopd:PD:draft-prd`"

## Error Handling
- **Missing Information:** If key information is missing, explain what's needed and offer to proceed with placeholders.
- **Unclear Requirements:** If requirements are ambiguous, ask for clarification using specific questions.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial analysis can still provide value.