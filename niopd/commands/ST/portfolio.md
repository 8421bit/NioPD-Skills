---
argument-hint: [--organization=<org_name>] [--method=<analysis_method>]
description: Conducts comprehensive product portfolio analysis to optimize strategic decision-making.
---

# Command: /niopd:ST:portfolio

This command conducts a comprehensive product portfolio analysis to evaluate the strategic positioning, performance, and potential of products within an organization's portfolio.

## Theoretical Foundation

### Origin and Development
Product portfolio management emerged from financial portfolio theory. The **BCG Matrix** (Boston Consulting Group Growth-Share Matrix) was pioneered by **Bruce Henderson** in 1970, revolutionizing strategic product management. The **GE-McKinsey Matrix** was developed later in the 1970s as a more sophisticated alternative.

### Core Principle
Portfolio analysis provides a **strategic framework for allocating resources** across multiple products by evaluating their relative performance, market position, and growth potential. The goal is to create a balanced portfolio that maximizes overall organizational value.

### BCG Matrix (Default Framework)

**Four Quadrants**:
1. **Stars** (High Growth, High Share): Invest to maintain leadership
   - High resource consumption
   - Future cash cows
   - Require sustained investment

2. **Cash Cows** (Low Growth, High Share): Harvest for profits
   - Generate excess cash
   - Fund Stars and Question Marks
   - Require minimal investment

3. **Question Marks/Problem Children** (High Growth, Low Share): Selective investment
   - High resource consumption
   - Uncertain future
   - Invest to become Stars or divest

4. **Dogs** (Low Growth, Low Share): Divest or harvest
   - Low profitability
   - Resource drain
   - Consider exit strategies

### GE-McKinsey 9-Box Matrix
A more nuanced approach using:
- **Y-Axis**: Industry Attractiveness (market growth, profitability, size)
- **X-Axis**: Business Strength (market share, capabilities, brand)
- **Three Categories**: Invest/Grow, Selectivity/Earnings, Harvest/Divest

### When to Use
- Annual strategic planning cycles
- Resource allocation decisions
- M&A evaluation
- Product rationalization
- Portfolio optimization
- Investment prioritization

### Related Frameworks
- **Ansoff Matrix**: Market/product growth strategies
- **Product Life Cycle**: Introduction, growth, maturity, decline stages
- **SWOT Analysis**: Individual product evaluation
- **Strategic Fit Analysis**: Synergy and coherence assessment

### Best Practices
- Use multiple frameworks for comprehensive analysis
- Consider qualitative factors beyond financial metrics
- Regularly update analysis as markets evolve
- Balance short-term profits with long-term growth

## Usage
`/niopd:ST:portfolio [--organization=<org_name>] [--method=<analysis_method>]`

## Preflight Checklist

1.  **Validate Inputs:**
    -   Check if `--organization` argument is provided to specify the company or business unit.
    -   If `--organization` is not provided, ask the user to specify the organization.
    -   Check if `--method` argument is provided to specify the analysis approach.
    -   If `--method` is not provided, default to the BCG Matrix approach.

## Instructions

You are a specialized AI expert in product portfolio management and strategic analysis. Your goal is to conduct a thorough portfolio analysis that provides actionable insights for product investment, development, and divestment decisions.

### Step 1: Acknowledge and Gather Context
-   Acknowledge the request: "I'll conduct a product portfolio analysis for **<organization_name>**."
-   If a specific organization is provided with `--organization`, use that as the focus.
-   If not provided, ask the user: "Which organization's product portfolio would you like me to analyze?"
-   If an analysis method is provided with `--method`, use that approach.
-   If not provided, default to the BCG Matrix method and inform the user.

### Step 2: Portfolio Identification and Scope Definition
-   Identify all products in the portfolio:
    -   Current products and services
    -   Products in development
    -   Recently discontinued products (for context)
    -   Acquired or partnered products
-   Define the scope of analysis:
    -   Business units or divisions
    -   Product categories or lines
    -   Geographic markets
    -   Customer segments
-   Establish analysis criteria and timeframes

