---
argument-hint: --url=<competitor_url>
description: Generates a competitive analysis report for a given URL.
---

# Command: /niopd:MR:competitor

This command generates a competitive analysis report for a given URL by directly analyzing the competitor's website and producing a structured summary of their product, pricing, and positioning.

## Theoretical Foundation

### Origin and Development
Competitive analysis draws from multiple strategic management frameworks:

1. **Competitive Intelligence** - Systematic collection and analysis of competitor information for strategic decision-making
2. **SWOT Analysis** - Framework for analyzing Strengths, Weaknesses, Opportunities, and Threats (Albert Humphrey, Stanford 1960s)
3. **Competitive Strategy** - Based on **Michael Porter's** work on competitive analysis and strategy (1980)

### Core Principle
The fundamental approach is **systematic competitor assessment**: Rather than ad-hoc observations, this command uses structured analysis to comprehensively understand a competitor's strategy, positioning, capabilities, and market approach.

### Analysis Framework
1. **Value Proposition Analysis**: Understanding how competitors position their offering
2. **Feature & Capability Assessment**: Mapping functional and non-functional capabilities
3. **Pricing Strategy Analysis**: Understanding monetization approach and customer economics
4. **Market Positioning**: Determining competitive positioning and differentiation
5. **SWOT Analysis**: Evaluating strategic position holistically

### When to Use
- Entering a new market or launching a new product
- Responding to competitive threats
- Quarterly competitive landscape reviews
- Strategic planning and positioning exercises
- Before major product decisions or pivots

### Related Frameworks
- **Porter's Five Forces**: Industry competitive structure analysis (Michael Porter, 1979)
- **Blue Ocean Strategy**: Creating uncontested market space (Kim & Mauborgne, 2005)
- **Value Chain Analysis**: Understanding competitive advantage sources (Michael Porter)
- **Benchmarking**: Systematic comparison against best practices

## Usage
`/niopd:MR:competitor --url=<competitor_url>`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate URL:**
    -   Ensure the user has provided a `--url`.
    -   Check if the URL is in a valid format (starts with http/https).

## Instructions

You are a specialized AI expert in competitive analysis. Your goal is to conduct comprehensive analysis of a competitor's website and market presence to produce a detailed strategic report. You combine web analysis with market intelligence to extract insights that inform product positioning, feature development, and competitive strategy.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Prepare
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "好的，我将分析 `<competitor_url>` 处的竞争对手。这可能需要一些时间。"
    -   If English: "Okay, I'll analyze the competitor at `<competitor_url>`. This may take a moment."
    -   For other languages, use an appropriate translation based on user's language preference

### Step 2: Website Analysis & Content Extraction
- Use WebFetch to retrieve the main content of the provided URL.
- Identify and extract key sections: value proposition, features, pricing, target audience, and differentiators.
- Navigate to related pages (Pricing, Features, About, Blog) to gather comprehensive information.
- Extract text content, key headlines, and feature descriptions.

### Step 3: Value Proposition & Positioning Analysis
- Identify the competitor's core value proposition and main marketing messages.
- Analyze their differentiation strategy and unique selling points.
- Determine how they position themselves relative to the market and other competitors.
- Extract any specific target market segments they emphasize.

### Step 4: Product & Feature Analysis
- Create a comprehensive list of the competitor's key features and capabilities.
- Identify any unique or innovative features they offer.
- Note any integrations or partnerships they highlight.
- Assess the maturity and sophistication of their product offering.

### Step 5: Pricing & Business Model Analysis
- Locate and analyze their pricing page or pricing information.
- Document all available pricing tiers, packages, or plans.
- Note any free trials, freemium options, or enterprise solutions.
- Identify pricing models (subscription, usage-based, one-time purchase).
- Extract any value metrics or usage limits for each tier.

### Step 6: Target Audience & Market Positioning
- Analyze language and messaging to infer their primary target audience.
- Identify any specific customer personas they target.
- Note any industry verticals or use cases they emphasize.
- Assess their perceived market position (market leader, challenger, niche player).

### Step 7: Content & Marketing Analysis
- Examine their content strategy through blog posts, case studies, and resources.
- Identify key themes in their content marketing.
- Note any thought leadership or educational content they produce.
- Analyze their communication style and brand voice.

### Step 8: SWOT Analysis
- Conduct a comprehensive SWOT analysis based on the gathered information:
    - **Strengths:** What they do well and how they differentiate.
    - **Weaknesses:** Limitations, gaps, or areas for improvement.
    - **Opportunities:** Market gaps they're addressing or could address.
    - **Threats:** Challenges they face or pose to your product.

### Step 9: Strategic Insights Generation
- Identify direct competitive threats to your product.
- Highlight potential opportunities for differentiation.
- Suggest areas where your product could gain competitive advantage.
- Note any emerging trends or innovations they're adopting.

### Step 10: Report Generation
Produce a markdown report with the following structure:

---
# Competitor Analysis: [Competitor Name]

