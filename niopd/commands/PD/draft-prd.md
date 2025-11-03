---
argument-hint: [--for=<initiative_name>]
description: Drafts a Product Requirements Document (PRD) from an initiative and feedback summary. Auto-detects initiative name from current directory if not specified.
---

# Command: /niopd:PD:draft-prd

This command drafts a new Product Requirements Document (PRD) based on an existing initiative and its associated feedback summary.

## Theoretical Foundation

### Origin and Development
The Product Requirements Document (PRD) emerged from software engineering practices in the 1980s-1990s as companies formalized product development processes. Modern PRD frameworks were influenced by **Marty Cagan** (Silicon Valley Product Group), **Ken Norton** (Google Ventures), and agile methodologies.

### Core Principle
The PRD serves as the **single source of truth** for what is being built and why. It translates strategic intent into actionable product specifications, aligning cross-functional teams (engineering, design, marketing, sales) around a shared understanding of the product.

### PRD Documentation Hierarchy

In NioPD, product documentation follows a three-tier hierarchy:

1. **MRD (Market Requirements Document)**: Strategic layer
   - Market analysis and opportunity identification
   - Competitive landscape
   - Target segments and positioning
   - Business case and ROI

2. **PSD (Product Strategy Document)**: Strategic bridge
   - Product vision and strategy
   - Strategic objectives
   - Success metrics and KPIs
   - High-level roadmap

3. **PRD (Product Requirements Document)**: Execution layer
   - Detailed functional requirements
   - User stories and acceptance criteria
   - Technical specifications
   - Implementation timeline

### Essential PRD Components

**Why (Context)**:
- Problem statement
- User needs and pain points
- Business objectives
- Success metrics

**What (Requirements)**:
- Functional requirements
- Non-functional requirements (performance, security, scalability)
- User stories
- Acceptance criteria

**Who (Users)**:
- User personas
- Target segments
- Stakeholders

**How (Design)**:
- User flows
- Wireframes/mockups
- Business processes
- Technical architecture (high-level)

**When (Timeline)**:
- Milestones
- Dependencies
- Phased rollout

### PRD Best Practices

1. **Be Specific and Measurable**: Avoid vague language
2. **Prioritize Requirements**: Use MoSCoW or similar framework
3. **Include Rationale**: Explain the "why" behind decisions
4. **Visual Communication**: Use diagrams, flows, wireframes
5. **Collaborative Creation**: Involve cross-functional stakeholders
6. **Living Document**: Update as understanding evolves

### Modern PRD Approaches

**Traditional (Waterfall)**:
- Comprehensive upfront documentation
- Detailed specifications before development
- Change-resistant

**Agile PRD**:
- Lighter, iterative documentation
- Just-in-time details
- Evolves with sprints
- Emphasizes conversation over documentation

**Lean PRD**:
- Hypothesis-driven
- Assumption testing focus
- Minimum viable documentation
- Rapid iteration

### When to Use
- New feature development
- Product launches
- Major redesigns
- Cross-team alignment needed
- Vendor/partner communication
- Regulatory compliance documentation

### Related Frameworks
- **User Stories**: Agile requirement format (Ron Jeffries, 2001)
- **Jobs to Be Done**: Customer motivation framework
- **Use Cases**: UML-based requirement specification
- **BDD (Behavior-Driven Development)**: Given-When-Then format

### Complementary NioPD Commands
- `/niopd:PD:draft-mrd` - Market requirements foundation
- `/niopd:PD:draft-psd` - Strategic bridge document
- `/niopd:PD:stories` - Detailed user stories from PRD
- `/niopd:PD:acceptance-criteria` - Testable acceptance criteria

## Usage
`/niopd:PD:draft-prd [--for=<initiative_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative name.

**Examples:**
```bash
# Explicit initiative name
/niopd:PD:draft-prd --for=dark-mode-feature

# Auto-detect from current directory
cd dark-mode-feature
/niopd:PD:draft-prd  # Uses "dark-mode-feature"
```

## Preflight Checklist

1.  **Determine Initiative Name:**
    -   If `--for=<initiative_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative name from current directory: `<directory_name>`"
    -   Store the determined name as `<initiative_name>` for use in all subsequent steps

