---
argument-hint: [--for=<initiative_name>] [--sponsor=<sponsor_name>]
description: Generates a comprehensive Project Initiation Document (PID) that defines project objectives, scope, planning, and stakeholder responsibilities, ensuring team alignment before execution phase.
---

# Command: /niopd:PM:draft-pid

This command generates a **Project Initiation Document (PID)** - a critical document that must be approved by project management team and key stakeholders before entering the execution phase. The PID ensures unified understanding of project goals, scope, timeline, budget, and risk management strategies.

## Theoretical Foundation

### Origin and Development
The Project Initiation Document emerged from **PRINCE2** (PRojects IN Controlled Environments, UK Government, 1989) and **PMI's PMBOK** (Project Management Body of Knowledge, 1987) methodologies. The PID formalizes the transition from project concept to execution, providing governance and control.

### Core Principle
The PID serves as the **project charter and execution blueprint** - the formal authorization to proceed with a project. It answers "What are we building, why, how, when, and who?" ensuring all stakeholders have a shared understanding before significant resources are committed.

### PID vs. Other Project Documents

**Project Charter (PMI)**:
- High-level authorization
- Executive-focused
- Shorter (2-5 pages)
- Created in initiation phase

**Project Initiation Document (PRINCE2)**:
- Detailed project definition
- Team and stakeholder focused
- Comprehensive (15-30+ pages)
- Required for phase gate approval

**Project Plan**:
- Detailed execution schedule
- Task-level breakdown
- Resource assignments
- Derived from PID

### Essential PID Components

**1. Project Definition**:
- Business case justification
- Objectives (SMART: Specific, Measurable, Achievable, Relevant, Time-bound)
- Expected outcomes and benefits
- Success criteria

**2. Scope Statement**:
- In-scope deliverables
- Out-of-scope exclusions
- Boundaries and constraints
- Assumptions and dependencies

**3. Project Approach**:
- Methodology (Waterfall, Agile, Hybrid)
- Lifecycle phases
- Quality standards
- Technical approach

**4. Project Plan**:
- Timeline and milestones
- Work breakdown structure (WBS)
- Resource allocation
- Budget and cost breakdown

**5. Project Organization**:
- Stakeholder map
- Roles and responsibilities (RACI)
- Governance structure
- Communication plan

**6. Risk & Quality Management**:
- Risk register (top risks)
- Risk mitigation strategies
- Quality criteria
- Acceptance processes

### Project Management Frameworks

**PRINCE2 (Controlled)**:
- Process-driven (7 processes, 7 principles, 7 themes)
- Strong governance
- Formal documentation
- Phase gates and reviews

**PMI/PMBOK (Standard)**:
- 5 Process Groups: Initiating, Planning, Executing, Monitoring/Controlling, Closing
- 10 Knowledge Areas (Scope, Time, Cost, Quality, etc.)
- Flexible application
- Tool and technique focus

**Agile (Adaptive)**:
- Iterative and incremental
- Lightweight documentation
- Continuous planning
- Self-organizing teams

**Hybrid (Best of Both)**:
- Waterfall for predictable phases
- Agile for uncertain work
- PID for overall governance
- Sprints for execution

### Project Governance

**Steering Committee**:
- Senior stakeholder group
- Phase gate approvals
- Resource authorization
- Issue escalation

**Project Board (PRINCE2)**:
- **Executive**: Business justification owner
- **Senior User**: Represents users/customers
- **Senior Supplier**: Represents delivery team

**Decision Gates**:
- Gate 0: Concept approval
- Gate 1: PID approval (proceed to execution)
- Gate 2: Mid-project review
- Gate 3: Launch approval
- Gate 4: Post-launch review

### When to Create a PID

- All significant projects (>3 months, >3 people)
- Projects requiring budget approval
- Cross-functional initiatives
- Regulatory/compliance-driven projects
- Customer/partner commitments
- Strategic initiatives

### PID Approval Process

**1. Draft Creation** (PM):
- Gather requirements
- Consult stakeholders
- Create initial PID

**2. Review Cycle** (Stakeholders):
- Distribute for review
- Collect feedback
- Refine document

