---
argument-hint: [--for=<prd_name>]
description: Writes detailed user stories and acceptance criteria for a PRD, and updates the PRD with a user stories table section. Auto-detects PRD name from current directory if not specified.
---

# Command: /niopd:PD:stories

This command generates detailed user stories and acceptance criteria for a specific Product Requirements Document (PRD) and updates the PRD with a "用户故事" (User Stories) section in table format.

## Theoretical Foundation

### Origin and Development
User Stories were introduced by **Kent Beck** in the late 1990s as part of Extreme Programming (XP). The format was popularized by **Mike Cohn** in his 2004 book "User Stories Applied" and **Ron Jeffries** through the "3 C's" model (Card, Conversation, Confirmation).

### Core Principle
User Stories shift focus from writing about requirements to **talking about them**. They serve as placeholders for conversations, emphasizing user value over technical implementation. The goal is to capture "who, what, and why" in a simple, understandable format.

### The User Story Format

**Standard Template**:
"**As a** [persona], **I want** [action/capability], **so that** [benefit/value]"

**Components**:
1. **Persona**: Who benefits? (role or user type)
2. **Action**: What do they want to do? (capability or feature)
3. **Benefit**: Why do they want it? (value or outcome)

**Example**: "As a mobile user, I want dark mode, so that I can reduce eye strain at night."

### The Three C's (Ron Jeffries)

1. **Card**: Written placeholder
   - Brief description on index card or digital tool
   - Enough to remember and estimate
   - Not comprehensive documentation

2. **Conversation**: Verbal collaboration
   - Details emerge through discussion
   - Shared understanding develops
   - Questions answered iteratively

3. **Confirmation**: Acceptance criteria
   - Specific, testable conditions
   - Definition of "done"
   - Basis for testing

### INVEST Criteria (Bill Wake, 2003)

Good user stories are:
- **I**ndependent: Can be developed in any order
- **N**egotiable: Details flexible until implementation
- **V**aluable: Delivers value to users or business
- **E**stimable: Team can estimate effort
- **S**mall: Completable within one iteration
- **T**estable: Clear success criteria

### Acceptance Criteria Formats

**Given-When-Then (BDD)**:
- **Given** [precondition/context]
- **When** [action/event]
- **Then** [expected outcome]

Example:
- Given I'm logged into the app
- When I navigate to settings and toggle dark mode
- Then the app interface changes to dark color scheme

**Checklist Format**:
- [ ] Condition 1 is met
- [ ] Condition 2 is met
- [ ] Condition 3 is met

### Story Sizing

**T-Shirt Sizing**: XS, S, M, L, XL
**Fibonacci Sequence**: 1, 2, 3, 5, 8, 13, 21 (story points)
**Ideal Days**: Estimated days of focused work

### Story Hierarchy

1. **Epic**: Large body of work (months)
2. **Feature**: Group of related stories (weeks)
3. **User Story**: Single deliverable (days)
4. **Task**: Technical work item (hours)

### When to Use User Stories
- Agile/Scrum development
- Backlog management
- Sprint planning
- Feature specification
- Cross-functional communication
- User-centered design

### Story Mapping (Jeff Patton, 2005)

Organize stories into:
- **Backbone**: User journey steps (horizontal)
- **Walking Skeleton**: Minimum viable features (top row)
- **Priority Layers**: Additional capabilities (lower rows)

### Anti-Patterns to Avoid
- **Too Technical**: "As a developer, I want to refactor..."
- **Too Large**: Epics disguised as stories
- **No Value**: "I want [feature]" without "so that [benefit]"
- **Implementation Details**: Specifying "how" instead of "what"

### Related Frameworks
- **Use Cases**: UML-based requirement format
- **Job Stories**: JTBD-inspired format ("When [situation], I want to [motivation], so I can [outcome]")
- **Behavior-Driven Development (BDD)**: Given-When-Then scenarios

