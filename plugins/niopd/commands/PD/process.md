---
argument-hint: [--for=<prd_name>]
description: Adds business process diagrams to an existing PRD document. Auto-detects PRD name from current directory if not specified.
---

# Command: /niopd:PD:process

This command adds a comprehensive Business Process section to an existing Product Requirements Document (PRD), including workflow visualizations in both PlantUML and Mermaid syntax formats.

## Theoretical Foundation

### Origin and Development
Business Process Modeling emerged from **industrial engineering** and **operations management** in the early 20th century (**Frederick Taylor**, scientific management). Modern BPM was formalized in the 1990s through standards like **BPMN (Business Process Model and Notation)** by the **OMG (Object Management Group)** and work by **Michael Hammer** and **James Champy** ("Reengineering the Corporation", 1993).

### Core Principle
Business Process Modeling creates **visual representations of workflows** showing how work gets done within an organization. It documents the sequence of activities, decision points, responsibilities, and information flows to enable analysis, improvement, and automation.

### Process vs. Journey vs. Flow

**Business Process**:
- **Organization's perspective**: How the business operates
- **Focus**: Efficiency, compliance, automation
- **Actors**: Systems, roles, departments
- **Example**: "Order fulfillment: Order received → Inventory check → Payment → Shipping → Delivery"

**User Journey**:
- **User's perspective**: User experience across time
- **Focus**: Emotions, satisfaction, touchpoints
- **Actors**: User personas, channels
- **Example**: "Discovery → Evaluation → Purchase → Use → Advocacy"

**User Flow** (UI/UX):
- **Task completion perspective**: Screen-to-screen navigation
- **Focus**: Usability, interaction design
- **Actors**: User actions, system responses
- **Example**: "Login screen → Dashboard → Search → Results → Detail page"

### Business Process Components

**1. Activities/Tasks**:
- What work is performed
- Manual vs. automated
- Value-adding vs. non-value-adding

**2. Sequence Flow**:
- Order of activities
- Parallel vs. sequential
- Dependencies

**3. Gateways (Decision Points)**:
- Exclusive (XOR): One path chosen
- Inclusive (OR): Multiple paths possible
- Parallel (AND): All paths executed

**4. Swimlanes**:
- Roles/departments/systems
- Responsibility assignment
- Handoff visualization

**5. Events**:
- Start: Process trigger
- Intermediate: Milestones, timers
- End: Process completion

**6. Data Objects**:
- Inputs and outputs
- Documents and records
- Data flows

### BPMN (Business Process Model and Notation)

**Standard Elements**:
- **Flow Objects**: Events, Activities, Gateways
- **Connecting Objects**: Sequence flows, message flows, associations
- **Swimlanes**: Pools (organizations), Lanes (roles)
- **Artifacts**: Data objects, groups, annotations

**BPMN Levels**:
- **Level 1**: Simple process flow
- **Level 2**: Detailed workflow with exceptions
- **Level 3**: Fully executable (BPEL, workflow engines)

### Process Modeling Perspectives

**As-Is (Current State)**:
- Document existing processes
- Identify inefficiencies
- Baseline for improvement

**To-Be (Future State)**:
- Design improved processes
- Target state definition
- Implementation roadmap

**Should-Be (Ideal State)**:
- Best practice processes
- Unconstrained by current limitations
- Aspir ational vision

### Process Analysis Techniques

**Value Stream Mapping** (Lean Manufacturing):
- Identify value-adding steps
- Eliminate waste (Muda)
- Optimize flow

**Six Sigma DMAIC**:
- **Define**: Problem and goals
- **Measure**: Current performance
- **Analyze**: Root causes
- **Improve**: Solutions
- **Control**: Sustain improvements

**BPR (Business Process Reengineering)**:
- Radical redesign (not incremental)
- Technology-enabled transformation
- Cross-functional processes

### Process Quality Metrics

**Efficiency**:
- Cycle time (end-to-end duration)
- Processing time (actual work time)
- Wait time (delays and queues)

**Quality**:
- Defect rate
- Rework percentage
- First-time right rate

**Cost**:
- Process cost
- Labor cost
- Technology cost

**Flexibility**:
- Adaptability to change
- Exception handling capability
- Scalability

### When to Model Business Processes

- Process improvement initiatives
- System implementation (ERP, CRM)
- Regulatory compliance
- Training and onboarding
- Business continuity planning
- Outsourcing or automation decisions
- Product requirements documentation

### Process Documentation Best Practices

