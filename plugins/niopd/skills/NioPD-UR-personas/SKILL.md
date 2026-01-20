---
name: niopd-ur-personas
description: Creates detailed user personas from feedback, interview data, and behavioral analysis. Use for user segmentation, design alignment, stakeholder communication, or empathy building.
---

# User Persona Creation Skill

This skill creates evidence-based user personas that capture key user segments, their behaviors, goals, and pain points to guide product decisions.

## Theoretical Foundation

### Origin
Personas were popularized by **Alan Cooper** (1999) in "The Inmates Are Running the Asylum." They serve as archetypal users representing key segments.

### Persona Components

| Component | Description |
|-----------|-------------|
| **Demographics** | Age, role, context |
| **Goals** | What they want to achieve |
| **Pain Points** | Frustrations and challenges |
| **Behaviors** | How they act and decide |
| **Quote** | Voice of the segment |
| **Scenarios** | Context of product use |

### When to Use
- Starting a new design project
- Aligning cross-functional teams
- Prioritizing feature requests
- Communicating to stakeholders
- Onboarding new team members

## Instructions

### Step 1: Gather Data
Collect evidence from:
- User interview transcripts
- Feedback summaries
- Behavioral analytics
- Survey responses
- Support tickets

### Step 2: Identify Segments
Group users by:
- Goals and motivations
- Behavior patterns
- Job roles
- Experience levels
- Pain point clusters

### Step 3: Select Primary Personas
Choose 2-4 personas representing:
- **Primary**: Core target user
- **Secondary**: Important but not primary
- **Negative**: Who we're NOT designing for

### Step 4: Develop Persona Profiles
For each persona, create:

```markdown
## Persona: [Name]
**Segment**: [Type/Role]
**Photo**: [Illustrative, not real]

### Demographics
- Age: [Range]
- Role: [Job/Title]
- Context: [Where they use product]

### Goals
1. [Primary goal]
2. [Secondary goal]

### Pain Points
1. [Frustration 1]
2. [Frustration 2]

### Behaviors
- [Behavior pattern 1]
- [Behavior pattern 2]

### Quote
"[Representative voice of this segment]"

### Scenario
[Typical use case story]
```

### Step 5: Validate
- Cross-check with data sources
- Review with stakeholders
- Test for empathy and utility

### Step 6: Generate Document
**File path**: `02-reports/[YYYYMMDD]-personas-v0.md`

## Output Specifications
- **File Naming**: `[YYYYMMDD]-personas-v0.md`
- **Location**: `02-reports/`
- **Template**: `references/persona-template.md`

## Related Skills
- `niopd-ur-feedback`: Feedback analysis
- `niopd-ur-interview`: Interview summaries
- `niopd-ur-jtbd`: Jobs-to-be-Done
- `niopd-pd-stories`: User stories from personas