**3. Approval Gate** (Steering Committee):
- Present PID
- Answer questions
- Receive formal approval or conditional approval

**4. Baseline** (PM):
- Version and archive approved PID
- Becomes change control baseline
- All changes require approval

### Best Practices

1. **Start Early**: Begin PID during project conception
2. **Involve Stakeholders**: Co-create with key stakeholders
3. **Be Realistic**: Honest about scope, timeline, resources
4. **Quantify Benefits**: Measurable business outcomes
5. **Identify Risks Early**: Don't hide known risks
6. **Define Success Clearly**: Unambiguous acceptance criteria
7. **Keep Updated**: Living document during planning
8. **Baseline After Approval**: Lock and version control

### Related PM Concepts

- **Business Case**: Financial justification (input to PID)
- **Project Plan**: Detailed execution plan (derived from PID)
- **Status Reports**: Progress tracking against PID baseline
- **Change Control**: Managing deviations from PID

### Complementary NioPD Commands

- `/niopd:PD:draft-prd` - Product requirements (input to PID)
- `/niopd:PD:draft-psd` - Product strategy (input to PID)
- `/niopd:PM:resources` - Resource planning details
- `/niopd:PM:risk-analysis` - Risk management details
- `/niopd:PM:release` - Release planning from PID

## Usage
`/niopd:PM:draft-pid [--for=<initiative_name>] [--sponsor=<sponsor_name>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative name.

**Examples:**
```bash
# Explicit initiative name with sponsor
/niopd:PM:draft-pid --for=mobile-app-redesign --sponsor="John Smith"

# Auto-detect initiative name
cd mobile-app-redesign
/niopd:PM:draft-pid  # Uses "mobile-app-redesign"

# Auto-detect with sponsor
cd mobile-app-redesign
/niopd:PM:draft-pid --sponsor="John Smith"
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

3.  **Validate References:**
    -   Check if initiative file exists: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-initiative-v[version].md`
    -   Check if MRD exists: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-mrd-v[version].md`
    -   Check if PSD exists: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-psd-v[version].md`
    -   Check if PRD exists: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`
    -   Check if Release Plan exists: `niopd-workspace/plans/[YYYYMMDD]-<initiative_slug>-release-plan-v[version].md`
    -   These documents provide valuable context for PID generation

4.  **Check for Existing PID:**
    -   Check if a PID already exists in `niopd-workspace/plans/`
    -   If exists, ask user if they want to create a new version or update existing

## Instructions

You are Nio, a project management AI assistant specializing in creating comprehensive Project Initiation Documents. Your goal is to gather all necessary information and generate a PID that ensures team alignment and stakeholder approval before project execution.

**Core Principle:** The PID should be created in the primary language used by the user and serve as the authoritative source for project governance. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Context
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将帮您为 **<initiative_name>** 创建项目启动文档。该文档将定义项目目标、范围、计划和利益相关者职责。"
    -   If English: "I'll help you create a Project Initiation Document for **<initiative_name>**. This document will define project objectives, scope, planning, and stakeholder responsibilities."
    -   For other languages, use an appropriate translation based on user's language preference
-   Read reference documents if available:
    -   Initiative document: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-initiative-v[version].md`
    -   MRD: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-mrd-v[version].md`
    -   PSD: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-psd-v[version].md`
    -   PRD: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`
    -   Release Plan: `niopd-workspace/plans/[YYYYMMDD]-<initiative_slug>-release-plan-v[version].md`
-   Extract relevant information from these documents to populate PID sections

### Step 2: Project Definition
-   Guide user to define project fundamentals:
    -   "What is the business value this project delivers?"
    -   "Who are the target user groups?"
    -   "What are the expected outcomes and success criteria?"
    -   "What business problem does this project solve?"
-   Clarify project context:
    -   "How does this project align with organizational strategy?"
    -   "What is the business case justification?"
    -   "What are the project constraints (budget, timeline, resources)?"

