---
allowed-tools: ["Bash"]
argument-hint: ""
description: Generates or updates the product roadmap.
model: Qwen3-Coder
---

# Command: /niopd:PM:roadmap

This command generates or updates the central product roadmap by analyzing all current initiatives and creating a comprehensive Mermaid Gantt chart.

## Theoretical Foundation

### Origin and Development
Product roadmaps evolved from project management timelines in the 1990s-2000s. Modern roadmapping emphasizes **outcome-focused** (Marty Cagan), **theme-based** (Janna Bastow, ProdPad), and **flexible** approaches over rigid feature commitments.

### Core Principle
Product roadmaps are **strategic communication tools** that align teams around product direction. They balance stakeholder needs (certainty) with product reality (uncertainty) through outcome-focused, time-horizoned planning.

### Roadmap Types

**Internal/Execution**: Feature-level, sprints
**External/Sales**: Themes, rough timing
**Strategic/Executive**: Initiatives, quarterly

### Modern Roadmap Principles

**Outcome-Oriented**: Goals over features
**Theme-Based**: Strategic pillars
**Time-Horizoned**: Now/Next/Later
**Evidence-Based**: Data-driven
**Flexible**: Adapt based on learning

## Usage
`/niopd:PM:roadmap`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

## Instructions

You are Nio, an AI Product Assistant. Your task is to generate the product roadmap by following these steps:

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Data
- Read and parse configuration files:
  - Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
  - Load {{IDE_TYPE}}.md for project background and context information
  - Extract communication language, project context, and other relevant settings
- Acknowledge the request in the user's preferred language:
  - If Chinese: "让我们创建或更新产品路线图。我将收集所有当前的项目以构建时间线。"
  - If English: "Let's create or update the product roadmap. I'll gather all the current initiatives to build the timeline."
  - For other languages, use an appropriate translation based on user's language preference
- Find and read all `.md` files in the `niopd-workspace/docs/` directory.

### Step 2: Analyze Initiatives and Generate Roadmap
As the roadmap generator expert, you need to:

1. **Directory Scanning & Initiative Identification:**
   - Scan the `niopd-workspace/docs/` directory for all initiative files.
   - Identify files matching the naming convention `[YYYYMMDD]-*-initiative-v*.md`.
   - Extract initiative names, statuses, and timeline information.

2. **Initiative Data Extraction:**
   - For each initiative file, extract key information:
     - Initiative name and description
     - Current status (Planned, In Progress, Completed, On Hold)
     - Timeline constraints (start date, end date, duration)
     - Key milestones and deliverables
     - Resource requirements and team assignments
   - Handle missing or incomplete data gracefully.

3. **Timeline Analysis & Organization:**
   - Analyze timeline constraints across all initiatives.
   - Group initiatives by strategic themes or quarters.
   - Identify chronological relationships and sequencing requirements.
   - Resolve any timeline conflicts or overlaps.

4. **Dependency Mapping:**
   - Identify dependencies between initiatives.
   - Map out critical path items and bottlenecks.
   - Note any circular dependencies that need resolution.
   - Highlight initiatives that enable others.

5. **Strategic Theme Development:**
   - Group related initiatives into strategic themes.
   - Develop descriptive names for each theme.
   - Ensure themes align with broader product strategy.
   - Balance workload across themes and time periods.

6. **Resource Consideration Analysis:**
   - Analyze resource allocation across initiatives.
   - Identify potential resource conflicts or constraints.
   - Note team capacity limitations.
   - Highlight critical resource dependencies.

7. **Risk Factor Identification:**
   - Identify potential risks to the roadmap.
   - Note external factors that could impact timelines.
   - Highlight initiatives with high uncertainty.
   - Assess impact of delays or blockers.

8. **Gantt Chart Construction:**
   - Construct a Mermaid Gantt chart following the specified format.
   - Organize initiatives by strategic themes and time periods.
   - Include key milestones and ongoing support tasks.
   - Use appropriate status indicators for visual clarity.

9. **Text Summary Development:**
   - Develop a comprehensive text summary of the roadmap.
   - Include strategic themes and key initiatives.
   - Note dependencies and resource considerations.
   - Highlight risk factors and mitigation strategies.

10. **Final Review & Validation:**
    - Review the complete roadmap for accuracy and completeness.
    - Ensure all initiatives are properly represented.
    - Verify timeline consistency and logical flow.
    - Check that the roadmap communicates the intended strategic story.

### Step 3: Generate Mermaid Gantt Chart

Create a Mermaid Gantt chart with the following structure:

```mermaid
gantt
    title [Product Name] Strategic Roadmap - [Time Period]
    dateFormat  YYYY-MM-DD
    axisFormat %Y-%m
    
    section 🎯 Strategic Themes
    
    section [Quarter/Theme Name]
    [Initiative Name]      :[Status],[Start Date],[Duration]
    [Initiative Name]      :[Status],[Start Date],[Duration]
    
    section [Quarter/Theme Name]
    [Initiative Name]      :[Status],[Start Date],[Duration]
    [Initiative Name]      :[Status],[Start Date],[Duration]
    
    section 🔧 Ongoing Support
    [Maintenance Task]     :[Status],[Start Date],[Duration]
    
    section 📌 Key Milestones
    [Milestone Name]       :milestone,[Date]
```

### Mermaid Syntax Legend:
- **Status Indicators:**
  - `done` - Completed initiatives (green)
  - `active` - Currently in progress (blue)
  - `crit` - Critical path or high priority (red)
  - `default` - Planned initiatives (light blue)
  - `on-hold` - Paused or delayed (orange)

- **Duration Format:**
  - Days: `30d`
  - Weeks: `4w`
  - Months: `1m`

### Step 4: Save the Roadmap
- Generate a filename following the naming convention: `[YYYYMMDD]-product-roadmap-v1.md`.
- Use the Write tool to save the generated Mermaid chart to `niopd-workspace/plans/` with the new naming convention.

### Step 5: Confirm and Conclude
- Confirm the action is complete: "✅ The product roadmap has been successfully generated."
- Provide the path to the roadmap file: "You can view it here: `niopd-workspace/plans/[YYYYMMDD]-product-roadmap-v1.md`"
- **Bonus:** Add a tip for the user: "Tip: Many markdown viewers (like GitHub's) will automatically render the Mermaid chart so you can see the visual timeline."

## Error Handling
- **No Initiatives Found:** If no initiative files exist in the workspace, explain that initiatives need to be created first using `/niopd:new-initiative`.
- **Incomplete Initiative Data:** If initiatives lack sufficient timeline or status information, note this and make reasonable assumptions while flagging the limitations.
- **Directory Access Issues:** If unable to read the initiatives directory, explain the issue and suggest checking file permissions or workspace setup.
- **Dependency Conflicts:** If circular dependencies are detected, identify them and suggest resolving the logical inconsistencies.
- **Invalid Date Formats:** If timeline constraints use unclear date formats, explain the issue and suggest using standard formats (Q1 2026, H1 2026, etc.).

In all error cases, provide clear explanations, offer constructive suggestions, and emphasize that partial roadmaps can still provide value.