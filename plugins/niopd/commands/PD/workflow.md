---
argument-hint: [--phase=<phase_name>]
description: Guides users through the complete PRD development workflow with recommended next steps.
---

# Command: /niopd:PD:workflow

This command guides users through the complete PRD development workflow with recommended next steps.

## Theoretical Foundation

### Origin and Development
Product development workflows emerged from **software engineering process models** (Waterfall - Winston Royce, 1970; Spiral - Barry Boehm, 1986) and evolved through **Agile methodologies** (Agile Manifesto, 2001). Modern product workflows integrate **Lean Startup** (Eric Ries, 2011), **Design Thinking** (IDEO, Stanford d.school), and **Continuous Discovery** (Teresa Torres, 2021).

### Core Principle
A product development workflow defines the **structured sequence of activities** that transform an idea into a shipped product. It provides a repeatable process while allowing flexibility for iteration, learning, and adaptation based on user feedback and market conditions.

### Product Development Process Models

**Waterfall (Sequential)**:
1. Requirements gathering
2. Design
3. Implementation
4. Verification/Testing
5. Maintenance
- **Pros**: Clear phases, comprehensive documentation
- **Cons**: Inflexible, late user feedback

**Agile (Iterative)**:
1. Sprint Planning
2. Development
3. Testing
4. Review/Retrospective
- **Pros**: Flexible, frequent feedback, working software
- **Cons**: Less predictable, requires discipline

**Lean Startup (Hypothesis-Driven)**:
1. **Build**: MVP (Minimum Viable Product)
2. **Measure**: Metrics and user feedback
3. **Learn**: Validated learning
4. **Decide**: Pivot or Persevere
- **Pros**: Reduces waste, validates assumptions
- **Cons**: Requires measurement capability

**Design Thinking (Human-Centered)**:
1. **Empathize**: User research
2. **Define**: Problem framing
3. **Ideate**: Solution generation
4. **Prototype**: Build tangible concepts
5. **Test**: User validation
- **Pros**: User-centered, creative exploration
- **Cons**: Can be time-consuming

**Dual-Track Agile (Discovery + Delivery)**:
- **Discovery Track**: Research, validation, prototyping
- **Delivery Track**: Building, shipping, iterating
- **Parallel execution**: Discovery ahead of delivery
- **Pros**: Reduces risk, continuous learning

### NioPD's Documentation Workflow

The NioPD workflow follows a **structured yet flexible** approach:

