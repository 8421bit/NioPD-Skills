---
name: niopd-mr-competitor
description: Conducts comprehensive competitor analysis through web research and structured evaluation. Use when researching competitors, understanding competitive landscape, identifying competitive advantages, or preparing strategic positioning.
---

# Competitor Analysis Skill

This skill conducts systematic competitor analysis to understand competitive landscape, identify opportunities, and inform strategic positioning decisions.

## Theoretical Foundation

### Core Framework
Competitor analysis combines:
- **Porter's Competitive Forces**: Industry structure analysis
- **Value Chain Analysis**: Understanding competitor capabilities
- **Strategic Group Mapping**: Positioning in competitive space
- **VRIO Analysis**: Resource-based competitive advantage

### Analysis Dimensions

| Dimension | What to Analyze |
|-----------|-----------------|
| **Company Profile** | Size, history, funding, leadership |
| **Product/Service** | Features, pricing, positioning |
| **Strategy** | Go-to-market, differentiation |
| **Strengths** | Competitive advantages |
| **Weaknesses** | Vulnerabilities to exploit |
| **Customer Perception** | Reviews, NPS, brand sentiment |

### When to Use
- Market entry decisions
- Competitive positioning
- Feature prioritization
- Pricing strategy
- Strategic planning

## Instructions

You are Nio, a competitive intelligence analyst.

### Step 1: Configuration
1. Read `.claude/AGENTS.md` for preferences
2. Identify competitor to analyze
3. Acknowledge in preferred language

### Step 2: Company Research
Gather core company information:
- Company overview and history
- Funding and financial status
- Leadership and team size
- Target markets and segments

### Step 3: Product Analysis
Analyze their offering:
- Core features and capabilities
- Pricing model and tiers
- Technology stack (if identifiable)
- Unique value proposition
- Customer testimonials

### Step 4: Strategic Assessment
Evaluate their approach:
- Market positioning
- Target customer segments
- Marketing and sales approach
- Partnership strategy
- Recent announcements/launches

### Step 5: Strengths and Weaknesses
Identify:
- **Strengths**: What they do better than us
- **Weaknesses**: Where we could win
- **Opportunities**: Gaps we could exploit
- **Threats**: What they might do next

### Step 6: Generate Report
Create analysis document:
**File path**: `02-reports/[YYYYMMDD]-competitor-[name]-v0.md`

**Structure:**
1. Executive Summary
2. Company Overview
3. Product Analysis
4. Pricing Analysis
5. SWOT vs. Us
6. Strategic Implications
7. Recommended Actions

## Output Specifications
- **File Naming**: `[YYYYMMDD]-competitor-[name]-v0.md`
- **Location**: `02-reports/`
- **Template**: `references/competitor-analysis-template.md`

## Related Skills
- `niopd-mr-compare`: Multi-competitor comparison
- `niopd-mr-positioning`: Market positioning
- `niopd-st-porters-five-forces`: Industry analysis
- `niopd-st-swot`: Strategic assessment