### Step 3: Project Scope Definition
-   Define scope boundaries:
    -   "What product/service features are IN scope?"
    -   "What features are explicitly OUT of scope?"
    -   "What are the quality standards and acceptance criteria?"
    -   "What are the deliverables and their specifications?"
-   Validate scope understanding:
    -   "Are there any assumptions about scope we should document?"
    -   "What dependencies might affect scope?"

### Step 4: Planning Framework
-   Develop comprehensive planning:
    
    **Timeline Planning:**
    -   "What are the key project milestones?"
    -   "What is the target completion date?"
    -   "What are the phase-based delivery dates?"
    
    **Cost Planning:**
    -   "What is the approved project budget?"
    -   "How is budget allocated across phases?"
    -   "What are the cost control mechanisms?"
    
    **Resource Planning:**
    -   "What team roles and skills are required?"
    -   "How many people are needed for each role?"
    -   "What external resources or vendors are needed?"
    -   "What tools and infrastructure are required?"

### Step 5: Stakeholder & Governance
-   Identify stakeholders and governance structure:
    -   "Who is the project sponsor?"
    -   "Who are the key stakeholders and their roles?"
    -   "Who has decision-making authority?"
    -   "What is the approval process for changes?"
    -   "How often are steering committee meetings held?"

### Step 6: Risk & Quality Management
-   Assess risks:
    -   "What are the top 5 project risks?"
    -   "What is the probability and impact of each risk?"
    -   "What mitigation strategies are in place?"
    -   "Who owns each risk?"
    
-   Define quality management:
    -   "What quality standards apply to this project?"
    -   "What quality control methods will be used?"
    -   "Who is responsible for quality assurance?"
    -   "What testing and validation processes are required?"

### Step 7: Generate PID Document

Create a comprehensive PID using the following structure:

---
# Project Initiation Document (PID)
## {{initiative_name}}

**Document Version:** v{{version}}  
**Date:** {{YYYYMMDD}}  
**Status:** {{Draft/Approved/Active}}  
**Project Sponsor:** {{sponsor_name}}  
**Project Manager:** {{pm_name}}

---

## 1. Executive Summary
*2-3 paragraph overview of project purpose, scope, timeline, and expected business value*

---

## 2. Project Definition

### 2.1 Business Context
- **Business Problem:** {{problem_statement}}
- **Business Opportunity:** {{opportunity_description}}
- **Strategic Alignment:** {{how_aligns_with_strategy}}

### 2.2 Project Objectives
**Primary Objective:**
{{primary_objective}}

**Secondary Objectives:**
1. {{objective_1}}
2. {{objective_2}}
3. {{objective_3}}

### 2.3 Target Users/Beneficiaries
| User Group | Description | Expected Benefit |
|------------|-------------|------------------|
| {{group}} | {{description}} | {{benefit}} |
| {{group}} | {{description}} | {{benefit}} |

### 2.4 Expected Outcomes
**Business Outcomes:**
- {{outcome_1}}
- {{outcome_2}}

**User Outcomes:**
- {{outcome_1}}
- {{outcome_2}}

**Technical Outcomes:**
- {{outcome_1}}
- {{outcome_2}}

### 2.5 Success Criteria
| Metric | Target | Measurement Method | Owner |
|--------|--------|-------------------|-------|
| {{metric}} | {{target}} | {{method}} | {{owner}} |
| {{metric}} | {{target}} | {{method}} | {{owner}} |

---

## 3. Project Scope

### 3.1 In Scope
**Features & Deliverables:**
1. **{{deliverable_name}}**
   - Description: {{description}}
   - Acceptance Criteria: {{criteria}}
   - Priority: {{P0/P1/P2}}

2. **{{deliverable_name}}**
   - Description: {{description}}
   - Acceptance Criteria: {{criteria}}
   - Priority: {{P0/P1/P2}}

**Systems/Platforms:**
- {{system_1}}
- {{system_2}}

**User Groups:**
- {{user_group_1}}
- {{user_group_2}}

### 3.2 Out of Scope
**Explicitly Excluded:**
- {{excluded_item_1}} - Rationale: {{reason}}
- {{excluded_item_2}} - Rationale: {{reason}}

