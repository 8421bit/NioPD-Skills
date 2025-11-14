---
argument-hint: [--market=<market_name>] [--product=<product_name>] [--analysis=<analysis_type>]
description: Analyzes market gaps and opportunities to identify potential growth areas and strategic initiatives.
---

# Command: /niopd:BS:market-opportunity

This command analyzes market gaps and opportunities to identify potential growth areas and strategic initiatives.

## Theoretical Foundation

### Origin and Development
Market opportunity analysis combines multiple strategic frameworks:

1. **Market Gap Analysis** - Identifying unmet needs and underserved segments in competitive markets
2. **Opportunity Assessment** - Multi-criteria evaluation frameworks from strategic management theory
3. **Growth Strategy** - Based on **Ansoff's Growth Matrix** (Igor Ansoff, 1957): Market Penetration, Market Development, Product Development, Diversification

### Core Principle
The fundamental approach is **systematic opportunity discovery**: Rather than relying on intuition alone, this method uses structured analysis to identify, evaluate, and prioritize market opportunities based on objective criteria.

### The Opportunity Assessment Framework
Opportunities are evaluated across three dimensions:

1. **Attractiveness** (Market-focused)
   - Market size and growth potential
   - Profitability and revenue potential
   - Customer willingness to pay

2. **Feasibility** (Capability-focused)
   - Technical capability and resources
   - Time to market
   - Required investment vs. available resources

3. **Strategic Fit** (Alignment-focused)
   - Alignment with company vision and goals
   - Competitive advantage potential
   - Core competency leverage

### Scoring Methodology
- Each dimension rated 1-5
- Composite score = (Attractiveness + Feasibility + Strategic Fit) / 3
- Higher scores indicate higher-priority opportunities

### Types of Market Opportunities
1. **New Customer Segments**: Underserved demographics or psychographics
2. **Geographic Expansion**: New regions or markets
3. **Product Extensions**: Adjacent products or features
4. **New Business Models**: Alternative monetization or delivery
5. **Emerging Trends**: Technology or behavior shifts creating new needs

### When to Use
- Exploring growth strategies for existing products
- Identifying white space in competitive markets
- Prioritizing among multiple potential initiatives
- Validating strategic hypotheses about market gaps
- Preparing for strategic planning sessions

### Related Frameworks
- **Blue Ocean Strategy**: Creating uncontested market space (Kim & Mauborgne, 2005)
- **Jobs to Be Done (JTBD)**: Understanding customer needs (Clayton Christensen)
- **TAM/SAM/SOM Analysis**: Market sizing framework
- **Porter's Five Forces**: Industry competitive analysis (Michael Porter, 1979)
- **Value Proposition Canvas**: Customer-value fit (Alexander Osterwalder)

### Complementary NioPD Commands
- `/niopd:ST:swot` - Analyze strengths, weaknesses, opportunities, threats
- `/niopd:MR:trends` - Research market trends and dynamics
- `/niopd:UR:personas` - Understand target customer segments
- `/niopd:BS:new-initiative` - Create initiative from identified opportunity

## Usage
`/niopd:BS:market-opportunity [--market=<market_name>] [--product=<product_name>] [--analysis=<analysis_type>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Market Context:**
    -   If the `--market` argument is not provided, prompt the user to specify the market context.
    -   Confirm that the market context is valid and meaningful.

3.  **Validate Product Context:**
    -   If the `--product` argument is not provided, prompt the user to specify the product context.
    -   Confirm that the product context is valid and meaningful.

4.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/reports` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in market analysis and opportunity identification. Your goal is to help users analyze market gaps and opportunities to identify potential growth areas and strategic initiatives.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Data
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request with a message in the user's preferred language:
    -   If Chinese: "我将帮您分析 **<product_name>** 在 **<market_name>** 市场中的市场机会。"
    -   If English: "I'll help you analyze market opportunities for **<product_name>** in the **<market_name>** market."
    -   For other languages, use an appropriate translation based on user's language preference
-   If the `--market` argument wasn't provided, ask the user in their preferred language: "What market context would you like to analyze for opportunities?" and wait for their response.
-   If the `--product` argument wasn't provided, ask the user in their preferred language: "What product or service would you like to focus on?" and wait for their response.
-   If the `--analysis` argument wasn't provided, ask the user in their preferred language: "What type of market opportunity analysis would you prefer to conduct?" and wait for their response.

### Step 2: Market Context Analysis
-   Help the user define the market context:
    -   "What is the current size and growth rate of the **<market_name>** market?"
    -   "Who are the key players in this market?"
    -   "What are the major trends shaping this market?"
    -   "What are the key challenges in this market?"
-   Wait for the user's responses.

### Step 3: Product Context Analysis
-   Guide the user through analyzing the product context:
    -   "What is the current positioning of **<product_name>** in the market?"
    -   "What are the key features and benefits of **<product_name>**?"
    -   "What are the strengths and weaknesses of **<product_name>**?"
    -   "How does **<product_name>** compare to key competitors?"
-   Wait for the user's responses.

### Step 4: Market Gap Identification
-   Help the user identify market gaps:
    -   "What unmet needs exist in the **<market_name>** market?"
    -   "What pain points do customers currently experience?"
    -   "What underserved customer segments exist?"
    -   "What emerging trends are creating new opportunities?"
-   Wait for the user's responses.

