---
argument-hint: [--from=<behavior_filename>] [--for=<initiative_name>]
description: Analyzes user behavior data to identify product improvement opportunities. Auto-detects initiative name from current directory if not specified.
---

# Command: /niopd:UR:behavior

This command analyzes user behavior data (such as query details, user journey details) and generates a behavior summary report to identify product improvement opportunities.

## Theoretical Foundation

### Origin and Development
User behavior analysis integrates principles from:

1. **Behavioral Analytics** - Quantitative analysis of user actions and patterns
2. **Funnel Analysis** - Understanding user progression and drop-off
3. **Cohort Analysis** - Tracking user groups over time

### Core Principle
The fundamental approach is **data-driven user understanding**: Analyzing actual user behavior (what users DO) rather than what they say they do, to identify patterns, drop-offs, and opportunities that inform product optimization.

### Key Analysis Types

**1. Funnel Analysis**:
- Track user progression through steps
- Identify drop-off points
- Calculate conversion rates
- Optimize critical paths

**2. Path Analysis**:
- Understand common user flows
- Identify unexpected navigation patterns
- Discover shortcuts and workarounds
- Find dead ends and loops

**3. Cohort Analysis**:
- Compare user groups over time
- Track retention and engagement
- Identify successful user patterns
- Measure feature adoption

**4. Engagement Analysis**:
- Time spent on features/pages
- Feature usage frequency
- Session depth and duration
- Return visit patterns

### Behavior Metrics
- **Activation Rate**: % completing key actions
- **Engagement Score**: Frequency × Breadth × Depth
- **Drop-off Rate**: % abandoning at each step
- **Time on Task**: Duration for specific actions
- **Error Rate**: Frequency of failed actions

### When to Use
- Analyzing product analytics data
- Identifying UX friction points
- Optimizing conversion funnels
- Understanding feature usage patterns
- Prioritizing improvements based on impact
- Validating hypotheses with actual behavior

### Behavioral Insights vs. Attitudinal Research
- **Behavioral (What users DO)**: Analytics, usage data, A/B tests
- **Attitudinal (What users SAY)**: Surveys, interviews, feedback
- **Best Practice**: Combine both for complete understanding

### Related Methodologies
- **Product Analytics**: Tools like Mixpanel, Amplitude, Google Analytics
- **Event Tracking**: Monitoring specific user actions
- **Heatmaps**: Visual representation of click/scroll behavior
- **Session Replay**: Watching actual user sessions

## Usage
`/niopd:UR:behavior [--from=<behavior_filename>] [--for=<initiative_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative name.

**Examples:**
```bash
# Explicit initiative name and file
/niopd:UR:behavior --from=user-behavior.csv --for=dark-mode-feature

# Auto-detect initiative from current directory
cd dark-mode-feature
/niopd:UR:behavior --from=user-behavior.csv  # Uses "dark-mode-feature"

# Auto-detect both file and initiative
cd dark-mode-feature
/niopd:UR:behavior  # Auto-finds behavior file in sources/
```

## Preflight Checklist

1.  **Determine Initiative Name:**
    -   If `--for=<initiative_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative name from current directory: `<directory_name>`"
    -   Store the determined name as `<initiative_name>` for use in all subsequent steps

2.  **Check Behavior File:****
    -   If `--from` is provided, verify that the file `niopd-workspace/sources/<behavior_filename>` exists.
    -   If `--from` is not provided, search for files in `niopd-workspace/sources/` that contain "behavior", "query", or "用户行为" in their names.
    -   If multiple files are found, ask the user to specify which file to use.
    -   If no files are found, inform the user: "❌ I couldn't find any behavior files in `niopd-workspace/sources/`. Please make sure behavior files exist or provide a specific file with `--from=<filename>`."

## Instructions

You are a specialized AI expert in analyzing user behavior data. Your goal is to process user behavior data and transform it into actionable insights for product improvement.

### Step 1: Acknowledge and Prepare
-   Acknowledge the request: "On it! I'll analyze user behavior data for the **<initiative_name>** initiative."
-   If a specific file was provided with `--from`, use that file.
-   If no file was specified, search for behavior files in `niopd-workspace/sources/`:
    -   List all files in `niopd-workspace/sources/`
    -   Filter for files containing "behavior", "query", or "用户行为" in their names (case-insensitive)
    -   If exactly one file is found, use it automatically
    -   If multiple files are found, list them and ask the user to specify which one to use
    -   If no files are found, inform the user and stop the process