**Future Considerations:**
- {{future_item_1}} - Deferred to: {{phase/version}}
- {{future_item_2}} - Deferred to: {{phase/version}}

### 3.3 Quality Standards
**Product Quality:**
- Performance: {{standard}}
- Reliability: {{standard}}
- Usability: {{standard}}
- Security: {{standard}}

**Process Quality:**
- Code coverage: {{target}}
- Documentation: {{standard}}
- Review process: {{process}}

### 3.4 Constraints
**Technical Constraints:**
- {{constraint_1}}
- {{constraint_2}}

**Business Constraints:**
- Budget: {{budget_limit}}
- Timeline: {{deadline}}
- Resources: {{resource_constraint}}

**Regulatory/Compliance:**
- {{compliance_requirement_1}}
- {{compliance_requirement_2}}

---

## 4. Project Planning

### 4.1 Timeline & Milestones

**Project Duration:** {{start_date}} to {{end_date}} ({{duration}})

**Phase-Based Timeline:**

| Phase | Start Date | End Date | Duration | Key Deliverables | Status |
|-------|-----------|----------|----------|-----------------|--------|
| Initiation | {{date}} | {{date}} | {{duration}} | PID, Project Charter | {{status}} |
| Planning | {{date}} | {{date}} | {{duration}} | Detailed Plans, Requirements | {{status}} |
| Execution | {{date}} | {{date}} | {{duration}} | Product Increments | {{status}} |
| Testing | {{date}} | {{date}} | {{duration}} | QA Reports, Bug Fixes | {{status}} |
| Launch | {{date}} | {{date}} | {{duration}} | Production Release | {{status}} |
| Closure | {{date}} | {{date}} | {{duration}} | Lessons Learned, Handover | {{status}} |

**Key Milestones:**
1. **{{milestone_name}}** - {{date}}
   - Deliverables: {{deliverables}}
   - Success Criteria: {{criteria}}
   - Dependencies: {{dependencies}}

2. **{{milestone_name}}** - {{date}}
   - Deliverables: {{deliverables}}
   - Success Criteria: {{criteria}}
   - Dependencies: {{dependencies}}

**Critical Path Activities:**
- {{activity_1}} - Impact: {{impact}}
- {{activity_2}} - Impact: {{impact}}

### 4.2 Budget & Cost Planning

**Total Project Budget:** {{total_budget}}

**Budget Breakdown:**

| Category | Allocated Budget | % of Total | Justification |
|----------|-----------------|------------|---------------|
| Personnel | {{amount}} | {{percentage}} | {{justification}} |
| Infrastructure | {{amount}} | {{percentage}} | {{justification}} |
| Software/Tools | {{amount}} | {{percentage}} | {{justification}} |
| External Services | {{amount}} | {{percentage}} | {{justification}} |
| Contingency | {{amount}} | {{percentage}} | {{justification}} |
| **Total** | **{{total}}** | **100%** | |

**Cost Control Mechanisms:**
- Budget review frequency: {{frequency}}
- Approval process for overruns: {{process}}
- Cost tracking method: {{method}}
- Variance tolerance: {{percentage}}

**Funding Source:**
- {{source_1}}: {{amount}}
- {{source_2}}: {{amount}}

### 4.3 Resource Planning

**Team Structure:**

| Role | Name | Allocation (%) | Responsibilities | Start Date | End Date |
|------|------|---------------|-----------------|-----------|----------|
| Project Manager | {{name}} | {{%}} | Overall project delivery | {{date}} | {{date}} |
| Product Owner | {{name}} | {{%}} | Requirements, priorities | {{date}} | {{date}} |
| Tech Lead | {{name}} | {{%}} | Technical direction | {{date}} | {{date}} |
| Developers | {{names}} | {{%}} | Development | {{date}} | {{date}} |
| QA Engineers | {{names}} | {{%}} | Testing, quality | {{date}} | {{date}} |
| UX Designers | {{names}} | {{%}} | Design | {{date}} | {{date}} |

**Resource Requirements:**
- **Peak capacity needed:** {{date}} - {{number}} people
- **Skills required:** {{skill_list}}
- **External resources:** {{vendor/contractor_list}}

