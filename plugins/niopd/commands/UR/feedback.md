---
argument-hint: [--from=<feedback_filename>] [--for=<initiative_name>]
description: Analyzes a feedback file and generates a summary report. Auto-detects initiative name from current directory if not specified.
---

# Command: /niopd:UR:feedback

This command analyzes an imported feedback file and generates a summary report.

## Theoretical Foundation

### Origin and Development
Feedback analysis synthesizes principles from multiple disciplines:

1. **Thematic Analysis** - Systematic approach to identifying patterns in qualitative data (Braun & Clarke, 2006)
2. **Sentiment Analysis** - Computational analysis of emotions and opinions in text
3. **Voice of Customer (VOC)** - Systematic capture and analysis of customer feedback for improvement

### Core Principle
The fundamental approach is **systematic qualitative analysis**: Transforming unstructured, raw customer feedback into structured insights through coding, categorization, and thematic analysis to inform product decisions.

### Analysis Process
1. **Data Preprocessing**: Cleaning and normalizing feedback text
2. **Theme Identification**: Grouping related feedback into meaningful categories
3. **Sentiment Analysis**: Assessing emotional tone and intensity
4. **Quantification**: Measuring frequency and impact of themes
5. **Actionable Insights**: Translating findings into product recommendations

### Feedback Categories
- **Pain Points**: Problems and frustrations
- **Feature Requests**: Desired capabilities
- **Positive Feedback**: What users appreciate
- **Usage Patterns**: Behavioral insights
- **Competitive Mentions**: Market positioning insights

### When to Use
- After collecting customer surveys or feedback forms
- Processing support ticket themes
- Analyzing app store reviews or social media comments
- Regular feedback analysis cycles (weekly, monthly, quarterly)
- Pre-roadmap planning to identify priorities

### Related Methodologies
- **Grounded Theory**: Theory development from data (Glaser & Strauss, 1967)
- **Content Analysis**: Systematic text categorization
- **Natural Language Processing (NLP)**: Automated text analysis
- **Customer Feedback Loop**: Continuous improvement cycle

## Usage
`/niopd:UR:feedback [--from=<feedback_filename>] [--for=<initiative_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative name.

**Examples:**
```bash
# Explicit initiative name and file
/niopd:UR:feedback --from=user-feedback.csv --for=dark-mode-feature

# Auto-detect initiative from current directory
cd dark-mode-feature
/niopd:UR:feedback --from=user-feedback.csv  # Uses "dark-mode-feature"

# Auto-detect both file and initiative
cd dark-mode-feature
/niopd:UR:feedback  # Auto-finds feedback file in sources/
```

## Preflight Checklist

1.  **Check Configuration File:**
    - Check if `niopd-workspace/config/niopd.config.json` exists
    - If it exists, load and apply configuration settings
    - If not, continue with default behavior

2.  **Determine Initiative Name:**
    -   If `--for=<initiative_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative name from current directory: `<directory_name>`"
    -   Store the determined name as `<initiative_name>` for use in all subsequent steps

3.  **Check Feedback File:****
    -   If `--from` is provided, verify that the file `niopd-workspace/sources/<feedback_filename>` exists.
    -   If `--from` is not provided, search for files in `niopd-workspace/sources/` that contain "feedback" or "用户反馈" in their names.
    -   If multiple files are found, ask the user to specify which file to use.
    -   If no files are found, inform the user: "❌ I couldn't find any feedback files in `niopd-workspace/sources/`. Please make sure feedback files exist or provide a specific file with `--from=<filename>`."

## Instructions

You are a specialized AI expert in analyzing and synthesizing user feedback. Your goal is to process large volumes of raw, unstructured feedback and transform it into a comprehensive, actionable summary for a Product Manager.

### Core Principle
Always ensure that your analysis is grounded in the core principle of systematic qualitative analysis: transforming unstructured, raw customer feedback into structured insights through coding, categorization, and thematic analysis to inform product decisions.

