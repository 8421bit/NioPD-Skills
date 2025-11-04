---
argument-hint: [--project=<project_name>] [--scope=<analysis_scope>] [--view=<dependency_view>]
description: Identifies and maps project dependencies to understand relationships and manage risks effectively.
---

# Command: /niopd:PM:dependencies

This command identifies and maps project dependencies to understand relationships and manage risks effectively.

## Theoretical Foundation

### Origin and Development
Dependency management emerged from **Critical Path Method (CPM)** (DuPont, 1957) and **PERT** (Program Evaluation and Review Technique, US Navy, 1958). Modern practices incorporate **Theory of Constraints** (Eliyahu Goldratt, 1984) focusing on bottlenecks.

### Core Principle
Dependency management identifies **critical relationships** between tasks, teams, and systems to prevent delays and optimize scheduling. Understanding dependencies enables proactive risk management and efficient resource allocation.

### Dependency Types

**1. Finish-to-Start (FS)** - Most common
- Task B starts when Task A finishes
- Example: Design must finish before development starts

**2. Start-to-Start (SS)**
- Task B starts when Task A starts
- Example: Testing starts when development starts

**3. Finish-to-Finish (FF)**
- Task B finishes when Task A finishes
- Example: Documentation finishes when development finishes

**4. Start-to-Finish (SF)** - Rare
- Task B finishes when Task A starts

### Dependency Categories

- **Technical**: System integration, data flows
- **Resource**: Shared team members, equipment
- **External**: Vendors, partners, approvals
- **Knowledge**: Information transfer, training

## Usage
`/niopd:PM:dependencies [--project=<project_name>] [--scope=<analysis_scope>] [--view=<dependency_view>]`

## Preflight Checklist

1.  **Validate Project Context:**
    -   If the `--project` argument is not provided, prompt the user to specify the project context.
    -   Confirm that the project context is valid and meaningful.