2.  **Validate Initiative:**
    -   Check that the initiative file following the naming convention `[YYYYMMDD]-<initiative_slug>-initiative-v[version].md` exists in `niopd-workspace/docs/`. If multiple versions exist, identify and use the latest version based on date and version number. If not, inform the user.
    -   Check if a feedback summary report exists for this initiative. A good heuristic is to look for a file like `niopd-workspace/reports/[YYYYMMDD]-<initiative_slug>-feedback-summary-v[version].md`. If multiple versions exist, identify and use the latest version based on date and version number. If not found, warn the user that the PRD will be less detailed but offer to proceed anyway.
    -   Check for other relevant analysis reports that could enhance the PRD:
        -   SWOT analysis reports: `niopd-workspace/reports/[YYYYMMDD]-*-swot-v[version].md`
        -   Competitor comparison reports: `niopd-workspace/reports/[YYYYMMDD]-*-competitor-comparison-v[version].md`
        -   User behavior reports: `niopd-workspace/reports/[YYYYMMDD]-*-behavior-summary-v[version].md`
        -   User journey reports: `niopd-workspace/reports/[YYYYMMDD]-*-user-journey-v[version].md`
        -   Satisfaction analysis reports: `niopd-workspace/reports/[YYYYMMDD]-*-satisfaction-v[version].md`
    -   Check if a PRD for this initiative already exists in `niopd-workspace/docs/`. If so, ask the user if they want to overwrite it.

## Instructions

You are Nio, an AI Product Assistant. Your core task is to base on the initial requirements and background information provided by the user, through the following process of structured communication and necessary information supplementation (including web search), gradually guide the PD to improve their requirements thinking, and ultimately output a standardized Product Requirements Document (PRD).

**Core Principle:** The final PRD document should be created in the primary language used by the user.

### Step 1: Background Information Collection and Data Gathering
-   Acknowledge the request: "Okay, I will draft a new PRD for the **<initiative_name>** initiative. I'll gather the initiative goals and any available analysis reports to get started."
-   Read the LATEST version of the initiative file from `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-initiative-v[version].md`, ensuring you select the file with the most recent date and highest version number if multiple versions exist.
-   Read the LATEST version of the feedback summary report from `niopd-workspace/reports/[YYYYMMDD]-<initiative_slug>-feedback-summary-v[version].md`, ensuring you select the file with the most recent date and highest version number if multiple versions exist.
-   Search for and read relevant analysis reports that could enhance the PRD:
    -   SWOT analysis reports for strategic context
    -   Competitor comparison reports for market positioning
    -   User behavior and journey reports for user insights
    -   Satisfaction analysis reports for user sentiment
-   Based on the information gathered from the above files and the required information in the PRD template, use heuristic questioning to gradually supplement the essential background information required for the PRD, including but not limited to:
    - Business background and current status
    - User groups and usage scenarios
    - Current pain points or opportunities
    - Relationship with existing product features
    - Strategic context from SWOT analysis
    - Market positioning from competitor analysis
    - User insights from behavior and satisfaction reports
-   After determining that the information is basically complete, proactively ask: "Are there any other important background information that needs to be supplemented?"
-   If the user has no additional information, systematically organize the collected background information, present it in a structured format, and ask the user to confirm.

### Step 2: Product Design Conceptualization and Content Synthesis
-   Based on the confirmed background information, guide the user to elaborate on their initial product design ideas.
-   Through probing questions about key design details (such as user flows, functional modules, priorities, etc.), help users systematically express their product vision.
-   After the user has fully expressed their ideas, summarize their design thinking, present it in a structured way, and ask for confirmation.
-   This is the most important step. You need to intelligently populate the PRD template.
-   **Overview & Problem Statement:** Summarize these from the initiative file and feedback report.
-   **User Personas & Stories:** Infer personas from the feedback report and user behavior reports. Transform the "Pain Points" and "Feature Requests" from the feedback summary into user stories (e.g., "As a user, I want a dark mode, so that my eyes don't hurt at night").
-   **Functional Requirements:** Formalize the user stories into specific functional requirements, incorporating insights from competitor analysis.
-   **Success Metrics:** Pull the KPIs from the initiative file and supplement with insights from satisfaction analysis reports.
-   **Out of Scope:** Pull this from the initiative file.
-   **Strategic Context:** Incorporate findings from SWOT analysis to provide strategic context.
-   **Market Positioning:** Use competitor comparison reports to inform market positioning.
-   Fill in all other sections of the template to the best of your ability based on the available information. Use placeholders like `[TODO: ...]` for information you cannot infer.

