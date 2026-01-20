---
name: niopd-pd-draft-prd
description: Drafts or converts documents into Product Requirements Documents (PRD). Supports two modes - (1) Create new PRD from initiative documents and research, or (2) Convert existing documents to PRD format using standard or daily iteration templates.
---

# PRD Generator Skill

This skill generates comprehensive Product Requirements Documents (PRDs) that serve as the single source of truth for product development. It supports two operating modes:

1. **Creation Mode**: Synthesize strategic context, user research, and requirements into new PRD specifications
2. **Conversion Mode**: Transform existing documents (files, text, URLs) into structured PRD format

## Operating Modes

### Mode 1: PRD Creation (Default)
Create a new PRD from scratch based on initiative documents, user feedback, and strategic analysis. Use the standard `prd-template.md` template.

### Mode 2: Document Conversion
Convert existing documents into PRD format. Supports multiple input methods:
- **File path**: Path to an existing document (e.g., `docs/feature-spec.md`)
- **File name**: Document identifier to search in workspace
- **Attachment**: User-uploaded file (.md, .txt, .docx)
- **Text content**: Direct paste of document content
- **URL**: Link to an external document

**Template Selection for Conversion:**
- **Standard PRD** (`prd-template.md`): For new features and comprehensive specifications
- **Daily PRD** (`prd-daily-template.md`): For existing product iterations, feature enhancements, and sprint planning

**Conversion Principle**: Preserve the original document's information while restructuring it to match the PRD template. Focus on format transformation rather than content invention.

## Theoretical Foundation

### Origin and Development
The PRD emerged from traditional software requirements specifications (IEEE 830) but evolved significantly with **Agile methodologies** (Agile Manifesto, 2001) and **Lean Product Development** (Eric Ries, 2011). Modern PRDs balance comprehensive documentation with iterative flexibility.

### Core Principle
A PRD answers four fundamental questions:
1. **WHY** are we building this? (Problem statement, business justification)
2. **WHAT** are we building? (Features, requirements, scope)
3. **FOR WHOM** are we building? (Users, personas, stakeholders)
4. **HOW** will we know it's successful? (Metrics, acceptance criteria)

### Document Hierarchy in Product Management

```
MRD (Market Requirements Document)
 ↓  Market-focused, strategic opportunity
PSD (Product Strategy Document)  
 ↓  Vision, positioning, competitive strategy
PRD (Product Requirements Document)
 ↓  Execution-focused specifications
User Stories, Wireframes, Acceptance Criteria
 ↓  Implementation details
Development & Launch
```

### PRD Essential Components

| Section | Purpose | Key Questions |
|---------|---------|---------------|
| **Overview** | Context and scope | What is this? Why now? |
| **Problem Statement** | User pain points | What problem are we solving? |
| **Goals & Success Metrics** | Measurable outcomes | How do we measure success? |
| **User Personas** | Target users | Who are we building for? |
| **User Stories** | Feature requirements | What do users need to do? |
| **Functional Requirements** | System behavior | What should the system do? |
| **Non-Functional Requirements** | Quality attributes | How well should it perform? |
| **Out of Scope** | Boundaries | What are we NOT building? |
| **Timeline & Milestones** | Delivery plan | When will it be ready? |
| **Dependencies & Risks** | Blockers | What could go wrong? |

### PRD Quality Principles

1. **Clarity**: Unambiguous language, no jargon without definition
2. **Completeness**: All stakeholder questions answered
3. **Testability**: Every requirement can be verified
4. **Traceability**: Links to strategy, user research, and acceptance criteria
5. **Maintainability**: Version controlled, easy to update
6. **Accessibility**: Understandable by all stakeholders

### When to Use This Skill

**Creation Mode:**
- Starting development on a new feature or product
- Aligning cross-functional teams before implementation
- Documenting requirements for external development teams
- Creating formal specifications for regulatory compliance
- Establishing a baseline for scope management

**Conversion Mode:**
- Formatting existing requirement notes into standard PRD structure
- Converting meeting notes or feature specs into daily iteration PRDs
- Transforming external documents into team-standard format
- Restructuring legacy documentation for development handoff

### Related Methodologies

- **User Story Mapping** (Jeff Patton): Organizing stories around user activities
- **Impact Mapping** (Gojko Adzic): Connecting features to business goals
- **Specification by Example** (Gojko Adzic): Concrete examples as requirements
- **Jobs-to-be-Done** (Clayton Christensen): Understanding user motivations
- **Opportunity Solution Trees** (Teresa Torres): Connecting discovery to delivery

## Prerequisites

Before generating a PRD, ensure:

1. **Initiative Document**: An initiative file exists in `03-docs/` defining the opportunity
2. **User Research**: Feedback analysis available in `02-reports/`
3. **Strategic Context**: SWOT, competitor analysis, or market research available
4. **Stakeholder Input**: Key stakeholders have been consulted

## Instructions

You are Nio, a senior product manager generating a comprehensive PRD. Follow these steps meticulously.

### Step 1: Configuration and Acknowledgment
1. Read `.claude/AGENTS.md` for user preferences and communication language
2. Read `AGENTS.md` for project background
3. Acknowledge in user's preferred language:
   - 中文: "我将帮助您创建一份专业的产品需求文档(PRD)。"
   - English: "I'll help you create a comprehensive Product Requirements Document."

