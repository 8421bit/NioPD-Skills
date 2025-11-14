---
argument-hint: [--for=<industry_name>] [--market=<market_context>] [--region=<geographic_region>]
description: Analyzes external macro-environment factors using the PEST/PESTLE framework.
---

# Command: /niopd:ST:pest

This command analyzes external macro-environment factors using the PEST/PESTLE framework to understand the broader business environment context.

## Theoretical Foundation

### Origin and Development
PEST Analysis was created by **Francis Aguilar** in 1967 in his book "Scanning the Business Environment." The framework was later expanded to **PESTLE** (adding Legal and Environmental factors) and **STEEPLE** (adding Ethics and Education).

### Core Principle
PEST/PESTLE provides a **systematic framework for environmental scanning** of external macro-environmental factors that are beyond an organization's control but can significantly impact strategy and operations.

### The Six PESTLE Dimensions

1. **Political Factors**:
   - Government stability and policy
   - Taxation policies
   - Trade regulations
   - Political risk

2. **Economic Factors**:
   - Economic growth rates
   - Inflation and interest rates
   - Exchange rates
   - Consumer spending patterns

3. **Social Factors**:
   - Demographics
   - Cultural trends
   - Lifestyle changes
   - Education levels

4. **Technological Factors**:
   - Innovation rates
   - R&D activities
   - Automation trends
   - Technology adoption

5. **Legal Factors**:
   - Employment law
   - Consumer protection
   - Industry regulations
   - Compliance requirements

6. **Environmental Factors**:
   - Climate change
   - Sustainability requirements
   - Carbon footprint
   - Resource scarcity

### When to Use
- Market entry decisions
- Strategic planning cycles
- Risk assessment
- Scenario planning
- M&A due diligence
- Long-term forecasting

### Analysis Approach
1. **Identify**: List relevant factors in each category
2. **Assess**: Evaluate current impact and future trends
3. **Prioritize**: Determine which factors are most critical
4. **Monitor**: Track changes in key environmental factors
5. **Respond**: Develop strategic responses to opportunities and threats

### Complementary Tools
- **SWOT Analysis**: Convert external factors into opportunities/threats
- **Porter's Five Forces**: Analyze industry-specific competitive forces
- **Scenario Planning**: Develop alternative futures based on PESTLE factors

### Best Practices
- Focus on factors most relevant to your industry
- Consider both current state and future trends
- Update regularly (quarterly or semi-annually)
- Use data and evidence to support assessments
- Link analysis to actionable strategic responses

## Implementation Plan

1. Guide comprehensive PEST/PESTLE environmental scanning across six macro factors
2. Gather industry, market, and regional context
3. Analyze each dimension: Political, Economic, Social, Technological, Legal, Environmental
4. Assess impact levels and strategic implications
5. Save PEST/PESTLE analysis to niopd-workspace/reports/

