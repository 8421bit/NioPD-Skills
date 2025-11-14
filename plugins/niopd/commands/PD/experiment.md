---
argument-hint: [--feature=<feature_name>] [--hypothesis=<hypothesis_statement>] [--metric=<success_metric>]
description: Designs and plans feature experiments to test hypotheses and validate product decisions with data.
---

# Command: /niopd:PD:experiment

This command designs and plans feature experiments to test hypotheses and validate product decisions with data.

## Theoretical Foundation

### Origin and Development
Product experimentation emerged from the scientific method and was adapted for digital products in the 2000s. **Ronny Kohavi** (Microsoft, Amazon) pioneered A/B testing at scale. The methodology was popularized by **Eric Ries** ("The Lean Startup", 2011) and **Dan Siroker** (Optimizely founder).

### Core Principle
Product experiments apply the **scientific method to product development**: formulate hypotheses, design controlled tests, collect data, and make evidence-based decisions. The goal is to validate assumptions before committing significant resources.

### The Scientific Method for Products

1. **Observe**: Identify a problem or opportunity
2. **Question**: What do we want to learn?
3. **Hypothesize**: Formulate testable prediction
4. **Experiment**: Design and run controlled test
5. **Analyze**: Evaluate results statistically
6. **Conclude**: Make data-driven decision
7. **Iterate**: Refine and test again

### Hypothesis Format

**If-Then-Because Structure**:
"**If** [we make this change], **then** [this outcome will occur], **because** [this is our rationale]."

**Example**: "If we add social proof badges, then conversion rate will increase by 10%, because users trust recommendations from peers."

### Types of Product Experiments

**A/B Test (Split Test)**:
- Control (A) vs. Treatment (B)
- Random assignment
- Single variable change
- Statistical comparison

**Multivariate Test (MVT)**:
- Multiple variables simultaneously
- Tests interaction effects
- Requires larger sample size
- Example: Testing headline + image + CTA combinations

**A/B/n Test**:
- Multiple treatment variants
- Example: A (control), B (variant 1), C (variant 2)

**Bandit Test**:
- Dynamic traffic allocation
- Shifts traffic to winning variant over time
- Minimizes opportunity cost

### Key Metrics

**Primary Metric**: Main success criterion
- Conversion rate
- Revenue per user
- Engagement (DAU, session length)

**Secondary Metrics**: Supporting indicators
- Click-through rate
- Time to conversion
- Feature adoption

**Guardrail Metrics**: Safety checks
- Error rates
- Load time
- User satisfaction (NPS)
- Revenue (ensure no negative impact)

### Statistical Concepts

**Statistical Significance**:
- Confidence level: Typically 95% (p < 0.05)
- Probability result isn't due to chance

**Statistical Power**:
- Typically 80%
- Ability to detect true effect

**Sample Size**:
- Larger samples = more reliable results
- Depends on: baseline rate, minimum detectable effect, significance, power

**Minimum Detectable Effect (MDE)**:
- Smallest change worth detecting
- Trade-off: sensitivity vs. sample size

### Common Pitfalls

**Peeking Problem**:
- Checking results too early
- Inflates false positive rate
- Solution: Pre-define stopping criteria

**Multiple Testing Problem**:
- Testing many metrics increases false positives
- Solution: Bonferroni correction or pre-specify primary metric

**Simpson's Paradox**:
- Trend reverses when data is segmented
- Solution: Analyze segments separately

**Novelty Effect**:
- Initial excitement biases results
- Solution: Run experiments long enough (2+ weeks)

**Selection Bias**:
- Non-random assignment
- Solution: Ensure proper randomization

### Experimentation Frameworks

**HEART Framework (Google)**:
- **H**appiness: User satisfaction (NPS, CSAT)
- **E**ngagement: Usage frequency/depth
- **A**doption: New user activation
- **R**etention: Repeat usage
- **T**ask Success: Completion rate, time, errors

**ICE Score (Prioritization)**:
- **I**mpact: Expected impact (1-10)
- **C**onfidence: Certainty in estimate (0-100%)
- **E**ase: Implementation effort (1-10)
- Score = (Impact × Confidence) / Ease

### When to Use Experiments
- High-impact product changes
- Uncertain outcomes
- Measurable success criteria
- Sufficient traffic for statistical power
- Reversible changes

### Lean Startup Build-Measure-Learn

1. **Build**: Create minimum viable test
2. **Measure**: Collect data on key metrics
3. **Learn**: Validate or invalidate hypothesis
4. **Decide**: Persevere, pivot, or stop

