---
argument-hint: [--for=<initiative_name>|--for=<product_name>] [--method=<analysis_method>]
description: Analyzes customer satisfaction data to identify improvement opportunities and measure success. Auto-detects initiative/product name from current directory if not specified.
---

# Command: /niopd:UR:satisfaction

This command analyzes customer satisfaction data to identify improvement opportunities, measure success, and track trends over time.

## Theoretical Foundation

### Origin and Development
Customer satisfaction measurement integrates multiple frameworks:

1. **Net Promoter Score (NPS)** - Developed by **Fred Reichheld** at Bain & Company (2003)
2. **Customer Satisfaction Score (CSAT)** - Traditional satisfaction measurement
3. **Customer Effort Score (CES)** - Introduced by CEB (now Gartner) focusing on ease of experience

### Core Principle
The fundamental approach is **multi-dimensional satisfaction measurement**: Rather than relying on a single metric, comprehensive satisfaction analysis uses multiple measures to understand different aspects of customer experience and predict loyalty.

### Primary Satisfaction Metrics

**1. Net Promoter Score (NPS)**:
- **Question**: "How likely are you to recommend us to a friend?" (0-10)
- **Calculation**: % Promoters (9-10) - % Detractors (0-6)
- **Strengths**: Predicts loyalty and growth; simple; industry benchmarks available
- **Range**: -100 to +100
- **Good Score**: 50+ considered excellent

**2. Customer Satisfaction Score (CSAT)**:
- **Question**: "How satisfied are you with [product/experience]?" (1-5)
- **Calculation**: (Satisfied + Very Satisfied) / Total Responses × 100
- **Strengths**: Measures transaction-specific satisfaction; easy to understand
- **Good Score**: 80%+ typically considered good

**3. Customer Effort Score (CES)**:
- **Question**: "How easy was it to [complete task]?" (1-7)
- **Calculation**: % who found it easy (6-7 on 7-point scale)
- **Strengths**: Predicts repurchase and loyalty; identifies friction
- **Insight**: Low effort → higher loyalty than high satisfaction

### Satisfaction Analysis Framework
1. **Metric Collection**: Gather NPS, CSAT, CES data
2. **Segmentation**: Analyze by customer type, feature, journey stage
3. **Driver Analysis**: Identify what influences satisfaction
4. **Trend Analysis**: Track changes over time
5. **Benchmarking**: Compare to industry standards
6. **Action Planning**: Convert insights to improvements

### When to Use
- Regular satisfaction tracking (quarterly, post-release)
- After major product changes
- Competitive benchmarking
- Customer health monitoring
- Churn prediction and prevention
- ROI justification for improvements

### Satisfaction vs. Loyalty
- **Satisfaction**: Current contentment level
- **Loyalty**: Future behavioral intent (repurchase, recommend)
- **Key Insight**: Satisfaction doesn't always predict loyalty

### Related Methodologies
- **Customer Lifetime Value (CLV)**: Predict economic value of satisfaction
- **Sentiment Analysis**: Analyze qualitative feedback
- **Churn Analysis**: Understand satisfaction's role in retention
- **Voice of Customer (VOC)**: Broader feedback program

## Usage
`/niopd:UR:satisfaction [--for=<initiative_name>|--for=<product_name>] [--method=<analysis_method>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative/product name.

**Examples:**
```bash
# Explicit initiative with method
/niopd:UR:satisfaction --for=dark-mode-feature --method=nps

# Auto-detect initiative, specify method
cd dark-mode-feature
/niopd:UR:satisfaction --method=nps  # Uses "dark-mode-feature"

# Auto-detect initiative, comprehensive analysis
cd dark-mode-feature
/niopd:UR:satisfaction  # Uses "dark-mode-feature", comprehensive approach
```

## Preflight Checklist

1.  **Determine Initiative/Product Name:**
    -   If `--for=<initiative_name>` or `--for=<product_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative/product name from current directory: `<directory_name>`"
    -   Store the determined name for use in all subsequent steps

