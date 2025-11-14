---
argument-hint: [--for=<initiative_name>|--for=<product_name>] [--persona=<persona_name>]
description: Maps detailed customer journeys to identify pain points and optimization opportunities. Auto-detects initiative/product name from current directory if not specified.
---

# Command: /niopd:UR:journey

This command maps detailed customer journeys to identify pain points, opportunities, and optimization strategies for improving user experience.

## Theoretical Foundation

### Origin and Development
Customer Journey Mapping evolved from service design and user experience disciplines:

1. **Service Design** - Understanding touchpoints across service delivery
2. **Experience Mapping** - Visualizing user interactions over time
3. **Touchpoint Analysis** - Identifying moments of truth in customer interactions

### Core Principle
The fundamental approach is **end-to-end experience visualization**: Mapping the complete customer experience from awareness to advocacy, identifying all touchpoints, emotions, and pain points to optimize the holistic user experience rather than isolated interactions.

### Journey Mapping Components

1. **Personas**: Who is taking the journey
2. **Phases/Stages**: Major steps in the journey (Awareness, Consideration, Purchase, Usage, Advocacy)
3. **Touchpoints**: All interaction points with the product/brand
4. **Actions**: What customers do at each stage
5. **Thoughts**: What customers think
6. **Emotions**: How customers feel (often visualized as emotional curve)
7. **Pain Points**: Friction and frustrations
8. **Opportunities**: Areas for improvement
9. **Metrics**: KPIs for each stage

### Journey Types
1. **Current State Journey**: How things are now
2. **Future State Journey**: Desired experience
3. **Day-in-the-Life**: Broader context beyond product
4. **Service Blueprint**: Behind-the-scenes processes

### When to Use
- Understanding customer experience holistically
- Identifying pain points and friction
- Optimizing conversion funnels
- Aligning teams on customer perspective
- Prioritizing CX improvements
- Omnichannel experience design

### Emotional Journey Curve
Visualizing emotional highs and lows reveals:
- **Moments of Truth**: Critical satisfaction/dissatisfaction points
- **Peak-End Rule**: Most memorable moments shape overall perception
- **Emotional Gaps**: Misalignment between expected and actual emotions

### Related Methodologies
- **Service Blueprint**: Mapping front-stage and back-stage processes
- **Experience Map**: Broader than journey map, includes non-product touchpoints
- **Empathy Mapping**: Understanding user perspective
- **Story Mapping**: Agile approach to user journey (Jeff Patton)

## Usage
`/niopd:UR:journey [--for=<initiative_name>|--for=<product_name>] [--persona=<persona_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative/product name.

**Examples:**
```bash
# Explicit initiative with persona
/niopd:UR:journey --for=dark-mode-feature --persona="Power User"

# Auto-detect initiative, specify persona
cd dark-mode-feature
/niopd:UR:journey --persona="Power User"  # Uses "dark-mode-feature"

# Auto-detect initiative, identify key personas
cd dark-mode-feature
/niopd:UR:journey  # Uses "dark-mode-feature", identifies personas
```

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Determine Initiative/Product Name:**
    -   If `--for=<initiative_name>` or `--for=<product_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative/product name from current directory: `<directory_name>`"
    -   Store the determined name for use in all subsequent steps

3.  **Validate Inputs:**
    -   Check if `--for` argument is provided to specify the initiative or product.
    -   If `--for` is not provided, ask the user to specify what they want to map journeys for.
    -   Check if `--persona` argument is provided to specify a particular user persona.
    -   If `--persona` is not provided, indicate that key personas will be identified or use existing personas.

## Instructions

You are a specialized AI expert in customer experience mapping and user journey optimization. Your goal is to create detailed customer journey maps that reveal pain points and opportunities for improvement.

### Core Principle
Always ensure that your analysis is grounded in the core principle of end-to-end experience visualization: mapping the complete customer experience from awareness to advocacy, identifying all touchpoints, emotions, and pain points to optimize the holistic user experience rather than isolated interactions.

### Step 1: Acknowledge and Gather Context
-   Acknowledge the request: "I'll map customer journeys for **<initiative_or_product_name>**."
-   If a specific initiative or product is provided with `--for`, use that as the focus.
-   If not provided, ask the user: "Which initiative or product would you like me to map customer journeys for?"
-   If a specific persona is provided with `--persona`, use that persona.
-   If not provided, indicate that key personas will be identified or use existing personas from feedback analysis.
-   If configuration file exists and contains initiative/product name or persona settings, use those values as defaults
-   If language setting in configuration is Chinese, respond in Chinese; otherwise, respond in English