### Step 3: Analysis Method Selection
Available analysis methods include:
1.  **BCG Matrix** - Growth-share matrix categorization
2.  **GE-McKinsey Matrix** - Industry attractiveness/business strength matrix
3.  **Ansoff Matrix** - Market penetration/growth strategies
4.  **Product Life Cycle Analysis** - Introduction to decline stages
5.  **Portfolio Balance Analysis** - Risk and return optimization

#### Default: BCG Matrix Approach
-   **X-Axis:** Market Growth Rate (Low to High)
-   **Y-Axis:** Relative Market Share (Low to High)
-   **Quadrants:** Stars, Cash Cows, Question Marks, Dogs

### Step 4: Data Collection and Research
-   Gather quantitative data for each product:
    -   Revenue and profitability figures
    -   Market share and growth rates
    -   Investment levels and resource allocation
    -   Customer metrics and satisfaction scores
    -   Competitive positioning data
-   Collect qualitative information:
    -   Strategic importance and alignment
    -   Innovation potential and differentiation
    -   Risk factors and dependencies
    -   Synergies with other products
-   Research market and industry context

### Step 5: Financial Performance Analysis
-   Analyze financial metrics for each product:
    -   Revenue trends and growth rates
    -   Profitability margins (gross, operating, net)
    -   Return on Investment (ROI)
    -   Cash flow generation and requirements
    -   Cost structure and efficiency
-   Compare performance against benchmarks:
    -   Industry averages
    -   Internal targets
    -   Competitor performance
-   Identify financial outliers and patterns

### Step 6: Market Position Assessment
-   Evaluate market dynamics for each product:
    -   Market size and growth potential
    -   Competitive landscape and positioning
    -   Customer demand and satisfaction
    -   Market trends and disruptions
-   Assess relative competitive position:
    -   Market share compared to competitors
    -   Brand strength and recognition
    -   Customer loyalty and retention
    -   Distribution and channel effectiveness

### Step 7: Strategic Importance Evaluation
-   Determine strategic value of each product:
    -   Alignment with corporate strategy
    -   Contribution to core competencies
    -   Enabling capabilities for other products
    -   Innovation and learning potential
-   Assess portfolio balance:
    -   Risk diversification
    -   Resource allocation efficiency
    -   Synergy opportunities
    -   Strategic fit and coherence

### Step 8: Portfolio Matrix Positioning
Position each product in the selected analysis framework:

#### BCG Matrix Positioning
-   **Stars:** High growth, high market share
-   **Cash Cows:** Low growth, high market share
-   **Question Marks:** High growth, low market share
-   **Dogs:** Low growth, low market share

#### GE-McKinsey Matrix Positioning
-   **High Attractiveness/High Strength:** Invest and grow
-   **High Attractiveness/Medium Strength:** Selective investment
-   **High Attractiveness/Low Strength:** Harvest or divest
-   **Medium Attractiveness/High Strength:** Manage for earnings
-   **Medium Attractiveness/Medium Strength:** Maintain position
-   **Medium Attractiveness/Low Strength:** Divest
-   **Low Attractiveness/High Strength:** Harvest for cash
-   **Low Attractiveness/Medium Strength:** Divest or harvest
-   **Low Attractiveness/Low Strength:** Exit quickly

### Step 9: Portfolio Gap Analysis
-   Identify portfolio gaps and imbalances:
    -   Overconcentration in certain quadrants
    -   Missing opportunities in attractive markets
    -   Resource allocation mismatches
    -   Risk concentration issues
-   Evaluate portfolio completeness:
    -   Market coverage adequacy
    -   Customer segment representation
    -   Technology and capability balance
    -   Geographic diversification

### Step 10: Strategic Recommendations
Based on the portfolio analysis, develop specific strategic recommendations:

#### Product Investment Strategies
1.  **Build:** Increase investment in high-potential products
2.  **Hold:** Maintain current investment levels
3.  **Harvest:** Focus on short-term cash generation
4.  **Divest:** Exit or sell underperforming products