2.  **Validate Inputs:**
    -   Check if `--for` argument is provided to specify the initiative or product.
    -   If `--for` is not provided, ask the user to specify what they want to analyze satisfaction for.
    -   Check if `--method` argument is provided to specify the analysis approach.
    -   If `--method` is not provided, default to comprehensive satisfaction analysis.

## Instructions

You are a specialized AI expert in customer satisfaction analysis and experience optimization. Your goal is to analyze satisfaction data to provide actionable insights for improvement.

### Step 1: Acknowledge and Gather Context
-   Acknowledge the request: "I'll analyze customer satisfaction for **<initiative_or_product_name>** using **<analysis_method>** approach."
-   If a specific initiative or product is provided with `--for`, use that as the focus.
-   If not provided, ask the user: "Which initiative or product would you like to analyze for customer satisfaction?"
-   If an analysis method is provided with `--method`, use that approach.
-   If not provided, default to comprehensive satisfaction analysis and inform the user.

### Step 2: Data Source Identification
-   Identify available satisfaction data sources:
    -   Customer surveys (NPS, CSAT, CES)
    -   User feedback and reviews
    -   Support ticket analysis
    -   Usage analytics and behavioral data
    -   Social media sentiment
    -   Focus group and interview insights
    -   Competitive benchmarking data
-   Determine data quality and completeness:
    -   Sample sizes and response rates
    -   Data recency and relevance
    -   Collection methodologies
    -   Potential biases and limitations

### Step 3: Analysis Method Selection
Available analysis methods include:
1.  **Comprehensive Analysis** - Full satisfaction assessment with multiple metrics
2.  **NPS Deep Dive** - Net Promoter Score focused analysis
3.  **CSAT Evaluation** - Customer Satisfaction Score analysis
4.  **CES Assessment** - Customer Effort Score evaluation
5.  **Trend Analysis** - Historical satisfaction pattern review
6.  **Segment Analysis** - Satisfaction by customer segments
7.  **Driver Analysis** - Key satisfaction factor identification

#### Default: Comprehensive Analysis Approach
-   Multi-metric satisfaction assessment
-   Correlation and causation analysis
-   Benchmarking against industry standards
-   Trend identification and prediction

### Step 4: Satisfaction Metric Analysis
Analyze key satisfaction metrics:

#### Net Promoter Score (NPS)
-   Calculate overall NPS:
    -   Promoters (9-10 ratings)
    -   Passives (7-8 ratings)
    -   Detractors (0-6 ratings)
-   Benchmark against industry standards
-   Analyze NPS trends over time
-   Identify key drivers of promoter and detractor scores

#### Customer Satisfaction Score (CSAT)
-   Calculate average satisfaction ratings
-   Analyze satisfaction by feature or aspect
-   Identify satisfaction gaps and opportunities
-   Compare satisfaction across customer segments

#### Customer Effort Score (CES)
-   Measure ease of use and interaction
-   Identify high-effort pain points
-   Analyze effort reduction opportunities
-   Correlate effort with satisfaction and loyalty

### Step 5: Customer Segment Analysis
-   Analyze satisfaction by customer segments:
    -   Demographic segments (age, location, etc.)
    -   Behavioral segments (usage patterns, frequency)
    -   Lifecycle segments (new, active, churned)
    -   Value segments (high, medium, low value)
-   Identify segment-specific satisfaction patterns:
    -   Unique needs and expectations
    -   Segment-specific pain points
    -   Tailored improvement opportunities

### Step 6: Qualitative Feedback Analysis
-   Analyze open-ended feedback:
    -   Customer comments and suggestions
    -   Support ticket themes and issues
    -   Review sentiment and common themes
    -   Social media mentions and discussions
-   Identify key themes and patterns:
    -   Recurring praise and complaints
    -   Specific feature feedback
    -   Usability and experience insights
    -   Competitive mentions and comparisons

### Step 7: Satisfaction Driver Analysis
-   Identify key satisfaction drivers:
    -   Feature performance and reliability
    -   User interface and experience
    -   Customer support and service
    -   Pricing and value perception
    -   Documentation and resources