### Step 1: Acknowledge and Prepare
-   Acknowledge the request: "On it! I'll analyze feedback for the **<initiative_name>** initiative."
-   If a specific file was provided with `--from`, use that file.
-   If no file was specified, search for feedback files in `niopd-workspace/sources/`:
    -   List all files in `niopd-workspace/sources/`
    -   Filter for files containing "feedback" or "用户反馈" in their names (case-insensitive)
    -   If exactly one file is found, use it automatically
    -   If multiple files are found, list them and ask the user to specify which one to use
    -   If no files are found, inform the user and stop the process
-   If configuration file exists and contains initiative name or feedback file settings, use those values as defaults
-   If language setting in configuration is Chinese, respond in Chinese; otherwise, respond in English

### Step 2: File Analysis & Validation
- Determine the file format (CSV, JSON, TXT, etc.) and structure.
- For structured formats (CSV/JSON), identify relevant columns/fields containing feedback text.
- For unstructured formats, parse the entire content as feedback text.
- Validate that the file contains sufficient data for meaningful analysis (at least 5 feedback items).

### Step 3: Data Preprocessing
- Clean and normalize the feedback text (remove excessive whitespace, standardize punctuation).
- Identify and separate distinct feedback items or responses.
- Detect and handle duplicates or near-duplicates.
- Identify any structured metadata (dates, user IDs, ratings, categories) that can enhance analysis.

### Step 4: Theme Identification & Categorization
- Apply advanced thematic analysis to group related pieces of feedback into meaningful themes.
- A theme should represent a recurring topic or idea mentioned by multiple users (e.g., "Difficulty with UI Navigation," "Request for Dark Mode," "Performance Issues on Mobile").
- For each theme, identify 3-5 representative user quotes that best exemplify the theme.
- Classify each theme into one of the following categories:
    - **Pain Point:** A problem or frustration users are experiencing.
    - **Feature Request:** A specific feature or improvement users are asking for.
    - **Positive Feedback:** Something users like about the product.
    - **Usage Pattern:** Insights about how users interact with the product.
    - **Competitive Mention:** References to competitors or comparisons with other products.
    - **Other Insight:** Any other valuable information that doesn't fit the above categories.

### Step 5: Sentiment & Intensity Analysis
- Assess the sentiment of each feedback item (Positive, Neutral, Negative).
- Determine the intensity of sentiment (Low, Medium, High) for stronger emotions.
- Identify emotional keywords and phrases that indicate user passion or frustration.
- Calculate overall sentiment distribution across all feedback.

### Step 6: Quantification & Prioritization
- Count the frequency of each theme across all feedback items.
- Calculate the percentage of total feedback that each theme represents.
- Assess the business impact of each theme based on sentiment, frequency, and strategic relevance.
- Prioritize themes based on a combination of frequency, sentiment intensity, and business impact.

### Step 7: Contextual Enhancement
- Cross-reference themes with the initiative context to highlight particularly relevant insights.
- Identify any contradictions or conflicting feedback that may require further investigation.
- Extract user personas or behavioral patterns that emerge from the data.
- Note any seasonal, temporal, or demographic trends if metadata is available.

### Step 8: Actionable Insight Generation
- For each major theme, suggest 1-2 concrete, actionable next steps.
- Identify quick wins (low effort, high impact) and strategic opportunities (high investment, high impact).
- Highlight any critical issues that require immediate attention.
- Suggest areas for further research or data collection.

### Step 9: Feedback Summary Report Generation
Produce a markdown report with the following structure:

---
# Feedback Summary Report: [Feedback Source]

## Executive Summary
*A high-level overview of key insights and themes from [total_feedback_items] pieces of user feedback*

## Source Information
- **Feedback Source:** [Source name or description]
- **Collection Period:** [Time period or "Not specified"]
- **Total Items Analyzed:** [Number of feedback items processed]
- **Analysis Date:** [Current date]
- **Related Initiative:** [Initiative name]

## Key Themes & Insights

### 🔥 Top Pain Points

#### Pain Point 1: [Descriptive title]
- **Frequency:** [Number] mentions ([Percentage]% of feedback)
- **Severity:** [High/Medium/Low]
- **Description:** [Detailed description of the pain point]
- **User Quote:** *"Direct quote from user"*
- **Impact:** [Business impact description]