**Infrastructure & Tools:**
- Development environment: {{env}}
- CI/CD pipeline: {{tool}}
- Project management: {{tool}}
- Collaboration: {{tool}}
- Monitoring: {{tool}}

---

## 5. Governance & Stakeholder Management

### 5.1 Project Governance Structure

**Governance Hierarchy:**
```
Steering Committee
    ↓
Project Sponsor
    ↓
Project Manager
    ↓
Project Team
```

**Steering Committee:**
- Members: {{member_list}}
- Meeting Frequency: {{frequency}}
- Decision Authority: {{scope_of_authority}}

**Project Sponsor:**
- Name: {{sponsor_name}}
- Role: {{role}}
- Responsibilities:
  - Final decision authority on scope changes
  - Budget approval
  - Conflict resolution
  - Strategic alignment oversight

### 5.2 Stakeholder Analysis

| Stakeholder | Role | Interest Level | Influence Level | Communication Needs | Engagement Strategy |
|-------------|------|---------------|----------------|--------------------|--------------------|
| {{name}} | {{role}} | High/Med/Low | High/Med/Low | {{needs}} | {{strategy}} |
| {{name}} | {{role}} | High/Med/Low | High/Med/Low | {{needs}} | {{strategy}} |

### 5.3 Communication Plan

**Regular Communications:**
| Audience | Communication Type | Frequency | Channel | Owner |
|----------|-------------------|-----------|---------|-------|
| Steering Committee | Status Report | Monthly | Email + Meeting | PM |
| Project Team | Daily Standup | Daily | Video Call | PM |
| Stakeholders | Progress Update | Weekly | Email | PM |
| Leadership | Executive Summary | Bi-weekly | Dashboard | Sponsor |

**Escalation Process:**
- **Level 1:** Team discussion → Project Manager
- **Level 2:** Project Manager → Project Sponsor
- **Level 3:** Project Sponsor → Steering Committee
- **Escalation Timeframe:** {{timeframe}}

### 5.4 Change Management

**Change Request Process:**
1. Submit change request form
2. Impact assessment (scope, timeline, budget)
3. Stakeholder review
4. Approval/rejection by appropriate authority
5. Implementation or communication of decision

**Approval Authority:**
| Change Type | Approval Authority | Timeframe |
|-------------|-------------------|-----------|
| Minor (< {{threshold}}) | Project Manager | 2 days |
| Medium ({{range}}) | Project Sponsor | 5 days |
| Major (> {{threshold}}) | Steering Committee | 10 days |

---

## 6. Risk Management

### 6.1 Risk Assessment

| Risk ID | Risk Description | Category | Probability | Impact | Risk Score | Mitigation Strategy | Owner | Status |
|---------|-----------------|----------|-------------|--------|------------|---------------------|-------|--------|
| R-001 | {{description}} | Technical | H/M/L | H/M/L | {{score}} | {{strategy}} | {{owner}} | Active |
| R-002 | {{description}} | Resource | H/M/L | H/M/L | {{score}} | {{strategy}} | {{owner}} | Active |
| R-003 | {{description}} | Budget | H/M/L | H/M/L | {{score}} | {{strategy}} | {{owner}} | Monitoring |

**Risk Categories:**
- Technical: Technology, integration, performance
- Resource: Availability, skills, capacity
- Budget: Cost overruns, funding
- Schedule: Delays, dependencies
- External: Market, regulatory, vendor

**Risk Scoring:**
- **Probability:** High (>60%), Medium (30-60%), Low (<30%)
- **Impact:** High (Major impact), Medium (Moderate impact), Low (Minor impact)
- **Risk Score:** Probability × Impact

### 6.2 Risk Response Strategies

**High-Priority Risks (Score > 7):**
1. **{{risk_name}}**
   - Response Strategy: {{Avoid/Mitigate/Transfer/Accept}}
   - Action Plan: {{detailed_actions}}
   - Contingency Plan: {{backup_plan}}
   - Monitoring: {{how_monitored}}