#### Portfolio Optimization Initiatives
1.  **[Initiative]:** [Action, rationale, and expected outcome]
2.  **[Initiative]:** [Action, rationale, and expected outcome]

### Step 11: Resource Allocation Framework
-   Develop resource allocation recommendations:
    -   Budget distribution across products
    -   Personnel and talent allocation
    -   Technology and infrastructure investment
    -   Marketing and sales resource assignment
-   Create prioritization frameworks:
    -   Investment priority rankings
    -   Risk-adjusted return assessments
    -   Strategic value scoring models

### Step 12: Implementation Roadmap
-   Define implementation phases:
    -   Immediate actions (0-6 months)
    -   Medium-term initiatives (6-18 months)
    -   Long-term strategic moves (18+ months)
-   Identify resource requirements:
    -   Financial investments needed
    -   Personnel and skill requirements
    -   Technology and infrastructure needs
-   Establish success metrics:
    -   Portfolio performance indicators
    -   Individual product metrics
    -   Strategic alignment measures

### Step 13: Risk Assessment and Mitigation
-   Identify portfolio-level risks:
    -   Market volatility and disruption risks
    -   Competitive response risks
    -   Resource constraint risks
    -   Dependency and concentration risks
-   Develop risk mitigation strategies:
    -   Diversification approaches
    -   Contingency planning
    -   Early warning systems
    -   Risk monitoring frameworks

### Step 14: Product Portfolio Analysis Report Generation
Produce a markdown report with the following structure:

---
# Product Portfolio Analysis: [Organization Name]

## Executive Summary
*A high-level overview of portfolio findings and strategic recommendations*

## Analysis Context
- **Organization:** [Company or business unit analyzed]
- **Analysis Method:** [BCG Matrix, GE-McKinsey, or other]
- **Analysis Date:** [Current date]
- **Portfolio Scope:** [Products and business units included]
- **Time Period:** [Historical data period analyzed]

## Portfolio Overview
### Product Inventory
| Product Name | Category | Revenue (Latest) | Profitability | Market Share | Life Cycle Stage |
|--------------|----------|------------------|---------------|--------------|------------------|
| [Product 1] | [Category] | [Amount] | [Percentage] | [Share] | [Stage] |
| [Product 2] | [Category] | [Amount] | [Percentage] | [Share] | [Stage] |

### Portfolio Financial Summary
- **Total Portfolio Revenue:** [Amount and growth rate]
- **Overall Profitability:** [Margin percentage]
- **Cash Generation:** [Net cash flow]
- **Investment Requirements:** [Capital needed]

## Portfolio Analysis Results

### [Selected Method] Matrix
```
[Text-based representation of the selected analysis matrix]
[Position each product in the appropriate quadrant/cell]
[Include axis labels and quadrant names]
```

### Product Categorization
#### [Quadrant/Category Name]
- **[Product Name]:** [Brief description and strategic position]
- **Performance Metrics:** [Key financial and market data]
- **Strategic Implications:** [What the position means]

#### [Quadrant/Category Name]
- **[Product Name]:** [Brief description and strategic position]
- **Performance Metrics:** [Key financial and market data]
- **Strategic Implications:** [What the position means]

## Detailed Product Assessments

### [Product Name]
#### Financial Performance
- **Revenue Trend:** [3-year trend and growth rate]
- **Profitability:** [Margins and profitability analysis]
- **ROI:** [Return on investment metrics]
- **Cash Flow:** [Generation or consumption]

#### Market Position
- **Market Share:** [Relative position vs. competitors]
- **Growth Rate:** [Market and product growth]
- **Competitive Position:** [Strengths and weaknesses]
- **Customer Metrics:** [Satisfaction, loyalty, retention]

#### Strategic Assessment
- **Strategic Fit:** [Alignment with corporate strategy]
- **Synergies:** [Value creation with other products]
- **Innovation Potential:** [Future development opportunities]
- **Risk Profile:** [Key risks and vulnerabilities]

## Portfolio Insights

### Strengths
1. **[Strength]:** [Description and strategic value]
2. **[Strength]:** [Description and strategic value]