### Complementary NioPD Commands
- `/niopd:PD:acceptance-criteria` - Detailed acceptance criteria
- `/niopd:PD:draft-prd` - PRD foundation
- `/niopd:UR:personas` - User persona research
- `/niopd:UR:jtbd` - Understanding user motivations

## Usage
`/niopd:PD:stories [--for=<prd_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the PRD/initiative name.

**Examples:**
```bash
# Explicit PRD name
/niopd:PD:stories --for=dark-mode-feature

# Auto-detect from current directory
cd dark-mode-feature
/niopd:PD:stories  # Uses "dark-mode-feature"
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
    -   Check for related analysis reports that could enhance user story creation:
        -   Feedback summary reports: `niopd-workspace/reports/[YYYYMMDD]-<initiative_slug>-feedback-summary-v[version].md`
        -   User personas reports: `niopd-workspace/reports/[YYYYMMDD]-*-personas-v[version].md`
        -   User journey reports: `niopd-workspace/reports/[YYYYMMDD]-*-user-journey-v[version].md`
        -   User behavior reports: `niopd-workspace/reports/[YYYYMMDD]-*-behavior-summary-v[version].md`
        -   Satisfaction analysis reports: `niopd-workspace/reports/[YYYYMMDD]-*-satisfaction-v[version].md`

## Instructions

You are a specialized AI expert in writing detailed user stories and acceptance criteria from PRD documents. Your goal is to transform high-level requirements into specific, testable user stories that development teams can implement.

**Core Principle:** The final user stories document should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Data
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将帮您为 **<prd_name>** PRD 创建详细的用户故事和验收标准。"
    -   If English: "I'll help you create detailed user stories and acceptance criteria for the **<prd_name>** PRD."
    -   For other languages, use an appropriate translation based on user's language preference
-   Read the LATEST version of the PRD file from `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`, ensuring you select the file with the most recent date and highest version number if multiple versions exist.
-   Search for and read relevant analysis reports that could enhance user story creation:
    -   Feedback summary reports for user pain points and feature requests
    -   User personas reports for detailed user characteristics
    -   User journey reports for workflow insights
    -   User behavior reports for usage patterns
    -   Satisfaction analysis reports for user sentiment
-   Ensure that you are reading the most recent version by checking the date and version in the filename.

### Step 2: PRD Analysis & Validation
- Read and analyze the provided PRD file.
- Verify that the file exists and is readable.
- Identify key sections: functional requirements, non-functional requirements, user personas.
- Note any missing or incomplete information.
- Incorporate insights from related analysis reports to enrich the understanding of requirements.

### Step 3: Persona Identification & Analysis
- Extract user personas defined in the PRD.
- Enhance personas with details from user personas reports if available.
- If personas are not well-defined, create generic personas based on context and user behavior reports.
- Analyze each persona's goals, needs, and behaviors using insights from user journey and behavior reports.
- Identify key user journeys and workflows from user journey reports.

### Step 4: Functional Requirement Mapping
- Identify all functional requirements in the PRD.
- Map requirements to user personas and their goals.
- Enhance requirements with insights from feedback summary reports, specifically "Pain Points" and "Feature Requests".
- Note any ambiguous or unclear requirements.
- Extract specific features and capabilities to be implemented.

### Step 5: Non-Functional Requirement Mapping
- Identify all non-functional requirements in the PRD.
- Categorize requirements (performance, security, accessibility, etc.).
- Map requirements to technical stakeholders and implementation considerations.
- Enhance non-functional requirements with insights from satisfaction analysis reports.
- Note any technical constraints or limitations.

### Step 6: User Story Creation
- For each functional requirement, create user stories following the format:
  "As a [persona], I want to [action], so that [benefit]."
- Ensure stories are specific, testable, and valuable.
- Assign appropriate priorities (High/Medium/Low) to each story.
- Estimate story points if provided in the PRD.