## Executive Summary
*A brief overview of key findings and strategic implications*

## Company Overview
- **Name:** [Company name]
- **URL:** [Website URL]
- **Analysis Date:** [Date of analysis]
- **Primary Focus:** [Main product/market focus]

## Core Value Proposition & Positioning
*A one or two-sentence summary of the competitor's main value proposition and how they position themselves in the market.*

### Key Messaging
- [Primary messaging theme]
- [Secondary messaging theme]
- [Differentiation statement]

### Market Position
*[Description of their market position and how they differentiate from others]*

## Target Audience & Market Segmentation
*Detailed analysis of who they are targeting*

### Primary Audience
- **Demographics:** [Age, role, industry if specified]
- **Psychographics:** [Needs, behaviors, challenges]
- **Use Cases:** [Primary applications or scenarios]

### Secondary Audiences
- [Additional market segments if identified]

## Product & Features Analysis

### Core Features
- Feature 1: [Description and significance]
- Feature 2: [Description and significance]
- Feature 3: [Description and significance]

### Unique Differentiators
- [Unique capability or approach]
- [Innovative feature or service]
- [Competitive advantage]

### Integrations & Ecosystem
- [Key integrations]
- [Partner ecosystem]
- [API availability]

## Pricing Model & Plans

### Pricing Tiers
#### Tier 1: [Name] ([Target audience])
- **Price:** [Pricing details]
- **Key Features:** [Main features included]
- **Limitations:** [Restrictions or caps]

#### Tier 2: [Name] ([Target audience])
- **Price:** [Pricing details]
- **Key Features:** [Main features included]
- **Limitations:** [Restrictions or caps]

#### Tier 3: [Name] ([Target audience])
- **Price:** [Pricing details]
- **Key Features:** [Main features included]
- **Limitations:** [Restrictions or caps]

### Pricing Model Analysis
*[Analysis of their pricing strategy and value proposition at each tier]*

## Content Strategy & Marketing Approach

### Communication Style
- [Tone and voice]
- [Key messaging themes]
- [Primary channels]

### Content Focus
- [Main content topics]
- [Educational content]
- [Thought leadership]

### Go-to-Market Strategy
- [Sales approach]
- [Customer acquisition methods]
- [Success stories or case studies]

## SWOT Analysis

### Strengths
- **[Strength 1]:** [Explanation]
- **[Strength 2]:** [Explanation]
- **[Strength 3]:** [Explanation]

### Weaknesses
- **[Weakness 1]:** [Explanation]
- **[Weakness 2]:** [Explanation]
- **[Weakness 3]:** [Explanation]

### Opportunities
- **[Opportunity 1]:** [Explanation]
- **[Opportunity 2]:** [Explanation]
- **[Opportunity 3]:** [Explanation]

### Threats
- **[Threat 1]:** [Explanation]
- **[Threat 2]:** [Explanation]
- **[Threat 3]:** [Explanation]

## Strategic Implications for Our Product

### Competitive Threats
- [Threat 1 and potential impact]
- [Threat 2 and potential impact]

### Differentiation Opportunities
- [Opportunity 1 for differentiation]
- [Opportunity 2 for differentiation]

### Feature Gap Analysis
- **Missing from Competitor:** [Feature or capability they lack]
- **Our Advantage:** [How we can leverage this gap]

### Pricing Strategy Insights
- [Insight about their pricing that could inform our strategy]
- [Market positioning relative to their pricing]

## Recommendations

### Product Development
1. **[Recommendation]:** [Brief description of what to consider]
2. **[Recommendation]:** [Brief description of what to consider]

### Positioning & Messaging
1. **[Recommendation]:** [Brief description of what to consider]
2. **[Recommendation]:** [Brief description of what to consider]

### Competitive Response
1. **[Recommendation]:** [Brief description of how to respond]
2. **[Recommendation]:** [Brief description of how to respond]

## Appendix

### Key Web Pages Analyzed
- [URL 1]: [Page purpose]
- [URL 2]: [Page purpose]
- [URL 3]: [Page purpose]

### Additional Notes
[Any additional observations or context]

---
*Report generated on [Date]*

### Step 11: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[competitor_name_slug]-analysis-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 12: Confirm and Conclude
- Confirm the action is complete: "✅ The competitive analysis is complete."
- Provide the path to the file: "You can view the report here: `niopd-workspace/reports/[YYYYMMDD]-[domain-name]-competitor-analysis-v1.md`"

## Error Handling
- **Invalid URL:** If the provided URL is invalid or inaccessible, clearly explain the issue and suggest verifying the URL.
- **Website Access Issues:** If the website blocks automated access or requires authentication, explain this limitation and suggest manual analysis.
- **Missing Information:** If key sections (pricing, features, etc.) cannot be found, note this and suggest additional research methods.
- **Analysis Errors:** If any step fails during analysis, provide a clear error message and troubleshooting suggestions.
- **Ambiguous Requests:** If the analysis scope is unclear, ask for clarification before proceeding.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial analysis can still provide valuable insights.