### Weaknesses
1. **[Weakness]:** [Description and strategic impact]
2. **[Weakness]:** [Description and strategic impact]

### Opportunities
1. **[Opportunity]:** [Description and potential value]
2. **[Opportunity]:** [Description and potential value]

### Threats
1. **[Threat]:** [Description and potential impact]
2. **[Threat]:** [Description and potential impact]

## Strategic Recommendations

### Product Strategies
#### Build Investments
1. **[Product]:** [Investment rationale and approach]
2. **[Product]:** [Investment rationale and approach]

#### Hold Positions
1. **[Product]:** [Maintenance strategy and rationale]
2. **[Product]:** [Maintenance strategy and rationale]

#### Harvest for Cash
1. **[Product]:** [Harvesting approach and timeline]
2. **[Product]:** [Harvesting approach and timeline]

#### Divest Considerations
1. **[Product]:** [Exit strategy and rationale]
2. **[Product]:** [Exit strategy and rationale]

### Portfolio Optimization Initiatives
1. **[Initiative]:** [Action, rationale, and expected outcome]
2. **[Initiative]:** [Action, rationale, and expected outcome]

## Resource Allocation Framework

### Investment Priorities
| Priority | Product/Initiative | Investment Required | Expected ROI | Timeline |
|----------|-------------------|---------------------|--------------|----------|
| 1 | [Product/Initiative] | [Amount] | [Percentage] | [Timeline] |
| 2 | [Product/Initiative] | [Amount] | [Percentage] | [Timeline] |

### Resource Distribution
- **R&D Investment:** [Percentage allocation by product category]
- **Marketing Budget:** [Distribution across products]
- **Sales Resources:** [Allocation by product and market]
- **Support Functions:** [Shared services and overhead]

## Implementation Roadmap

### Phase 1: Immediate Actions (0-6 months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, tools]
- **Success Metrics:** [How to measure progress]

### Phase 2: Medium-term Initiatives (6-18 months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, tools]
- **Success Metrics:** [How to measure progress]

### Phase 3: Long-term Strategic Moves (18+ months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, tools]
- **Success Metrics:** [How to measure progress]

## Risk Assessment
### High-Priority Risks
1. **[Risk]:** [Description and likelihood]
   - **Impact:** [Potential consequences]
   - **Mitigation Strategy:** [How to address or reduce risk]

2. **[Risk]:** [Description and likelihood]
   - **Impact:** [Potential consequences]
   - **Mitigation Strategy:** [How to address or reduce risk]

## Monitoring and Review Framework
### Key Performance Indicators
- **Portfolio Metrics:** [Overall portfolio performance measures]
- **Product Metrics:** [Individual product success indicators]
- **Financial Metrics:** [Revenue, profitability, cash flow targets]
- **Strategic Metrics:** [Alignment and value creation measures]

### Review Schedule
- **Monthly:** [Quick pulse checks and updates]
- **Quarterly:** [Comprehensive performance reviews]
- **Annually:** [Strategic portfolio assessments]

## Data Sources and Methodology
- **Research Methods:** [How the analysis was conducted]
- **Sources:** [List of sources consulted]
- **Limitations:** [Known limitations of the analysis]
- **Assumptions:** [Key assumptions made in the analysis]

---

### Step 13: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[organization_slug]-portfolio-analysis-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 14: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the product portfolio analysis for **<organization_name>**."
- Provide the path to the file: "You can view the detailed portfolio analysis here: `niopd-workspace/reports/[YYYYMMDD]-[organization_slug]-portfolio-analysis-v[version].md`"
- Suggest next steps: "Consider using `/niopd:ST:swot` for strategic analysis or `/niopd:ST:canvas` for business model evaluation."

## Error Handling
- **Missing Organization:** If no organization is specified, ask the user to clarify which portfolio to analyze.
- **Method Issues:** If an invalid analysis method is specified, list available options and ask for selection.
- **Insufficient Data:** If adequate product information cannot be found, explain the limitations and suggest focusing on available products.
- **Research Limitations:** If web search capabilities are unavailable, inform the user and recommend manual research or using existing data.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.