### Step 7: Acceptance Criteria Development
- For each user story, develop clear acceptance criteria.
- Use the Given/When/Then format for testable criteria.
- Ensure criteria cover happy path, alternative flows, and error conditions.
- Include specific, measurable validation conditions.

### Step 8: Edge Case Identification
- Identify potential edge cases for each user story.
- Consider error conditions, boundary values, and exceptional scenarios.
- Develop alternative flows and their validation criteria.
- Note any complex business logic or special handling requirements.

### Step 9: Cross-Cutting Story Development
- Create stories for non-functional requirements:
  - Performance requirements
  - Security requirements
  - Accessibility requirements
  - Technical debt and maintenance tasks
- Ensure these stories follow the same format and quality standards.

### Step 10: Story Mapping & Prioritization
- Organize user stories into logical epics and themes.
- Group related stories together for coherent implementation.
- Prioritize stories based on business value and dependencies.
- Create a visual story map showing relationships and flow.

### Step 11: Requirements Traceability
- Map each functional requirement to corresponding user stories.
- Ensure all PRD requirements are addressed by at least one story.
- Note any requirements that require multiple stories.
- Create a traceability matrix for verification.

### Step 12: Validation & Quality Check
- Review all user stories for completeness and quality.
- Ensure stories follow the INVEST principles (Independent, Negotiable, Valuable, Estimable, Small, Testable).
- Verify that acceptance criteria are specific and testable.
- Check for any missing requirements or gaps in coverage.

### Step 13: Assumptions & Dependencies Documentation
- Document any assumptions made during story creation.
- Identify dependencies between stories or external factors.
- Note any clarifications needed from stakeholders.
- Include this information in the final report.

### Step 14: User Stories Report Generation
Produce a markdown report with the following structure:

---
# User Stories: [Initiative/Feature Name]

## Executive Summary
*A brief overview of the user stories created and their alignment with PRD objectives*

## Stories by Persona
### [Persona Name]
#### Story 1: [Brief descriptive title]
- **As a** [persona], **I want to** [action], **so that** [benefit]
- **Priority:** [High/Medium/Low]
- **Story Points:** [Estimate if provided]

##### Acceptance Criteria
1. **[Given]** [precondition], **when** [action], **then** [expected outcome]
2. **[Given]** [precondition], **when** [action], **then** [expected outcome]
3. **[Given]** [precondition], **when** [action], **then** [expected outcome]

##### Edge Cases & Alternatives
- **[Edge Case]:** [Description and expected handling]
- **[Alternative Flow]:** [Description and validation criteria]

#### Story 2: [Brief descriptive title]
- **As a** [persona], **I want to** [action], **so that** [benefit]
- **Priority:** [High/Medium/Low]
- **Story Points:** [Estimate if provided]

##### Acceptance Criteria
1. **[Given]** [precondition], **when** [action], **then** [expected outcome]
2. **[Given]** [precondition], **when** [action], **then** [expected outcome]
3. **[Given]** [precondition], **when** [action], **then** [expected outcome]
4. **[Given]** [precondition], **when** [action], **then** [expected outcome]

### [Next Persona Name]
[Repeat story structure for each persona]

## Cross-Cutting Stories
### Non-Functional Requirements
#### Performance
- **As a** [user/system], **I want** [performance characteristic], **so that** [benefit]
- **Acceptance Criteria:**
  1. [Measurable performance criterion]
  2. [Measurable performance criterion]

#### Security
- **As a** [security stakeholder], **I want** [security feature], **so that** [risk mitigated]
- **Acceptance Criteria:**
  1. [Security validation criterion]
  2. [Security validation criterion]

#### Accessibility
- **As a** [user with disability], **I want** [accessibility feature], **so that** [equal access]
- **Acceptance Criteria:**
  1. [Accessibility validation criterion]
  2. [Accessibility validation criterion]