2. **{{risk_name}}**
   - Response Strategy: {{Avoid/Mitigate/Transfer/Accept}}
   - Action Plan: {{detailed_actions}}
   - Contingency Plan: {{backup_plan}}
   - Monitoring: {{how_monitored}}

### 6.3 Risk Monitoring & Review

- **Risk Review Frequency:** {{frequency}}
- **Risk Register Updates:** {{frequency}}
- **Risk Owner Responsibilities:** Monthly risk status reporting
- **Escalation Triggers:** New high-priority risks, risk score increases

---

## 7. Quality Management

### 7.1 Quality Objectives

**Quality Goals:**
- Defect density: < {{target}} defects per 1000 LOC
- Test coverage: > {{target}}%
- Customer satisfaction: > {{target}}
- System uptime: > {{target}}%

### 7.2 Quality Assurance Process

**QA Activities:**
| Activity | Description | Frequency | Owner | Criteria |
|----------|-------------|-----------|-------|----------|
| Code Review | Peer review of code changes | Per PR | Tech Lead | 100% of code |
| Unit Testing | Automated unit tests | Continuous | Developers | >80% coverage |
| Integration Testing | System integration tests | Per build | QA Team | All integrations |
| User Acceptance Testing | End-user validation | Pre-release | Product Owner | All features |
| Performance Testing | Load and stress testing | Per milestone | QA Team | Meet SLA |
| Security Testing | Vulnerability scanning | Weekly | Security Team | Zero critical |

### 7.3 Quality Control Methods

**Testing Strategy:**
- Unit testing: {{framework}}
- Integration testing: {{approach}}
- E2E testing: {{tool}}
- Performance testing: {{tool}}
- Security testing: {{tool}}

**Acceptance Criteria:**
- Feature completeness: 100% of P0 requirements
- Bug severity threshold: Zero P0/P1 bugs
- Performance benchmarks: {{benchmarks}}
- Security compliance: {{standards}}

### 7.4 Quality Metrics & Reporting

**Tracked Metrics:**
- Defect escape rate
- Test pass rate
- Code quality score
- Technical debt ratio
- Customer-reported issues

**Quality Reports:**
- Daily: Test execution status
- Weekly: Quality metrics dashboard
- Milestone: Quality assessment report

---

## 8. Dependencies & Assumptions

### 8.1 Internal Dependencies

| Dependency | Description | Owner | Status | Impact if Delayed |
|------------|-------------|-------|--------|------------------|
| {{dependency}} | {{description}} | {{owner}} | On Track/At Risk | {{impact}} |
| {{dependency}} | {{description}} | {{owner}} | On Track/At Risk | {{impact}} |

### 8.2 External Dependencies

| Dependency | Vendor/Partner | SLA | Contingency Plan | Status |
|------------|---------------|-----|------------------|--------|
| {{dependency}} | {{vendor}} | {{sla}} | {{plan}} | On Track/At Risk |
| {{dependency}} | {{vendor}} | {{sla}} | {{plan}} | On Track/At Risk |

### 8.3 Key Assumptions

| Assumption | Impact if Wrong | Validation Method | Owner |
|------------|----------------|-------------------|-------|
| {{assumption}} | {{impact}} | {{method}} | {{owner}} |
| {{assumption}} | {{impact}} | {{method}} | {{owner}} |

**Critical Assumptions:**
- {{critical_assumption_1}}
- {{critical_assumption_2}}

---

## 9. Success Criteria & Project Closure

### 9.1 Project Success Criteria

**Must-Have Criteria:**
- ✓ All P0 deliverables completed and accepted
- ✓ Quality standards met
- ✓ Budget variance < {{percentage}}
- ✓ Timeline variance < {{percentage}}
- ✓ Stakeholder approval obtained

**Desired Criteria:**
- All P1 deliverables completed
- Customer satisfaction > {{target}}
- Team satisfaction > {{target}}

### 9.2 Project Closure Process

**Closure Activities:**
1. Final deliverable handover
2. Documentation completion
3. Knowledge transfer
4. Lessons learned session
5. Team recognition
6. Budget reconciliation
7. Contract closure

