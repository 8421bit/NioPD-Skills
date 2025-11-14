---
argument-hint: --topic="<Your research topic>"
description: Researches market trends for a given topic.
---

# Command: /niopd:MR:trends

This command researches market trends for a given topic by conducting comprehensive web research and producing a detailed market analysis report.

## Theoretical Foundation

### Origin and Development
Market trend analysis combines elements from:

1. **Environmental Scanning** - Systematic monitoring of external environment (Francis Aguilar, 1967)
2. **Trend Forecasting** - Identifying and projecting patterns of change
3. **Competitive Intelligence** - Systematic collection and analysis of market information

### Core Principle
The fundamental approach is **systematic environmental monitoring**: Rather than reactive observation, proactive research identifies emerging patterns, shifts, and signals that indicate future market direction, enabling anticipatory strategy.

### Trend Categories

**1. Mega Trends**:
- Long-term, global shifts (10-30 years)
- Examples: Demographic changes, climate change, urbanization
- High impact, slow-moving, high certainty

**2. Macro Trends**:
- Industry-wide shifts (5-10 years)
- Examples: Digital transformation, sustainability focus
- Moderate speed, moderate certainty

**3. Micro Trends**:
- Niche or emerging patterns (1-5 years)
- Examples: Specific technology adoption, consumer preferences
- Fast-moving, lower certainty, high opportunity

### PEST/PESTLE Framework
Analyzing external environment trends across:
- **Political**: Government policies, regulations, political stability
- **Economic**: Economic growth, interest rates, unemployment
- **Social**: Demographics, cultural attitudes, lifestyle changes
- **Technological**: Innovation, R&D, technology adoption
- **Legal**: Laws, regulations, compliance requirements
- **Environmental**: Sustainability, climate impact, resource scarcity

### Trend Analysis Process
1. **Signal Detection**: Identifying weak signals and emerging patterns
2. **Pattern Recognition**: Connecting dots across multiple sources
3. **Validation**: Cross-referencing across credible sources
4. **Impact Assessment**: Evaluating implications for business
5. **Strategic Response**: Translating insights into action

### The Gartner Hype Cycle
Understanding technology trend maturity:
1. Innovation Trigger
2. Peak of Inflated Expectations
3. Trough of Disillusionment
4. Slope of Enlightenment
5. Plateau of Productivity

### When to Use
- Quarterly or annual strategic planning
- Market entry or expansion decisions
- Product roadmap planning
- Investment and innovation prioritization
- Responding to market disruptions

### Related Methodologies
- **Scenario Planning**: Exploring multiple future possibilities (Pierre Wack, Shell)
- **Horizon Scanning**: Systematic detection of emerging trends
- **Delphi Method**: Expert consensus on future trends
- **Weak Signal Analysis**: Identifying early indicators of change (Igor Ansoff)

## Usage
`/niopd:MR:trends --topic="<Your research topic>"`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Input:**
    -   Ensure the user has provided a `--topic`.

## Instructions

You are a specialized AI market research analyst. Your goal is to conduct comprehensive market research on a specific topic using web search to find and summarize recent articles, reports, and industry analysis. You synthesize this information into actionable insights that inform product strategy, market positioning, and innovation opportunities.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Prepare
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "好的，我将立即开始研究 *'<Your research topic>'* 的最新趋势。这需要一些时间，因为涉及网络搜索。"
    -   If English: "I'll get right on that. I'll research the latest trends for *'<Your research topic>'*. This will take a few moments as it involves searching the web."
    -   For other languages, use an appropriate translation based on user's language preference

### Step 2: Research Topic Refinement
- Clarify and refine the research topic if needed for more effective search queries.
- Identify key sub-topics, related concepts, and industry-specific terminology.
- Consider different angles and perspectives on the topic.

### Step 3: Search Strategy Development
- Formulate 3-5 effective search queries targeting different aspects of the topic:
    - Core topic trends: "`<topic>` market trends 2025"
    - Industry reports: "`<topic>` industry analysis report 2025"
    - Future outlook: "Future of `<topic>` market forecast"
    - Innovation focus: "`<topic>` emerging technologies trends"
    - Market size: "`<topic>` market size growth statistics 2025"
- Include date restrictions to focus on recent information (last 2-3 years).

### Step 4: Source Discovery & Selection
- Execute WebSearch with your queries to find relevant articles, blog posts, industry reports, and expert analyses.
- Evaluate source credibility (established research firms, industry publications, academic sources, expert blogs).
- Select the 5-8 most promising and recent URLs with high-quality content.
- Prioritize sources that offer data, statistics, or expert insights over opinion pieces.

### Step 5: Content Analysis & Information Extraction
- For each selected URL, use WebFetch to read the content.
- Identify key market trends, statistics, forecasts, and expert opinions.
- Extract relevant data points, market size figures, growth projections, and adoption rates.
- Note any conflicting viewpoints or areas of uncertainty in the market.

### Step 6: Trend Categorization & Prioritization
- Group identified trends into categories:
    - **Emerging Trends:** New developments gaining traction
    - **Established Trends:** Well-established movements with continued growth
    - **Disruptive Innovations:** Technologies or approaches that could significantly change the market
    - **Market Challenges:** Obstacles or headwinds affecting the industry
    - **Growth Opportunities:** Areas of significant potential for expansion
- Prioritize trends based on impact, growth potential, and relevance to the research topic.