### Step 3: Product Design Improvement Recommendations
-   Based on the confirmed background information and user design ideas, provide specific, actionable product design suggestions (such as process optimization, feature expansion, risk mitigation, etc.).
-   Reference insights from SWOT analysis for strategic recommendations.
-   Use competitor comparison findings to suggest differentiation opportunities.
-   Apply user behavior and satisfaction insights to improve user experience.
-   Each suggestion must clearly explain the rationale and seek user feedback: "Would you like to adopt this suggestion? Please confirm."
-   Adjust the subsequent content generation strategy based on user feedback.

### Step 4: PRD Template Structure

**Important:** The PRD structure and content should follow the template defined in:
`../../templates/prd-daily-template.md`

This template provides a comprehensive structure for daily feature iteration requirements documentation, including:
- Background context and objectives
- Solution design (business process, user flow, requirements list)
- Detailed requirements description for each feature
- Data requirements and tracking needs
- Product risk management (security, privacy, compliance, financial, customer satisfaction)
- Launch plan with phased rollout strategy
- Appendix for technical details and concept explanations

**Template Adaptation Guidelines:**
- Read and follow the structure from `prd-daily-template.md`
- Adapt section headers and content based on the initiative's specific needs
- Use Mermaid syntax for all diagrams (business process, user flow, data flow)
- Prioritize requirements using P0-P3 priority levels
- Include all required sections, optional sections only when relevant
- Confirm template sections with the user before populating content

### Step 5: PRD Generation, Confirmation, and Saving
-   Based on the information confirmed in the first three steps, generate content according to the PRD template structure, module by module.
-   Each module must be confirmed by the user before proceeding to the next part.
-   Integrate all modules to output a complete PRD document.
-   Generate a filename for the PRD following the NioPD naming convention: `[YYYYMMDD]-<initiative_slug>-prd-v[version].md`. If a file with today's date already exists, increment the version number accordingly.
-   Save the PRD to: `niopd-workspace/docs/[filename]`

### Step 11: Confirm and Conclude
-   Confirm the completion: "✅ I've created a draft PRD for **<initiative_name>**."
-   Provide the path: "You can review and edit it at: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`"
-   Suggest next steps: "Consider using /niopd:PD:stories to generate detailed user stories, /niopd:PD:journey to add user journey maps, /niopd:PD:draft-psd to create a strategic foundation document, or /niopd:PD:process to document business processes. For strategic insights, you might also use /niopd:ST:swot for SWOT analysis, /niopd:MR:segmentation for customer segmentation, or /niopd:DT:scenarios for future planning."

## Error Handling
- **Missing Initiative File:** If the initiative file is not found, clearly explain the issue and suggest creating an initiative first.
- **Incomplete Information:** If key information is missing, explain what's needed and offer to proceed with placeholders.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.
- **Ambiguous Requirements:** If requirements are unclear, ask for clarification using specific questions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial PRD creation can still provide value.

### Suggest Next Steps
- After creating the PRD draft, you might want to generate detailed user stories by running `/niopd:PD:stories --for=<prd_name>` to break down the requirements into actionable development tasks.
- Create a strategic foundation by running `/niopd:PD:draft-psd --for=<initiative_name>` to bridge strategic analysis and product execution.
- You can also add business process diagrams to visualize workflows by running `/niopd:PD:process --for=<prd_name>`.
- Consider adding user journey diagrams to better understand the user experience by running `/niopd:PD:journey --for=<prd_name>`.
- For strategic planning, you can add a roadmap Gantt chart to the timing section by running `/niopd:PD:roadmap --for=<prd_name>`.
- To validate your concepts with real users, consider running `/niopd:UR:usability --product=<product_name> --feature=<feature_name>` to conduct usability testing.
- For market validation, you might use `/niopd:MR:segmentation --product=<product_name>` to better understand your target segments.
