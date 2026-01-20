---
name: niopd-pm-daci-framework
description: Applies DACI decision-making framework to clarify roles and responsibilities in decisions. Use for cross-functional decisions, stakeholder alignment, or decision documentation.
---

# DACI Decision Framework Skill

This skill applies the DACI framework to clarify decision-making roles and ensure effective cross-functional decisions.

## Theoretical Foundation

### DACI Roles

| Role | Responsibility |
|------|----------------|
| **D**river | Owns the decision process, ensures it happens |
| **A**pprover | Makes the final call, accountable for outcome |
| **C**ontributors | Provide input, expertise, perspectives |
| **I**nformed | Need to know the decision but don't participate |

### Key Principles
- **One Approver**: Only one person has final say
- **Clear Driver**: Someone owns moving it forward
- **Right Contributors**: Not too many, not too few
- **Appropriate Informed**: Don't over-communicate

### When to Use
- Cross-functional decisions
- Major feature directions
- Resource allocation
- Process changes
- Strategic choices
- Conflict resolution

## Instructions

### Step 1: Define the Decision
- "What decision needs to be made?"
- "Why is this decision important?"
- "When does it need to be made?"
- "What are the options?"

### Step 2: Assign Roles
| Role | Person(s) | Why |
|------|-----------|-----|
| Driver | [Name] | [Reason] |
| Approver | [Name] | [Reason] |
| Contributors | [Names] | [What they bring] |
| Informed | [Names] | [Why they need to know] |

### Step 3: Gather Input
Driver facilitates:
- Collect contributor perspectives
- Document options and trade-offs
- Synthesize recommendation

### Step 4: Make Decision
Approver:
- Reviews input and recommendation
- Makes final decision
- Documents rationale

### Step 5: Communicate
Driver:
- Informs all stakeholders
- Documents decision and reasoning
- Clarifies next steps

### Step 6: Generate Document
**File path**: `03-docs/[YYYYMMDD]-daci-[decision]-v0.md`

**Format:**
```markdown
## Decision: [Title]

### DACI
| Role | Person |
|------|--------|
| Driver | [Name] |
| Approver | [Name] |
| Contributors | [Names] |
| Informed | [Names] |

### Options Considered
1. [Option A]: [Pros/Cons]
2. [Option B]: [Pros/Cons]

### Decision Made
[Decision statement]

### Rationale
[Why this decision]

### Next Steps
1. [Action]
```

## Output Specifications
- **File Naming**: `[YYYYMMDD]-daci-[decision]-v0.md`
- **Location**: `03-docs/`
- **Template**: `references/daci-template.md`

## Related Skills
- `niopd-pm-risk-analysis`: Decision risks
- `niopd-po-stakeholder-update`: Communication
- `niopd-st-swot`: Option analysis