### Related Concepts
- **MVP (Minimum Viable Product)**: Smallest version to test
- **Prototype Testing**: Qualitative validation
- **Usability Testing**: Behavioral observation
- **Feature Flags**: Technical implementation for experiments

### Complementary NioPD Commands
- `/niopd:UR:usability` - Qualitative user testing
- `/niopd:PD:draft-prd` - Document experiment results
- `/niopd:ST:ost` - Opportunity-solution tree
- `/niopd:PO:metrics` - Define success metrics

## Usage
`/niopd:PD:experiment [--feature=<feature_name>] [--hypothesis=<hypothesis_statement>] [--metric=<success_metric>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Feature Context:**
    -   If the `--feature` argument is not provided, prompt the user to specify the feature context.
    -   Confirm that the feature context is valid and meaningful.

3.  **Validate Hypothesis:**
    -   If the `--hypothesis` argument is not provided, prompt the user to specify the hypothesis.
    -   Confirm that the hypothesis is clear and testable.

4.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/reports` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in product experimentation and hypothesis testing. Your goal is to help users design and plan feature experiments to test hypotheses and validate product decisions with data.

**Core Principle:** The final experiment design should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Data
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将帮您为 **<feature_name>** 功能设计和规划实验。"
    -   If English: "I'll help you design and plan an experiment for the **<feature_name>** feature."
    -   For other languages, use an appropriate translation based on user's language preference
-   If the `--feature` argument wasn't provided, ask the user in their preferred language: "您想对哪个功能进行实验？" and wait for their response.
-   If the `--hypothesis` argument wasn't provided, ask the user in their preferred language: "您想通过这个实验测试什么假设？" and wait for their response.
-   If the `--metric` argument wasn't provided, ask the user in their preferred language: "您将使用什么成功指标来评估实验？" and wait for their response.

### Step 2: Hypothesis Refinement
-   Help the user refine their hypothesis using the "If-Then" format:
    -   "If we [make a specific change to the feature], then [we expect a specific outcome] because [rationale]."
    -   "Is your hypothesis specific, measurable, and testable?"
    -   "What is the expected direction and magnitude of the change?"
-   Wait for the user's responses.

### Step 3: Experiment Design Framework
-   Explain the key elements of experiment design:
    -   "We need to define our independent variable (what we're changing) and dependent variable (what we're measuring)."
    -   "We need to identify our control group (current experience) and treatment group (new experience)."
    -   "We need to determine our sample size and experiment duration."
    -   "We need to establish our success criteria and statistical significance threshold."
-   Ask the user: "Do you understand these experiment design principles, or would you like me to explain any in more detail?" and wait for their response.

### Step 4: Variable Definition
-   Help the user clearly define the variables:
    -   "What exactly are we changing in the treatment group?"
    -   "How will we ensure the control group remains unchanged?"
    -   "What is our primary success metric?"
    -   "What are our secondary metrics and guardrail metrics?"
-   Wait for the user's responses.

### Step 5: Sample Size Calculation
-   Guide the user through sample size calculation:
    -   "What is the baseline conversion rate for our success metric?"
    -   "What is the minimum detectable effect we want to measure?"
    -   "What statistical power do we want to achieve? (typically 80%)"
    -   "What significance level will we use? (typically 95%)"
-   Wait for the user's responses.

### Step 6: Experiment Duration Planning
-   Help the user plan the experiment duration:
    -   "Based on our sample size calculation, how long do we need to run the experiment?"
    -   "Are there any seasonal or external factors that might affect our results?"
    -   "Should we run the experiment during a specific time period?"
    -   "How will we handle new user acquisition during the experiment?"
-   Wait for the user's responses.

### Step 7: Segmentation Strategy
-   Guide the user through defining segmentation:
    -   "Should we segment our results by user type, behavior, or demographics?"
    -   "Are there any specific user groups we want to analyze separately?"
    -   "How will segmentation help us understand the experiment results?"
-   Wait for the user's responses.

### Step 8: Implementation Planning
-   Help the user plan the technical implementation:
    -   "What tools and platforms will we use to implement the experiment?"
    -   "Who will be responsible for setting up the experiment?"
    -   "What is our timeline for implementation?"
    -   "How will we ensure proper randomization and assignment?"
-   Wait for the user's responses.

### Step 9: Monitoring Plan
-   Guide the user through establishing a monitoring plan:
    -   "How will we monitor the experiment while it's running?"
    -   "What metrics will we track daily or weekly?"
    -   "What alerts or thresholds should we set up?"
    -   "Who will be responsible for monitoring the experiment?"