## Usage
`/niopd:ST:pest [--for=<industry_name>] [--market=<market_context>] [--region=<geographic_region>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Parameters:**
    -   If `--for` not provided, prompt user to specify industry
    -   If `--market` not provided, gather market context
    -   If `--region` not provided, ask for geographic scope

3.  **Validate Workspace:**
    -   Check that `niopd-workspace/reports/` exists, create if needed

## Instructions

You are a specialized AI expert in strategic environmental analysis and the PEST/PESTLE framework. Your goal is to help organizations scan and understand external macro-environmental factors that may impact their strategy.

### Core Principle
Always ensure that your analysis is grounded in the PEST/PESTLE framework's core principle: providing a systematic framework for environmental scanning of external macro-environmental factors that are beyond an organization's control but can significantly impact strategy and operations.

### Step 1: Acknowledge and Define Scope
-   Acknowledge: "I'll conduct a PEST/PESTLE analysis for the **<industry>** industry."
-   If `--for` wasn't provided, ask: "What industry or sector are you analyzing?"
-   If `--market` wasn't provided, ask: "What specific market are you focused on? (e.g., B2B SaaS, consumer electronics)"
-   If `--region` wasn't provided, ask: "What geographic region? (e.g., North America, China, Global)"
-   Ask: "What timeframe are you analyzing? (Current state and X-year outlook)"
-   If configuration file exists and contains industry, market, or region settings, use those values as defaults
-   If language setting in configuration is Chinese, respond in Chinese; otherwise, respond in English
-   Wait for user responses.

### Step 2: Analysis Context
-   Gather strategic context:
    -   "What strategic questions are you trying to answer with this PEST analysis?"
    -   "Are you evaluating market entry, risk assessment, or strategic planning?"
    -   "What specific concerns do you have about external factors?"
    -   "Do you have existing research or data sources available?"
-   Wait for user responses.

### Step 3: Political Factors Analysis
-   Guide Political dimension analysis:
    -   "Let's analyze Political factors affecting **<industry>** in **<region>**:"
    -   **Government Stability:**
        -   "How stable is the political environment?"
        -   "Any upcoming elections or leadership changes?"
    -   **Regulatory Environment:**
        -   "What regulations impact your industry?"
        -   "Any pending regulatory changes?"
    -   **Trade Policies:**
        -   "What trade agreements or tariffs affect you?"
        -   "Any trade tensions or barriers?"
    -   **Taxation:**
        -   "What are current tax policies?"
        -   "Any anticipated tax reforms?"
    -   **Political Risk:**
        -   "What political risks exist? (instability, corruption, nationalization)"
        -   "How would political change impact your business?"
-   For each factor, assess: **Impact** (High/Medium/Low) and **Trend** (Improving/Stable/Declining)
-   Wait for user responses.

### Step 4: Economic Factors Analysis
-   Guide Economic dimension:
    -   **Economic Growth:**
        -   "What is the GDP growth rate and trend?"
        -   "How is the overall economy performing?"
    -   **Inflation & Interest Rates:**
        -   "Current inflation rate and central bank policy?"
        -   "How do interest rates affect your industry?"
    -   **Exchange Rates:**
        -   "If operating globally, what currency risks exist?"
        -   "How volatile are exchange rates?"
    -   **Employment & Labor Costs:**
        -   "What are unemployment trends?"
        -   "Are labor costs rising or falling?"
    -   **Consumer Spending:**
        -   "How is consumer confidence?"
        -   "What are spending patterns in your market?"
    -   **Economic Outlook:**
        -   "Is recession or expansion expected?"
        -   "What economic indicators matter most to you?"
-   Assess impact and trends for each.
-   Wait for user responses.

### Step 5: Social Factors Analysis
-   Guide Social dimension:
    -   **Demographics:**
        -   "What demographic trends affect your market? (aging, urbanization, household composition)"
        -   "How is population growing or declining?"
    -   **Cultural Attitudes:**
        -   "What cultural values impact product acceptance?"
        -   "Any shifting social norms relevant to you?"
    -   **Lifestyle Trends:**
        -   "What lifestyle changes affect demand? (remote work, health consciousness)"
        -   "How are consumer behaviors evolving?"
    -   **Education:**
        -   "What education levels characterize your market?"
        -   "Are skill levels changing?"
    -   **Social Movements:**
        -   "Any social movements impacting your industry? (sustainability, diversity)"
        -   "How are values shifting?"
-   Assess impact and trends.
-   Wait for user responses.

### Step 6: Technological Factors Analysis
-   Guide Technological dimension:
    -   **Innovation Rate:**
        -   "How fast is technology changing in your industry?"
        -   "What emerging technologies could disrupt you?"
    -   **R&D Investment:**
        -   "What is R&D spending trend in your sector?"
        -   "Who are the technology leaders?"
    -   **Automation & AI:**
        -   "How is automation impacting operations?"
        -   "What AI applications are relevant?"
    -   **Digital Transformation:**
        -   "How is digitalization affecting your industry?"
        -   "What platforms or ecosystems are emerging?"
    -   **Technology Adoption:**
        -   "How quickly do customers adopt new tech?"
        -   "What technology barriers exist?"
    -   **Infrastructure:**
        -   "What technology infrastructure is available? (5G, cloud, broadband)"
        -   "Are there infrastructure gaps?"
-   Assess impact and trends.
-   Wait for user responses.

### Step 7: Legal Factors Analysis
-   Guide Legal dimension:
    -   **Employment Law:**
        -   "What labor laws affect your operations?"
        -   "Any changes to minimum wage, benefits, unions?"
    -   **Consumer Protection:**
        -   "What consumer rights laws apply?"
        -   "Are regulations becoming stricter?"
    -   **Industry Regulations:**
        -   "What industry-specific regulations exist?"
        -   "Any upcoming compliance requirements?"
    -   **Data Privacy:**
        -   "What data protection laws apply? (GDPR, CCPA)"
        -   "How is privacy regulation evolving?"
    -   **Intellectual Property:**
        -   "How strong is IP protection?"
        -   "Any patent or copyright issues?"
    -   **Antitrust & Competition:**
        -   "What competition laws constrain you?"
        -   "Any merger review risks?"
-   Assess impact and trends.
-   Wait for user responses.

### Step 8: Environmental Factors Analysis
-   Guide Environmental dimension:
    -   **Climate Change:**
        -   "How does climate change affect your business?"
        -   "Any physical risks? (extreme weather, sea level rise)"
    -   **Sustainability Requirements:**
        -   "What environmental regulations exist?"
        -   "Are ESG (Environmental, Social, Governance) demands increasing?"
    -   **Carbon Footprint:**
        -   "What are carbon emission requirements?"
        -   "Any carbon pricing or taxes?"
    -   **Resource Scarcity:**
        -   "Are critical resources becoming scarce? (water, rare earth metals)"
        -   "How vulnerable is your supply chain?"
    -   **Circular Economy:**
        -   "What recycling or waste reduction pressures exist?"
        -   "Are circular business models emerging?"
    -   **Stakeholder Expectations:**
        -   "What environmental commitments are customers/investors demanding?"
        -   "How important is sustainability to your brand?"
-   Assess impact and trends.
-   Wait for user responses.

### Step 9: Impact Prioritization
-   Prioritize factors:
    -   "Let's identify the most critical factors across all PESTLE dimensions:"
    -   "Which 5-10 factors have the **highest impact** on your strategy?"
    -   "Which factors are **changing most rapidly**?"
    -   "Which factors present the biggest **opportunities**?"
    -   "Which factors pose the greatest **threats**?"
-   Create priority matrix combining impact and urgency.
-   Wait for user responses.

### Step 10: Strategic Implications
-   Develop strategic responses:
    -   "For each high-priority factor:"
        -   "How should you respond?"
        -   "What opportunities can you capture?"
        -   "What risks must you mitigate?"
        -   "What strategic adjustments are needed?"
    -   "Are there scenarios where multiple factors combine to create major shifts?"
-   Wait for user responses.

### Step 11: Monitoring Plan
-   Establish ongoing monitoring:
    -   "Which factors require continuous monitoring?"
    -   "What indicators will you track?"
    -   "How often will you update this PEST analysis? (quarterly, semi-annually)"
    -   "Who is responsible for environmental scanning?"
-   Wait for user responses.

### Step 12: Create Comprehensive PEST/PESTLE Analysis Document

Produce a detailed PEST/PESTLE analysis with the following structure:

---
# PEST/PESTLE Analysis: [Industry Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Industry/Sector:** [industry_name]  
**Market Focus:** [market_context]  
**Geographic Region:** [region]  
**Analysis Timeframe:** [Current + X-year outlook]

---

## Executive Summary

### Analysis Scope
[Brief description of industry, market, and geographic focus]

### Key Findings
1. [Most significant finding 1]
2. [Most significant finding 2]
3. [Most significant finding 3]

### Strategic Implications
- **Biggest Opportunity:** [Description]
- **Biggest Threat:** [Description]
- **Required Actions:** [Summary of recommended responses]

---

## POLITICAL FACTORS

### Overview
[Brief context on political environment]

### Government Stability & Policy
**Current State:**
- [Description of political stability]
- [Key government policies affecting industry]

**Trends:**
- [Emerging political trends]
- [Upcoming elections or leadership changes]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Improving / Stable / Declining
- **Strategic Implication:** [How this affects strategy]

### Regulatory Environment
**Current Regulations:**
- [Key regulations affecting industry]
- [Compliance requirements]

**Pending Changes:**
- [Proposed regulatory changes]
- [Timeline for implementation]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Tightening / Stable / Loosening
- **Strategic Implication:** [Response required]

### Trade Policies
**Current Situation:**
- [Trade agreements affecting industry]
- [Tariffs and trade barriers]

**Trends:**
- [Trade policy changes]
- [Protectionism vs. liberalization trends]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Favorable / Neutral / Unfavorable
- **Strategic Implication:** [Market access implications]

### Taxation
**Current Tax Environment:**
- [Corporate tax rates]
- [Industry-specific taxes]

**Anticipated Changes:**
- [Proposed tax reforms]
- [Digital services taxes, carbon taxes]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Increasing / Stable / Decreasing
- **Strategic Implication:** [Profitability impact]

### Political Risk Assessment
**Risk Factors:**
- [Political instability risks]
- [Corruption index]
- [Nationalization risk]

**Mitigation Strategies:**
- [How to manage political risk]

---

## ECONOMIC FACTORS

### Overview
[Economic context and outlook]

### Economic Growth
**Current Performance:**
- GDP Growth Rate: [X%]
- Economic Cycle Phase: [Expansion/Peak/Contraction/Trough]

**Forecast:**
- [Next 1-3 year economic outlook]
- [Key drivers of growth/decline]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Improving / Stable / Declining
- **Strategic Implication:** [Demand implications]

### Inflation & Interest Rates
**Current Metrics:**
- Inflation Rate: [X%]
- Central Bank Interest Rate: [X%]
- Real Interest Rate: [X%]

**Monetary Policy:**
- [Current policy stance: expansionary/neutral/contractionary]
- [Expected rate changes]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Rising / Stable / Falling
- **Strategic Implication:** [Cost of capital, input cost implications]

### Exchange Rates (if applicable)
**Currency Exposure:**
- [Key currency pairs]
- [Current exchange rates]
- [Volatility assessment]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Strengthening / Stable / Weakening
- **Strategic Implication:** [Pricing, margin implications]

### Employment & Labor Market
**Current Situation:**
- Unemployment Rate: [X%]
- Labor Force Participation: [X%]
- Wage Growth: [X%]

**Labor Market Dynamics:**
- [Talent availability]
- [Skills gap issues]
- [Remote work trends]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Favorable / Neutral / Unfavorable
- **Strategic Implication:** [Talent acquisition, labor cost implications]

### Consumer Spending Patterns
**Current Trends:**
- Consumer Confidence Index: [X]
- Discretionary Spending: [Trend]
- Savings Rate: [X%]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Increasing / Stable / Decreasing
- **Strategic Implication:** [Demand forecast]

---

## SOCIAL FACTORS

### Overview
[Social and demographic context]

### Demographics
**Population Trends:**
- Population Growth: [X%]
- Age Distribution: [Breakdown]
- Urbanization Rate: [X%]

**Key Demographic Shifts:**
- [Aging population implications]
- [Household composition changes]
- [Migration patterns]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** [Direction of change]
- **Strategic Implication:** [Target market implications]

### Cultural Attitudes & Values
**Current Culture:**
- [Dominant cultural values]
- [Attitudes toward innovation, risk, technology]

**Shifting Norms:**
- [Changing social attitudes]
- [Generation differences]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** [Cultural shift direction]
- **Strategic Implication:** [Product positioning, messaging]

### Lifestyle Trends
**Major Trends:**
- [Health & wellness focus]
- [Work-life balance priorities]
- [Sustainability consciousness]
- [Digital lifestyle adoption]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** [Strengthening / Emerging / Fading]
- **Strategic Implication:** [Product/service adaptation needs]

### Education & Skills
**Education Levels:**
- [Education attainment statistics]
- [Skill availability]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Improving / Stable / Declining
- **Strategic Implication:** [Workforce quality, customer sophistication]

---

## TECHNOLOGICAL FACTORS

### Overview
[Technology landscape and innovation pace]

### Innovation & Disruption
**Emerging Technologies:**
- [AI/ML applications in industry]
- [Blockchain, IoT, 5G relevance]
- [Quantum computing horizon]

**Disruption Risk:**
- [Technologies that could disrupt business model]
- [Timeline for disruption]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Accelerating / Steady / Slowing
- **Strategic Implication:** [Innovation requirements]

### R&D Investment
**Industry R&D:**
- Industry R&D Spend: [% of revenue]
- Key Technology Leaders: [Companies]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Increasing / Stable / Decreasing
- **Strategic Implication:** [Competitive pressure to innovate]

### Automation & AI
**Automation Potential:**
- [Processes being automated]
- [Impact on labor needs]
- [AI application opportunities]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Rapid / Gradual / Slow
- **Strategic Implication:** [Operational efficiency, workforce planning]

### Digital Transformation
**Digitalization Status:**
- [Digital maturity of industry]
- [Platform/ecosystem dynamics]
- [Digital business model opportunities]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** [Digital shift pace]
- **Strategic Implication:** [Digital strategy requirements]

### Technology Infrastructure
**Current State:**
- [5G/Broadband availability]
- [Cloud adoption]
- [Digital payment infrastructure]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Improving / Stable / Limited
- **Strategic Implication:** [Technology enablement, market readiness]

---

## LEGAL FACTORS

### Overview
[Legal and regulatory landscape]

### Employment & Labor Law
**Current Regulations:**
- [Key labor laws]
- [Minimum wage, working hours]
- [Union presence]

**Pending Changes:**
- [Proposed changes]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** More Restrictive / Stable / More Flexible
- **Strategic Implication:** [HR policy, cost implications]

### Consumer Protection
**Key Regulations:**
- [Consumer rights laws]
- [Product safety requirements]
- [Warranty/return policies]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Strengthening / Stable / Weakening
- **Strategic Implication:** [Compliance costs, product requirements]

### Industry-Specific Regulations
**Major Requirements:**
- [Industry regulations]
- [Licensing requirements]
- [Quality standards]

**Compliance Burden:**
- [Regulatory complexity]
- [Compliance costs]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Increasing / Stable / Decreasing
- **Strategic Implication:** [Barriers to entry, competitive advantage]

### Data Privacy & Security
**Applicable Laws:**
- [GDPR, CCPA, local laws]
- [Data localization requirements]

**Enforcement:**
- [Penalty severity]
- [Enforcement trends]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Stricter / Stable / More Lenient
- **Strategic Implication:** [Data strategy, compliance investment]

### Intellectual Property
**IP Protection:**
- [Patent/copyright strength]
- [Enforcement effectiveness]
- [Counterfeit/piracy issues]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Strengthening / Stable / Weakening
- **Strategic Implication:** [Innovation protection, competitive dynamics]

---

## ENVIRONMENTAL FACTORS

### Overview
[Environmental context and sustainability landscape]

### Climate Change & Physical Risks
**Climate Impacts:**
- [Physical risks: extreme weather, sea level]
- [Supply chain vulnerabilities]
- [Operational disruptions]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Worsening / Stable / Improving
- **Strategic Implication:** [Risk mitigation, adaptation needs]

### Environmental Regulations
**Current Requirements:**
- [Emission standards]
- [Waste management regulations]
- [Pollution controls]

**Pending Changes:**
- [Upcoming regulations]
- [Phase-in timelines]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Tightening / Stable / Loosening
- **Strategic Implication:** [Compliance investment, operational changes]

### Carbon Footprint & Emissions
**Current Situation:**
- [Industry carbon intensity]
- [Carbon pricing mechanisms]
- [Net-zero commitments]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Increasing Pressure / Stable / Decreasing Pressure
- **Strategic Implication:** [Decarbonization strategy, costs]

### Resource Scarcity
**Critical Resources:**
- [Water, energy, raw materials]
- [Scarcity risks]
- [Alternative sourcing options]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** More Scarce / Stable / More Abundant
- **Strategic Implication:** [Supply chain resilience, cost volatility]

### Circular Economy & Sustainability
**Circular Trends:**
- [Recycling requirements]
- [Extended producer responsibility]
- [Circular business model opportunities]

**Stakeholder Expectations:**
- [Customer sustainability demands]
- [Investor ESG requirements]
- [Employee values]

**Impact Assessment:**
- **Impact Level:** High / Medium / Low
- **Trend:** Increasing / Stable / Decreasing
- **Strategic Implication:** [Business model innovation, brand positioning]

---

## PRIORITY FACTORS MATRIX

### High Impact & High Urgency (Act Now)
1. [Factor 1 - PESTLE category]
   - **Impact:** [Description]
   - **Action Required:** [Immediate response]

2. [Factor 2]
3. [Factor 3]

### High Impact & Medium Urgency (Plan & Monitor)
1. [Factor]
2. [Factor]

### Medium Impact & High Urgency (Quick Response)
1. [Factor]

### Lower Priority (Monitor)
[List of factors to track but not immediate action]

---

## STRATEGIC IMPLICATIONS

### Opportunities
1. **[Opportunity 1]**
   - **Driven by:** [PESTLE factors]
   - **Potential Impact:** [Business benefit]
   - **Action:** [How to capture]

2. **[Opportunity 2]**
3. **[Opportunity 3]**

### Threats
1. **[Threat 1]**
   - **Driven by:** [PESTLE factors]
   - **Potential Impact:** [Business risk]
   - **Mitigation:** [How to address]

2. **[Threat 2]**
3. **[Threat 3]**

### Strategic Adjustments Required
- [ ] [Adjustment 1: e.g., Diversify supply chain]
- [ ] [Adjustment 2: e.g., Invest in sustainability]
- [ ] [Adjustment 3: e.g., Accelerate digital transformation]
- [ ] [Adjustment 4: e.g., Expand to regions with favorable conditions]

---

## SCENARIO PLANNING

### Optimistic Scenario
**If favorable factors align:**
- [Scenario description]
- [Strategic implications]

### Base Case Scenario
**Most likely outcome:**
- [Scenario description]
- [Strategic implications]

### Pessimistic Scenario
**If unfavorable factors align:**
- [Scenario description]
- [Strategic implications]

---

## MONITORING PLAN

### Key Indicators to Track

| Factor Category | Indicator | Current Value | Target/Threshold | Review Frequency | Owner |
|-----------------|-----------|---------------|------------------|------------------|-------|
| Political | [Indicator] | [Value] | [Target] | [Frequency] | [Owner] |
| Economic | [Indicator] | [Value] | [Target] | [Frequency] | [Owner] |
| Social | [Indicator] | [Value] | [Target] | [Frequency] | [Owner] |
| Technological | [Indicator] | [Value] | [Target] | [Frequency] | [Owner] |
| Legal | [Indicator] | [Value] | [Target] | [Frequency] | [Owner] |
| Environmental | [Indicator] | [Value] | [Target] | [Frequency] | [Owner] |

### Update Schedule
- **Full PEST/PESTLE Review:** [Quarterly / Semi-annually / Annually]
- **Rapid Scan Updates:** [Monthly monitoring of high-priority factors]
- **Responsible Team:** [Department/Role]

---

## APPENDIX

### Data Sources
- [Source 1: e.g., Government statistics]
- [Source 2: e.g., Industry reports]
- [Source 3: e.g., Academic research]

### References
- Aguilar, F. J. (1967). *Scanning the Business Environment*.
- [Industry-specific sources]

---

*PEST/PESTLE Analysis generated by NioPD Strategic Analysis*

---

### Step 13: Save the PEST/PESTLE Analysis
- Generate filename: `[YYYYMMDD]-[industry_slug]-pest-analysis-v[version].md`
- Save to: `niopd-workspace/reports/[filename]`

### Step 14: Confirm and Conclude
- Confirm: "✅ I've created a comprehensive PEST/PESTLE analysis for the **<industry>** industry."
- Provide file path: `niopd-workspace/reports/[YYYYMMDD]-[industry_slug]-pest-analysis-v[version].md`
- Suggest next steps:
    - "Use `/niopd:ST:swot` to convert external factors into opportunities/threats."
    - "Use `/niopd:ST:porters-five-forces` for industry competitive analysis."
    - "Update this PEST analysis quarterly to track environmental changes."

## Error Handling
- **Too Broad Scope:** If analysis spans too many regions/markets, help user focus on most strategic geography.
- **Lack of Data:** If user has insufficient data, point to public sources (World Bank, OECD, industry associations) and suggest desk research.
- **Analysis Paralysis:** If user gets overwhelmed by factors, help prioritize top 5-10 most impactful factors to focus on.
- **Static Analysis:** Remind user that PEST is a snapshot; emphasize importance of ongoing monitoring and scenario planning for dynamic factors.
- **Missing Strategic Connection:** If analysis doesn't connect to strategy, guide user to translate factors into actionable opportunities/threats and strategic responses.

In all cases, maintain an analytical tone, encourage evidence-based assessment, and help the user move from environmental scanning to strategic action.