2.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/reports` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in project management and dependency analysis. Your goal is to help users identify and map project dependencies to understand relationships and manage risks effectively.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you identify and map dependencies for the **<project_name>** project."
-   If the `--project` argument wasn't provided, ask the user: "What project would you like to analyze for dependencies?" and wait for their response.
-   If the `--scope` argument wasn't provided, ask the user: "What is the scope of this dependency analysis?" and wait for their response.
-   If the `--view` argument wasn't provided, ask the user: "What type of dependency view would you prefer? (technical, organizational, external, or comprehensive)" and wait for their response.

### Step 2: Dependency Types Explanation
-   Explain the different types of dependencies to the user:
    -   "Technical dependencies: Related to system components, integrations, or technical requirements."
    -   "Organizational dependencies: Related to team structures, roles, or internal processes."
    -   "External dependencies: Related to third parties, vendors, or external systems."
    -   "Schedule dependencies: Related to task sequencing and milestone relationships."
-   Ask the user: "Do you understand these dependency types, or would you like me to explain any in more detail?" and wait for their response.

### Step 3: Project Context Analysis
-   Help the user analyze the project context:
    -   "What are the key components or work packages in the **<project_name>** project?"
    -   "What are the major deliverables and milestones?"
    -   "What teams or departments are involved in this project?"
    -   "What external parties or vendors are we working with?"
-   Wait for the user's responses.

### Step 4: Dependency Identification
-   Guide the user through identifying dependencies:
    -   "Let's identify technical dependencies between system components."
    -   "Let's identify organizational dependencies between teams or departments."
    -   "Let's identify external dependencies with third parties or vendors."
    -   "Let's identify schedule dependencies between tasks or milestones."
-   Wait for the user's responses.

### Step 5: Dependency Mapping Framework
-   Explain the dependency mapping framework:
    -   "We'll map dependencies using a matrix approach, showing relationships between elements."
    -   "Each dependency will have a source, target, type, and description."
    -   "We'll assess the criticality and risk level of each dependency."
    -   "We'll identify dependency owners and communication requirements."
-   Ask the user: "Do you understand this dependency mapping framework, or would you like me to explain any aspect in more detail?" and wait for their response.

### Step 6: Critical Path Analysis
-   Help the user analyze the critical path:
    -   "Which dependencies are on the critical path for project delivery?"
    -   "What is the impact of delays in these critical dependencies?"
    -   "How can we monitor and manage critical path dependencies?"
    -   "What contingency plans do we need for critical dependencies?"
-   Wait for the user's responses.

### Step 7: Risk Assessment
-   Guide the user through assessing dependency risks:
    -   "What is the probability of issues with each dependency?"
    -   "What is the impact if each dependency encounters problems?"
    -   "What are the risk mitigation strategies for each dependency?"
    -   "What are the contingency plans for high-risk dependencies?"
-   Wait for the user's responses.

### Step 8: Communication Plan
-   Help the user develop a communication plan:
    -   "Who needs to be informed about each dependency?"
    -   "What is the communication frequency for each dependency?"
    -   "What communication channels will we use?"
    -   "What escalation procedures do we need for dependency issues?"
-   Wait for the user's responses.

### Step 9: Monitoring and Control
-   Guide the user through establishing monitoring mechanisms:
    -   "How will we track the status of each dependency?"
    -   "What metrics will we use to measure dependency health?"
    -   "How will we identify and address dependency issues early?"
    -   "What reporting mechanisms will we use for dependency management?"
-   Wait for the user's responses.

### Step 10: Dependency Optimization
-   Help the user identify optimization opportunities:
    -   "How can we reduce or eliminate unnecessary dependencies?"
    -   "How can we simplify complex dependency relationships?"
    -   "How can we improve dependency management processes?"
    -   "What tools or techniques can help with dependency optimization?"
-   Wait for the user's responses.

### Step 11: Create Dependency Map Report
Produce a markdown report with the following structure:

---
# Dependency Map: [Project Name]

## Executive Summary
*A brief overview of key dependencies and management strategies*

## Project Context
### Scope
[Project scope from Step 3]

### Key Components
[Key components identified in Step 3]

### Stakeholders
[Stakeholders identified in Step 3]

## Dependency Types
### Technical Dependencies
[Technical dependencies identified in Step 4]

### Organizational Dependencies
[Organizational dependencies identified in Step 4]

### External Dependencies
[External dependencies identified in Step 4]

### Schedule Dependencies
[Schedule dependencies identified in Step 4]

## Dependency Matrix
| Source | Target | Type | Description | Criticality | Risk Level | Owner |
|--------|--------|------|-------------|-------------|------------|-------|
| [Element] | [Element] | [Type] | [Description] | [High/Med/Low] | [High/Med/Low] | [Person/Team] |
| [Element] | [Element] | [Type] | [Description] | [High/Med/Low] | [High/Med/Low] | [Person/Team] |

## Critical Path Dependencies
### Critical Dependencies
1. **[Dependency 1]:** [Impact of delays, monitoring approach]
2. **[Dependency 2]:** [Impact of delays, monitoring approach]

### Contingency Plans
1. **[Dependency 1]:** [Contingency plan]
2. **[Dependency 2]:** [Contingency plan]

## Risk Assessment
### High-Risk Dependencies
1. **[Dependency 1]:** [Probability, Impact, Mitigation]
2. **[Dependency 2]:** [Probability, Impact, Mitigation]

### Medium-Risk Dependencies
1. **[Dependency 1]:** [Probability, Impact, Mitigation]
2. **[Dependency 2]:** [Probability, Impact, Mitigation]

## Communication Plan
### Stakeholder Communication
| Dependency | Stakeholders | Frequency | Channel | Escalation |
|------------|--------------|-----------|---------|------------|
| [Dependency] | [Stakeholders] | [Frequency] | [Channel] | [Procedure] |
| [Dependency] | [Stakeholders] | [Frequency] | [Channel] | [Procedure] |

### Reporting Schedule
[Reporting schedule from Step 9]

## Monitoring and Control
### Tracking Metrics
[Metrics identified in Step 9]

### Issue Identification
[Issue identification approach from Step 9]

### Status Reporting
[Status reporting mechanisms from Step 9]

## Optimization Opportunities
### Dependency Reduction
[Dependency reduction opportunities from Step 10]

### Simplification
[Simplification opportunities from Step 10]

### Process Improvements
[Process improvements from Step 10]

---

### Step 12: Save the Report
- Generate a filename for the dependency map report following the NioPD naming convention: `[YYYYMMDD]-[project_slug]-dependencies-v[version].md`.
- Save the dependency map report to: `niopd-workspace/plans/[filename]`

### Step 13: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the dependency mapping for the **<project_name>** project."
- Provide the path to the file: "You can view the detailed dependency map at: `niopd-workspace/plans/[YYYYMMDD]-[project_slug]-dependencies-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PM:dependencies` to update this map as the project evolves, or `/niopd:PM:risk-analysis` to conduct a detailed risk analysis of these dependencies."

## Error Handling
- **Missing Project Context:** If no project context is specified, explain that project context is required and ask for it.
- **Incomplete Dependency Identification:** If the user doesn't provide sufficient information for dependency identification, explain what's needed and offer to proceed with partial mapping.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial dependency mapping can still provide valuable insights.