-   Wait for the user's responses.

### Step 10: Analysis Framework
-   Help the user establish an analysis framework:
    -   "What statistical tests will we use to analyze the results?"
    -   "How will we handle outliers or anomalous data?"
    -   "What segments or cohorts will we analyze?"
    -   "How will we interpret the results in the context of our hypothesis?"
-   Wait for the user's responses.

### Step 11: Risk Assessment
-   Guide the user through assessing experiment risks:
    -   "What are the potential negative impacts of this experiment?"
    -   "How can we mitigate these risks?"
    -   "What guardrail metrics should we monitor?"
    -   "What is our rollback plan if results are negative?"
-   Wait for the user's responses.

### Step 12: Documentation and Communication
-   Help the user plan documentation and communication:
    -   "How will we document the experiment design and results?"
    -   "Who needs to be informed about this experiment?"
    -   "How will we communicate results to stakeholders?"
    -   "What learnings should we capture for future experiments?"
-   Wait for the user's responses.

### Step 13: Create Experiment Design Report
Produce a markdown report with the following structure:

---
# Feature Experiment Design: [Feature Name]

## Executive Summary
*A brief overview of the experiment hypothesis, design, and expected outcomes*

## Hypothesis
### Original Hypothesis
[Original hypothesis provided by user]

### Refined Hypothesis
[Refined "If-Then-Because" hypothesis from Step 2]

## Experiment Design
### Independent Variable
[What we're changing from Step 4]

### Dependent Variable
[What we're measuring from Step 4]

### Control Group
[Control group definition from Step 4]

### Treatment Group
[Treatment group definition from Step 4]

## Success Metrics
### Primary Metric
[Primary success metric from Step 4]

### Secondary Metrics
[Secondary metrics identified in Step 4]

### Guardrail Metrics
[Guardrail metrics identified in Step 11]

## Sample Size and Duration
### Sample Size Calculation
[Sample size calculation details from Step 5]

### Experiment Duration
[Experiment duration plan from Step 6]

### Start and End Dates
- **Start Date:** [Planned start date]
- **End Date:** [Planned end date]

## Segmentation
### Analysis Segments
[Segments identified in Step 7]

### Segment Rationale
[Rationale for each segment]

## Implementation
### Tools and Platforms
[Tools identified in Step 8]

### Implementation Team
[Team responsibilities from Step 8]

### Timeline
[Implementation timeline from Step 8]

### Quality Assurance
[QA measures for proper implementation]

## Monitoring Plan
### Daily Monitoring
[Daily metrics to track from Step 9]

### Weekly Monitoring
[Weekly metrics to track from Step 9]

### Alert Thresholds
[Alert thresholds from Step 9]

### Monitoring Responsibilities
[Monitoring responsibilities from Step 9]

## Analysis Framework
### Statistical Tests
[Statistical tests identified in Step 10]

### Outlier Handling
[Outlier handling approach from Step 10]

### Segment Analysis
[Segment analysis plan from Step 10]

### Success Criteria
[Success criteria and significance thresholds]

## Risk Assessment
### Potential Risks
[Risks identified in Step 11]

### Mitigation Strategies
[Mitigation strategies from Step 11]

### Rollback Plan
[Rollback plan from Step 11]

## Documentation and Communication
### Documentation Plan
[Documentation plan from Step 12]

### Stakeholder Communication
[Communication plan from Step 12]

### Learning Capture
[Learning capture approach from Step 12]

---

### Step 14: Save the Report
- Generate a filename for the experiment design report following the NioPD naming convention: `[YYYYMMDD]-[feature_slug]-experiment-v[version].md`.
- Save the experiment design report to: `niopd-workspace/docs/[filename]`

### Step 15: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the experiment design for the **<feature_name>** feature."
- Provide the path to the file: "You can view the detailed experiment design report at: `niopd-workspace/docs/[YYYYMMDD]-[feature_slug]-experiment-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PD:experiment` to design follow-up experiments based on these results, or `/niopd:PM:kpis` to track the success metrics during the experiment."

## Error Handling
- **Missing Feature Context:** If no feature context is specified, explain that feature context is required and ask for it.
- **Missing Hypothesis:** If no hypothesis is specified, explain that a testable hypothesis is required and ask for it.
- **Incomplete Experiment Design:** If the user doesn't provide sufficient information for experiment design, explain what's needed and offer to proceed with partial design.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial experiment design can still provide valuable guidance.