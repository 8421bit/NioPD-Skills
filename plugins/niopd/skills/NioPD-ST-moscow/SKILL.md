---
name: niopd-st-moscow
description: Applies MoSCoW prioritization method to categorize requirements by importance. Use for scope negotiations, release planning, or stakeholder alignment on priorities.
---

# MoSCoW Prioritization Skill

This skill applies the MoSCoW method to systematically categorize requirements, helping teams focus on what's truly essential.

## Theoretical Foundation

### Origin
MoSCoW was developed by **Dai Clegg** at Oracle in 1994 as part of the Dynamic Systems Development Method (DSDM). The name is an acronym for the four priority categories.

### The Four Categories

| Category | Meaning | Criteria |
|----------|---------|----------|
| **Must Have** | Critical–no viable product without | Non-negotiable |
| **Should Have** | Important but not vital | High value, not critical |
| **Could Have** | Desirable if time permits | Nice to have |
| **Won't Have** | Explicitly excluded (this time) | Out of scope |

### Key Principle
At most **60%** of effort should go to Must Haves, ensuring buffer for the unexpected.

### When to Use
- Release planning
- Scope negotiation
- Stakeholder alignment
- Resource allocation
- MVP definition

## Instructions

### Step 1: Gather All Requirements
List all features/requirements from:
- PRD
- Backlog
- Stakeholder requests
- User feedback

### Step 2: Define "Must Have" Criteria
Clarify with stakeholders:
- What makes something absolutely critical?
- What cannot be compromised?
- What breaks the product if missing?

### Step 3: Categorize Each Item
For each requirement:
- **Must**: Would the product fail without this?
- **Should**: Is it very important but survivable without?
- **Could**: Is it nice to have if time permits?
- **Won't**: Should we explicitly exclude this?

### Step 4: Validate Must Haves
Challenge each "Must Have":
- Is this truly essential?
- What would happen without it?
- Could we ship and add later?

### Step 5: Check 60% Rule
Calculate effort distribution:
- Must Haves: ≤60% of effort
- If over: Re-evaluate what's truly "Must"

### Step 6: Document and Communicate
**File path**: `02-reports/[YYYYMMDD]-moscow-priorities-v0.md`

**Format:**
```markdown
## Must Have
- [Requirement]: [Rationale]

## Should Have
- [Requirement]: [Rationale]

## Could Have
- [Requirement]: [Rationale]

## Won't Have (This Release)
- [Requirement]: [Why excluded]
```

## Output Specifications
- **File Naming**: `[YYYYMMDD]-moscow-priorities-v0.md`
- **Location**: `02-reports/`
- **Template**: `references/moscow-template.md`

## Related Skills
- `niopd-st-rice`: Quantitative prioritization
- `niopd-ur-kano`: Satisfaction-based categorization
- `niopd-pd-roadmap`: Roadmap planning
- `niopd-pm-release`: Release planning
