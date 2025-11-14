---
argument-hint: [--for=<initiative_name>|--for=<product_name>] [--version=<version_number>]
description: Plans and manages product releases with detailed timelines and coordination requirements. Auto-detects initiative/product name from current directory if not specified.
---

# Command: /niopd:PM:release

This command plans and manages product releases with detailed timelines, resource allocation, and coordination requirements across teams.

## Theoretical Foundation

### Origin and Development
Release management emerged from **Software Configuration Management** (1970s) and **ITIL** (IT Infrastructure Library, 1980s). Modern practices integrate **Continuous Delivery** (Jez Humble, 2010) and **DevOps** principles for faster, safer releases.

### Core Principle
Release management ensures **reliable, coordinated deployment** of software to production. It balances speed (frequent releases) with stability (quality gates), managing risk through planning, testing, and phased rollouts.

### Release Strategies

**Big Bang** (Waterfall):
- One large release
- Long development cycles
- High risk, high coordination

**Phased Rollout**:
- Gradual deployment to subsets
- Reduce blast radius
- Monitor before full release

**Blue-Green Deployment**:
- Two identical environments
- Switch traffic instantly
- Easy rollback

**Canary Release**:
- Small % to test group
- Gradual increase
- Early issue detection

**Feature Flags**:
- Code deployed, features off
- Enable selectively
- Decouple deploy from release

### Semantic Versioning

**Format**: MAJOR.MINOR.PATCH (e.g., 2.1.5)
- **MAJOR**: Breaking changes
- **MINOR**: New features (backward compatible)
- **PATCH**: Bug fixes

## Usage
`/niopd:PM:release [--for=<initiative_name>|--for=<product_name>] [--version=<version_number>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative/product name.

**Examples:**
```bash
# Explicit initiative and version
/niopd:PM:release --for=dark-mode-feature --version=2.0.0

# Auto-detect initiative, specify version
cd dark-mode-feature
/niopd:PM:release --version=2.0.0  # Uses "dark-mode-feature"

# Auto-detect both initiative and version
cd dark-mode-feature
/niopd:PM:release  # Uses "dark-mode-feature" and determines next version
```

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2.  **Determine Initiative/Product Name:**
    -   If `--for=<initiative_name>` or `--for=<product_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative/product name from current directory: `<directory_name>`"
    -   Store the determined name for use in all subsequent steps

3.  **Validate Inputs:**
    -   Check if `--for` argument is provided to specify the initiative or product.
    -   If `--for` is not provided, ask the user to specify what they want to plan a release for.
    -   Check if `--version` argument is provided to specify the release version.
    -   If `--version` is not provided, determine the next version number based on existing releases.

## Instructions

You are a specialized AI expert in release planning and project management. Your goal is to create comprehensive release plans that ensure successful product launches with proper coordination and risk management.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Context
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将为 **<initiative_or_product_name>** 版本 **<version_number>** 制定发布计划。"
    -   If English: "I'll plan a release for **<initiative_or_product_name>** version **<version_number>**."
    -   For other languages, use an appropriate translation based on user's language preference
-   If a specific initiative or product is provided with `--for`, use that as the focus.
-   If not provided, ask the user in their preferred language: "Which initiative or product would you like to plan a release for?"
-   If a version number is provided with `--version`, use that version.
-   If not provided, research existing versions and suggest the next version number.

### Step 2: Release Scope Definition
-   Define the release scope:
    -   Features and functionality included
    -   Bug fixes and improvements
    -   Technical debt resolution
    -   Performance optimizations
    -   Security enhancements
-   Determine release objectives:
    -   Business goals and KPIs
    -   Customer impact and value
    -   Market timing requirements
    -   Competitive considerations

### Step 3: Stakeholder Identification
-   Identify key stakeholders:
    -   Development teams and engineers
    -   Product managers and designers
    -   Quality assurance and testing teams
    -   Operations and infrastructure teams
    -   Marketing and sales teams
    -   Customer support teams
    -   Executive sponsors and leadership
-   Define stakeholder roles and responsibilities:
    -   Decision-making authority
    -   Contribution requirements
    -   Communication needs
    -   Approval processes

### Step 4: Feature and Task Breakdown
-   Break down release scope into features:
    -   User stories and acceptance criteria
    -   Technical tasks and subtasks
    -   Dependencies between features
    -   Effort estimates and complexity
-   Prioritize features:
    -   Must-have vs. nice-to-have
    -   Customer impact and value
    -   Technical dependencies
    -   Risk and uncertainty factors

### Step 5: Resource Assessment
-   Assess required resources:
    -   Development personnel and skills
    -   Testing and QA resources
    -   Infrastructure and environment needs
    -   Third-party services and licenses
    -   Budget and financial considerations
-   Identify resource constraints:
    -   Availability and capacity limits
    -   Skill gaps and training needs
    -   Budget limitations
    -   External dependencies