### Technical Debt & Maintenance
#### Story: [Technical task description]
- **As a** [developer/tech lead], **I want to** [technical action], **so that** [maintainability/scalability benefit]
- **Acceptance Criteria:**
  1. [Technical validation criterion]
  2. [Technical validation criterion]

## Story Mapping
### Epic: [Main Feature Epic Name]
1. **[Story Title]** - [Priority] - [Story Points]
2. **[Story Title]** - [Priority] - [Story Points]
3. **[Story Title]** - [Priority] - [Story Points]

### Epic: [Supporting Feature Epic Name]
1. **[Story Title]** - [Priority] - [Story Points]
2. **[Story Title]** - [Priority] - [Story Points]

## Requirements Traceability
### PRD Section 4. Functional Requirements
- **FR1:** Addressed by stories [Story IDs]
- **FR2:** Addressed by stories [Story IDs]

### PRD Section 5. Non-Functional Requirements
- **NFR1:** Addressed by stories [Story IDs]
- **NFR2:** Addressed by stories [Story IDs]

## Validation Checklist
- [ ] All PRD functional requirements covered
- [ ] All PRD non-functional requirements covered
- [ ] Acceptance criteria are testable and specific
- [ ] Edge cases identified and addressed
- [ ] User flows are complete and logical
- [ ] Stories follow INVEST principles
- [ ] Acceptance criteria follow Given/When/Then format

## Assumptions & Dependencies
### Assumptions
- **[Assumption]:** [Description and potential impact if incorrect]

### Dependencies
- **[Dependency]:** [Description and impact on story implementation]

---
*Report generated on [Date]*
*Based on PRD: [PRD File Name]*

### Step 11: Save the Updated PRD
- Generate a filename for the updated PRD following the NioPD naming convention: `[YYYYMMDD]-<initiative_slug>-prd-v[version].md`.
- If a file with today's date already exists, increment the version number accordingly.
- Save the updated PRD to: `niopd-workspace/docs/[filename]`

### Step 12: Confirm and Conclude
-   Confirm the action is complete: "✅ I've generated detailed user stories and acceptance criteria for **<prd_name>** and updated the PRD with a user stories table section."
-   Provide the path to the file: "You can view them here: `niopd-workspace/reports/[YYYYMMDD]-<initiative_slug>-user-stories-v[version].md`"
-   Inform the user that the PRD has been updated with the user stories table section
-   Suggest next steps: "Consider using /niopd:PD:journey to add user journey maps, /niopd:PD:process to document business processes, /niopd:PD:integrate to incorporate additional insights from analysis reports, or /niopd:PO:faq to create a FAQ document. For a complete PRD workflow, use /niopd:PD:workflow to guide you through the next steps."

## Error Handling
- **Incomplete PRD:** If the PRD lacks sufficient detail for story creation, explain what information is missing and suggest requesting clarification.
- **Ambiguous Requirements:** If PRD requirements are unclear, note the ambiguity and provide interpretations with suggestions for clarification.
- **Missing Personas:** If user personas are not well-defined in the PRD, create generic personas based on context or suggest defining them.
- **Conflicting Information:** If the PRD contains contradictory information, highlight the conflicts and suggest resolution approaches.
- **Technical Limitations:** If requirements seem technically infeasible, note this with alternative suggestions.

In all error cases, provide clear explanations, suggest alternatives or additional information needed, and emphasize that partial story creation can still provide value.

### Suggest Next Steps
- After generating user stories and updating the PRD, you might want to create a comprehensive FAQ document by running `/niopd:PO:faq --for=<prd_name>` to address common questions about the feature.
- Consider adding user journey maps to visualize the user experience by running `/niopd:PD:journey --for=<prd_name>`.
- You can also add business process diagrams to visualize workflows by running `/niopd:PD:process --for=<prd_name>`.
- For strategic planning, you can add a roadmap Gantt chart to the timing section by running `/niopd:PD:roadmap --for=<prd_name>`.