### Step 2: File Analysis & Validation
- Determine the file format (CSV, JSON, TXT, etc.) and structure.
- For structured formats (CSV/JSON), identify relevant columns/fields containing behavior data.
- For unstructured formats, parse the entire content as behavior data.
- Validate that the file contains sufficient data for meaningful analysis (at least 10 behavior records).

### Step 3: Data Preprocessing
- Clean and normalize the behavior data.
- Identify and separate distinct behavior patterns or user journeys.
- Detect and handle duplicates or near-duplicates.
- Identify any structured metadata (timestamps, user IDs, session IDs, page paths, actions) that can enhance analysis.

### Step 4: Behavior Pattern Identification
- Apply advanced pattern analysis to group related user behaviors into meaningful patterns.
- A pattern should represent a recurring user journey or interaction sequence (e.g., "Search → Filter → Exit", "Add to Cart → Abandon", "Login → Settings → Profile Update").
- For each pattern, identify 3-5 representative examples that best exemplify the pattern.
- Classify each pattern into one of the following categories:
    - **Drop-off Point:** A point in the user journey where users frequently abandon the process.
    - **Engagement Peak:** A point where users spend significant time or show high interaction.
    - **Navigation Issue:** A point where users show confusion or take unexpected paths.
    - **Conversion Funnel:** A sequence of steps leading to a desired outcome.
    - **Feature Usage:** How users interact with specific features or functionality.
    - **Error Pattern:** Repeated sequences that lead to errors or dead ends.

### Step 5: Initiative Context Alignment
- Review the initiative context and goals from the initiative document.
- Align identified behavior patterns with the initiative's objectives.
- Highlight patterns that directly impact the initiative's success metrics.
- Identify any conflicting patterns that might hinder the initiative's progress.

### Step 6: Opportunity Identification
- For each behavior pattern, identify potential product improvement opportunities.
- Classify opportunities by impact and effort:
    - **Quick Wins:** Low effort, high impact improvements
    - **Major Opportunities:** High effort, high impact improvements
    - **Strategic Enhancements:** Long-term improvements that align with product vision
    - **Technical Debt:** Issues that need addressing but may not directly impact users
- Prioritize opportunities based on their alignment with initiative goals and business impact.

### Step 7: Quantification & Metrics
- Calculate key metrics for each behavior pattern:
    - **Conversion Rate:** Percentage of users who complete the desired action
    - **Drop-off Rate:** Percentage of users who abandon at each step
    - **Time on Task:** Average time spent on specific actions or pages
    - **Error Rate:** Frequency of errors or failed actions
    - **Repeat Usage:** Frequency of returning to specific features
- Compare metrics against industry benchmarks or historical data if available.

### Step 8: User Journey Mapping
- Create visual representations of key user journeys based on the behavior data.
- Identify pain points and friction in the user experience.
- Map out alternative paths users take when the primary path is problematic.
- Highlight successful user journeys that could be optimized or replicated.

### Step 9: Behavior Summary Report Generation
Produce a markdown report with the following structure:

---
# Behavior Analysis Summary: [Behavior Data Source]

## Executive Summary
*A high-level overview of key behavior insights and opportunities from [total_behavior_records] user behavior records*

## Source Information
- **Behavior Data Source:** [Source name or description]
- **Analysis Period:** [Time period or "Not specified"]
- **Total Records Analyzed:** [Number of behavior records processed]
- **Analysis Date:** [Current date]
- **Related Initiative:** [Initiative name]

## Key Behavior Patterns

### 🚨 Critical Drop-off Points

#### Drop-off Point 1: [Descriptive title]
- **Frequency:** [Number] users ([Percentage]% of total)
- **Location:** [Page/Feature where drop-off occurs]
- **Description:** [Detailed description of the drop-off pattern]
- **User Example:** *"[Example user journey]"*
- **Impact:** [Business impact description]

[Repeat for 2-3 major drop-off points]

### ⚡ Engagement Peaks

#### Peak 1: [Descriptive title]
- **Frequency:** [Number] users ([Percentage]% of total)
- **Location:** [Page/Feature with high engagement]
- **Description:** [Detailed description of the engagement pattern]
- **User Example:** *"[Example user journey]"*
- **Opportunity:** [How to leverage this engagement]

[Repeat for 2-3 major engagement peaks]

### 🔄 Navigation Issues

#### Issue 1: [Descriptive title]
- **Frequency:** [Number] users ([Percentage]% of total)
- **Location:** [Page/Feature where navigation issues occur]
- **Description:** [Detailed description of the navigation problem]
- **User Example:** *"[Example user journey]"*
- **Confusion Factor:** [Assessment of user confusion level]

