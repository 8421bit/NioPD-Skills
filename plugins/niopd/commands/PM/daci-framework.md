---
argument-hint: [--decision=<decision_topic>] [--stakeholders=<stakeholder_list>] [--options=<decision_options>]
description: Applies the DACI framework to clarify roles in decisions (Driver, Approver, Contributors, Informed).
---

# Command: /niopd:PM:daci-framework

This command applies the DACI framework to clarify roles in decisions, ensuring clear accountability and effective decision-making processes.

## Theoretical Foundation

### Origin and Development
The DACI framework was developed by **Intuit** in the early 2000s as a decision-making model to clarify roles and accelerate decisions in cross-functional teams. It evolved from RACI (Responsible, Accountable, Consulted, Informed) but emphasizes one **Driver** and one **Approver** for faster execution.

### Core Principle
DACI provides **role clarity in decision-making** by explicitly assigning one person to drive the process and one to make the final call, while ensuring appropriate input and communication. This prevents decision paralysis and diffused accountability.

### DACI Roles Defined

**D - Driver (One Person)**:
- **Leads** the decision-making process
- **Gathers** input from contributors
- **Facilitates** discussions and analysis
- **Recommends** a course of action
- **Executes** after approval
- **NOT** the final decision-maker

**A - Approver (One Person)**:
- **Makes** the final decision
- **Has** authority and accountability
- **Considers** driver's recommendation
- **Can** accept, reject, or request more info
- **Must** be consulted before finalization

**C - Contributors (Multiple People)**:
- **Provide** input and expertise
- **Are** consulted during process
- **Give** recommendations
- **No** veto power
- **Participate** in discussions

**I - Informed (Multiple People)**:
- **Receive** updates on decision
- **Are** notified after decision made
- **Do NOT** provide input
- **Need** to know for implementation
- **Can** ask clarifying questions

### DACI vs. RACI

**RACI** (Traditional):
- **R**esponsible: Does the work
- **A**ccountable: Final authority (only one)
- **C**onsulted: Two-way communication
- **I**nformed: One-way communication
- **Challenge**: Can have multiple "R"s, unclear who drives

**DACI** (Modern):
- **Single Driver**: Clear process owner
- **Single Approver**: Clear decision authority
- **Faster**: Streamlined for speed
- **Better for**: Product teams, cross-functional decisions

### When to Use DACI

- **Cross-functional decisions**: Multiple teams involved
- **Strategic choices**: Significant impact
- **Resource allocation**: Budget, headcount decisions
- **Product decisions**: Feature prioritization, roadmap
- **Organizational changes**: Process, structure changes
- **Conflicting stakeholders**: Need clear authority

### DACI Decision Process

**1. Frame the Decision**:
- What needs to be decided?
- By when?
- What criteria matter?

**2. Assign DACI Roles**:
- Who should drive?
- Who has final authority?
- Who has relevant expertise?
- Who needs to know?

**3. Gather Input**:
- Driver collects contributor input
- Research and analysis
- Options evaluation

**4. Make Recommendation**:
- Driver proposes decision
- Includes rationale
- Presents to Approver

**5. Decide**:
- Approver makes call
- Considers all input
- Communicates decision

**6. Inform & Execute**:
- Notify "Informed" group
- Driver leads implementation
- Monitor outcomes

### Choosing the Right Driver

Good Driver characteristics:
- **Closest** to the decision
- **Available** to dedicate time
- **Trusted** by contributors
- **Organized** to manage process
- **Neutral** enough to be objective

### Choosing the Right Approver

Good Approver characteristics:
- **Authority** to make decision
- **Accountability** for outcomes
- **Context** on broader implications
- **Availability** to decide promptly
- **NOT** the most senior person (escalate only when needed)

### Common Pitfalls

❌ **No clear Driver**: Decision stalls
❌ **Multiple Approvers**: Consensus paralysis
❌ **Too many Contributors**: Analysis paralysis
❌ **Driver = Approver**: No objectivity
❌ **No deadline**: Decision drags
❌ **Forgetting to Inform**: Poor communication

### Complementary NioPD Commands

- `/niopd:PM:draft-pid` - Project governance structure
- `/niopd:ST:swot` - Decision analysis framework
- `/niopd:PM:risk-analysis` - Risk assessment for decisions
- `/niopd:PO:stakeholder-update` - Communicate decisions

## Implementation Plan

1. Create a structured DACI framework analysis:
   - Decision topic and context
   - Stakeholder identification and roles
   - Option evaluation and recommendation
   - Decision execution plan

2. Gather input data about the decision topic, stakeholders, and options

3. Generate detailed DACI role assignments for each stakeholder

4. Provide decision framework and execution plan

5. Save the DACI Framework report to niopd-workspace/plans/

## Usage
`/niopd:PM:daci-framework [--decision=<decision_topic>] [--stakeholders=<stakeholders>] [--options=<options>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Parameters:**
    -   If `--decision` is not provided, prompt the user to specify the decision topic.
    -   Optional: `--stakeholders` and `--options` can be provided or gathered interactively.

3.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/plans` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in decision-making frameworks and organizational governance. Your goal is to help teams clarify decision roles using the DACI framework to ensure efficient, accountable decision-making.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Data
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request with a message in the user's preferred language:
    -   If Chinese: "我将帮您应用DACI框架来明确 **<decision_topic>** 决策的角色。"
    -   If English: "I'll help you apply the DACI framework to clarify decision roles for: **<decision_topic>**."
    -   For other languages, use an appropriate translation based on user's language preference
