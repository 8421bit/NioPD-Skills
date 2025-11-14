---
argument-hint: [--topic=<planning_topic>] [--timeframe=<analysis_timeframe>] [--scope=<analysis_scope>]
description: Explores multiple future scenarios to prepare for uncertainty and make robust strategic decisions.
---

# Command: /niopd:DT:scenarios

This command explores multiple future scenarios to prepare for uncertainty and make robust strategic decisions.

## Theoretical Foundation

### Origin and Development
Scenario planning was pioneered by **Herman Kahn** at the RAND Corporation in the 1950s for military strategy, and later refined by **Pierre Wack** and **Peter Schwartz** at **Royal Dutch Shell** in the 1970s. Shell famously used scenario planning to anticipate the 1973 oil crisis.

### Core Principle
Scenario planning acknowledges that the future is inherently uncertain and unpredictable. Rather than trying to predict one future, organizations develop multiple plausible future scenarios to prepare for a range of possibilities and make more robust strategic decisions.

### The Scenario Planning Process
1. **Identify Focal Issue**: Define the strategic question or decision
2. **Analyze Driving Forces**: Identify trends and uncertainties
3. **Select Critical Uncertainties**: Choose the most impactful unknowns
4. **Develop Scenario Logic**: Create scenario framework (often 2x2 matrix)
5. **Flesh Out Scenarios**: Build detailed narratives for each future
6. **Analyze Implications**: Assess impact on strategy for each scenario
7. **Monitor and Adapt**: Track indicators and adjust strategies

### Key Characteristics
1. **Multiple Futures**: Explores 3-4 distinct plausible futures
2. **Driving Forces**: Based on trends and critical uncertainties
3. **Narratives**: Rich stories about how each future unfolds
4. **Strategic Resilience**: Identifies robust strategies across scenarios
5. **Early Warning Signals**: Monitors which scenario is emerging

### The 2x2 Matrix Approach
Most commonly, scenarios are built on a **2x2 matrix** with:
- **X-axis**: One critical uncertainty (e.g., technological change: slow vs. rapid)
- **Y-axis**: Another critical uncertainty (e.g., regulatory environment: restrictive vs. permissive)
- **Four Quadrants**: Each representing a distinct future scenario

### When to Use
- Long-term strategic planning (5-20 years)
- High uncertainty environments
- Disruptive industry changes
- Major capital investment decisions
- Crisis preparedness and resilience planning

### Famous Applications
- **Royal Dutch Shell**: Oil crisis preparation (1970s)
- **Singapore Government**: Long-term national planning
- **Mont Fleur Scenarios**: South African transition (1991-1992)
- **Global Business Network**: Corporate strategy consulting

### Scenario Types
1. **Exploratory Scenarios**: "What could happen?"
2. **Normative Scenarios**: "What should happen?"
3. **Predictive Scenarios**: "What will likely happen?"
4. **Operational Scenarios**: Short-term tactical planning

### Related Methodologies
- **SWOT Analysis**: Strengths, Weaknesses, Opportunities, Threats
- **PEST/PESTLE Analysis**: Macro-environmental scanning
- **Delphi Method**: Expert consensus building
- **Backcasting**: Working backward from desired future
- **Horizon Scanning**: Systematic detection of emerging trends

### Benefits
- Challenges conventional thinking
- Prepares for multiple futures
- Identifies early warning signals
- Builds organizational flexibility
- Facilitates strategic conversations

## Usage
`/niopd:DT:scenarios [--topic=<planning_topic>] [--timeframe=<analysis_timeframe>] [--scope=<analysis_scope>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Planning Topic:**
    -   If the `--topic` argument is not provided, prompt the user to specify the planning topic.
    -   Confirm that the planning topic is valid and meaningful.

3.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/sources` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in strategic thinking and scenario planning. Your goal is to help users explore multiple future scenarios to prepare for uncertainty and make robust strategic decisions.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Data
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request with a message in the user's preferred language:
    -   If Chinese: "我将帮您探索 **<planning_topic>** 的未来情景。"
    -   If English: "I'll help you explore future scenarios for **<planning_topic>**."
    -   For other languages, use an appropriate translation based on user's language preference