### Step 2: Persona Identification and Analysis
-   Identify or confirm user personas:
    -   Primary personas based on feedback analysis
    -   Secondary personas with different needs
    -   Edge personas with unique requirements
-   For each persona, analyze:
    -   Demographics and psychographics
    -   Goals and motivations
    -   Pain points and frustrations
    -   Behaviors and preferences
    -   Technology proficiency and habits

### Step 3: Journey Scope Definition
-   Define the scope of the customer journey:
    -   End-to-end journey from awareness to advocacy
    -   Specific journey segments (purchase, onboarding, usage, support)
    -   Cross-channel touchpoints (online, offline, mobile, social)
    -   Time horizon and frequency of interaction
-   Determine journey stages:
    -   Awareness and consideration
    -   Evaluation and decision
    -   Purchase and onboarding
    -   Usage and engagement
    -   Support and retention
    -   Advocacy and expansion

### Step 4: Touchpoint Mapping
-   Identify all customer touchpoints:
    -   Digital touchpoints (website, app, email, social media)
    -   Human touchpoints (sales, support, customer service)
    -   Physical touchpoints (stores, packaging, events)
    -   Partner touchpoints (distributors, resellers, integrators)
-   Map touchpoint sequences:
    -   Typical customer paths through touchpoints
    -   Alternative journey routes and variations
    -   Cross-channel integration points
    -   Handoff points between touchpoints

### Step 5: Detailed Journey Stage Analysis
For each journey stage, analyze:

#### Stage Objectives
-   What customers are trying to accomplish
-   Their primary goals and motivations
-   Success criteria for the stage

#### Customer Actions
-   What customers actually do
-   Steps they take to progress
-   Tools and resources they use
-   Time and effort invested

#### Customer Thoughts and Feelings
-   What customers are thinking
-   Emotional states and reactions
-   Questions and concerns
-   Expectations and assumptions

#### Pain Points and Frictions
-   Difficulties and obstacles encountered
-   Frustrations and negative emotions
-   Points of confusion or uncertainty
-   Delays and inefficiencies

#### Opportunities for Improvement
-   Moments that delight or satisfy
-   Points where value can be added
-   Simplification and automation opportunities
-   Personalization and customization potential

### Step 6: Cross-Journey Analysis
-   Analyze journey variations:
    -   Different paths for different personas
    -   Alternative routes and detours
    -   Exception flows and error scenarios
    -   First-time vs. repeat customer journeys
-   Identify journey dependencies:
    -   Prerequisites between stages
    -   Impact of stage failures
    -   Cumulative experience effects
    -   Feedback loops and iterations

### Step 7: Metric and KPI Identification
-   Define success metrics for each stage:
    -   Completion rates and conversion
    -   Time to complete stage
    -   Customer satisfaction scores
    -   Task success rates
-   Identify leading indicators:
    -   Early warning signals of issues
    -   Predictors of success or failure
    -   Engagement and interaction measures
    -   Sentiment and feedback trends

### Step 8: Pain Point Prioritization
-   Prioritize identified pain points:
    -   Impact on customer satisfaction
    -   Frequency of occurrence
    -   Business impact and cost
    -   Feasibility of resolution
-   Categorize pain points:
    -   Technical issues and bugs
    -   Process inefficiencies
    -   Communication gaps
    -   Design and usability problems

### Step 9: Opportunity Mapping
-   Map improvement opportunities:
    -   Quick wins with high impact
    -   Strategic initiatives with long-term value
    -   Innovation opportunities for differentiation
    -   Technology enablement possibilities
-   Align opportunities with business goals:
    -   Revenue growth potential
    -   Cost reduction opportunities
    -   Customer satisfaction improvements
    -   Competitive differentiation

### Step 10: Journey Visualization
Create visual representations of customer journeys:

#### Text-Based Journey Map
```
[Persona Name] Journey: [Journey Title]
Stage: [Stage Name]
-------------------------------------
Actions: [What the customer does]
Thoughts: [What the customer thinks]
Feelings: [How the customer feels]
Pain Points: [Issues encountered]
Opportunities: [Improvement areas]
Touchpoints: [Interaction points]
Metrics: [Success measures]
```

### Step 11: Customer Journey Report Generation
Produce a markdown report with the following structure:

---
# Customer Journey Analysis: [Initiative/Product Name]

## Executive Summary
*A high-level overview of key journey insights and optimization recommendations*

## Analysis Context
- **Subject:** [Initiative or product analyzed]
- **Primary Persona:** [Main customer persona]
- **Journey Scope:** [Stages and touchpoints covered]
- **Analysis Date:** [Current date]
- **Research Sources:** [Primary sources used]