-   Determine driver importance and performance:
    -   How important each factor is to satisfaction
    -   How well the product performs on each factor
    -   Gap analysis between importance and performance

### Step 8: Benchmarking and Competitive Analysis
-   Benchmark against industry standards:
    -   Industry average satisfaction scores
    -   Best-in-class performance benchmarks
    -   Competitive positioning analysis
-   Identify performance gaps:
    -   Areas where performance lags behind benchmarks
    -   Opportunities for differentiation
    -   Competitive advantages to leverage

### Step 9: Trend Analysis
-   Analyze satisfaction trends over time:
    -   Score improvements or declines
    -   Seasonal and cyclical patterns
    -   Impact of product releases and changes
    -   Correlation with business metrics
-   Predict future satisfaction patterns:
    -   Trend extrapolation and forecasting
    -   Early warning signal identification
    -   Proactive improvement opportunities

### Step 10: Improvement Opportunity Identification
-   Prioritize improvement opportunities:
    -   Impact on satisfaction scores
    -   Feasibility of implementation
    -   Resource requirements
    -   Alignment with business goals
-   Categorize opportunities:
    -   Quick wins with immediate impact
    -   Strategic initiatives with long-term value
    -   Innovation opportunities for differentiation
    -   Process improvements for efficiency

### Step 11: Customer Satisfaction Report Generation
Produce a markdown report with the following structure:

---
# Customer Satisfaction Analysis: [Initiative/Product Name]

## Executive Summary
*A high-level overview of satisfaction findings and key recommendations*

## Analysis Context
- **Subject:** [Initiative or product analyzed]
- **Analysis Method:** [Comprehensive, NPS, CSAT, or other]
- **Analysis Date:** [Current date]
- **Data Period:** [Time period covered by analysis]
- **Data Sources:** [Primary sources used]

## Satisfaction Metrics Overview
### Net Promoter Score (NPS)
- **Overall NPS:** [Score and industry comparison]
- **Promoters (9-10):** [Percentage and count]
- **Passives (7-8):** [Percentage and count]
- **Detractors (0-6):** [Percentage and count]
- **Trend:** [Improvement or decline over time]

### Customer Satisfaction Score (CSAT)
- **Overall CSAT:** [Average score and benchmark]
- **By Feature/Aspect:** [Scores for key areas]
- **Trend:** [Improvement or decline over time]
- **Segment Variations:** [Differences by customer type]

### Customer Effort Score (CES)
- **Overall CES:** [Average effort rating]
- **High-effort Pain Points:** [Areas requiring too much effort]
- **Low-effort Successes:** [Areas that are easy to use]
- **Correlation with Satisfaction:** [How effort relates to other metrics]

## Customer Segment Analysis
### [Segment Name]
- **Satisfaction Score:** [NPS/CSAT for this segment]
- **Key Characteristics:** [Demographics or behaviors]
- **Unique Insights:** [Segment-specific findings]
- **Improvement Opportunities:** [Tailored recommendations]

[Repeat for each key segment]

## Qualitative Insights
### Key Themes from Feedback
#### Positive Feedback Themes
1. **[Theme]:** [Description and frequency]
2. **[Theme]:** [Description and frequency]

#### Improvement Opportunity Themes
1. **[Theme]:** [Description and frequency]
2. **[Theme]:** [Description and frequency]

### Representative Customer Quotes
#### Praise
- *"[Direct quote from satisfied customer]"*
- *"[Direct quote from satisfied customer]"*

#### Constructive Feedback
- *"[Direct quote with improvement suggestion]"*
- *"[Direct quote with improvement suggestion]"*

## Satisfaction Driver Analysis
### Key Satisfaction Drivers
| Driver | Importance | Performance | Gap |
|--------|------------|-------------|-----|
| [Driver Name] | [High/Medium/Low] | [Score] | [Gap size] |
| [Driver Name] | [High/Medium/Low] | [Score] | [Gap size] |

### Driver Insights
1. **[Driver Name]:** [Analysis and recommendations]
2. **[Driver Name]:** [Analysis and recommendations]