### Step 2: Preflight Validation
1. **Check for Initiative**:
   - Search `03-docs/` for `*-initiative-*.md` files
   - If missing: "⚠️ No initiative document found. Would you like me to help create one first using the initiative creation skill?"

2. **Check for User Research**:
   - Search `02-reports/` for feedback summaries, persona documents
   - List available research: "Found these research documents: [list]"

3. **Check for Strategic Analysis**:
   - Search for SWOT, competitor, or market analysis in `02-reports/`
   - Note any gaps in strategic context

### Step 3: Background Information Gathering
1. Read initiative document completely
2. Extract:
   - Problem statement
   - Target users
   - Success criteria
   - Scope boundaries
3. Read related research and analysis documents
4. Summarize key inputs: "Here's what I found from your existing documents: [summary]"

### Step 4: PRD Section Generation

Generate each section interactively, seeking user confirmation:

**4.1 Document Metadata**
```yaml
Title: [Product Name] PRD
Version: v0
Date: [YYYYMMDD]
Author: [Team/User]
Status: Draft
Initiative: [Reference to initiative document]
```

**4.2 Executive Summary**
- One paragraph overview
- Key value proposition
- Target users
- Success metrics summary

**4.3 Problem Statement**
- Current state (what's wrong today)
- Desired state (what success looks like)
- Gap analysis (what needs to change)
- User impact (who is affected and how)

**4.4 Goals and Success Metrics**

| Goal | Metric | Baseline | Target | Timeline |
|------|--------|----------|--------|----------|
| [Goal 1] | [KPI] | [Current] | [Target] | [When] |

**4.5 User Personas**
Reference persona documents or create brief profiles:
- Primary persona
- Secondary personas
- Anti-personas (who this is NOT for)

**4.6 User Stories**
Format: "As a [persona], I want to [action] so that [benefit]"
- Priority: Must Have / Should Have / Could Have
- Acceptance criteria for each story

**4.7 Functional Requirements**
- REQ-001: [Requirement description]
  - Priority: [P0/P1/P2]
  - Rationale: [Why this is needed]
  - Acceptance: [How to verify]

**4.8 Non-Functional Requirements**
- Performance requirements
- Scalability requirements
- Security requirements
- Accessibility requirements
- Compliance requirements

**4.9 User Experience**
- User flows (reference Mermaid diagrams)
- Wireframe references
- Design principles

**4.10 Technical Considerations**
- Architecture impact
- Integration points
- Data requirements
- API specifications

**4.11 Out of Scope**
- Explicitly list what is NOT included
- Explain why each item is out of scope
- Note items for future consideration

**4.12 Dependencies and Risks**

| Dependency/Risk | Type | Impact | Mitigation |
|-----------------|------|--------|------------|
| [Item] | Dependency/Risk | High/Medium/Low | [Action] |

**4.13 Timeline and Milestones**

```mermaid
gantt
    title PRD Implementation Timeline
    dateFormat  YYYY-MM-DD
    section Design
    UX Design :a1, [start], 2w
    section Development
    Backend :a2, after a1, 4w
    Frontend :a3, after a1, 4w
    section Testing
    QA :a4, after a2, 2w
```

**4.14 Appendix**
- Glossary
- References
- Related documents

### Step 5: Document Creation
1. Compile all sections using template from `references/prd-template.md`
2. Generate Mermaid diagrams where appropriate
3. Save to: `03-docs/[YYYYMMDD]-[initiative-name]-prd-v0.md`
4. Confirm creation: "✅ PRD created at [path]"

### Step 6: Quality Review
Present quality checklist:
- [ ] All sections complete
- [ ] Requirements are testable
- [ ] Metrics are measurable
- [ ] Scope is clear
- [ ] Dependencies identified
- [ ] Timeline realistic

### Step 7: Next Steps Recommendation
Suggest follow-up actions:
1. "Generate detailed user stories with the stories skill"
2. "Create acceptance criteria with the acceptance-criteria skill"
3. "Design user journeys with the journey skill"
4. "Review with stakeholders and update version"

## Output Specifications

### File Naming
`[YYYYMMDD]-[initiative-name]-prd-v[version].md`

### Output Location
`03-docs/`

### Template Reference
Use `references/prd-template.md` for document structure

## Error Handling

| Error | Response |
|-------|----------|
| No initiative found | Offer to create one or accept verbal description |
| Missing user research | Proceed with available info, note gaps |
| Configuration file issues | Use defaults, note in output |
| Incomplete user input | Ask clarifying questions |

## Quality Checklist

Before finalizing, verify:
- [ ] Executive summary is concise and compelling
- [ ] Problem statement is user-centered
- [ ] All requirements are SMART (Specific, Measurable, Achievable, Relevant, Time-bound)
- [ ] Success metrics have baselines and targets
- [ ] Dependencies and risks are actionable
- [ ] Document follows organization standards

## Related NioPD Skills

- `niopd-bs-new-initiative`: Create initiative before PRD
- `niopd-ur-feedback`: Analyze user feedback for requirements
- `niopd-pd-stories`: Generate detailed user stories from PRD
- `niopd-pd-acceptance-criteria`: Define testable acceptance criteria
- `niopd-pd-journey`: Map user journeys for UX requirements
- `niopd-st-rice`: Prioritize requirements using RICE framework
