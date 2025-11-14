---
argument-hint: [--for=<initiative_name>] [year|month|week|day]
description: Generates a stakeholder update for an initiative with optional time period filtering. Auto-detects initiative name from current directory if not specified.
---

# Command: /niopd:PO:stakeholder-update

This command generates a high-level stakeholder update for a specific initiative, with optional time period filtering to focus on recent activities.

## Theoretical Foundation

### Origin and Development
Stakeholder communication frameworks emerged from **Project Management** (PMI PMBOK, 1987) and **Change Management** (Kotter, Prosci ADKAR). Modern approaches emphasize **transparent**, **frequent**, and **audience-tailored** communication for alignment and decision-making.

### Core Principle
Stakeholder updates provide **strategic communication** that informs decision-makers, aligns teams, and builds trust. Effective updates are **concise**, **data-driven**, **actionable**, and **audience-appropriate** - balancing transparency with clarity.

### Stakeholder Communication Principles

**Audience Segmentation**:
- **Executives**: Strategy, outcomes, risks
- **Peers/Partners**: Progress, dependencies
- **Team**: Detailed execution, blockers
- **Customers**: Value, availability, impact

**Update Cadence**:
- **Weekly**: Team standups
- **Bi-weekly**: Cross-functional syncs
- **Monthly**: Leadership reviews
- **Quarterly**: Board/executive updates

**Effective Structure**:
1. **Context**: What we're building, why
2. **Progress**: What's done, what's next
3. **Metrics**: How we're tracking
4. **Risks**: What could go wrong
5. **Decisions**: What we need from you

### Communication Frameworks

**STAR** (Situation, Task, Action, Result):
- Situation: Current context
- Task: Objectives and goals
- Action: What's being done
- Result: Outcomes achieved

**3Ws** (What, So What, Now What):
- What: Facts and data
- So What: Implications and impact
- Now What: Actions and decisions

## Usage
`/niopd:PO:stakeholder-update [--for=<initiative_name>] [year|month|week|day]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative name.

**Examples:**
```bash
# Explicit initiative with time period
/niopd:PO:stakeholder-update --for=dark-mode-feature month

# Auto-detect initiative, specify time period
cd dark-mode-feature
/niopd:PO:stakeholder-update month  # Uses "dark-mode-feature"

# Auto-detect initiative, comprehensive update
cd dark-mode-feature
/niopd:PO:stakeholder-update  # Uses "dark-mode-feature", all time
```

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Determine Initiative Name:**
    -   If `--for=<initiative_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative name from current directory: `<directory_name>`"
    -   Store the determined name as `<initiative_name>` for use in all subsequent steps

3.  **Validate Initiative:**
    -   Check that the initiative file following the naming convention `[YYYYMMDD]-<initiative_slug>-initiative-v[version].md` exists in `niopd-workspace/docs/`. If not, inform the user.
    -   Check that the corresponding PRD file following the naming convention `[YYYYMMDD]-<initiative_slug>-prd-v[version].md` exists in `niopd-workspace/docs/`. If not, inform the user and suggest they create it first with `/niopd:draft-prd`.
    -   Identify the latest version of each file based on the date and version number in the filename.
    -   Validate the optional time period parameter if provided (must be one of: year, month, week, day).

## Instructions

You are a specialized AI expert in product operations and stakeholder communications. Your goal is to transform complex product documentation into clear, strategic communications that inform decision-making and drive alignment.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Parse Parameters
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "好的。我将为 **<initiative_name>** 项目准备一份利益相关者更新。"
    -   If English: "I can do that. I'll prepare a stakeholder update for the **<initiative_name>** initiative."
    -   For other languages, use an appropriate translation based on user's language preference
-   Parse the optional time period parameter:
    -   If no time period is specified, generate a comprehensive update covering all historical data.
    -   If "year" is specified, focus on activities and progress from the past year.
    -   If "month" is specified, focus on activities and progress from the past month.
    -   If "week" is specified, focus on activities and progress from the past week.
    -   If "day" is specified, focus on activities and progress from the past day.
-   Read the LATEST version of the initiative file from `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-initiative-v[version].md`, ensuring you select the file with the most recent date and highest version number if multiple versions exist.
-   Read the LATEST version of the PRD file from `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`, ensuring you select the file with the most recent date and highest version number if multiple versions exist.
-   Ensure that you are reading the most recent versions by checking the date and version in the filename.

