---
argument-hint: [--project=<project_name>] [--scope=<project_scope>] [--timeline=<project_timeline>]
description: Plans team and budget allocation to ensure optimal resource utilization throughout project execution.
---

# Command: /niopd:PM:resources

This command plans team and budget allocation to ensure optimal resource utilization throughout project execution.

## Theoretical Foundation

### Origin and Development
Resource management emerged from **Operations Research** (WWII, 1940s) and **Critical Chain Project Management** (Eliyahu Goldratt, 1997). Modern approaches integrate **Resource Leveling** and **Capacity Planning** techniques.

### Core Principle
Resource management ensures **right people, right skills, right time** by balancing demand with supply. It optimizes utilization while avoiding overallocation, preventing burnout and delays.

### Resource Types

**Human Resources**:
- Team members (FTE)
- Contractors/consultants
- Subject matter experts

**Financial Resources**:
- Budget allocations
- Cost reserves
- Contingency funds

**Physical Resources**:
- Equipment and tools
- Infrastructure
- Facilities

### Resource Allocation Techniques

**Resource Leveling**:
- Smooth out peaks and valleys
- May extend schedule
- Reduce overallocation

**Resource Smoothing**:
- Optimize within fixed schedule
- Use float/slack
- Maintain deadlines

**Critical Chain**:
- Buffer management
- Focus on constraints
- Protect critical path

## Usage
`/niopd:PM:resources [--project=<project_name>] [--scope=<project_scope>] [--timeline=<project_timeline>]`

## Preflight Checklist

1.  **Validate Project Context:**
    -   If the `--project` argument is not provided, prompt the user to specify the project context.
    -   Confirm that the project context is valid and meaningful.

