---
name: niopd-pd-acceptance-criteria
description: Creates detailed acceptance criteria for user stories. Use for sprint planning, QA preparation, or developer handoff.
---

# Acceptance Criteria Skill

This skill creates testable acceptance criteria using Given-When-Then format.

## Theoretical Foundation

### Gherkin Syntax
```
GIVEN [context/precondition]
WHEN [action/trigger]
THEN [expected outcome]
```

### Good Criteria Are
- Testable (can verify pass/fail)
- Independent (each stands alone)
- Specific (no ambiguity)
- Complete (all scenarios covered)

## Instructions

### Step 1: Identify Story
What user story are we specifying?

### Step 2: List Scenarios
- Happy path
- Edge cases
- Error cases

### Step 3: Write Criteria
For each scenario:
```
GIVEN [context]
WHEN [action]
THEN [outcome]
```

### Step 4: Validate
- [ ] All scenarios covered
- [ ] Each criterion is testable
- [ ] No ambiguity remains

### Step 5: Generate Document
**File path**: `03-docs/[YYYYMMDD]-acceptance-criteria-v0.md`

## Output Specifications
- **File Naming**: `[YYYYMMDD]-acceptance-criteria-v0.md`
- **Location**: `03-docs/`
- **Template**: `references/acceptance-criteria-template.md`