[Repeat for 2-3 major navigation issues]

## Initiative Alignment

### Direct Impact on [Initiative Name]
- **Alignment Score:** [High/Medium/Low]
- **Key Metrics Affected:** [List of metrics that relate to the initiative]
- **Opportunities:** [How behavior insights can improve the initiative]

### Potential Conflicts
- **Conflict 1:** [Description of potential conflict between behavior patterns and initiative goals]
- **Mitigation Strategy:** [Suggested approach to address the conflict]

## Product Improvement Opportunities

### Quick Wins (0-30 days)
1. **[Opportunity Title]:** [Brief description]
   - **Impact:** [Expected impact]
   - **Effort:** Low
   - **Owner:** [Suggested role or team]

[Repeat for 2-3 quick wins]

### Major Opportunities (1-3 months)
1. **[Opportunity Title]:** [Brief description]
   - **Impact:** [Expected impact]
   - **Effort:** Medium
   - **Dependencies:** [Key dependencies]

[Repeat for 2-3 major opportunities]

### Strategic Enhancements (3+ months)
1. **[Enhancement Title]:** [Brief description]
   - **Vision Alignment:** [How this aligns with product vision]
   - **Investment:** High
   - **Expected ROI:** [Estimated return on investment]

[Repeat for 1-2 strategic enhancements]

## Key Metrics & Performance

### Conversion Funnel Analysis
1. **[Step Name]:** [Conversion rate] ([Users who proceeded] / [Users who entered])
2. **[Step Name]:** [Conversion rate] ([Users who proceeded] / [Users who entered])

### Time on Task
- **Average Session Duration:** [Time]
- **Key Page Average Time:** [Time]
- **Feature Interaction Time:** [Time]

### Error Analysis
- **Overall Error Rate:** [Percentage]
- **Common Error Types:**
  1. **[Error Type]:** [Frequency] occurrences
  2. **[Error Type]:** [Frequency] occurrences

## User Journey Insights

### Successful Journeys
- **Journey 1:** *"[Step-by-step user journey]"*
  - **Completion Rate:** [Percentage]
  - **User Satisfaction:** [If available]

### Problematic Journeys
- **Journey 1:** *"[Step-by-step user journey]"*
  - **Drop-off Point:** [Where users abandon]
  - **Suggested Fix:** [How to improve this journey]

## Recommendations for Next Steps

### Immediate Actions
1. **[Action Title]:** [Brief description]
2. **[Action Title]:** [Brief description]

### Research Priorities
1. **[Research Priority]:** [Brief description of what to investigate]
2. **[Research Priority]:** [Brief description of what to investigate]

### Product Development Focus
1. **[Development Focus Area]:** [Rationale for prioritizing this area]
2. **[Development Focus Area]:** [Rationale for prioritizing this area]

## Methodology & Data Quality

### Analysis Approach
- **Pattern Recognition:** Statistical analysis combined with user journey mapping
- **Metrics Calculation:** Standard web analytics methodology
- **Opportunity Identification:** Impact vs. effort matrix

### Data Quality Notes
- **Data Completeness:** [Percentage]% of expected data received
- **Known Limitations:** [Description of any data limitations]
- **Sample Bias:** [Assessment of potential bias in the behavior data]

## Appendix

### Detailed Statistics
[Optional: Include detailed breakdowns if needed]

### Raw Data Summary
- **Source File:** [Original filename]
- **Processing Date:** [Date processed]
- **Analysis Tool:** NioPD Behavior Analyzer v1.0

---

### Step 10: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_slug]-behavior-summary-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 11: Confirm and Conclude
- Confirm the action is complete: "✅ I've analyzed the behavior data from `<behavior_filename>` and generated a behavior summary report."
- Provide the path to the file: "You can view it here: `niopd-workspace/reports/[YYYYMMDD]-[initiative_slug]-behavior-summary-v[version].md`"
- Suggest next steps: "Consider using `/niopd:UR:feedback` to analyze user feedback related to these behavior patterns."

## Error Handling
- **Missing Arguments:** If required arguments are missing, ask the user for the required information.
- **File Not Found:** If the behavior file doesn't exist, inform the user and provide guidance.
- **Initiative Not Found:** If the initiative doesn't exist, suggest creating it first.
- **Multiple Files Found:** If multiple behavior files are found without a specific selection, list them and ask the user to choose.
- **No Files Found:** If no behavior files are found in the sources directory, inform the user.
- **Insufficient Data:** If the behavior file doesn't contain enough data for analysis, explain the requirement.
- **File Access Issues:** If there are permission issues, display appropriate error messages.