**1. Right Level of Detail**:
- Too high-level = not actionable
- Too detailed = maintenance burden
- Audience-appropriate granularity

**2. Use Standard Notation**:
- BPMN for formal processes
- Flowcharts for simple processes
- Swimlane diagrams for multi-actor processes

**3. Validate with Stakeholders**:
- Process participants review
- Walk through scenarios
- Update based on feedback

**4. Version Control**:
- Track changes over time
- Document rationale for changes
- Maintain historical versions

**5. Link to Other Documentation**:
- User stories
- System requirements
- Technical specifications

### Process Automation

**BPM Systems (BPMS)**:
- Workflow engines
- Process orchestration
- Task management

**RPA (Robotic Process Automation)**:
- Rule-based automation
- UI interaction bots
- Legacy system integration

**Low-Code/No-Code Platforms**:
- Visual process design
- Rapid automation
- Citizen developers

### Related Methodologies

- **Lean**: Eliminate waste (Toyota Production System)
- **Six Sigma**: Reduce variation (Motorola, GE)
- **Theory of Constraints**: Identify bottlenecks (Eliyahu Goldratt)
- **Agile BPM**: Iterative process improvement

### Complementary NioPD Commands

- `/niopd:PD:journey` - User journey mapping (user perspective)
- `/niopd:PD:wireframe` - UI flows (interface perspective)
- `/niopd:PD:stories` - User stories (requirement perspective)
- `/niopd:PM:daci` - Decision-making processes
- `/niopd:ST:design-thinking` - Process innovation

## Usage
`/niopd:PD:process [--for=<prd_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the PRD/initiative name.

**Examples:**
```bash
# Explicit PRD name
/niopd:PD:process --for=dark-mode-feature

# Auto-detect from current directory
cd dark-mode-feature
/niopd:PD:process  # Uses "dark-mode-feature"
```

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Determine PRD Name:**
    -   If `--for=<prd_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected PRD name from current directory: `<directory_name>`"
    -   Store the determined name as `<prd_name>` for use in all subsequent steps

3.  **Validate PRD:**
    -   Check that the PRD file following the naming convention `[YYYYMMDD]-<initiative_slug>-prd-v[version].md` exists in `niopd-workspace/docs/`. If not, inform the user.
    -   Identify the latest version of the PRD file based on the date and version number in the filename.
    -   Verify that the PRD file contains the required sections for business process analysis.
    -   Check for related analysis reports that could enhance business process analysis:
        -   User behavior reports: `niopd-workspace/reports/[YYYYMMDD]-*-behavior-summary-v[version].md`
        -   Feedback summary reports: `niopd-workspace/reports/[YYYYMMDD]-<initiative_slug>-feedback-summary-v[version].md`
        -   User journey reports: `niopd-workspace/reports/[YYYYMMDD]-*-user-journey-v[version].md`

## Instructions

You are a specialized AI expert in business process modeling and visualization. Your goal is to analyze an existing PRD and create comprehensive business process diagrams that illustrate the key workflows and operations described in the document.

**Core Principle:** The final business process diagrams should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Data
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将帮您为 **<prd_name>** PRD 添加业务流程图。"
    -   If English: "I'll help you add business process diagrams to the **<prd_name>** PRD."
    -   For other languages, use an appropriate translation based on user's language preference
-   Read the LATEST version of the PRD file from `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`, ensuring you select the file with the most recent date and highest version number if multiple versions exist.
-   Search for and read relevant analysis reports that could enhance business process analysis:
    -   User behavior reports for insights into current workflows
    -   Feedback summary reports for process pain points and improvement suggestions
    -   User journey reports for end-to-end process understanding
-   Ensure that you are reading the most recent version by checking the date and version in the filename.

### Step 2: PRD Analysis & Validation
- Read and analyze the provided PRD file thoroughly.
- Verify that the file exists and is readable.
- Identify key sections that contain process-related information:
  - Overview and Problem Statement
  - Functional Requirements
  - User Personas & Stories
  - Implementation Plan
  - Rollout Plan
- Note any existing business process information or workflow descriptions.
- Incorporate insights from analysis reports to enrich the understanding of current processes and identify improvement opportunities.

### Step 3: Business Process Identification
- Identify all business processes described or implied in the PRD.
- Extract key workflows from user stories and functional requirements.
- Map out the main business operations that the feature will support.
- Identify process participants (users, systems, external entities) using insights from user behavior reports.
- Note any process variations or alternative flows, informed by feedback summary reports.