-   If the `--decision` argument wasn't provided, ask the user in their preferred language: "What decision needs to be made?" and wait for their response.
-   If the `--stakeholders` argument wasn't provided, ask the user in their preferred language: "Who are the key stakeholders for this decision?" and wait for their response.
-   If the `--options` argument wasn't provided, ask the user in their preferred language: "What options are you considering?" and wait for their response.

### Step 2: Decision Context Analysis
-   Help the user define the decision context:
    -   "What problem or opportunity is driving this decision?"
    -   "What is the timeline for making this decision?"
    -   "What is the scope of impact? (team, department, company, external)"
    -   "What are the success criteria for a good decision?"
-   Wait for the user's responses.

### Step 3: Stakeholder Identification
-   Identify all relevant stakeholders:
    -   "Let's list all people or groups affected by or involved in this decision."
    -   For each stakeholder:
        -   "What is their role/position?"
        -   "What is their level of interest? (High/Medium/Low)"
        -   "What is their level of influence? (High/Medium/Low)"
        -   "What expertise or perspective do they bring?"
-   Wait for the user's responses.

### Step 4: Driver Assignment
-   Assign the Driver role:
    -   "Who should be the Driver - the person leading this decision process?"
    -   "This person will:"
        -   "Define the decision process and timeline"
        -   "Gather input from Contributors"
        -   "Facilitate discussions"
        -   "Present recommendation to the Approver"
    -   "Does this person have the authority and capacity to drive this?"
-   Wait for the user's responses.

### Step 5: Approver Assignment
-   Assign the Approver role:
    -   "Who should be the Approver - the person making the final decision?"
    -   "This should be someone who:"
        -   "Has the authority to commit resources"
        -   "Will be accountable for the outcome"
        -   "Can make the decision in a timely manner"
    -   "Note: There should be only ONE Approver to avoid decision paralysis."
-   Wait for the user's responses.

### Step 6: Contributors Identification
-   Identify Contributors:
    -   "Who should be Contributors - people providing input and expertise?"
    -   For each Contributor:
        -   "What specific expertise do they bring?"
        -   "What input do you need from them?"
        -   "When do you need their input?"
        -   "How will you engage with them? (meetings, surveys, documents)"
-   Wait for the user's responses.

### Step 7: Informed Parties Identification
-   Identify who needs to be Informed:
    -   "Who needs to be Informed - people who should know about the decision but don't provide input?"
    -   For each Informed party:
        -   "What do they need to know?"
        -   "When do they need to be informed? (before, during, after decision)"
        -   "How will you communicate with them?"
-   Wait for the user's responses.

### Step 8: Decision Criteria Definition
-   Define decision criteria:
    -   "What are the primary objectives this decision should achieve?"
    -   "How will you measure if it's a good decision?"
    -   "What are the must-have requirements (deal-breakers)?"
    -   "What are the nice-to-have preferences?"
    -   "What is your risk tolerance for this decision?"
-   Wait for the user's responses.

### Step 9: Options Analysis
-   Analyze available options:
    -   For each option:
        -   "What are the pros and cons?"
        -   "What is the estimated cost and effort?"
        -   "What are the risks?"
        -   "How well does it meet the decision criteria?"
    -   "Are there any hybrid or alternative options to consider?"
-   Wait for the user's responses.

### Step 10: Decision Process Planning
-   Plan the decision process:
    -   "What is the timeline for each phase?"
        -   "Input gathering"
        -   "Analysis and recommendation"
        -   "Approval"
        -   "Communication"
    -   "What meetings or discussions are needed?"
    -   "What documentation will be created?"
-   Wait for the user's responses.

### Step 11: Communication Planning
-   Plan stakeholder communication:
    -   "How will you engage each stakeholder group?"
    -   "What is the communication frequency?"
    -   "What channels will you use? (email, meetings, dashboards)"
    -   "How will you handle feedback and concerns?"
-   Wait for the user's responses.

### Step 12: Create DACI Framework Document

Produce a markdown DACI framework document that includes all the information gathered. The document should follow a clear structure with:
- Decision context and background
- DACI role assignments (Driver, Approver, Contributors, Informed)
- Stakeholder analysis
- Decision options with pros/cons
- Decision criteria and evaluation
- Timeline and process
- Communication plan

### Step 13: Save the DACI Document
- Generate a filename following the NioPD naming convention: `[YYYYMMDD]-[decision_slug]-daci-v[version].md`.
- Save the document to: `niopd-workspace/plans/[filename]`

### Step 14: Confirm and Conclude
- Confirm the action is complete: "✅ I've created the DACI framework document for the decision: **<decision_topic>**."
- Provide the path to the file: "You can view it at: `niopd-workspace/plans/[YYYYMMDD]-[decision_slug]-daci-v[version].md`"
- Suggest next steps: "Consider scheduling a kickoff meeting with the Driver and Contributors to review roles and timeline."

## Error Handling
- **Unclear Decision:** If the decision topic is vague, help the user clarify and scope it appropriately.
- **Too Many Approvers:** If multiple Approvers are suggested, explain the risks and help identify the single decision-maker.
- **Missing Stakeholders:** If key stakeholders aren't identified, prompt the user to consider additional groups that might be affected.
- **Unrealistic Timeline:** If the decision timeline conflicts with stakeholder availability, highlight the issue and suggest adjustments.

In all error cases, provide constructive guidance, explain the DACI principles, and help the user create an effective decision-making structure.
