---
argument-hint: [--topic=<market_topic>] [--competitors=<competitor_list>]
description: Performs automated competitor comparison analysis based on market research.
---

# Command: /niopd:MR:compare

This command performs automated competitor comparison analysis by researching the market landscape and comparing key competitors based on various factors.

## Theoretical Foundation

### Origin and Development
Competitor comparison methodology integrates multiple strategic analysis tools:

1. **Comparative Analysis** - Systematic side-by-side evaluation across multiple dimensions
2. **Competitive Benchmarking** - Measuring performance against industry standards and competitors
3. **Strategic Group Analysis** - Grouping competitors with similar strategies (Michael Porter)

### Core Principle
The fundamental approach is **multi-dimensional competitive mapping**: Rather than analyzing competitors in isolation, this command compares multiple players across standardized criteria to reveal competitive dynamics, positioning gaps, and strategic opportunities.

### Comparison Dimensions
1. **Product/Features**: Functional capabilities and feature sets
2. **Pricing**: Pricing models, tiers, and value propositions
3. **Market Reach**: Geographic presence and segment focus
4. **Innovation**: R&D investment and technological advancement
5. **Market Position**: Share, brand strength, and customer satisfaction

### Analytical Outputs
- **Competitive Positioning Map**: Visual representation of competitive landscape
- **Feature Comparison Matrix**: Side-by-side capability comparison
- **SWOT Analysis**: Per-competitor strategic assessment
- **Gap Analysis**: Identifying white space and opportunities

### When to Use
- Market entry or expansion decisions
- Product feature prioritization and roadmap planning
- Strategic positioning and differentiation exercises
- Investment decisions requiring competitive context
- Periodic competitive intelligence updates

### Related Methodologies
- **Perceptual Mapping**: Visual representation of competitive positioning
- **Game Theory**: Strategic interaction and competitive dynamics
- **Resource-Based View**: Competitive advantage from unique resources (Barney, 1991)

## Usage
`/niopd:MR:compare [--topic=<market_topic>] [--competitors=<competitor_list>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Inputs:**
    -   Check if `--topic` argument is provided. If not, ask the user for the market topic or domain to analyze.
    -   Check if `--competitors` argument is provided. If not, the system will automatically identify key competitors.

## Instructions

You are a specialized AI expert in market research and competitive analysis. Your goal is to research and compare competitors in a given market space to provide actionable insights.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Context
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将对 **<market_topic>** 进行竞争对手比较分析。"
    -   If English: "I'll perform a competitor comparison analysis for **<market_topic>**."
    -   For other languages, use an appropriate translation based on user's language preference
-   If a market topic is provided with `--topic`, use that as the focus area.
-   If no topic is provided, ask the user in their preferred language: "What market or product domain would you like me to analyze for competitor comparison?"
-   If specific competitors are provided with `--competitors`, use that list.
-   If no competitors are provided, indicate that you'll identify key players automatically.

### Step 2: Market Landscape Research
-   Use web search capabilities to research the market topic:
    -   Identify the overall market size and growth trends
    -   Determine key market segments and niches
    -   Understand the competitive landscape and major players
    -   Identify emerging trends and market shifts
-   Document key findings about the market context and dynamics

### Step 3: Competitor Identification
-   If specific competitors were not provided, automatically identify key competitors:
    -   Search for major players in the market space
    -   Identify direct competitors (similar products/services)
    -   Identify indirect competitors (alternative solutions)
    -   Include both established players and emerging competitors
    -   Select 3-5 most relevant competitors for detailed analysis
-   If competitors were provided, validate and research those specific companies

### Step 4: Competitor Deep Dive Analysis
For each identified competitor, research and analyze:

#### Company Overview
-   Company background and history
-   Size (revenue, employees, market presence)
-   Geographic reach and market focus
-   Key executives and leadership

#### Product/Service Analysis
-   Core offerings and features
-   Pricing models and strategies
-   Target customer segments
-   Unique value propositions
-   Recent product launches or updates

#### Market Position
-   Market share and positioning
-   Competitive advantages
-   Brand perception and reputation
-   Customer satisfaction and reviews

#### Business Model
-   Revenue streams and business model
-   Distribution channels and partnerships
-   Go-to-market strategy
-   Customer acquisition approach

#### Strategic Initiatives
-   Recent news and announcements
-   Funding rounds or financial performance
-   Partnerships and acquisitions
-   Expansion plans or new market entries

### Step 5: Comparative Analysis Framework
Create a structured comparison across key dimensions:

#### Product/Feature Comparison
-   Feature matrix comparing core functionalities
-   Strengths and weaknesses of each offering
-   Differentiation factors
-   Gap analysis

#### Pricing Comparison
-   Price points and pricing structures
-   Value proposition per price tier
-   Competitive positioning on price

#### Market Reach Comparison
-   Geographic presence
-   Customer segment focus
-   Market penetration levels

#### Innovation Comparison
-   R&D investment and focus areas
-   Recent innovations and product updates
-   Technology advantages or disadvantages

### Step 6: SWOT Analysis for Each Competitor
Perform a SWOT (Strengths, Weaknesses, Opportunities, Threats) analysis for each competitor:

#### Strengths
-   Core competencies and advantages
-   Market position and brand strength
-   Financial stability and resources

#### Weaknesses
-   Limitations and vulnerabilities
-   Market gaps or blind spots
-   Resource constraints

#### Opportunities
-   Market expansion possibilities
-   Emerging trends they can capitalize on
-   Partnership or acquisition opportunities

#### Threats
-   Competitive pressures
-   Market disruptions
-   Regulatory or economic challenges

### Step 7: Competitive Positioning Map
Create a visual representation of competitive positioning:
-   Plot competitors on a 2x2 matrix based on key differentiating factors
-   Identify market leaders, challengers, niche players, and followers
-   Highlight positioning gaps and opportunities

### Step 8: Market Trend Analysis
-   Identify current market trends affecting competition
-   Analyze how each competitor is responding to trends
-   Predict future competitive dynamics
-   Assess potential market disruptions

### Step 9: Competitive Intelligence Summary
Generate insights and recommendations:

#### Key Findings
-   Most competitive aspects of the market
-   Clear winners and laggards in different categories
-   Emerging competitive threats
-   Market evolution patterns

#### Strategic Implications
-   How this analysis should inform product strategy
-   Areas for competitive differentiation
-   Potential market opportunities
-   Risk mitigation strategies

### Step 10: Competitor Comparison Report Generation
Produce a markdown report with the following structure:

---
# Competitor Comparison Analysis: [Market Topic]

## Executive Summary
*A high-level overview of key competitive insights and market dynamics*

## Analysis Context
- **Market Topic:** [Market or product domain]
- **Analysis Date:** [Current date]
- **Competitors Analyzed:** [List of companies]
- **Research Sources:** [Primary sources used]

## Market Landscape Overview
- **Market Size:** [Estimated market size and growth]
- **Key Segments:** [Major market segments identified]
- **Growth Trends:** [Current market growth patterns]
- **Regulatory Environment:** [Relevant regulations or changes]

## Competitor Profiles

### [Competitor 1 Name]
#### Company Overview
- **Founded:** [Year]
- **Headquarters:** [Location]
- **Employees:** [Number]
- **Revenue:** [Most recent figures]

#### Product/Service Offering
- **Core Product:** [Main offering]
- **Key Features:** [Differentiating features]
- **Target Market:** [Primary customer segments]
- **Pricing:** [Price range or model]

#### Market Position
- **Market Share:** [Estimated share if available]
- **Brand Recognition:** [Perception in market]
- **Customer Satisfaction:** [Review scores or feedback]

#### Recent Developments
- **News:** [Recent announcements or launches]
- **Partnerships:** [Key partnerships or integrations]
- **Funding:** [Recent funding rounds if applicable]

### [Competitor 2 Name]
[Repeat structure for each competitor]

## Comparative Analysis

### Feature Comparison Matrix
| Feature | [Competitor 1] | [Competitor 2] | [Competitor 3] | [Your Product] |
|---------|----------------|----------------|----------------|----------------|
| [Feature 1] | [Rating/Simple] | [Rating/Simple] | [Rating/Simple] | [Rating/Simple] |
| [Feature 2] | [Rating/Simple] | [Rating/Simple] | [Rating/Simple] | [Rating/Simple] |

### Pricing Analysis
- **Entry Level:** [Price comparison]
- **Mid-tier:** [Price comparison]
- **Enterprise:** [Price comparison]
- **Value Proposition:** [Analysis of price vs. features]

### Market Positioning
- **Leaders:** [Companies leading in market]
- **Challengers:** [Companies actively competing]
- **Niche Players:** [Specialized companies]
- **Followers:** [Companies copying market leaders]

## SWOT Analysis

### [Competitor 1 Name]
#### Strengths
1. **[Strength]:** [Description]
2. **[Strength]:** [Description]

#### Weaknesses
1. **[Weakness]:** [Description]
2. **[Weakness]:** [Description]

#### Opportunities
1. **[Opportunity]:** [Description]
2. **[Opportunity]:** [Description]

#### Threats
1. **[Threat]:** [Description]
2. **[Threat]:** [Description]

[Repeat for each competitor]

## Competitive Positioning Map
```
[Text-based representation of 2x2 positioning matrix]
Y-Axis: [Differentiating factor 1]
X-Axis: [Differentiating factor 2]