-   If the `--topic` argument wasn't provided, ask the user in their preferred language: "What topic or decision would you like to explore future scenarios for?" and wait for their response.
-   If the `--timeframe` argument wasn't provided, ask the user in their preferred language: "What timeframe should we focus on for this scenario analysis?" and wait for their response.
-   If the `--scope` argument wasn't provided, ask the user in their preferred language: "What is the scope of this scenario analysis?" and wait for their response.

### Step 2: Scenario Planning Framework
-   Explain the scenario planning framework to the user:
    -   "Scenario planning helps us prepare for uncertainty by exploring multiple plausible futures."
    -   "We'll identify key driving forces and uncertainties that could shape the future."
    -   "We'll develop distinct scenarios that represent different combinations of these forces."
    -   "We'll analyze the implications of each scenario and develop robust strategies."
-   Ask the user: "Do you understand this scenario planning framework, or would you like me to explain any aspect in more detail?" and wait for their response.

### Step 3: Driving Forces Analysis
-   Help the user identify key driving forces:
    -   "What are the major social, technological, economic, environmental, and political trends affecting **<planning_topic>**?"
    -   "Which of these forces are certain to continue, and which are uncertain?"
    -   "What are the key uncertainties that could significantly impact the future?"
    -   "How do these forces interact with each other?"
-   Wait for the user's responses.

### Step 4: Critical Uncertainties Selection
-   Guide the user through selecting critical uncertainties:
    -   "From the identified uncertainties, which two have the greatest potential impact and uncertainty?"
    -   "These will become the axes for our scenario matrix."
    -   "What is the range of possible outcomes for each critical uncertainty?"
    -   "How might these uncertainties evolve over our **<timeframe>** timeframe?"
-   Wait for the user's responses.

### Step 5: Scenario Matrix Development
-   Help the user develop a scenario matrix:
    -   "Let's create a 2x2 matrix with our two critical uncertainties as axes."
    -   "Each quadrant represents a different future scenario."
    -   "What does each quadrant represent in terms of the combination of uncertainties?"
    -   "What are the key characteristics of each scenario?"
-   Wait for the user's responses.

### Step 6: Scenario Narratives Creation
-   Guide the user through creating detailed scenario narratives:
    -   "Let's develop rich narratives for each scenario that tell a compelling story."
    -   "What does the world look like in each scenario by **<timeframe>**?"
    -   "What are the key events or developments that led to each scenario?"
    -   "What are the implications for **<planning_topic>** in each scenario?"
-   Wait for the user's responses.

### Step 7: Scenario Validation
-   Help the user validate scenarios for plausibility:
    -   "Is each scenario internally consistent and plausible?"
    -   "Are the scenarios sufficiently distinct from each other?"
    -   "Do the scenarios span the range of possible futures?"
    -   "What evidence supports or challenges each scenario?"
-   Wait for the user's responses.

### Step 8: Implications Analysis
-   Guide the user through analyzing implications:
    -   "What are the key implications of each scenario for **<planning_topic>**?"
    -   "How would different strategies perform in each scenario?"
    -   "What opportunities and threats emerge in each scenario?"
    -   "What early warning indicators should we monitor for each scenario?"
-   Wait for the user's responses.

### Step 9: Strategic Options Development
-   Help the user develop strategic options:
    -   "What strategic options are robust across multiple scenarios?"
    -   "What options are optimal for specific scenarios?"
    -   "What no-regret moves should we consider regardless of the future?"
    -   "What adaptive strategies allow us to respond as scenarios unfold?"
-   Wait for the user's responses.

### Step 10: Monitoring and Signposts
-   Guide the user through establishing monitoring mechanisms:
    -   "What early warning signs indicate which scenario is unfolding?"
    -   "What key indicators should we track over time?"
    -   "How will we update our scenarios as new information emerges?"
    -   "What triggers would cause us to shift our strategic approach?"
-   Wait for the user's responses.

### Step 11: Create Scenario Planning Report
Produce a markdown report with the following structure:

---
# Scenario Planning Report: [Planning Topic]

## Executive Summary
*A brief overview of key scenarios and strategic recommendations*

## Planning Context
### Topic
[Planning topic from user input]

### Timeframe
[Timeframe from user input]

### Scope
[Scope from user input]