### Step 2: Document Location & Validation
- Locate the initiative file in `niopd-workspace/docs/`.
- If a PRD file is referenced, locate it in `niopd-workspace/docs/`.
- Verify that files exist and are readable.
- Check that files contain the required sections for update creation.
- Calculate the date range based on the time period parameter:
    -   For "year": From today's date minus 1 year to today
    -   For "month": From today's date minus 1 month to today
    -   For "week": From today's date minus 1 week to today
    -   For "day": From today's date minus 1 day to today

### Step 3: Strategic Context Analysis
- Extract initiative goals and strategic alignment from the initiative file.
- Identify the business problem being solved.
- Understand the initiative's importance to broader company objectives.
- Note key stakeholders and business units impacted.
- When filtering by time period, focus on recent strategic adjustments or context changes within that timeframe.

### Step 4: Progress & Achievement Review (Time-Filtered)
- Identify recently completed milestones and deliverables within the specified time period.
- Extract key metrics and performance data relevant to the time period.
- Analyze current focus areas and work in progress that emerged or continued during the time period.
- Note significant achievements and their business impact that occurred during the time period.
- For comprehensive updates (no time filter), include all historical progress with emphasis on recent achievements.

### Step 5: Upcoming Priorities Planning
- Identify next 30-day priorities and action items (regardless of time filter for forward-looking sections).
- Extract next quarter deliverables and strategic focus areas.
- Note key milestone dates and timelines.
- Develop a visual timeline representation.
- When using time filters, provide context on how recent progress affects future priorities.

### Step 6: Risk & Issue Assessment (Time-Filtered)
- Identify current risks and their potential impact that emerged or evolved during the time period.
- Note recently resolved issues and their resolutions within the time period.
- Assess risk mitigation strategies and ownership for recent risks.
- Identify high-priority and medium-priority concerns that are relevant to the time period.
- For comprehensive updates, include a summary of ongoing risks with emphasis on recent developments.

### Step 7: Resource & Budget Analysis
- Extract team composition and key roles.
- Analyze current team size and capacity utilization.
- Review budget position and spending to date.
- Note any resource constraints or support needs that became apparent during the time period.
- When using time filters, focus on resource changes or budget impacts that occurred during the timeframe.

### Step 8: Strategic Insight Development (Time-Filtered)
- Identify market impact observations and insights that emerged during the time period.
- Note learning and innovation developments that occurred during the time period.
- Extract key insights gained during execution within the time period.
- Identify emerging opportunities that became apparent during the time period.
- For comprehensive updates, summarize overall strategic insights with emphasis on recent findings.

### Step 9: Recommendation Formulation
- Develop specific decisions needed and their deadlines (forward-looking, not time-filtered).
- Identify support requests and resource needs based on recent developments.
- Formulate key actions for leadership, team, and stakeholders that address recent challenges or opportunities.
- Prioritize recommendations based on impact and urgency.
- When using time filters, ensure recommendations are relevant to the timeframe's challenges and opportunities.

### Step 10: Q&A Preparation
- Anticipate likely questions from stakeholders based on recent developments.
- Prepare clear, concise responses to common inquiries about recent progress.
- Identify key data points to reference in responses that are relevant to the time period.
- Develop supporting information for complex topics that emerged during the time period.

### Step 11: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_slug]-update-v[version].md`.
- Save the report to: `niopd-workspace/docs/[filename]`

### Step 12: Confirm and Conclude
- Confirm the action is complete: "✅ The stakeholder update has been generated."
- Provide the path to the file: "You can view it here: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-stakeholder-[time_period]-v[version].md`"
- If no time period is specified: "You can view it here: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-stakeholder-v[version].md`"
- Note: The filename follows the naming convention `[YYYYMMDD]-<initiative_slug>-stakeholder-[time_period]-v[version].md` where `<initiative_slug>` matches the naming convention used in the corresponding initiative file (`[YYYYMMDD]-<initiative_slug>-initiative-v[version].md`) and PRD file (`[YYYYMMDD]-<initiative_slug>-prd-v[version].md`).

## Error Handling
- **Missing Documents:** If either the initiative or PRD file is missing, explain the impact and suggest creating the missing document.
- **Inconsistent Information:** If there are conflicts between initiative and PRD content, note these discrepancies and recommend verification.
- **Incomplete Data:** If key sections are missing from either document, explain how this affects the update quality and suggest completing documentation.
- **Status Ambiguity:** If current status is unclear, note this limitation and suggest establishing clearer tracking mechanisms.
- **Audience Mismatch:** If the target audience isn't clearly defined, provide a general business-focused update while noting it can be tailored further.
- **Invalid Time Period:** If an invalid time period parameter is provided, inform the user that valid options are: year, month, week, day. Generate a comprehensive update if the parameter is invalid.

In all error cases, provide clear explanations, suggest improvements, and focus on delivering maximum value with available information.