### Step 4: Stakeholder & Role Analysis
- Extract user personas and roles from the PRD.
- Enhance role definitions with insights from user behavior reports.
- Identify system components and external services.
- Map stakeholders to their roles in each business process.
- Determine decision points and approval workflows using feedback insights.
- Note any handoffs between different roles or systems.

### Step 5: Workflow Sequence Analysis
- Identify the sequential steps in each business process.
- Determine the order of operations and dependencies.
- Map out decision points and branching logic.
- Identify parallel processes and concurrent activities.
- Note any loops, iterations, or feedback mechanisms.
- Enhance workflow understanding with insights from user journey reports.

### Step 6: Process Boundaries & Scope Definition
- Define the start and end points of each business process.
- Identify process inputs and outputs.
- Determine process boundaries and interfaces with other systems.
- Clarify what is in scope and out of scope for each process.
- Note any assumptions about external systems or processes.

### Step 7: Business Rules & Constraints Identification
- Extract business rules from functional requirements.
- Identify validation rules and data constraints.
- Note approval requirements and authorization levels.
- Identify timing constraints and service level agreements.
- Document any regulatory or compliance requirements.

### Step 8: Exception & Error Handling Analysis
- Identify potential error conditions and exceptions.
- Map out error handling and recovery processes.
- Note fallback procedures and contingency plans.
- Identify failure points and their impact on the business.
- Document error notification and escalation procedures.

### Step 9: Performance & Quality Requirements
- Extract performance requirements related to business processes.
- Identify quality metrics and success criteria.
- Note capacity and scalability considerations.
- Document availability and reliability requirements.
- Identify monitoring and reporting needs.

### Step 10: Business Process Modeling - PlantUML Format
Create detailed business process diagrams using PlantUML Activity Diagram syntax:

1. **Main Workflow Diagram:**
   - Use activity diagrams to show the primary business process flow
   - Include swimlanes for different roles or systems
   - Show decision points with branching logic
   - Include object flows for data and documents
   - Add notes for important business rules or constraints

2. **Alternative Flow Diagrams:**
   - Create separate diagrams for major alternative flows
   - Show exception handling processes
   - Illustrate error recovery workflows
   - Document parallel or concurrent processes

### Step 11: Business Process Modeling - Mermaid Format
Create equivalent business process diagrams using Mermaid Flowchart and Graph syntax:

1. **Main Workflow Diagram:**
   - Use flowcharts to show the primary business process flow
   - Include subgraphs for different roles or systems
   - Show decision points with conditional flows
   - Add styling for different types of activities
   - Include links and descriptions for clarity

2. **Alternative Flow Diagrams:**
   - Create separate diagrams for major alternative flows
   - Show exception handling processes
   - Illustrate error recovery workflows
   - Document parallel or concurrent processes

### Step 12: Business Process Documentation
Generate comprehensive documentation for each business process:

1. **Process Overview:**
   - Purpose and objectives
   - Scope and boundaries
   - Key performance indicators
   - Business value and benefits

2. **Detailed Process Steps:**
   - Step-by-step description of each activity
   - Input and output for each step
   - Responsible roles and stakeholders
   - Required resources and tools
   - Time estimates and dependencies

3. **Decision Points:**
   - Criteria for each decision
   - Possible outcomes and next steps
   - Responsible decision makers
   - Required information or approvals

4. **Exception Handling:**
   - Error conditions and triggers
   - Recovery procedures
   - Escalation paths
   - Contingency plans

### Step 13: Business Process Section Generation
Produce a markdown section that can be added to the PRD with the following structure:

```
---
## 13. Business Processes
*Detailed workflow diagrams and process descriptions that illustrate how the feature will be used in practice*

### Process Overview
*A high-level summary of the key business processes supported by this feature*

#### Main Business Process
This feature supports the following primary business process: [Brief description of the main workflow]

#### Key Process Participants
- **[Role/System]:** [Responsibilities and involvement]
- **[Role/System]:** [Responsibilities and involvement]

#### Business Value
[Description of how this process delivers value to the organization or users]

### Detailed Process Workflows

#### Main Workflow: [Process Name]
*The primary workflow that users will follow to accomplish their goals*

##### Workflow Diagrams
###### PlantUML Activity Diagram
``plantuml
@startuml
' PlantUML activity diagram for the main workflow
' Include swimlanes, activities, decisions, and flows
@enduml
```

###### Mermaid Flowchart
```mermaid
flowchart TD
    %% Mermaid flowchart for the main workflow
    %% Include nodes, edges, and styling
```