**Phase 1: Discovery & Strategy**
1. **Initiative Creation**: Define opportunity (`/niopd:BS:new-initiative`)
2. **Market Analysis**: MR commands (trends, segmentation, competitors)
3. **User Research**: UR commands (feedback, personas, JTBD)
4. **Strategic Analysis**: ST commands (SWOT, PEST, Porter's Five Forces)

**Phase 2: Strategic Documentation**
1. **MRD (Market Requirements)**: Market perspective (`/niopd:PD:draft-mrd`)
2. **PSD (Product Strategy)**: Strategic synthesis (`/niopd:PD:draft-psd`)

**Phase 3: Detailed Requirements**
1. **PRD (Product Requirements)**: Execution specs (`/niopd:PD:draft-prd`)
2. **User Stories**: Agile requirements (`/niopd:PD:stories`)
3. **Acceptance Criteria**: Testable conditions (`/niopd:PD:acceptance-criteria`)

**Phase 4: Design & Planning**
1. **User Journeys**: Experience mapping (`/niopd:PD:journey`)
2. **Business Processes**: Workflow diagrams (`/niopd:PD:process`)
3. **Wireframes**: UI concepts (`/niopd:PD:wireframe`)
4. **Roadmap**: Timeline planning (`/niopd:PD:roadmap`)

**Phase 5: Execution & Operations**
1. **Project Management**: PM commands (KPIs, releases, updates)
2. **Product Operations**: PO commands (metrics, FAQ, stakeholder updates)

### Document Hierarchy Integration

```
MRD (Market Layer)
 ↓
PSD (Strategy Bridge)
 ↓  
PRD (Execution Layer)
 ↓
User Stories, Wireframes, Roadmap
 ↓
Development & Launch
```

### Workflow Flexibility

**Not Always Linear**:
- Can start at any phase based on context
- Iterate back to earlier phases based on learning
- Skip phases if not applicable

**Adapt to Project Type**:
- **New Product**: Full MRD → PSD → PRD flow
- **Feature Addition**: Start with PRD, reference existing strategy
- **Optimization**: User research → PRD updates
- **Bug Fix**: Skip strategy, go straight to requirements

### Process Gates and Reviews

**Gate 1: Opportunity Validation**
- Is this worth pursuing?
- Market size sufficient?
- Strategic fit confirmed?
- **Decision**: Proceed to MRD or stop

**Gate 2: Strategic Alignment**
- Strategy clear and agreed?
- Priorities aligned with resources?
- Success metrics defined?
- **Decision**: Proceed to PRD or refine strategy

**Gate 3: Requirements Ready**
- Requirements complete and unambiguous?
- Acceptance criteria testable?
- Design validated with users?
- **Decision**: Greenlight development or iterate

**Gate 4: Launch Readiness**
- Quality standards met?
- Success metrics tracking ready?
- Go-to-market plan in place?
- **Decision**: Ship or delay

### Stakeholder Involvement

**Phase 1 (Discovery)**:
- Product Management: Lead
- Users/Customers: Research participants
- Sales/Marketing: Market insights
- Leadership: Strategic guidance

**Phase 2 (Strategy)**:
- Product Management: Lead
- Leadership: Review and approve
- Engineering: Feasibility input
- Design: UX perspective

**Phase 3 (Requirements)**:
- Product Management: Lead
- Engineering: Technical review
- Design: Design review
- QA: Testability review

**Phase 4 (Execution)**:
- Engineering: Lead
- Product Management: Support
- Design: Collaboration
- QA: Quality assurance

### Best Practices

1. **Start with Why**: Problem before solution
2. **Involve Users Early**: Continuous discovery
3. **Document Decisions**: Rationale for choices
4. **Iterate Based on Learning**: Adapt the plan
5. **Balance Speed and Quality**: Right level of rigor
6. **Maintain Traceability**: Connect strategy to execution

### Related Frameworks

- **Stage-Gate Process**: Robert G. Cooper (phase-gate reviews)
- **Scrum**: Sprint-based development (Schwaber & Sutherland)
- **Shape Up**: Basecamp's 6-week cycles (Ryan Singer)
- **GIST Planning**: Goals, Ideas, Steps, Tasks (Itamar Gilad)

### Complementary NioPD Commands

All PD, MR, UR, ST, PM, and PO commands integrate into this workflow. The `/niopd:PD:workflow` command serves as a **navigation guide** through the complete NioPD system.

## Usage
`/niopd:PD:workflow [--phase=<phase_name>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Validate Inputs:**
    -   Check if `--phase` argument is provided for the workflow phase.

## Instructions

You are Nio, an AI Product Assistant. Your task is to guide users through the complete PRD development workflow.

**Core Principle:** The final workflow guidance should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Data
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将引导您完成完整的PRD开发工作流程。"
    -   If English: "I'll guide you through the complete PRD development workflow."
    -   For other languages, use an appropriate translation based on user's language preference
-   If the `--phase` argument wasn't provided, ask the user in their preferred language: "您想从PRD工作流程的哪个阶段开始？" and wait for their response.

### Step 2: Explain the Complete PRD Workflow
-   Present the complete PRD development workflow:
    1.  **Discovery & Analysis:**
        -   Conduct market research with `/niopd:MR:*` commands
        -   Analyze user feedback with `/niopd:UR:*` commands
        -   Perform strategic analysis with `/niopd:ST:*` commands
    2.  **PRD Drafting:**
        -   Create initial PRD with `/niopd:PD:draft`
        -   Integrate analysis reports with `/niopd:PD:integrate`
    3.  **Detailing & Refinement:**
        -   Generate user stories with `/niopd:PD:stories`
        -   Add user journeys with `/niopd:PD:journey`
        -   Document processes with `/niopd:PD:process`
        -   Create personas with `/niopd:UR:personas`
    4.  **Planning & Strategy:**
        -   Add roadmap with `/niopd:PD:roadmap`
        -   Define metrics with `/niopd:PM:feature-metrics`
        -   Prioritize with `/niopd:PD:kano-model`, `/niopd:PD:moscow-prioritization`, or `/niopd:PD:rice-prioritization`
    5.  **Validation & Optimization:**
        -   Create opportunity-solution trees with `/niopd:PD:opportunity-solution-tree`
        -   Analyze competitive positioning with `/niopd:MR:compare-products`
        -   Generate wireframes with `/niopd:PD:wireframe`
        -   Define acceptance criteria with `/niopd:PD:acceptance-criteria`

### Step 3: Guide Through Current Phase
-   Based on the user's selected phase, guide them through the appropriate workflow:
    -   If "Requirements Discovery & Definition":
        -   "Let's start with creating your initial PRD draft using /niopd:PD:draft"
        -   "After that, we'll analyze customer jobs-to-be-done with /niopd:PD:jobs-to-be-done"
        -   "Finally, we'll create detailed user personas with /niopd:UR:personas"
    
    -   If "Requirements Refinement & Prioritization":
        -   "Let's generate user stories with /niopd:PD:stories"
        -   "Then we'll define detailed acceptance criteria with /niopd:PD:acceptance-criteria"
        -   "Next, we'll classify features using the Kano model with /niopd:PD:kano-model"
        -   "We'll prioritize requirements with /niopd:PD:moscow-prioritization"
        -   "Finally, we'll score initiatives using the RICE framework with /niopd:PD:rice-prioritization"
    
    -   If "User Experience Design":
        -   "Let's create user journey maps with /niopd:PD:journey"
        -   "Then we'll design low-fidelity wireframes with /niopd:PD:wireframe"
        -   "Finally, we'll document business processes with /niopd:PD:process"
    
    -   If "Market & Competitive Analysis":
        -   "Let's build opportunity-solution trees with /niopd:PD:opportunity-solution-tree"
        -   "Then we'll analyze the competitive landscape with /niopd:MR:compare-products"
    
    -   If "Planning & Measurement":
        -   "Let's create an implementation roadmap with /niopd:PD:roadmap"
        -   "Then we'll define success metrics with /niopd:PM:feature-metrics"
    
    -   If "Implementation & Tracking":
        -   "Let's plan product releases with /niopd:PM:release"
        -   "Then we'll track key performance indicators with /niopd:PM:kpis"

### Step 4: Provide Next Steps
-   Based on the current phase, recommend the next steps in the workflow:
    -   "After completing this phase, I recommend moving to [next phase]"
    -   "The next command you should run is [next command]"
    -   "This will help you [benefit of next step]"

### Step 5: Confirm and Conclude
-   Confirm the guidance: "✅ I've provided guidance for the [phase] phase of your PRD workflow."
-   Suggest next steps: "Run the recommended command to continue your PRD development process."

## Error Handling
- **Missing Information:** If key information is missing, explain what's needed and offer to proceed with placeholders.
- **Unclear Requirements:** If requirements are ambiguous, ask for clarification using specific questions.
- **Configuration File Errors:** If there are issues reading the configuration files, inform the user in their preferred language and proceed with default settings.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial workflow guidance can still provide value. Use the user's preferred language for all error messages and communications.