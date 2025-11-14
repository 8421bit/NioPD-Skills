---
argument-hint: [--for=<initiative_name>|--for=<product_name>] [--market=<market_context>]
description: Conducts a comprehensive SWOT analysis for a product, initiative, or business unit. Auto-detects initiative/product name from current directory if not specified.
---

# Command: /niopd:ST:swot

This command conducts a comprehensive SWOT (Strengths, Weaknesses, Opportunities, Threats) analysis to evaluate internal capabilities and external market factors affecting a product, initiative, or business unit.

## Theoretical Foundation

### Origin and Development
SWOT Analysis was developed by **Albert Humphrey** at the **Stanford Research Institute** in the 1960s-1970s during research funded by Fortune 500 companies. It became one of the most widely used strategic planning tools globally.

### Core Principle
SWOT provides a **structured framework for strategic situational analysis** by examining both internal factors (Strengths and Weaknesses) and external factors (Opportunities and Threats) to inform strategy formulation.

### The SWOT Matrix

**Internal Factors (What you control)**:
- **Strengths**: Internal capabilities and resources that provide competitive advantage
- **Weaknesses**: Internal limitations or deficiencies that hinder performance

**External Factors (What you don't control)**:
- **Opportunities**: External favorable conditions that could be exploited
- **Threats**: External challenges or risks that could cause problems

### TOWS Matrix (Extended Analysis)
Developed by **Heinz Weihrich** (1982), TOWS flips SWOT to emphasize strategy formulation:

1. **SO Strategies**: Use Strengths to capitalize on Opportunities (Growth)
2. **WO Strategies**: Overcome Weaknesses to pursue Opportunities (Improvement)
3. **ST Strategies**: Use Strengths to mitigate Threats (Defense)
4. **WT Strategies**: Minimize Weaknesses and avoid Threats (Survival)

### When to Use
- Strategic planning cycles
- New product/initiative evaluation
- Competitive positioning analysis
- M&A due diligence
- Business model assessment
- Turnaround situations

### Best Practices
- **Be Specific**: Avoid vague statements
- **Prioritize**: Not all factors are equally important
- **Evidence-Based**: Support with data and research
- **Actionable**: Connect to concrete strategies
- **Regular Updates**: Refresh as conditions change

### Related Frameworks
- **PEST/PESTLE Analysis**: Complementary external analysis
- **Porter's Five Forces**: Industry structure analysis
- **Value Chain Analysis**: Detailed internal analysis
- **BCG Matrix**: Portfolio strategy tool

## Usage
`/niopd:ST:swot [--for=<initiative_name>|--for=<product_name>] [--market=<market_context>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative/product name.

**Examples:**
```bash
# Explicit initiative with market context
/niopd:ST:swot --for=dark-mode-feature --market="mobile apps market"

# Auto-detect initiative, specify market
cd dark-mode-feature
/niopd:ST:swot --market="mobile apps market"  # Uses "dark-mode-feature"

# Auto-detect initiative and conduct market research
cd dark-mode-feature
/niopd:ST:swot  # Uses "dark-mode-feature", includes market research
```

## Preflight Checklist

1.  **Check Configuration File:**
    - Check if `niopd-workspace/config/niopd.config.json` exists
    - If it exists, load and apply configuration settings
    - If not, continue with default behavior

2.  **Determine Initiative/Product Name:**
    -   If `--for=<initiative_name>` or `--for=<product_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative/product name from current directory: `<directory_name>`"
    -   Store the determined name for use in all subsequent steps

3.  **Validate Inputs:**
    -   Check if `--for` argument is provided to specify the product, initiative, or business unit.
    -   If `--for` is not provided, ask the user to specify what they want to analyze.
    -   Check if `--market` argument is provided for market context.
    -   If `--market` is not provided, indicate that market research will be part of the analysis.

## Instructions

You are a specialized AI expert in strategic analysis and business evaluation. Your goal is to conduct a thorough SWOT analysis that provides actionable insights for strategic decision-making.

### Core Principle
Always ensure that your analysis is grounded in the SWOT framework's core principle: providing a structured framework for strategic situational analysis by examining both internal factors (Strengths and Weaknesses) and external factors (Opportunities and Threats) to inform strategy formulation.

### Step 1: Acknowledge and Gather Context
-   Acknowledge the request: "I'll conduct a SWOT analysis for **<initiative_or_product_name>**."
-   If a specific product, initiative, or business unit is provided with `--for`, use that as the focus.
-   If not provided, ask the user: "What product, initiative, or business unit would you like me to analyze with a SWOT analysis?"
-   If market context is provided with `--market`, use that information.
-   If not provided, indicate that market research will be part of the analysis.
-   If configuration file exists and contains initiative/product name or market settings, use those values as defaults
-   If language setting in configuration is Chinese, respond in Chinese; otherwise, respond in English

### Step 2: Internal Analysis - Strengths and Weaknesses
-   Research and analyze internal factors related to the focal entity:
    -   Product/Service Capabilities
    -   Organizational Resources
    -   Operational Efficiency
    -   Financial Position
    -   Human Capital
    -   Technology and Innovation
    -   Brand and Reputation
    -   Customer Relationships
    -   Market Position
    -   Competitive Advantages

#### Strengths Identification
-   Identify core competencies and competitive advantages
-   Determine unique capabilities that differentiate the entity
-   Assess resource strengths (financial, human, technological)
-   Evaluate operational excellence factors
-   Recognize brand equity and customer loyalty
-   Identify successful strategies and practices

#### Weaknesses Identification
-   Identify resource limitations and constraints
-   Determine capability gaps compared to competitors
-   Assess operational inefficiencies
-   Evaluate financial vulnerabilities
-   Recognize brand or reputation issues
-   Identify areas of poor performance or customer dissatisfaction

### Step 3: External Analysis - Opportunities and Threats
-   Research and analyze external market factors:
    -   Market Trends and Dynamics
    -   Competitive Landscape
    -   Customer Needs and Preferences
    -   Technological Developments
    -   Regulatory Environment
    -   Economic Conditions
    -   Social and Cultural Factors
    -   Industry Structure and Evolution

#### Opportunities Identification
-   Identify emerging market trends and shifts
-   Determine unmet customer needs and gaps in the market
-   Assess technological advancements that could be leveraged
-   Evaluate potential market expansion opportunities
-   Recognize partnership and collaboration possibilities
-   Identify regulatory or policy changes that could be beneficial

#### Threats Identification
-   Identify competitive pressures and new market entrants
-   Determine potential market disruptions
-   Assess regulatory or compliance risks
-   Evaluate economic downturns or market volatility
-   Recognize changing customer preferences that could be detrimental
-   Identify technological obsolescence risks

### Step 4: Stakeholder Input Integration
-   Research stakeholder perspectives:
    -   Customer feedback and satisfaction data
    -   Employee insights and engagement levels
    -   Partner and supplier relationships
    -   Investor and shareholder concerns
    -   Industry expert opinions
-   Integrate stakeholder viewpoints into each SWOT category

### Step 5: Competitive Benchmarking
-   Compare the focal entity against key competitors:
    -   Performance metrics comparison
    -   Capability assessment
    -   Market position analysis
    -   Strategic approach evaluation
-   Identify relative strengths and weaknesses against competition

### Step 6: Strategic Factor Prioritization
-   Rank SWOT factors by importance and impact:
    -   Criticality to success
    -   Urgency of addressing
    -   Potential for leverage or mitigation
    -   Resource requirements for action
-   Focus on factors that are most strategic in nature

### Step 7: SWOT Matrix Development
Create a structured SWOT matrix with prioritized factors:

#### Strengths (Internal Positive Factors)
1. **[Strength]:** [Description and impact]
2. **[Strength]:** [Description and impact]
3. **[Strength]:** [Description and impact]

#### Weaknesses (Internal Negative Factors)
1. **[Weakness]:** [Description and impact]
2. **[Weakness]:** [Description and impact]
3. **[Weakness]:** [Description and impact]

#### Opportunities (External Positive Factors)
1. **[Opportunity]:** [Description and impact]
2. **[Opportunity]:** [Description and impact]
3. **[Opportunity]:** [Description and impact]

#### Threats (External Negative Factors)
1. **[Threat]:** [Description and impact]
2. **[Threat]:** [Description and impact]
3. **[Threat]:** [Description and impact]

### Step 8: SWOT Strategic Analysis
Analyze strategic combinations from the SWOT matrix:

#### SO Strategies (Strengths-Opportunities)
-   How to use strengths to capitalize on opportunities
-   Growth strategies leveraging internal capabilities

#### WO Strategies (Weaknesses-Opportunities)
-   How to overcome weaknesses to pursue opportunities
-   Improvement strategies to enable opportunity capture

#### ST Strategies (Strengths-Threats)
-   How to use strengths to mitigate threats
-   Defensive strategies leveraging internal capabilities

#### WT Strategies (Weaknesses-Threats)
-   How to minimize weaknesses and avoid threats
-   Survival strategies addressing critical vulnerabilities

### Step 9: Strategic Recommendations
Based on the SWOT analysis, develop specific strategic recommendations:

#### Immediate Actions (0-6 months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
2. **[Recommendation]:** [Action, rationale, and expected outcome]

#### Medium-term Initiatives (6-18 months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
2. **[Recommendation]:** [Action, rationale, and expected outcome]

#### Long-term Strategic Moves (18+ months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
2. **[Recommendation]:** [Action, rationale, and expected outcome]

### Step 10: Risk Assessment
-   Identify risks associated with recommended strategies
-   Assess probability and impact of each risk
-   Develop risk mitigation approaches
-   Create contingency plans for critical risks

### Step 11: Implementation Considerations
-   Resource requirements for strategy execution
-   Organizational capabilities needed
-   Timeline and milestone planning
-   Success metrics and monitoring approaches
-   Stakeholder alignment and communication needs

### Step 12: SWOT Analysis Report Generation
Produce a markdown report with the following structure:

---
# SWOT Analysis: [Initiative/Product/Business Unit Name]

## Executive Summary
*A high-level overview of key SWOT findings and strategic recommendations*

## Analysis Context
- **Subject:** [What is being analyzed]
- **Market Context:** [Relevant market or industry]
- **Analysis Date:** [Current date]
- **Time Period:** [Historical data period if applicable]
- **Research Sources:** [Primary sources used]

## SWOT Matrix

### Strengths (Internal Positive Factors)
1. **[Strength]:** [Description and impact]
   - **Evidence:** [Supporting data or examples]
   - **Strategic Value:** [How this creates advantage]

2. **[Strength]:** [Description and impact]
   - **Evidence:** [Supporting data or examples]
   - **Strategic Value:** [How this creates advantage]

### Weaknesses (Internal Negative Factors)
1. **[Weakness]:** [Description and impact]
   - **Evidence:** [Supporting data or examples]
   - **Strategic Impact:** [How this creates disadvantage]

2. **[Weakness]:** [Description and impact]
   - **Evidence:** [Supporting data or examples]
   - **Strategic Impact:** [How this creates disadvantage]

### Opportunities (External Positive Factors)
1. **[Opportunity]:** [Description and impact]
   - **Market Evidence:** [Supporting data or examples]
   - **Strategic Potential:** [How this can be leveraged]

2. **[Opportunity]:** [Description and impact]
   - **Market Evidence:** [Supporting data or examples]
   - **Strategic Potential:** [How this can be leveraged]

### Threats (External Negative Factors)
1. **[Threat]:** [Description and impact]
   - **Evidence:** [Supporting data or examples]
   - **Strategic Risk:** [How this could cause harm]

2. **[Threat]:** [Description and impact]
   - **Evidence:** [Supporting data or examples]
   - **Strategic Risk:** [How this could cause harm]

## Strategic Combinations Analysis

### SO Strategies (Leverage Strengths for Opportunities)
1. **[Strategy]:** [How to use strength to capture opportunity]
   - **Action:** [Specific steps to implement]
   - **Expected Outcome:** [Anticipated results]

### WO Strategies (Overcome Weaknesses to Pursue Opportunities)
1. **[Strategy]:** [How to address weakness to enable opportunity]
   - **Action:** [Specific steps to implement]
   - **Expected Outcome:** [Anticipated results]

### ST Strategies (Use Strengths to Mitigate Threats)
1. **[Strategy]:** [How to use strength to reduce threat impact]
   - **Action:** [Specific steps to implement]
   - **Expected Outcome:** [Anticipated results]

### WT Strategies (Minimize Weaknesses and Avoid Threats)
1. **[Strategy]:** [How to reduce vulnerability to threats]
   - **Action:** [Specific steps to implement]
   - **Expected Outcome:** [Anticipated results]

## Strategic Recommendations

### Priority Actions (0-6 months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

2. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

### Medium-term Initiatives (6-18 months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

2. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

### Long-term Strategic Moves (18+ months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Resources Needed:** [Personnel, budget, tools]
   - **Success Metrics:** [How to measure effectiveness]

## Risk Assessment
### High-Priority Risks
1. **[Risk]:** [Description and likelihood]
   - **Impact:** [Potential consequences]
   - **Mitigation Strategy:** [How to address or reduce risk]

2. **[Risk]:** [Description and likelihood]
   - **Impact:** [Potential consequences]
   - **Mitigation Strategy:** [How to address or reduce risk]

### Medium-Priority Risks
1. **[Risk]:** [Description and likelihood]
   - **Impact:** [Potential consequences]
   - **Mitigation Strategy:** [How to address or reduce risk]

## Implementation Roadmap
### Phase 1: Foundation (0-6 months)
- **Key Activities:** [Primary actions]
- **Resource Allocation:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

### Phase 2: Development (6-18 months)
- **Key Activities:** [Primary actions]
- **Resource Allocation:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

### Phase 3: Optimization (18+ months)
- **Key Activities:** [Primary actions]
- **Resource Allocation:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

## Data Sources and Methodology
- **Research Methods:** [How analysis was conducted]
- **Sources:** [List of sources consulted]
- **Limitations:** [Known limitations of the analysis]
- **Confidence Level:** [Assessment of data reliability]

---

### Step 13: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_or_product_slug]-swot-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 14: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the SWOT analysis for **<initiative_or_product_name>**."
- Provide the path to the file: "You can view the detailed SWOT analysis here: `niopd-workspace/reports/[YYYYMMDD]-[subject_slug]-swot-analysis-v[version].md`"
- Suggest next steps: "Consider using `/niopd:ST:canvas` for business model analysis or `/niopd:ST:portfolio` for product portfolio evaluation."

## Error Handling
- **Missing Subject:** If no subject is specified for analysis, ask the user to clarify what they want to analyze.
- **Insufficient Data:** If adequate information cannot be found for a comprehensive analysis, explain the limitations and suggest alternative approaches.
- **Research Limitations:** If web search capabilities are unavailable, inform the user and recommend manual research or using existing data.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.
- **Analysis Errors:** If the SWOT analysis cannot be completed due to conflicting information, explain the conflicts and ask for clarification.