[Repeat for 2-3 major pain points]

### 🚀 Feature Requests

#### Request 1: [Descriptive title]
- **Frequency:** [Number] mentions ([Percentage]% of feedback)
- **Priority:** [High/Medium/Low]
- **Description:** [Detailed description of the feature request]
- **User Quote:** *"Direct quote from user"*
- **Business Value:** [Estimated business value]

[Repeat for 2-3 major feature requests]

### 💡 Positive Feedback & Strengths

#### Strength 1: [Area of strength]
- **Frequency:** [Number] mentions
- **Description:** [Description of what users like]
- **User Quote:** *"Direct quote from user"*

[Repeat for key strengths]

## User Sentiment Analysis

### Overall Sentiment Distribution
- **Positive:** [Percentage]% ([Number] items)
- **Neutral:** [Percentage]% ([Number] items)
- **Negative:** [Percentage]% ([Number] items)

[Additional sentiment breakdowns if relevant]

## Actionable Insights

### Immediate Actions (0-30 days)
1. **[Action Title]:** [Brief description]
   - **Impact:** [Expected impact]
   - **Effort:** [Low/Medium/High]
   - **Owner:** [Suggested role or team]

[Repeat for 1-2 immediate actions]

### Short-term Actions (1-3 months)
1. **[Action Title]:** [Brief description]
   - **Impact:** [Expected impact]
   - **Effort:** [Low/Medium/High]
   - **Dependencies:** [Key dependencies]

[Repeat for 1-2 short-term actions]

## Supporting Quotes

### Pain Points
- *"[Direct quote from user]"* - [User identifier if available]
- *"[Direct quote from user]"* - [User identifier if available]

### Feature Requests
- *"[Direct quote from user]"* - [User identifier if available]
- *"[Direct quote from user]"* - [User identifier if available]

### Positive Feedback
- *"[Direct quote from user]"* - [User identifier if available]
- *"[Direct quote from user]"* - [User identifier if available]

## Methodology & Data Quality

### Analysis Approach
- **Categorization Method:** Thematic analysis with manual validation
- **Sentiment Analysis:** Hybrid approach combining keyword detection with contextual understanding
- **Theme Identification:** Iterative grouping with frequency validation

### Data Quality Notes
- **Data Completeness:** [Percentage]% of expected data received
- **Known Limitations:** [Description of any data limitations]
- **Sample Bias:** [Assessment of potential bias in the feedback sample]

## Recommendations for Next Steps

### Research Priorities
1. **[Research Priority]:** [Brief description of what to investigate]
2. **[Research Priority]:** [Brief description of what to investigate]

### Product Development Focus
1. **[Development Focus Area]:** [Rationale for prioritizing this area]
2. **[Development Focus Area]:** [Rationale for prioritizing this area]

## Appendix

### Detailed Statistics
[Optional: Include detailed breakdowns if needed]

### Raw Data Summary
- **Source File:** [Original filename]
- **Processing Date:** [Date processed]
- **Analysis Tool:** NioPD Feedback Synthesizer v2.0

---

### Step 10: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_slug]-feedback-summary-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 11: Confirm and Conclude
- Confirm the action is complete: "✅ I've analyzed the feedback from `<feedback_filename>` and generated a summary report."
- Provide the path to the file: "You can view it here: `niopd-workspace/reports/[YYYYMMDD]-[initiative_slug]-feedback-summary-v[version].md`"

## Error Handling
- **Missing Arguments:** If required arguments are missing, ask the user for the required information.
- **File Not Found:** If the feedback file doesn't exist, inform the user and provide guidance.
- **Initiative Not Found:** If the initiative doesn't exist, suggest creating it first.
- **Multiple Files Found:** If multiple feedback files are found without a specific selection, list them and ask the user to choose.
- **No Files Found:** If no feedback files are found in the sources directory, inform the user.
- **Insufficient Data:** If the feedback file doesn't contain enough data for analysis, explain the requirement.
- **File Access Issues:** If there are permission issues, display appropriate error messages.