### Step 5: Opportunity Assessment Framework
-   Explain the opportunity assessment framework to the user:
    -   "We'll assess each opportunity by attractiveness, feasibility, and strategic fit."
    -   "Attractiveness factors include market size, growth potential, and profitability."
    -   "Feasibility factors include technical capability, resources, and time to market."
    -   "Strategic fit factors include alignment with company goals and competitive advantage."
-   Ask the user: "Do you understand this framework, or would you like me to explain any part in more detail?" and wait for their response.

### Step 6: Opportunity Generation
-   Guide the user through generating market opportunities:
    -   "Based on our analysis, what market opportunities can we identify for **<product_name>**?"
    -   "Let's consider opportunities in new customer segments, geographic expansion, product extensions, and new business models."
-   Wait for the user's responses.

### Step 7: Opportunity Evaluation
-   Help the user evaluate each identified opportunity:
    -   For each opportunity, ask: "How attractive is this opportunity? (1-5)"
    -   For each opportunity, ask: "How feasible is this opportunity? (1-5)"
    -   For each opportunity, ask: "How well does this opportunity fit our strategy? (1-5)"
    -   Calculate a composite score for each opportunity.
-   Wait for the user's responses.

### Step 8: Opportunity Prioritization
-   Guide the user through prioritizing opportunities:
    -   "Based on our evaluation, which opportunities should we prioritize?"
    -   "Let's consider high attractiveness, high feasibility, and strong strategic fit opportunities first."
-   Wait for the user's responses.

### Step 9: Strategic Recommendations
-   Help the user develop strategic recommendations:
    -   "What specific actions should we take to pursue the prioritized opportunities?"
    -   "What resources will be needed to implement these recommendations?"
    -   "What is the expected timeline for implementation?"
    -   "What are the key success factors for each recommendation?"
-   Wait for the user's responses.

### Step 10: Risk Assessment
-   Guide the user through assessing risks:
    -   "What are the key risks associated with pursuing these opportunities?"
    -   "What are the potential market, technical, and execution risks?"
    -   "How can we mitigate these risks?"
-   Wait for the user's responses.

### Step 11: Create Market Opportunity Analysis Report
Produce a markdown report with the following structure:

---
# Market Opportunity Analysis Report: [Product Name] in [Market Name]

## Executive Summary
*A brief overview of key market opportunities and strategic recommendations*

## Market Context
### Market Size and Growth
[Market size and growth information from Step 2]

### Key Players
[Key players identified in Step 2]

### Market Trends
[Market trends identified in Step 2]

### Market Challenges
[Market challenges identified in Step 2]

## Product Context
### Current Positioning
[Current positioning from Step 3]

### Key Features and Benefits
[Key features and benefits from Step 3]

### Strengths and Weaknesses
[Strengths and weaknesses from Step 3]

### Competitive Comparison
[Competitive comparison from Step 3]

## Market Gaps
### Unmet Needs
[Unmet needs identified in Step 4]

### Customer Pain Points
[Customer pain points identified in Step 4]

### Underserved Segments
[Underserved segments identified in Step 4]

### Emerging Trends
[Emerging trends identified in Step 4]

## Identified Opportunities
### Opportunity 1
- **Description:** [Opportunity description]
- **Attractiveness Score:** [Score from Step 7]
- **Feasibility Score:** [Score from Step 7]
- **Strategic Fit Score:** [Score from Step 7]
- **Composite Score:** [Composite score]

### Opportunity 2
- **Description:** [Opportunity description]
- **Attractiveness Score:** [Score from Step 7]
- **Feasibility Score:** [Score from Step 7]
- **Strategic Fit Score:** [Score from Step 7]
- **Composite Score:** [Composite score]

## Strategic Recommendations
### Recommendation 1
- **Action:** [Specific action]
- **Resources Needed:** [Resources required]
- **Timeline:** [Expected timeline]
- **Success Factors:** [Key success factors]

### Recommendation 2
- **Action:** [Specific action]
- **Resources Needed:** [Resources required]
- **Timeline:** [Expected timeline]
- **Success Factors:** [Key success factors]

## Risk Assessment
### Key Risks
[Risks identified in Step 10]

### Mitigation Strategies
[Mitigation strategies identified in Step 10]

---

### Step 12: Save the Report
- Generate a filename for the market opportunity analysis report following the NioPD naming convention: `[YYYYMMDD]-[product_slug]-market-opportunity-v[version].md`.
- Save the market opportunity analysis report to: `niopd-workspace/reports/[filename]`

### Step 13: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the market opportunity analysis for **<product_name>** in the **<market_name>** market."
- Provide the path to the file: "You can view the detailed market opportunity analysis report at: `niopd-workspace/sources/[YYYYMMDD]-[product_slug]-market-opportunity-v[version].md`"
- Suggest next steps: "Consider using `/niopd:BS:market-opportunity` to update this analysis as market conditions change, or `/niopd:BS:new-initiative` to create a new product initiative based on these opportunities."

## Error Handling
- **Configuration File Errors:** If there are issues reading or parsing configuration files, inform the user in their preferred language and continue with default settings.
- **Missing Market Context:** If no market context is specified, explain that market context is required and ask for it.
- **Missing Product Context:** If no product context is specified, explain that product context is required and ask for it.
- **Incomplete Opportunity Evaluation:** If the user doesn't provide sufficient information for opportunity evaluation, explain what's needed and offer to proceed with partial analysis.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial market opportunity analysis can still provide value.