2.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/reports` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in project management and resource planning. Your goal is to help users plan team and budget allocation to ensure optimal resource utilization throughout project execution.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you plan team and budget allocation for the **<project_name>** project."
-   If the `--project` argument wasn't provided, ask the user: "What project would you like to plan resources for?" and wait for their response.
-   If the `--scope` argument wasn't provided, ask the user: "What is the scope of the **<project_name>** project?" and wait for their response.
-   If the `--timeline` argument wasn't provided, ask the user: "What is the timeline for the **<project_name>** project?" and wait for their response.

### Step 2: Project Scope Analysis
-   Help the user analyze the project scope in detail:
    -   "What are the key deliverables for the **<project_name>** project?"
    -   "What are the major milestones and dependencies?"
    -   "What are the technical and functional requirements?"
    -   "What constraints or limitations exist for this project?"
-   Wait for the user's responses.

### Step 3: Work Breakdown Structure
-   Guide the user through creating a work breakdown structure:
    -   "Let's break down the project into major work packages or phases."
    -   "What are the key activities within each work package?"
    -   "How do these activities relate to each other?"
    -   "What are the dependencies between activities?"
-   Wait for the user's responses.

### Step 4: Team Role Identification
-   Help the user identify required team roles:
    -   "What roles are needed for this project? (Project Manager, Developers, Designers, QA, etc.)"
    -   "What are the responsibilities for each role?"
    -   "What skills and expertise are required for each role?"
    -   "Do we have existing team members who can fill these roles?"
-   Wait for the user's responses.

### Step 5: Resource Estimation
-   Guide the user through estimating resource requirements:
    -   "How much effort will each work package require?"
    -   "What is the estimated duration for each activity?"
    -   "What resources are needed for each task? (people, equipment, software, etc.)"
    -   "What are the peak resource demands during the project?"
-   Wait for the user's responses.

### Step 6: Team Capacity Assessment
-   Help the user assess current team capacity:
    -   "What is the availability of each team member?"
    -   "What other commitments do team members have?"
    -   "What is the total capacity we have available for this project?"
    -   "Are there any gaps between required resources and available capacity?"
-   Wait for the user's responses.

### Step 7: Budget Planning
-   Guide the user through planning the project budget:
    -   "What are the major cost categories for this project? (labor, materials, software, etc.)"
    -   "What is the estimated cost for each work package?"
    -   "What is the total project budget?"
    -   "What contingency reserves should we include?"
-   Wait for the user's responses.

### Step 8: Resource Allocation Strategy
-   Help the user develop a resource allocation strategy:
    -   "How will we assign resources to different activities?"
    -   "What is our approach to resource leveling?"
    -   "How will we handle resource conflicts or overallocation?"
    -   "What is our strategy for managing resource constraints?"
-   Wait for the user's responses.

### Step 9: Risk Assessment
-   Guide the user through assessing resource-related risks:
    -   "What are the key risks related to resource availability?"
    -   "What are the risks related to budget constraints?"
    -   "What are the risks related to skill gaps or expertise?"
    -   "How can we mitigate these risks?"
-   Wait for the user's responses.

### Step 10: Resource Optimization
-   Help the user optimize resource utilization:
    -   "How can we improve resource efficiency?"
    -   "What opportunities exist for resource sharing?"
    -   "How can we reduce resource waste or redundancy?"
    -   "What tools or techniques can help with resource optimization?"
-   Wait for the user's responses.

### Step 11: Monitoring and Control Plan
-   Guide the user through establishing monitoring and control mechanisms:
    -   "How will we track resource utilization during the project?"
    -   "What metrics will we use to measure resource efficiency?"
    -   "How will we handle resource changes or adjustments?"
    -   "What reporting mechanisms will we use for resource management?"
-   Wait for the user's responses.

### Step 12: Create Resource Plan Report
Produce a markdown report with the following structure:

---
# Resource Plan: [Project Name]

## Executive Summary
*A brief overview of key resource allocations and budget planning*

## Project Overview
### Scope
[Project scope from Step 2]

### Timeline
[Project timeline provided by user]

### Key Deliverables
[Key deliverables identified in Step 2]

## Work Breakdown Structure
### Work Packages
1. **[Work Package 1]:** [Description and key activities]
2. **[Work Package 2]:** [Description and key activities]

### Activity Dependencies
[Activity dependencies identified in Step 3]

## Team Structure
### Required Roles
1. **[Role 1]:** [Responsibilities and required skills]
2. **[Role 2]:** [Responsibilities and required skills]

### Team Members
1. **[Team Member 1]:** [Role, availability, other commitments]
2. **[Team Member 2]:** [Role, availability, other commitments]

## Resource Requirements
### Effort Estimates
- **Work Package 1:** [Effort estimate and duration]
- **Work Package 2:** [Effort estimate and duration]

### Resource Needs
- **Work Package 1:** [Required resources]
- **Work Package 2:** [Required resources]

### Peak Resource Demands
[Peak resource demands identified in Step 5]

## Capacity Analysis
### Team Availability
[Team capacity assessment from Step 6]

### Resource Gaps
[Resource gaps identified in Step 6]

### External Resources
[External resources or contractors needed]

## Budget Plan
### Cost Categories
1. **Labor:** [Estimated cost]
2. **Materials:** [Estimated cost]
3. **Software/Licenses:** [Estimated cost]

### Work Package Costs
- **Work Package 1:** [Estimated cost]
- **Work Package 2:** [Estimated cost]

### Total Budget
[Total project budget from Step 7]

### Contingency Reserves
[Contingency reserves identified in Step 7]

## Resource Allocation
### Assignment Matrix
| Activity | Responsible | Resources | Start Date | End Date |
|----------|-------------|-----------|------------|----------|
| [Activity 1] | [Person/Team] | [Resources] | [Date] | [Date] |
| [Activity 2] | [Person/Team] | [Resources] | [Date] | [Date] |

### Resource Leveling Strategy
[Resource allocation strategy from Step 8]

## Risk Assessment
### Resource Risks
1. **[Risk 1]:** [Description, probability, impact, mitigation]
2. **[Risk 2]:** [Description, probability, impact, mitigation]

### Budget Risks
1. **[Risk 1]:** [Description, probability, impact, mitigation]
2. **[Risk 2]:** [Description, probability, impact, mitigation]

## Optimization Opportunities
### Efficiency Improvements
[Efficiency improvements identified in Step 10]

### Resource Sharing
[Resource sharing opportunities identified in Step 10]

### Waste Reduction
[Waste reduction strategies identified in Step 10]

## Monitoring and Control
### Tracking Metrics
[Metrics identified in Step 11]

### Reporting Schedule
[Reporting mechanisms from Step 11]

### Change Management
[Resource change management approach]

---

### Step 13: Save the Report
- Generate a filename for the resource plan report following the NioPD naming convention: `[YYYYMMDD]-[project_slug]-resources-v[version].md`.
- Save the resource plan report to: `niopd-workspace/plans/[filename]`

### Step 14: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the resource plan for the **<project_name>** project."
- Provide the path to the file: "You can view the detailed resource plan at: `niopd-workspace/plans/[YYYYMMDD]-[project_slug]-resources-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PM:resources` to update this plan as the project progresses, or `/niopd:PM:kpis` to track resource utilization during project execution."

## Error Handling
- **Missing Project Context:** If no project context is specified, explain that project context is required and ask for it.
- **Incomplete Resource Estimation:** If the user doesn't provide sufficient information for resource estimation, explain what's needed and offer to proceed with partial planning.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial resource planning can still provide valuable guidance.