## Benchmarking and Competitive Analysis
### Industry Comparison
- **NPS vs. Industry Average:** [Your score vs. benchmark]
- **CSAT vs. Best-in-Class:** [Your score vs. leaders]
- **Key Differentiators:** [Where you excel or lag]

### Competitive Positioning
- **Strengths:** [Areas where you outperform competitors]
- **Weaknesses:** [Areas where competitors perform better]
- **Opportunities:** [Gaps to exploit for competitive advantage]

## Trend Analysis
### Historical Trends
- **NPS Trend:** [Graph or description of changes over time]
- **CSAT Trend:** [Graph or description of changes over time]
- **Key Milestones:** [Events that impacted satisfaction]

### Predictive Insights
- **Forecast:** [Expected future satisfaction patterns]
- **Early Warning Signals:** [Indicators to monitor]
- **Proactive Opportunities:** [Actions to take based on trends]

## Improvement Recommendations

### Immediate Actions (0-3 months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Impact:** [Expected improvement in satisfaction]
   - **Effort:** [Low/Medium/High implementation effort]
   - **Resources Needed:** [Personnel, budget, tools]

2. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Impact:** [Expected improvement in satisfaction]
   - **Effort:** [Low/Medium/High implementation effort]
   - **Resources Needed:** [Personnel, budget, tools]

### Medium-term Initiatives (3-12 months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Impact:** [Expected improvement in satisfaction]
   - **Effort:** [Low/Medium/High implementation effort]
   - **Resources Needed:** [Personnel, budget, tools]

2. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Impact:** [Expected improvement in satisfaction]
   - **Effort:** [Low/Medium/High implementation effort]
   - **Resources Needed:** [Personnel, budget, tools]

### Long-term Strategic Moves (12+ months)
1. **[Recommendation]:** [Action, rationale, and expected outcome]
   - **Impact:** [Expected improvement in satisfaction]
   - **Effort:** [Low/Medium/High implementation effort]
   - **Resources Needed:** [Personnel, budget, tools]

## Implementation Roadmap
### Phase 1: Foundation (0-3 months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

### Phase 2: Development (3-12 months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

### Phase 3: Optimization (12+ months)
- **Key Activities:** [Primary actions]
- **Resource Requirements:** [Personnel, budget, timeline]
- **Success Metrics:** [How to measure progress]

## Success Metrics and Monitoring
### Key Performance Indicators
- **NPS Target:** [Goal and measurement approach]
- **CSAT Target:** [Goal and measurement approach]
- **CES Target:** [Goal and measurement approach]
- **Customer Retention:** [Target and measurement]

### Monitoring Framework
- **Regular Reviews:** [Frequency and participants]
- **Real-time Monitoring:** [Tools and dashboards]
- **Feedback Loops:** [How insights inform improvements]
- **Reporting Schedule:** [When updates are shared]

## Data Sources and Methodology
- **Analysis Methods:** [How the analysis was conducted]
- **Sources:** [List of sources consulted]
- **Limitations:** [Known limitations of the analysis]
- **Validation Approach:** [How insights were verified]

---

### Step 12: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_slug]-satisfaction-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 13: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the customer satisfaction analysis for **<initiative_or_product_name>**."
- Provide the path to the file: "You can view the detailed satisfaction analysis here: `niopd-workspace/reports/[YYYYMMDD]-[initiative_slug]-satisfaction-v[version].md`"
- Suggest next steps: "Consider using `/niopd:UR:journey` to map experiences leading to these satisfaction scores or `/niopd:PM:kpis` to track satisfaction as a key metric."

## Error Handling
- **Missing Subject:** If no subject is specified for satisfaction analysis, ask the user to clarify what they want to analyze.
- **Method Issues:** If an invalid analysis method is specified, list available options and ask for selection.
- **Insufficient Data:** If adequate satisfaction data cannot be found, explain the limitations and suggest alternative approaches.
- **Data Quality Issues:** If data quality is poor, highlight limitations and recommend data collection improvements.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.