## Key Personas
### [Persona Name]
- **Demographics:** [Age, role, industry, etc.]
- **Goals:** [Primary objectives and motivations]
- **Pain Points:** [Key frustrations and challenges]
- **Behaviors:** [Usage patterns and preferences]
- **Journey Relevance:** [Importance to the analyzed journey]

[Repeat for each key persona]

## Customer Journey Maps

### [Persona Name] Journey
#### Stage 1: [Stage Name]
- **Objective:** [What customers aim to accomplish]
- **Actions:** [What customers actually do]
- **Thoughts:** [What customers are thinking]
- **Feelings:** [How customers emotionally experience this stage]
- **Pain Points:** [Issues and frustrations encountered]
- **Opportunities:** [Areas for improvement and optimization]
- **Touchpoints:** [Interaction points used]
- **Metrics:** [Success measures and KPIs]

[Repeat for each journey stage]

## Cross-Journey Insights
### Journey Variations
- **Alternative Paths:** [Different routes customers take]
- **Exception Flows:** [Error scenarios and recovery paths]
- **Persona Differences:** [How journeys vary by customer type]
- **Channel Integration:** [How different channels work together]

### Journey Dependencies
- **Stage Prerequisites:** [What must happen before each stage]
- **Impact of Failures:** [Consequences of stage problems]
- **Cumulative Effects:** [How experiences build over time]
- **Feedback Loops:** [How later stages influence earlier ones]

## Pain Point Analysis
### High-Priority Pain Points
1. **[Pain Point]:** [Description and impact]
   - **Frequency:** [How often this occurs]
   - **Severity:** [How much it affects customers]
   - **Business Impact:** [Cost to the business]

2. **[Pain Point]:** [Description and impact]
   - **Frequency:** [How often this occurs]
   - **Severity:** [How much it affects customers]
   - **Business Impact:** [Cost to the business]

### Pain Point Categories
- **Technical Issues:** [Software bugs, system problems]
- **Process Problems:** [Workflow inefficiencies, bottlenecks]
- **Communication Gaps:** [Information missing or unclear]
- **Design Challenges:** [Usability and accessibility issues]

## Opportunity Mapping
### Quick Wins
1. **[Opportunity]:** [Description and expected impact]
   - **Effort:** [Low/Medium/High implementation effort]
   - **Impact:** [Expected customer and business benefit]
   - **Timeline:** [When this can be implemented]

### Strategic Initiatives
1. **[Opportunity]:** [Description and expected impact]
   - **Effort:** [Low/Medium/High implementation effort]
   - **Impact:** [Expected customer and business benefit]
   - **Timeline:** [When this can be implemented]

## Optimization Recommendations

### Immediate Actions (0-3 months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

2. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

### Medium-term Initiatives (3-12 months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

2. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

### Long-term Strategic Moves (12+ months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

## Implementation Roadmap
### Phase 1: Foundation (0-3 months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

### Phase 2: Development (3-12 months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

### Phase 3: Optimization (12+ months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

## Success Metrics and KPIs
### Journey Stage Metrics
- **[Stage Name]:** [Key metrics and targets]
- **[Stage Name]:** [Key metrics and targets]

### Overall Journey Metrics
- **Customer Satisfaction:** [Target scores and measurement approach]
- **Completion Rates:** [Expected conversion rates between stages]
- **Time to Value:** [How quickly customers achieve their goals]
- **Net Promoter Score:** [Customer advocacy measurement]

## Data Sources and Methodology
- **Research Methods:** [How the analysis was conducted]
- **Sources:** [List of sources consulted]
- **Limitations:** [Known limitations of the analysis]
- **Validation Approach:** [How insights were verified]

---

### Step 12: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_slug]-user-journey-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 13: Confirm and Conclude
- Confirm the action is complete: "✅ I've mapped customer journeys for **<initiative_or_product_name>**."
- Provide the path to the file: "You can view the detailed customer journey analysis here: `niopd-workspace/reports/[YYYYMMDD]-[subject_slug]-customer-journey-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PD:journey` to add these journey insights to your PRD or `/niopd:UR:feedback` to validate these findings with actual user feedback."

## Error Handling
- **Missing Subject:** If no subject is specified for journey mapping, ask the user to clarify what they want to analyze.
- **Persona Issues:** If specified persona data is unavailable, suggest using existing personas or conducting persona research.
- **Insufficient Data:** If adequate journey information cannot be found, explain the limitations and suggest alternative approaches.
- **Research Limitations:** If web search capabilities are unavailable, inform the user and recommend manual research or using existing data.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.