## Scenario Planning Framework
### Approach
[Framework explanation from Step 2]

### Key Principles
[Key principles of scenario planning]

## Driving Forces
### Major Trends
1. **[Trend 1]:** [Description and impact]
2. **[Trend 2]:** [Description and impact]

### Key Uncertainties
1. **[Uncertainty 1]:** [Description and potential range]
2. **[Uncertainty 2]:** [Description and potential range]

## Scenario Matrix
### Critical Uncertainties
| Uncertainty | Low | High |
|-------------|-----|------|
| **[Uncertainty 1]** |     |      |
| **[Uncertainty 2]** |     |      |

### Scenarios
| Scenario | [Uncertainty 1] | [Uncertainty 2] | Description |
|----------|-----------------|-----------------|-------------|
| **Scenario 1** | Low | Low | [Brief description] |
| **Scenario 2** | Low | High | [Brief description] |
| **Scenario 3** | High | Low | [Brief description] |
| **Scenario 4** | High | High | [Brief description] |

## Scenario Narratives
### Scenario 1: [Name]
- **World View:** [Description of the world in this scenario]
- **Key Events:** [Major developments leading to this scenario]
- **Characteristics:** [Distinctive features of this future]

### Scenario 2: [Name]
- **World View:** [Description of the world in this scenario]
- **Key Events:** [Major developments leading to this scenario]
- **Characteristics:** [Distinctive features of this future]

### Scenario 3: [Name]
- **World View:** [Description of the world in this scenario]
- **Key Events:** [Major developments leading to this scenario]
- **Characteristics:** [Distinctive features of this future]

### Scenario 4: [Name]
- **World View:** [Description of the world in this scenario]
- **Key Events:** [Major developments leading to this scenario]
- **Characteristics:** [Distinctive features of this future]

## Implications Analysis
### Scenario 1 Implications
- **Opportunities:** [Key opportunities]
- **Threats:** [Key threats]
- **Strategic Impact:** [Impact on **<planning_topic>**]

### Scenario 2 Implications
- **Opportunities:** [Key opportunities]
- **Threats:** [Key threats]
- **Strategic Impact:** [Impact on **<planning_topic>**]

### Scenario 3 Implications
- **Opportunities:** [Key opportunities]
- **Threats:** [Key threats]
- **Strategic Impact:** [Impact on **<planning_topic>**]

### Scenario 4 Implications
- **Opportunities:** [Key opportunities]
- **Threats:** [Key threats]
- **Strategic Impact:** [Impact on **<planning_topic>**]

## Strategic Options
### Robust Strategies
1. **[Strategy 1]:** [Description and rationale]
2. **[Strategy 2]:** [Description and rationale]

### Scenario-Specific Strategies
- **Scenario 1:** [Optimal strategies]
- **Scenario 2:** [Optimal strategies]

### No-Regret Moves
1. **[Move 1]:** [Description and rationale]
2. **[Move 2]:** [Description and rationale]

## Monitoring and Signposts
### Early Warning Indicators
1. **[Indicator 1]:** [Description and significance]
2. **[Indicator 2]:** [Description and significance]

### Review Schedule
[Review schedule from Step 10]

### Update Triggers
[Update triggers from Step 10]

---

### Step 12: Save the Report
- Generate a filename for the scenario planning report following the NioPD naming convention: `[YYYYMMDD]-[topic_slug]-scenarios-v[version].md`.
- Save the scenario planning report to: `niopd-workspace/sources/[filename]`

### Step 13: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the scenario planning analysis for **<planning_topic>**."
- Provide the path to the file: "You can view the detailed scenario planning report at: `niopd-workspace/sources/[YYYYMMDD]-[topic_slug]-scenarios-v[version].md`"
- Suggest next steps: "Consider using `/niopd:DT:scenarios` to update this analysis as conditions change, or `/niopd:DT:first-principles` to examine fundamental assumptions in each scenario."

## Error Handling
- **Missing Planning Topic:** If no planning topic is specified, explain that a topic is required and ask for it.
- **Incomplete Scenario Development:** If the user doesn't provide sufficient information for scenario development, explain what's needed and offer to proceed with partial analysis.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial scenario planning can still provide valuable insights.