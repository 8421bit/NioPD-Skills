---
argument-hint: [--product=<product_name>] [--competitors=<competitor_list>] [--analysis=<analysis_type>]
description: Analyzes competitive landscape to identify market positioning and differentiation opportunities.
---

# Command: /niopd:MR:compare-products

This command analyzes the competitive landscape to identify market positioning and differentiation opportunities.

## Theoretical Foundation

### Origin and Development
Product comparison analysis synthesizes multiple competitive analysis frameworks:

1. **Competitive Positioning Analysis** - Understanding relative market positions
2. **Feature Parity Analysis** - Systematic capability comparison
3. **Strategic Group Mapping** - Clustering competitors by strategy (Michael Porter)

### Core Principle
The fundamental approach is **systematic competitive benchmarking**: Evaluating your product against competitors across multiple dimensions (features, pricing, positioning, market reach) to identify competitive advantages, gaps, and opportunities for differentiation.

### Comparison Framework
1. **Product Capabilities**: Feature-by-feature comparison
2. **Pricing & Value**: Economic positioning analysis
3. **Market Positioning**: Brand perception and target segments
4. **Go-to-Market**: Distribution and customer acquisition strategies
5. **Innovation**: Product development and technological advancement

### Analytical Outputs
- **Competitive Positioning Map**: 2x2 matrix showing market positions
- **Feature Comparison Matrix**: Detailed capability grid
- **SWOT per Competitor**: Strategic assessment for each player
- **Differentiation Opportunities**: Gaps and white space identification

### When to Use
- Product planning and feature prioritization
- Market positioning and messaging development
- Competitive response strategies
- Investment and resource allocation decisions
- Pre-launch competitive intelligence

### Related Frameworks
- **Kano Model**: Feature categorization (must-haves vs. delighters)
- **Value Curve Analysis**: Visual comparison of value factors (Blue Ocean Strategy)
- **Conjoint Analysis**: Feature-price trade-off research

## Usage
`/niopd:MR:compare-products [--product=<product_name>] [--competitors=<competitor_list>] [--analysis=<analysis_type>]`

## Preflight Checklist

1.  **Validate Inputs:**
    -   Check if `--product` argument is provided for the product name.
    -   If `--product` is not provided, ask the user to specify the product.
    -   Check if `--competitors` argument is provided for the competitor list.
    -   Check if `--analysis` argument is provided for the analysis type.

## Instructions

You are a specialized AI expert in market research and competitive analysis. Your goal is to analyze the competitive landscape to identify market positioning and differentiation opportunities.

### Step 1: Acknowledge and Gather Context
-   Acknowledge the request: "I'll analyze the competitive landscape for **<product_name>** to identify market positioning and differentiation opportunities."
-   If a product name is provided with `--product`, use that as the focus.
-   If not provided, ask the user: "Which product would you like to analyze?" and wait for their response.
-   If competitors are provided with `--competitors`, use that list.
-   If not provided, indicate that you'll identify key competitors automatically.
-   If analysis type is provided with `--analysis`, use that approach.
-   If not provided, default to comprehensive competitive analysis.

### Step 2: Market Research and Competitor Identification
-   Use web search capabilities to research the product market:
    -   Identify the overall market size and growth trends
    -   Determine key market segments and niches
    -   Understand the competitive landscape and major players
    -   Identify emerging trends and market shifts
-   If specific competitors were not provided, automatically identify key competitors:
    -   Search for major players in the market space
    -   Identify direct competitors (similar products/services)
    -   Include both established players and emerging competitors
    -   Select 3-5 most relevant competitors for detailed analysis

### Step 3: Competitor Deep Dive Analysis
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

### Step 4: Comparative Analysis Framework
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

### Step 5: SWOT Analysis for Each Competitor
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

### Step 6: Competitive Positioning Map
Create a visual representation of competitive positioning:
-   Plot competitors on a 2x2 matrix based on key differentiating factors
-   Identify market leaders, challengers, niche players, and followers
-   Highlight positioning gaps and opportunities

### Step 7: Market Trend Analysis
-   Identify current market trends affecting competition
-   Analyze how each competitor is responding to trends
-   Predict future competitive dynamics
-   Assess potential market disruptions

### Step 8: Competitive Intelligence Summary
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

### Step 9: Competitor Comparison Report Generation
Produce a markdown report with the following structure:

---
# Competitive Analysis: [Product Name]

## Executive Summary
*A high-level overview of key competitive insights and market dynamics*

## Analysis Context
- **Product:** [Product name]
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

### Step 10: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[product_slug]-competitive-analysis-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 11: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the competitive analysis for **<product_name>**."
- Provide the path to the file: "You can view the detailed report here: `niopd-workspace/reports/[YYYYMMDD]-[product_slug]-competitive-analysis-v[version].md`"
- Suggest next steps: "Consider using `/niopd:MR:positioning` for market positioning analysis or `/niopd:MR:trends` for broader market trend research."

## Error Handling
- **Missing Product:** If no product is specified for analysis, ask the user to clarify what they want to analyze.
- **Research Limitations:** If sufficient data cannot be found, explain the limitations and suggest alternative approaches.
- **Competitor Identification Issues:** If competitors cannot be clearly identified, provide the market research findings and ask for user input.
- **Web Search Errors:** If web search capabilities are unavailable, inform the user and suggest manual research or using existing data.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.