### Step 6: Timeline Planning
-   Develop release timeline:
    -   Key milestones and deliverables
    -   Development phases and sprints
    -   Testing and quality assurance phases
    -   Deployment and rollout schedule
    -   Marketing and communication timeline
-   Identify critical path activities:
    -   Tasks that directly impact release date
    -   Dependencies and blockers
    -   Parallel work opportunities
    -   Buffer and contingency time

### Step 7: Risk Assessment and Mitigation
-   Identify release risks:
    -   Technical risks and uncertainties
    -   Resource and personnel risks
    -   External dependency risks
    -   Market and competitive risks
    -   Quality and performance risks
-   Develop risk mitigation strategies:
    -   Contingency plans and alternatives
    -   Risk monitoring and escalation
    -   Fallback and rollback procedures
    -   Communication and stakeholder management

### Step 8: Quality Assurance Planning
-   Define quality criteria:
    -   Functional requirements and acceptance
    -   Performance and scalability targets
    -   Security and compliance requirements
    -   Usability and user experience standards
-   Plan testing activities:
    -   Unit testing and code coverage
    -   Integration and system testing
    -   User acceptance testing
    -   Performance and load testing
    -   Security testing and vulnerability assessment

### Step 9: Deployment and Rollout Strategy
-   Plan deployment approach:
    -   Deployment environments (dev, test, staging, production)
    -   Deployment methods and tools
    -   Rollback and recovery procedures
    -   Data migration and compatibility
-   Define rollout strategy:
    -   Phased rollout approach
    -   Target audience and segments
    -   Geographic and demographic considerations
    -   Monitoring and feedback collection

### Step 10: Communication and Coordination Plan
-   Develop communication strategy:
    -   Internal team communications
    -   Stakeholder updates and reporting
    -   Customer and user notifications
    -   Marketing and public relations
-   Establish coordination mechanisms:
    -   Regular status meetings and check-ins
    -   Issue escalation and resolution
    -   Change management processes
    -   Documentation and knowledge sharing

### Step 11: Release Planning Report Generation
Produce a markdown report with the following structure:

---
# Release Plan: [Initiative/Product Name] v[Version Number]

## Executive Summary
*A high-level overview of the release plan and key details*

## Release Context
- **Product/Initiative:** [Name and description]
- **Version:** [Release version number]
- **Release Date:** [Target release date]
- **Planning Date:** [Current date]
- **Release Manager:** [Person or team responsible]

## Release Scope
### Features Included
1. **[Feature Name]:** [Brief description and value]
2. **[Feature Name]:** [Brief description and value]

### Bug Fixes and Improvements
1. **[Fix/Improvement]:** [Brief description and impact]
2. **[Fix/Improvement]:** [Brief description and impact]

### Technical Debt Resolution
1. **[Task]:** [Brief description and benefits]
2. **[Task]:** [Brief description and benefits]

## Stakeholder Analysis
### Key Stakeholders
| Stakeholder | Role | Responsibilities | Communication Needs |
|-------------|------|------------------|---------------------|
| [Name/Team] | [Role] | [Responsibilities] | [Needs] |
| [Name/Team] | [Role] | [Responsibilities] | [Needs] |

### Decision-Making Authority
- **Product Decisions:** [Who has authority]
- **Technical Decisions:** [Who has authority]
- **Release Approval:** [Who approves release]
- **Budget Approval:** [Who approves budget]

## Feature Breakdown and Prioritization
### Must-Have Features
1. **[Feature Name]**
   - **Description:** [Detailed description]
   - **User Stories:** [Key user stories]
   - **Dependencies:** [What this depends on]
   - **Effort:** [Estimated effort and complexity]

2. **[Feature Name]**
   - **Description:** [Detailed description]
   - **User Stories:** [Key user stories]
   - **Dependencies:** [What this depends on]
   - **Effort:** [Estimated effort and complexity]

### Nice-to-Have Features
1. **[Feature Name]**
   - **Description:** [Detailed description]
   - **User Stories:** [Key user stories]
   - **Dependencies:** [What this depends on]
   - **Effort:** [Estimated effort and complexity]

## Resource Plan
### Personnel Requirements
| Role | Number Required | Skills Needed | Availability |
|------|-----------------|---------------|--------------|
| [Role] | [Number] | [Skills] | [Availability] |
| [Role] | [Number] | [Skills] | [Availability] |

### Infrastructure and Tools
- **Development Environments:** [Required environments]
- **Testing Tools:** [Required tools and licenses]
- **Deployment Infrastructure:** [Required systems and services]
- **Monitoring and Analytics:** [Required monitoring tools]

### Budget Considerations
- **Development Costs:** [Estimated costs]
- **Testing and QA Costs:** [Estimated costs]
- **Infrastructure Costs:** [Estimated costs]
- **Third-party Services:** [Estimated costs]

## Timeline and Milestones
### Release Timeline
```
[Text-based timeline representation]
Start Date → [Milestone 1] → [Milestone 2] → [Milestone 3] → Release Date
```

