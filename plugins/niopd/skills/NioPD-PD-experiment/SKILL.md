---
name: niopd-pd-experiment
description: Designs product experiments (A/B tests, pilots). Use for feature validation, optimization, or data-driven decisions.
---

# Experiment Design Skill

This skill designs rigorous product experiments for validation.

## Theoretical Foundation

### Experiment Components
- **Hypothesis**: What we believe will happen
- **Variables**: What we change (independent) and measure (dependent)
- **Control**: Baseline for comparison
- **Sample Size**: Statistical significance requirements
- **Duration**: How long to run

## Instructions

### Step 1: Define Hypothesis
"We believe [change] will cause [effect] for [users]."

### Step 2: Design Test
| Element | Control | Treatment |
|---------|---------|-----------|
| [Variable] | [Baseline] | [Change] |

### Step 3: Determine Metrics
- Primary: [What success looks like]
- Secondary: [Supporting metrics]
- Guardrails: [What not to break]

### Step 4: Calculate Sample Size
Based on:
- Minimum detectable effect
- Baseline conversion rate
- Statistical significance (typically 95%)

### Step 5: Plan Duration
Consider:
- Sample accumulation rate
- Weekly patterns
- External factors

### Step 6: Generate Document
**File path**: `04-plans/[YYYYMMDD]-experiment-v0.md`

## Output Specifications
- **File Naming**: `[YYYYMMDD]-experiment-v0.md`
- **Location**: `04-plans/`
- **Template**: `references/experiment-template.md`