**Closure Criteria:**
- All deliverables accepted by stakeholders
- All documentation completed and archived
- All resources released
- Final project report submitted
- Post-implementation review completed

---

## 10. Approval & Sign-off

### 10.1 Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Project Sponsor | {{name}} | _____________ | ______ |
| Project Manager | {{name}} | _____________ | ______ |
| Steering Committee Chair | {{name}} | _____________ | ______ |
| Key Stakeholder | {{name}} | _____________ | ______ |

### 10.2 Version History

| Version | Date | Author | Changes | Approver |
|---------|------|--------|---------|----------|
| v0.1 | {{date}} | {{author}} | Initial draft | - |
| v1.0 | {{date}} | {{author}} | Baseline approved | {{approver}} |

---

## 11. Appendices

### 11.1 Reference Documents
- Initiative Document: `{{path}}`
- MRD: `{{path}}`
- PSD: `{{path}}`
- PRD: `{{path}}`
- Release Plan: `{{path}}`

### 11.2 Glossary
- **PID:** Project Initiation Document
- **Steering Committee:** Governance body providing oversight
- **Project Sponsor:** Executive accountable for project success
- **Milestone:** Significant project checkpoint
- **Deliverable:** Tangible output produced by project

### 11.3 Supporting Materials
- Detailed project plan
- Resource allocation spreadsheet
- Risk register
- Stakeholder matrix

---

### Step 8: Interactive Content Generation
-   Guide user through each section systematically
-   Ask clarifying questions where information is unclear
-   Reference existing documents when possible
-   Validate completeness before proceeding to next section
-   Get user confirmation on critical decisions (budget, timeline, scope)

### Step 9: Save PID Document
-   Generate filename: `[YYYYMMDD]-<initiative_slug>-pid-v[version].md`
-   If file with today's date exists, increment version number
-   Save to: `niopd-workspace/plans/[filename]`
-   Create `plans/` directory if it doesn't exist

### Step 10: Confirm and Conclude
-   Confirm completion: "✅ I've created a Project Initiation Document for **<initiative_name>**."
-   Provide path: "You can review the PID at: `niopd-workspace/plans/[YYYYMMDD]-<initiative_slug>-pid-v[version].md`"
-   Explain next steps: "This PID document requires approval from:
    - Project Sponsor: {{sponsor_name}}
    - Steering Committee members
    - Key stakeholders
    
    Once approved, you can proceed with:
    - Detailed project planning: `/niopd:PM:agile-planning`
    - Risk management setup: `/niopd:PM:risk-analysis`
    - Resource allocation: `/niopd:PM:resources`
    - Release planning: `/niopd:PM:release`"

## Error Handling
- **Missing Reference Documents:** If key documents (Initiative, MRD, PSD, PRD) are not found, inform user and proceed with template placeholders
- **Incomplete Information:** If user cannot provide certain details, mark sections with `[TODO: Requires input from {{role}}]`
- **Budget/Timeline Conflicts:** If budget or timeline seems unrealistic, flag concerns and ask for validation
- **Unclear Scope:** If scope boundaries are ambiguous, ask specific clarifying questions
- **Missing Stakeholders:** If key stakeholders are not identified, recommend stakeholder analysis exercise

In all error cases, maintain helpful tone and emphasize that PID can be iteratively refined before approval.

## Next Steps After PID Creation

The PID serves as the foundational governance document. Use it to drive:

### Project Execution Planning
- **Detailed Planning:** `/niopd:PM:agile-planning` - Break down work into sprints
- **Resource Planning:** `/niopd:PM:resources` - Detailed resource allocation
- **Risk Management:** `/niopd:PM:risk-analysis` - Comprehensive risk assessment

### Project Tracking & Control
- **KPI Tracking:** `/niopd:PM:kpis` - Monitor project health metrics
- **Dependency Management:** `/niopd:PM:dependencies` - Track critical dependencies

### Stakeholder Management
- **Updates:** `/niopd:PO:stakeholder-update` - Regular stakeholder communications
- **Decision Framework:** `/niopd:PM:daci-framework` - Clarify decision authority
