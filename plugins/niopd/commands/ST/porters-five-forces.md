---
argument-hint: [--for=<industry_name>] [--market=<market_context>] [--region=<geographic_region>]
description: Analyzes industry competitiveness using Porter's Five Forces framework.
---

# Command: /niopd:ST:porters-five-forces

This command analyzes industry competitiveness using Porter's Five Forces framework to evaluate market attractiveness and competitive dynamics.

## Theoretical Foundation

### Origin and Development
Porter's Five Forces was introduced by **Michael E. Porter** (Harvard Business School) in his 1979 Harvard Business Review article "How Competitive Forces Shape Strategy" and elaborated in his 1980 book "Competitive Strategy." It remains one of the most influential business strategy frameworks.

### Core Principle
The framework analyzes **industry structure and competitive intensity** by examining five forces that determine the attractiveness and profitability potential of an industry. High competitive forces reduce profitability; low forces increase profit potential.

### The Five Forces

1. **Threat of New Entrants**
   - **Barriers to Entry**: Capital requirements, economies of scale, product differentiation, access to distribution, regulatory barriers
   - **High Threat**: Easy entry → increased competition → lower profitability
   - **Low Threat**: High barriers → protected incumbents → higher profitability

2. **Bargaining Power of Suppliers**
   - **Factors**: Supplier concentration, uniqueness of inputs, switching costs, forward integration threat
   - **High Power**: Suppliers can raise prices → lower profitability
   - **Low Power**: Multiple alternatives → better terms → higher profitability

3. **Bargaining Power of Buyers**
   - **Factors**: Buyer concentration, purchase volume, product standardization, switching costs, backward integration threat
   - **High Power**: Buyers demand lower prices → lower profitability
   - **Low Power**: Fragmented buyers → pricing power → higher profitability

4. **Threat of Substitutes**
   - **Factors**: Relative price-performance, switching costs, buyer propensity to substitute
   - **High Threat**: Alternative solutions limit pricing → lower profitability
   - **Low Threat**: No close substitutes → pricing freedom → higher profitability

5. **Competitive Rivalry**
   - **Factors**: Number of competitors, industry growth, fixed costs, exit barriers, product differentiation
   - **High Rivalry**: Price wars, high marketing costs → lower profitability
   - **Low Rivalry**: Stable competition → sustainable margins → higher profitability

### The Sixth Force
Porter later acknowledged **complementary products/services** as an important factor (popularized in the digital age with platform ecosystems).

### When to Use
- Industry analysis and market entry decisions
- Competitive strategy formulation
- M&A evaluation
- Investment decisions
- Strategic positioning analysis
- Business model innovation

### Strategic Implications
1. **Position Within Forces**: Find where competitive forces are weakest
2. **Exploit Changes**: Identify industry changes that alter forces
3. **Shape Forces**: Take actions to improve force structure

### Complementary Tools
- **PESTLE Analysis**: Macro-environment context
- **Value Chain Analysis**: Internal competitive advantage sources
- **Strategic Group Analysis**: Competitor clustering
- **Blue Ocean Strategy**: Create uncontested market space

