---
name: niopd-pd-stories
description: Generates user stories from PRD or initiative documents following agile best practices. Use for sprint planning, backlog creation, requirements decomposition, or development handoff.
---

# User Story Generation Skill

This skill generates well-structured user stories from product documents, following agile best practices and INVEST criteria.

## Theoretical Foundation

### Origin
User stories emerged from **Extreme Programming (XP)** and were formalized by **Mike Cohn** in his book "User Stories Applied" (2004).

### User Story Format
> "As a [persona], I want to [capability], so that [benefit]."

### INVEST Criteria

| Criterion | Meaning |
|-----------|---------|
| **I**ndependent | Can be developed in any order |
| **N**egotiable | Details can be discussed |
| **V**aluable | Provides value to user/business |
| **E**stimable | Can be estimated by team |
| **S**mall | Fits in a sprint |
| **T**estable | Has clear acceptance criteria |

### Story Levels
- **Epic**: Large feature area (weeks-months)
- **Feature**: Specific capability (days-weeks)
- **Story**: Single piece of work (hours-days)
- **Task**: Technical subtask (hours)

### When to Use
- Sprint planning
- Backlog refinement
- Requirements handoff
- Feature scoping
- Acceptance testing prep

## Instructions

### Step 1: Identify Source Document
Read from:
- PRD in `03-docs/`
- Initiative in `03-docs/`
- Requirements summary

### Step 2: Extract Requirements
List all capabilities mentioned:
- Functional requirements
- Non-functional requirements
- User needs
- Business rules

### Step 3: Generate Stories
For each capability:

```markdown
### Story: [Title]
**As a** [persona],
**I want to** [capability],
**So that** [benefit].

**Priority**: P0/P1/P2
**Estimate**: [Story Points]

**Acceptance Criteria**:
- [ ] Given [context], when [action], then [result]
- [ ] Given [context], when [action], then [result]

**Notes**: [Additional context]
```

### Step 4: Organize by Epic
Group related stories under epics:
- Epic 1: [Name]
  - Story 1.1
  - Story 1.2
- Epic 2: [Name]

### Step 5: Validate INVEST
For each story, verify:
- [ ] Independent from other stories
- [ ] Negotiable in implementation
- [ ] Valuable to user/business
- [ ] Estimable by team
- [ ] Small enough for sprint
- [ ] Testable with clear criteria

### Step 6: Generate Report
**File path**: `03-docs/[YYYYMMDD]-user-stories-v0.md`

## Output Specifications
- **File Naming**: `[YYYYMMDD]-user-stories-v0.md`
- **Location**: `03-docs/`
- **Template**: `references/user-story-template.md`

## Related Skills
- `niopd-pd-draft-prd`: PRD source
- `niopd-pd-acceptance-criteria`: Detailed criteria
- `niopd-pm-agile-planning`: Sprint planning
- `niopd-ur-personas`: Persona definitions