##### Process Steps
1. **[Step Name]:** [Detailed description of the activity]
   - **Input:** [Required input data or triggers]
   - **Output:** [Expected output or results]
   - **Role:** [Responsible party]
   - **System:** [Involved systems or tools]

2. **[Step Name]:** [Detailed description of the activity]
   - **Input:** [Required input data or triggers]
   - **Output:** [Expected output or results]
   - **Role:** [Responsible party]
   - **System:** [Involved systems or tools]

##### Decision Points
1. **[Decision Point]:** [Description of the decision to be made]
   - **Criteria:** [Factors that influence the decision]
   - **Outcomes:**
     - **If [Condition]:** [Next step or action]
     - **If [Condition]:** [Next step or action]

##### Business Rules
- **[Rule]:** [Description of the business rule or constraint]
- **[Rule]:** [Description of the business rule or constraint]

#### Alternative Workflow: [Process Name]
*An alternative or exception workflow that may occur under specific conditions*

##### Workflow Diagrams
###### PlantUML Activity Diagram
``plantuml
@startuml
' PlantUML activity diagram for the alternative workflow
@enduml
```

###### Mermaid Flowchart
```mermaid
flowchart TD
    %% Mermaid flowchart for the alternative workflow
```

##### Process Description
[Detailed description of when this workflow is used and how it differs from the main workflow]

### Process Metrics & Monitoring
*Key performance indicators and monitoring approaches for the business processes*

#### Success Metrics
- **[Metric]:** [Definition, target, and measurement approach]
- **[Metric]:** [Definition, target, and measurement approach]

#### Monitoring Approach
[Description of how process performance will be tracked and measured]

#### Quality Gates
[Description of checkpoints and validation criteria during process execution]

### Process Assumptions & Dependencies
*Key assumptions and external dependencies that affect the business processes*

#### Assumptions
- **[Assumption]:** [Description and potential impact if incorrect]
- **[Assumption]:** [Description and potential impact if incorrect]

#### Dependencies
- **[Dependency]:** [Description of the dependency and its impact]
- **[Dependency]:** [Description of the dependency and its impact]

---

```

### Step 14: PRD Integration
- Locate the appropriate position in the PRD to insert the Business Processes section (typically after Implementation Plan or before Risk Assessment).
- Ensure the section numbering is consistent with the existing PRD structure.
- Integrate the generated content into the PRD document.
- Update the table of contents if present in the PRD.

### Step 15: Save the Updated PRD
- Generate a filename for the updated PRD following the NioPD naming convention: `[YYYYMMDD]-<initiative_slug>-prd-v[version].md`.
- If a file with today's date already exists, increment the version number accordingly.
- Save the updated PRD to: `niopd-workspace/docs/[filename]`

### Step 16: Confirm and Conclude
-   Confirm the action is complete: "✅ I've added business process diagrams to the **<prd_name>** PRD."
-   Provide the path to the file: "You can review the updated PRD at: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`"
-   Suggest next steps: "Consider using /niopd:PD:roadmap to add a timeline, /niopd:PD:integrate to incorporate additional strategic insights, /niopd:PM:feature-metrics to define success metrics, or /niopd:PM:release to plan your release. For a complete PRD workflow, use /niopd:PD:workflow to guide you through the next steps."

## Error Handling
- **Missing PRD File:** If the PRD file is not found, clearly explain the issue and suggest verifying the file name or creating a PRD first.
- **Incomplete PRD Information:** If the PRD lacks sufficient information for process modeling, explain what additional information is needed and offer to proceed with placeholders.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.
- **Complex Process Identification:** If business processes are difficult to identify, suggest reviewing specific sections of the PRD or conducting a clarification session.
- **Diagram Generation Issues:** If there are problems generating diagrams, explain the limitations and offer alternative visualization approaches.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial business process documentation can still provide value.

### Suggest Next Steps
- After adding business process diagrams to the PRD, you might want to add user journey diagrams to better understand the user experience by running `/niopd:PD:journey --for=<prd_name>`.
- Consider generating detailed user stories and acceptance criteria by running `/niopd:PD:stories --for=<prd_name>` to break down the requirements into actionable development tasks.
- You can also add a roadmap Gantt chart to the timing section by running `/niopd:PD:roadmap --for=<prd_name>` for strategic planning.
- For user-facing documentation, you might want to generate a comprehensive FAQ document by running `/niopd:user:faq --for=<prd_name>`.