### Limitations to Consider
- Static snapshot (doesn't capture industry dynamics)
- Industry boundaries can be ambiguous
- Less applicable to network/platform businesses
- Should be updated regularly as conditions change

## Implementation Plan

1. Guide comprehensive Porter's Five Forces industry analysis
2. Gather industry, market, and competitive context
3. Analyze all five competitive forces in depth
4. Assess industry attractiveness and profitability potential  
5. Provide strategic positioning recommendations
6. Save Porter's Five Forces analysis to niopd-workspace/reports/

## Usage
`/niopd:ST:porters-five-forces [--for=<industry_name>] [--market=<market_context>] [--region=<geographic_region>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Parameters:**
    -   If `--for` not provided, prompt user to specify industry
    -   If `--market` not provided, gather market/segment context
    -   If `--region` not provided, ask for geographic scope

3.  **Validate Workspace:**
    -   Check that `niopd-workspace/reports/` exists, create if needed

## Instructions

You are a specialized AI expert in competitive strategy and Porter's Five Forces framework. Your goal is to help organizations analyze industry structure and competitive dynamics to determine profitability potential and strategic positioning.

### Core Principle
Always ensure that your analysis is grounded in the Porter's Five Forces framework's core principle: analyzing industry structure and competitive intensity by examining five forces that determine the attractiveness and profitability potential of an industry. High competitive forces reduce profitability; low forces increase profit potential.

### Step 1: Acknowledge and Define Industry Scope
-   Acknowledge: "I'll conduct a Porter's Five Forces analysis for the **<industry>** industry."
-   If `--for` wasn't provided, ask: "What industry are you analyzing?"
-   Clarify industry boundaries: "What defines this industry? (Products/services included)"
-   If `--region` wasn't provided, ask: "What geographic market? (Local, national, global)"
-   Ask: "What specific segment or niche within this industry?"
-   If configuration file exists and contains industry, market, or region settings, use those values as defaults
-   If language setting in configuration is Chinese, respond in Chinese; otherwise, respond in English
-   Wait for user responses.

### Step 2: Analysis Purpose
-   Gather strategic context:
    -   "Why are you analyzing this industry?"
        -   Market entry decision
        -   Competitive positioning
        -   Investment evaluation
        -   Strategic planning
    -   "What strategic decisions does this analysis inform?"
    -   "Do you have competitors/industry data available?"
-   Wait for user responses.

### Step 3: Force 1 - Threat of New Entrants
-   Analyze barriers to entry:
    -   "What capital investment is required to enter this industry?"
    -   "Are there significant economies of scale that favor incumbents?"
    -   "How strong is brand loyalty? Do existing players have patent protection?"
    -   "How difficult is access to distribution channels?"
    -   "What regulatory/licensing requirements exist?"
    -   "Do incumbents have cost advantages (technology, location, experience)?"
-   Assess: "Is it easy or difficult for new competitors to enter this market?"
-   Rate: "Threat Level: High / Medium / Low"
-   Trend: "Is this threat Increasing / Stable / Decreasing? Why?"
-   Wait for user responses.

### Step 4: Force 2 - Bargaining Power of Suppliers
-   Analyze supplier dynamics:
    -   "How many suppliers exist? Are they concentrated?"
    -   "How unique or differentiated are supplier inputs?"
    -   "What are the switching costs to change suppliers?"
    -   "Is there a threat of forward integration (suppliers becoming competitors)?"
    -   "How critical are supplier inputs to product quality?"
    -   "Can your industry substitute supplier inputs easily?"
-   Assess: "Can suppliers dictate terms, raise prices, or reduce quality?"
-   Rate: "Supplier Power: High / Medium / Low"
-   Trend: "Is supplier power Increasing / Stable / Decreasing? Why?"
-   Wait for user responses.

### Step 5: Force 3 - Bargaining Power of Buyers
-   Analyze buyer/customer dynamics:
    -   "How concentrated are buyers? Do few buyers control large volume?"
    -   "What portion of buyer costs does your product represent?"
    -   "How standardized is your product? Can buyers easily switch?"
    -   "Is there a threat of backward integration (buyers making it themselves)?"
    -   "How price-sensitive are buyers?"
    -   "Do buyers have full information on costs and alternatives?"
-   Assess: "Can buyers negotiate lower prices or demand better quality?"
-   Rate: "Buyer Power: High / Medium / Low"
-   Trend: "Is buyer power Increasing / Stable / Decreasing? Why?"
-   Wait for user responses.

### Step 6: Force 4 - Threat of Substitutes
-   Analyze substitute products/services:
    -   "What alternative solutions meet the same customer need?"
    -   "How does price-performance of substitutes compare?"
    -   "What are switching costs for customers to move to substitutes?"
    -   "How willing are customers to try alternatives?"
    -   "Are substitutes improving faster than industry products?"
    -   "What emerging technologies could create new substitutes?"
-   Assess: "How easily can customers replace your product with alternatives?"
-   Rate: "Substitute Threat: High / Medium / Low"
-   Trend: "Is this threat Increasing / Stable / Decreasing? Why?"
-   Wait for user responses.

### Step 7: Force 5 - Competitive Rivalry
-   Analyze competitive intensity:
    -   "How many competitors exist? Market concentration?"
    -   "What is the industry growth rate? (High growth reduces rivalry)"
    -   "Are products highly differentiated or commoditized?"
    -   "What are fixed costs and capacity utilization rates?"
    -   "Are there high exit barriers keeping struggling firms in market?"
    -   "How aggressive is competitive behavior? (Price wars, advertising battles)"
    -   "Is there strong brand identity among competitors?"
-   Assess: "How intense is competition among existing players?"
-   Rate: "Rivalry Intensity: High / Medium / Low"
-   Trend: "Is rivalry Increasing / Stable / Decreasing? Why?"
-   Wait for user responses.

### Step 8: The Sixth Force - Complementors (Optional)
-   Assess complementary products/services:
    -   "What complementary products enhance your product's value?"
    -   "Who controls key complements? How collaborative are they?"
    -   "Are complements abundant or scarce?"
    -   "Does your product enable platform/ecosystem dynamics?"
-   Note: This is particularly important for technology/platform businesses.
-   Wait for user responses.

### Step 9: Overall Industry Attractiveness Assessment
-   Synthesize all five forces:
    -   "Based on all five forces, rate overall industry attractiveness:"
        -   Highly Attractive (Low competitive forces)
        -   Moderately Attractive
        -   Neutral
        -   Moderately Unattractive  
        -   Highly Unattractive (High competitive forces)
    -   "What is the expected industry profitability potential?"
    -   "Which forces are most critical in this industry?"
-   Wait for user responses.

### Step 10: Strategic Positioning Analysis
-   Identify strategic implications:
    -   "Given these forces, where can you position advantageously?"
    -   "Which forces can you influence or shape to your advantage?"
    -   "What industry changes (technology, regulation, demographics) might alter forces?"
    -   "Should you enter/stay/exit this industry? Why?"
-   Wait for user responses.

### Step 11: Competitive Strategy Recommendations
-   Provide strategic options:
    -   For each high-threat force, ask:
        -   "How can you reduce this competitive pressure?"
        -   "Can you differentiate to reduce rivalry?"
        -   "Can you create switching costs to reduce buyer power?"
        -   "Can you build barriers to deter new entrants?"
    -   "What strategic moves would improve your position?"
-   Wait for user responses.

### Step 12: Industry Evolution Outlook
-   Assess future force dynamics:
    -   "What trends will change force strength over the next 3-5 years?"
    -   "Are new technologies creating substitutes or lowering barriers?"
    -   "How is consolidation affecting supplier/buyer power?"
    -   "What regulatory changes might impact competitive forces?"
-   Wait for user responses.

### Step 13: Create Comprehensive Porter's Five Forces Analysis Document

Produce a detailed Porter's Five Forces analysis with the following comprehensive structure:

---
# Porter's Five Forces Analysis: [Industry Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Industry:** [industry_name]  
**Market:** [market_segment]  
**Geographic Scope:** [region]

---

## Executive Summary

**Overall Industry Attractiveness:** [Highly Attractive / Moderately Attractive / Neutral / Moderately Unattractive / Highly Unattractive]

**Profitability Potential:** [High / Medium / Low]

**Key Findings:**
- [Most critical force impacting this industry]
- [Second most impactful force]
- [Strategic implication 1]
- [Strategic implication 2]

**Strategic Recommendation:** [Enter / Grow / Hold / Harvest / Exit] - [Rationale]

---

## Force 1: Threat of New Entrants

### Threat Level: [High / Medium / Low]
### Trend: [Increasing / Stable / Decreasing]

### Barriers to Entry Analysis

**Capital Requirements:**
- Initial investment needed: [Amount/Description]
- Working capital requirements: [Description]
- **Impact:** [High/Medium/Low barrier]

**Economies of Scale:**
- Minimum efficient scale: [Description]
- Incumbent cost advantages: [Description]
- **Impact:** [High/Medium/Low barrier]

**Product Differentiation & Brand Loyalty:**
- Brand strength of incumbents: [Description]
- Customer switching costs: [Description]
- Patent/IP protection: [Description]
- **Impact:** [High/Medium/Low barrier]

**Access to Distribution:**
- Distribution channel requirements: [Description]
- Incumbent control of channels: [Description]
- **Impact:** [High/Medium/Low barrier]

**Regulatory Barriers:**
- Licensing requirements: [Description]
- Compliance costs: [Description]
- Government restrictions: [Description]
- **Impact:** [High/Medium/Low barrier]

**Other Cost Disadvantages:**
- Proprietary technology: [Yes/No - Description]
- Favorable locations: [Description]
- Experience/learning curve: [Description]
- **Impact:** [High/Medium/Low barrier]

### Assessment
**Overall Barrier Height:** [High / Medium / Low]  
**Ease of Entry:** [Very Difficult / Difficult / Moderate / Easy / Very Easy]  
**Recent New Entrants:** [Examples, if any]  
**Threat Trend:** [Why increasing/decreasing/stable]

**Strategic Implication:**
[How this force affects strategy - defend barriers, build moats, deter entry]

---

## Force 2: Bargaining Power of Suppliers

### Supplier Power: [High / Medium / Low]
### Trend: [Increasing / Stable / Decreasing]

### Supplier Landscape

**Supplier Concentration:**
- Number of suppliers: [Few / Moderate / Many]
- Concentration ratio: [Description]
- **Impact:** [High/Medium/Low power]

**Uniqueness of Inputs:**
- Input differentiation: [Highly differentiated / Somewhat / Commodity]
- Availability of substitutes: [Many / Some / Few / None]
- **Impact:** [High/Medium/Low power]

**Switching Costs:**
- Cost to change suppliers: [High / Medium / Low]
- Technical integration requirements: [Description]
- **Impact:** [High/Medium/Low power]

**Forward Integration Threat:**
- Can suppliers become competitors?: [High / Medium / Low threat]
- Examples: [Description]
- **Impact:** [High/Medium/Low power]

**Importance to Supplier Business:**
- Industry's share of supplier revenue: [High / Medium / Low]
- **Impact:** [Inverse - Low share = High power]

**Input Impact on Quality/Cost:**
- Criticality of supplier inputs: [Critical / Important / Standard]
- **Impact:** [High/Medium/Low power]

### Assessment
**Overall Supplier Power:** [High / Medium / Low]  
**Key Suppliers:** [List critical supplier types]  
**Power Trend:** [Why increasing/decreasing/stable]

**Strategic Implication:**
[How this force affects strategy - diversify suppliers, vertical integration, partnerships]

---

## Force 3: Bargaining Power of Buyers

### Buyer Power: [High / Medium / Low]
### Trend: [Increasing / Stable / Decreasing]

### Buyer Landscape

**Buyer Concentration:**
- Customer concentration: [Few large / Many small / Mixed]
- Volume per buyer: [High / Medium / Low]
- **Impact:** [High/Medium/Low power]

**Purchase Importance:**
- Product cost as % of buyer budget: [High / Medium / Low]
- **Impact:** [High % = High power]

**Product Standardization:**
- Product differentiation: [Highly differentiated / Somewhat / Commodity]
- Switching costs for buyers: [High / Medium / Low]
- **Impact:** [Low differentiation = High power]

**Backward Integration Threat:**
- Can buyers make it themselves?: [High / Medium / Low threat]
- Examples: [Description]
- **Impact:** [High/Medium/Low power]

**Price Sensitivity:**
- Buyer profitability: [High / Medium / Low]
- Quality importance vs. price: [Quality-focused / Price-focused / Balanced]
- **Impact:** [High/Medium/Low power]

**Information Availability:**
- Buyer access to pricing/cost data: [Complete / Partial / Limited]
- **Impact:** [High/Medium/Low power]

### Assessment
**Overall Buyer Power:** [High / Medium / Low]  
**Key Buyer Segments:** [List major customer types]  
**Power Trend:** [Why increasing/decreasing/stable]

**Strategic Implication:**
[How this force affects strategy - differentiation, lock-in, relationship building]

---

## Force 4: Threat of Substitutes

### Substitute Threat: [High / Medium / Low]
### Trend: [Increasing / Stable / Decreasing]

### Substitute Analysis

**Alternative Solutions:**

| Substitute Product/Service | Price-Performance vs. Industry | Switching Cost | Adoption Likelihood |
|---------------------------|-------------------------------|----------------|--------------------|
| [Substitute 1] | [Better/Similar/Worse] | [High/Medium/Low] | [High/Medium/Low] |
| [Substitute 2] | [Better/Similar/Worse] | [High/Medium/Low] | [High/Medium/Low] |
| [Substitute 3] | [Better/Similar/Worse] | [High/Medium/Low] | [High/Medium/Low] |

**Price-Performance Tradeoff:**
- Relative price: [Description]
- Relative performance: [Description]
- Value proposition: [Better / Similar / Worse than industry]

**Switching Costs:**
- Cost to switch to substitute: [High / Medium / Low]
- Learning curve: [Steep / Moderate / Easy]
- **Impact:** [High switching costs reduce threat]

**Buyer Propensity to Substitute:**
- Customer willingness to try alternatives: [High / Medium / Low]
- Risk tolerance: [Description]

**Substitute Improvement Rate:**
- Technology advancement: [Faster / Similar / Slower than industry]
- Investment in substitutes: [High / Medium / Low]

**Emerging Substitutes:**
- [Technology/solution that could disrupt industry]
- [Timeline and likelihood]

### Assessment
**Overall Substitute Threat:** [High / Medium / Low]  
**Most Dangerous Substitute:** [Description]  
**Threat Trend:** [Why increasing/decreasing/stable]

**Strategic Implication:**
[How this force affects strategy - innovation, pricing, customer lock-in]

---

## Force 5: Competitive Rivalry

### Rivalry Intensity: [High / Medium / Low]
### Trend: [Increasing / Stable / Decreasing]

### Competitive Dynamics

**Number of Competitors:**
- Market concentration: [Highly concentrated / Moderate / Fragmented]
- Top 3-5 players' market share: [%]
- **Impact:** [Many competitors = High rivalry]

**Industry Growth Rate:**
- Current growth: [% per year]
- Growth trend: [Accelerating / Stable / Declining]
- **Impact:** [Slow growth = High rivalry]

**Product Differentiation:**
- Differentiation level: [Highly differentiated / Somewhat / Commodity]
- Brand importance: [High / Medium / Low]
- **Impact:** [Low differentiation = High rivalry]

**Fixed Costs & Capacity:**
- Fixed cost burden: [High / Medium / Low]
- Capacity utilization: [Over / At / Under capacity]
- **Impact:** [High fixed costs = Pressure to cut prices]

**Exit Barriers:**
- Asset specialization: [High / Medium / Low]
- Emotional/strategic commitment: [Description]
- Regulatory barriers to exit: [Description]
- **Impact:** [High barriers = Trapped competitors = High rivalry]

**Competitive Behavior:**
- Price competition intensity: [Intense / Moderate / Limited]
- Advertising/promotion battles: [Intense / Moderate / Limited]
- Innovation pace: [Rapid / Moderate / Slow]
- Gentlemanly competition vs. cutthroat: [Description]

### Key Competitors

| Competitor | Market Share | Strategy | Competitive Advantage |
|------------|--------------|----------|----------------------|
| [Competitor 1] | [%] | [Description] | [Advantage] |
| [Competitor 2] | [%] | [Description] | [Advantage] |
| [Competitor 3] | [%] | [Description] | [Advantage] |

### Assessment
**Overall Rivalry Intensity:** [High / Medium / Low]  
**Most Intense Battleground:** [Price / Quality / Innovation / Marketing]  
**Rivalry Trend:** [Why increasing/decreasing/stable]

**Strategic Implication:**
[How this force affects strategy - differentiate, consolidate, find niche]

---

## The Sixth Force: Complementors (If Applicable)

**Complementary Products/Services:** [Description]

**Impact on Industry:**
- Complements increase product value: [Yes/No - Description]
- Control of complements: [We control / Collaborative / Others control]
- Abundance of complements: [Many / Some / Few]

**Platform/Ecosystem Dynamics:** [If applicable]

**Strategic Implication:** [Collaboration opportunities, platform strategy]

---

## Overall Industry Analysis

### Force Summary Matrix

| Force | Strength | Trend | Impact on Profitability |
|-------|----------|-------|------------------------|
| Threat of New Entrants | [H/M/L] | [↑/→/↓] | [Positive/Neutral/Negative] |
| Supplier Power | [H/M/L] | [↑/→/↓] | [Positive/Neutral/Negative] |
| Buyer Power | [H/M/L] | [↑/→/↓] | [Positive/Neutral/Negative] |
| Threat of Substitutes | [H/M/L] | [↑/→/↓] | [Positive/Neutral/Negative] |
| Competitive Rivalry | [H/M/L] | [↑/→/↓] | [Positive/Neutral/Negative] |

### Industry Attractiveness Rating

**Overall Assessment:** [Highly Attractive / Moderately Attractive / Neutral / Moderately Unattractive / Highly Unattractive]

**Rationale:**
[Explain overall attractiveness based on force analysis]

**Expected Industry Profitability:**
- Current profitability level: [High / Medium / Low]
- Expected 3-5 year profitability: [Improving / Stable / Declining]
- ROI potential: [Above average / Average / Below average]

**Most Critical Forces:**
1. [Force name] - [Why it's most important]
2. [Force name] - [Why it's important]
3. [Force name] - [Why it's important]

---

## Strategic Implications & Recommendations

### Positioning Strategy

**Recommended Position:** [Description of where to compete]

**Rationale:**
- [Force-based reason 1]
- [Force-based reason 2]
- [Force-based reason 3]

### Strategies to Improve Competitive Position

**Reduce New Entrant Threat:**
- [Strategy 1: e.g., Build brand loyalty]
- [Strategy 2: e.g., Achieve scale economies]
- [Strategy 3: e.g., Lock up distribution]

**Reduce Supplier Power:**
- [Strategy 1: e.g., Diversify supplier base]
- [Strategy 2: e.g., Backward integration]
- [Strategy 3: e.g., Develop substitutes]

**Reduce Buyer Power:**
- [Strategy 1: e.g., Increase differentiation]
- [Strategy 2: e.g., Create switching costs]
- [Strategy 3: e.g., Serve fragmented buyers]

**Reduce Substitute Threat:**
- [Strategy 1: e.g., Continuous innovation]
- [Strategy 2: e.g., Improve price-performance]
- [Strategy 3: e.g., Customer education]

**Manage Competitive Rivalry:**
- [Strategy 1: e.g., Differentiate offering]
- [Strategy 2: e.g., Focus on growth segments]
- [Strategy 3: e.g., Collaborate on standards]

### Industry Evolution Outlook (3-5 Years)

**Expected Changes:**

| Trend | Impact on Forces | Strategic Response |
|-------|------------------|--------------------|
| [Trend 1: e.g., Consolidation] | [Force affected] | [How to respond] |
| [Trend 2: e.g., Technology disruption] | [Force affected] | [How to respond] |
| [Trend 3: e.g., Regulation change] | [Force affected] | [How to respond] |

**Scenario Planning:**
- **Best Case:** [What improves forces]
- **Base Case:** [Expected evolution]
- **Worst Case:** [What worsens forces]

### Final Recommendation

**Strategic Decision:** [Enter / Grow Aggressively / Grow Selectively / Hold / Harvest / Exit]

**Investment Thesis:**
[Clear recommendation based on force analysis with rationale]

**Key Success Factors:**
1. [Critical capability 1]
2. [Critical capability 2]
3. [Critical capability 3]

**Risk Factors:**
1. [Risk 1 related to forces]
2. [Risk 2 related to forces]
3. [Risk 3 related to forces]

**Next Steps:**
1. [Immediate action 1]
2. [Immediate action 2]
3. [Immediate action 3]

---

## Complementary Analyses Recommended

- **PESTLE Analysis** (`/niopd:ST:pest`) - Analyze macro-environment factors
- **SWOT Analysis** (`/niopd:ST:swot`) - Internal strengths/weaknesses vs. forces
- **Value Chain Analysis** - Identify competitive advantage sources
- **Strategic Group Mapping** - Understand competitor positioning
- **Scenario Planning** - Test strategy against force evolution

---

**Document Prepared By:** [Your name/team]  
**Last Updated:** [YYYYMMDD]  
**Next Review Date:** [Quarterly/Annually]

---

**Filename:** `[YYYYMMDD]-[industry_slug]-five-forces-v[version].md`  
**Save to:** `niopd-workspace/reports/[filename]`

### Step 14: Confirm and Conclude
- Confirm: "✅ I've created a comprehensive Porter's Five Forces analysis for the **<industry>** industry."
- Show file path: `niopd-workspace/reports/[filename]`
- Suggest next steps:
    - "For macro-environment context, use `/niopd:ST:pest`"
    - "For competitive positioning, use `/niopd:ST:swot`"
    - "To develop strategy, use `/niopd:ST:canvas` for business model analysis"

## Error Handling
- **Unclear Industry Boundaries:** Help user precisely define industry scope
- **Insufficient Data:** Guide to industry reports, trade associations, public filings
- **Static Analysis:** Emphasize analyzing trends and future force changes
- **Missing Strategic Action:** Connect force analysis to positioning decisions