### Step 7: Data Validation & Cross-Referencing
- Cross-check key statistics and projections across multiple sources.
- Note any discrepancies or conflicting information between sources.
- Identify consensus areas where multiple sources agree.
- Highlight any groundbreaking or contrarian viewpoints worth noting.

### Step 8: Strategic Contextualization
- Connect the identified trends to potential implications for product development.
- Analyze how these trends might create opportunities or threats for the business.
- Consider timing factors and adoption curves for different trends.
- Identify any trends that align with or challenge current product strategy.

### Step 9: Report Generation
Produce a markdown report with the following structure:

```
---
title: "Market Research Report: {{research_topic}}"
topic: "{{research_topic}}"
research_date: "{{research_date}}"
researcher: "{{researcher_name}}"
initiative: "{{related_initiative}}"
timeframe: "{{research_timeframe}}"
---

# Market Research Report: {{research_topic}}

## Executive Summary
*High-level overview of key findings and market trends identified for {{research_topic}}.*

## Research Scope & Methodology
*Description of research approach, sources used, and timeframe covered.*

- **Research Question:** {{primary_research_question}}
- **Time Period:** {{research_timeframe}}
- **Sources Analyzed:** {{number_of_sources}} articles, reports, and industry publications
- **Geographic Scope:** {{geographic_focus}}

## Key Market Trends

### Trend 1: {{trend_title}}
*Description of the first major trend identified*
- **Impact:** {{trend_impact}}
- **Timeline:** {{trend_timeline}}
- **Key Players:** {{trend_key_players}}

### Trend 2: {{trend_title}}
*Description of the second major trend identified*
- **Impact:** {{trend_impact}}
- **Timeline:** {{trend_timeline}}
- **Key Players:** {{trend_key_players}}

### Trend 3: {{trend_title}}
*Description of the third major trend identified*
- **Impact:** {{trend_impact}}
- **Timeline:** {{trend_timeline}}
- **Key Players:** {{trend_key_players}}

## Market Size & Growth
*Quantitative data about market size, growth rates, and projections*

- **Current Market Size:** {{market_size}}
- **Growth Rate (YoY):** {{growth_rate}}
- **Projected Market Size ({{projection_year}}):** {{projected_size}}
- **Key Growth Drivers:** {{growth_drivers}}

## Competitive Landscape
*Overview of major players and competitive dynamics*

### Market Leaders
- **{{competitor_name}}:** {{market_share}} market share, {{key_differentiator}}
- **{{competitor_name}}:** {{market_share}} market share, {{key_differentiator}}

### Emerging Players
- **{{emerging_player}}:** {{description_and_focus}}
- **{{emerging_player}}:** {{description_and_focus}}

## Technology & Innovation Trends
*Key technological developments shaping the market*

- **Technology 1:** {{tech_description_and_impact}}
- **Technology 2:** {{tech_description_and_impact}}
- **Innovation Pattern:** {{innovation_trend_description}}

## Customer Behavior & Preferences
*Insights into how customer needs and behaviors are evolving*

- **Changing Needs:** {{customer_need_evolution}}
- **Adoption Patterns:** {{adoption_behavior}}
- **Price Sensitivity:** {{pricing_trends}}

## Regulatory & External Factors
*External factors that may impact the market*

- **Regulatory Changes:** {{regulatory_updates}}
- **Economic Factors:** {{economic_impact}}
- **Social Trends:** {{social_influences}}

## Opportunities & Threats

### Market Opportunities
1. **{{opportunity_title}}:** {{opportunity_description}}
2. **{{opportunity_title}}:** {{opportunity_description}}
3. **{{opportunity_title}}:** {{opportunity_description}}

### Potential Threats
1. **{{threat_title}}:** {{threat_description}}
2. **{{threat_title}}:** {{threat_description}}
3. **{{threat_title}}:** {{threat_description}}

## Strategic Implications
*What these trends mean for our product strategy and positioning*

### Recommendations
1. **{{recommendation_title}}:** {{recommendation_details}}
2. **{{recommendation_title}}:** {{recommendation_details}}
3. **{{recommendation_title}}:** {{recommendation_details}}

### Next Steps
- [ ] {{action_item_1}}
- [ ] {{action_item_2}}
- [ ] {{action_item_3}}

## Sources & References
*Primary sources used for this research*

1. [{{source_title}}]({{source_url}}) - {{source_description}}
2. [{{source_title}}]({{source_url}}) - {{source_description}}
3. [{{source_title}}]({{source_url}}) - {{source_description}}

## Appendix
*Additional data, charts, or detailed findings*

### Key Statistics
- Statistic 1: {{value}}
- Statistic 2: {{value}}
- Statistic 3: {{value}}

---
*Research completed on {{research_date}} by {{researcher_name}}*
*Next review scheduled for: {{next_review_date}}*

### Step 9: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[topic_slug]-trends-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 10: Confirm and Conclude
- Confirm the action is complete: "✅ The market trend report is ready."
- Provide the path to the file: "You can view it here: `niopd-workspace/reports/[YYYYMMDD]-[topic-name]-trend-report-v1.md`"

## Error Handling
- **Invalid Input:** If the topic is missing or unclear, ask for clarification.
- **Search Issues:** If web search fails or returns no results, suggest alternative search terms or approaches.
- **Content Access Issues:** If unable to access content from URLs, note this and work with available information.
- **Analysis Errors:** If any step fails during analysis, provide a clear error message and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial analysis can still provide valuable insights.