[Competitor 1]: [Position description]
[Competitor 2]: [Position description]
[Competitor 3]: [Position description]
[Your Position]: [Position description]
```

## Market Trends and Future Outlook
- **Current Trends:** [Major trends affecting competition]
- **Competitor Responses:** [How competitors are adapting]
- **Future Predictions:** [Expected market evolution]
- **Disruption Potential:** [Likely disruptions or changes]

## Strategic Recommendations

### Competitive Advantages to Emulate
1. **[Recommendation]:** [What to learn from competitors]
2. **[Recommendation]:** [What to learn from competitors]

### Differentiation Opportunities
1. **[Opportunity]:** [How to differentiate]
2. **[Opportunity]:** [How to differentiate]

### Market Entry/Expansion Strategies
1. **[Strategy]:** [Recommended approach]
2. **[Strategy]:** [Recommended approach]

## Data Sources and Methodology
- **Research Methods:** [How data was collected]
- **Sources:** [List of sources consulted]
- **Limitations:** [Known limitations of the analysis]
- **Confidence Level:** [Assessment of data reliability]

---

### Step 11: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[market_topic_slug]-competitor-comparison-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 12: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the competitor comparison analysis for **<market_topic>**."
- Provide the path to the file: "You can view the detailed report here: `niopd-workspace/reports/[YYYYMMDD]-[market_topic_slug]-competitor-comparison-v[version].md`"
- Suggest next steps: "Consider using `/niopd:MR:positioning` for market positioning analysis or `/niopd:MR:trends` for broader market trend research."

## Error Handling
- **Missing Topic:** If no market topic is provided, ask the user to specify one.
- **Research Limitations:** If sufficient data cannot be found, explain the limitations and suggest alternative approaches.
- **Competitor Identification Issues:** If competitors cannot be clearly identified, provide the market research findings and ask for user input.
- **Web Search Errors:** If web search capabilities are unavailable, inform the user and suggest manual research or using existing data.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.