### Key Milestones
1. **[Milestone Name]** - [Date] - [Description and deliverables]
2. **[Milestone Name]** - [Date] - [Description and deliverables]
3. **[Milestone Name]** - [Date] - [Description and deliverables]

### Critical Path Activities
1. **[Activity]:** [Description and importance]
2. **[Activity]:** [Description and importance]

## Risk Assessment
### High-Priority Risks
1. **[Risk]:** [Description and likelihood]
   - **Impact:** [Potential consequences]
   - **Mitigation:** [How to address or reduce risk]
   - **Owner:** [Who is responsible for management]

2. **[Risk]:** [Description and likelihood]
   - **Impact:** [Potential consequences]
   - **Mitigation:** [How to address or reduce risk]
   - **Owner:** [Who is responsible for management]

### Risk Monitoring Plan
- **Regular Risk Reviews:** [Frequency and participants]
- **Risk Indicators:** [Early warning signs to watch]
- **Escalation Process:** [When and how to escalate]
- **Contingency Plans:** [Backup approaches if needed]

## Quality Assurance Plan
### Quality Criteria
- **Functional Requirements:** [Acceptance criteria]
- **Performance Targets:** [Speed, scalability, reliability]
- **Security Requirements:** [Compliance and protection]
- **Usability Standards:** [User experience expectations]

### Testing Strategy
#### Unit Testing
- **Coverage Target:** [Percentage goal]
- **Tools:** [Testing frameworks and tools]
- **Responsibility:** [Who conducts testing]

#### Integration Testing
- **Scope:** [What is tested]
- **Environment:** [Where testing occurs]
- **Schedule:** [When testing happens]

#### User Acceptance Testing
- **Participants:** [Who tests]
- **Test Cases:** [What is validated]
- **Feedback Process:** [How issues are reported]

## Deployment and Rollout Plan
### Deployment Approach
- **Environments:** [Dev, Test, Staging, Production]
- **Methods:** [Deployment tools and processes]
- **Rollback Procedures:** [How to revert if issues occur]
- **Data Migration:** [How data is handled]

### Rollout Strategy
- **Phased Approach:** [How release is rolled out]
- **Target Audience:** [Who gets the release first]
- **Geographic Considerations:** [Regional rollout plans]
- **Monitoring:** [What is tracked during rollout]

## Communication Plan
### Internal Communications
- **Team Meetings:** [Frequency and format]
- **Status Reports:** [Recipients and frequency]
- **Issue Escalation:** [Process and contacts]
- **Documentation:** [Where information is stored]

### External Communications
- **Customer Notifications:** [How users are informed]
- **Marketing Coordination:** [Promotion and announcements]
- **Public Relations:** [Media and press activities]
- **Support Team Preparation:** [Training and resources]

## Success Metrics
### Release Success Criteria
- **On-time Delivery:** [Target release date adherence]
- **Quality Metrics:** [Bug count, performance scores]
- **Customer Satisfaction:** [User feedback and adoption]
- **Business Impact:** [Revenue, usage, or other KPIs]

### Post-release Monitoring
- **Performance Monitoring:** [System health tracking]
- **User Feedback Collection:** [How feedback is gathered]
- **Issue Resolution:** [How problems are addressed]
- **Lessons Learned:** [Process improvement identification]

## Approval and Sign-off
### Required Approvals
- **Product Approval:** [Name and title]
- **Technical Approval:** [Name and title]
- **Quality Approval:** [Name and title]
- **Business Approval:** [Name and title]

### Sign-off Date
- **Planned Sign-off:** [Target date]
- **Actual Sign-off:** [When approval is received]

## Data Sources and Methodology
- **Planning Methods:** [How the plan was developed]
- **Sources:** [Information sources used]
- **Assumptions:** [Key assumptions made]
- **Limitations:** [Known limitations of the plan]

---

### Step 13: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_slug]-release-plan-v[version].md`.
- Save the report to: `niopd-workspace/plans/[filename]`

### Step 14: Confirm and Conclude
- Confirm the action is complete: "✅ I've created a release plan for **<initiative_or_product_name>** version **<version_number>**."
- Provide the path to the file: "You can view the detailed release plan here: `niopd-workspace/plans/[YYYYMMDD]-[initiative_slug]-release-plan-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PM:kpis` to track release progress, `/niopd:PO:stakeholder-update` to communicate status to stakeholders, or `/niopd:PM:resources` to plan detailed resource allocation for this release."

## Error Handling
- **Missing Subject:** If no subject is specified for release planning, ask the user to clarify what they want to plan.
- **Version Issues:** If version information is unclear, research existing versions and suggest appropriate numbering.
- **Insufficient Data:** If adequate scope or feature information cannot be found, explain the limitations and suggest focusing on available information.
- **Resource Constraints:** If resource requirements exceed availability, highlight constraints and suggest using `/niopd:PM:resources` for detailed resource planning.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.