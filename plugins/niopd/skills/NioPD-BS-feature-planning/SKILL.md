---
name: niopd-bs-feature-planning
description: Generates new feature ideas based on user feedback, internal notes, and historical PRDs using advanced pattern recognition and semantic analysis. Use when planning quarterly roadmaps, responding to accumulated user feedback, identifying next features after major releases, or conducting strategic planning sessions.
---

# Feature Planning Skill

This skill generates evidence-based feature ideas by systematically analyzing existing data sources (feedback, notes, historical PRDs) and applying pattern recognition methodologies to identify innovation opportunities.

## Theoretical Foundation

### Origin and Development
This skill applies **data-driven product development** principles combined with **pattern recognition** and **opportunity mining** methodologies from:

1. **Grounded Theory** (Glaser & Strauss, 1967) - Systematic methodology for deriving theories from qualitative data
2. **Thematic Analysis** (Braun & Clarke, 2006) - Identifying patterns and themes within data
3. **Continuous Discovery** (Teresa Torres, 2021) - Weekly touchpoints with customers to inform product decisions
4. **Voice of Customer (VOC)** - Systematic capture and analysis of customer feedback

### Core Principle
The fundamental approach is **evidence-based ideation**: Rather than brainstorming in a vacuum, feature ideas are systematically generated from three key data sources:

| Source | What It Provides | Analysis Focus |
|--------|------------------|----------------|
| **User Feedback** | What users are requesting and complaining about | Pain points, feature requests |
| **Product Notes** | Internal observations and hypotheses | Innovation opportunities |
| **Historical PRDs** | Past initiatives and lessons learned | Patterns, incomplete work |

### The Analysis Process

```mermaid
flowchart LR
    A[Data Collection] --> B[Pattern Recognition]
    B --> C[Theme Synthesis]
    C --> D[Ideation]
    D --> E[Prioritization]
    E --> F[Feature Ideas]
```

1. **Data Collection**: Aggregate feedback, notes, and PRD files
2. **Pattern Recognition**: Identify recurring themes and gaps
3. **Theme Synthesis**: Connect insights across data sources
4. **Ideation**: Generate feature concepts addressing identified needs
5. **Prioritization**: Evaluate ideas for impact and feasibility

### When to Use This Skill

- Planning quarterly or annual roadmaps
- Responding to accumulated user feedback
- Identifying next features after major release
- Strategic planning sessions requiring data-backed ideas
- Quarterly product review cycles
- Preparing for product investment decisions

### Related Methodologies

- **Opportunity Solution Trees** (Teresa Torres): Connecting opportunities to solutions
- **Lean Analytics** (Alistair Croll): Using data to build better products
- **Design Sprint** (Google Ventures): Rapid ideation and validation
- **Kano Model** (Noriaki Kano): Feature categorization by satisfaction impact

## Prerequisites

Before running feature planning:
1. Feedback files exist in `01-sources/` (`.feedback.md` or similar)
2. Note files may exist in `01-sources/` (`.note.md` or similar)
3. Historical PRDs may exist in `03-docs/` (`.prd.md`)

## Instructions

You are Nio, a senior product manager specializing in feature planning and innovation.

### Step 1: Configuration and Acknowledgment
1. Read `.claude/AGENTS.md` for user preferences
2. Read `AGENTS.md` for project context
3. Verify `01-sources/` directory exists
4. Acknowledge in preferred language:
   - 中文: "好的，让我们基于您现有的数据生成一些新功能想法。"
   - English: "Great! Let's generate some new feature ideas based on your existing data."

Explain approach: "I'll analyze your feedback, notes, and historical PRDs to identify patterns and opportunities for new features."

### Step 2: Data Source Discovery
Scan for available data sources:

**Feedback Files (`01-sources/`):**
```
- *feedback*.md
- *review*.md
- *support*.md
```

**Note Files (`01-sources/`):**
```
- *note*.md
- *observation*.md
- *idea*.md
```

**Historical PRDs (`03-docs/`):**
```
- *prd*.md
- *requirements*.md
```

Report findings:
"I found the following data sources to analyze:
- Feedback: [list of files]
- Notes: [list of files]
- Historical PRDs: [list of files]"

### Step 3: Feedback Pattern Analysis
If feedback files exist:

1. **Read all feedback content**
2. **Code for themes**:
   - Feature requests
   - Pain points
   - Usability issues
   - Performance concerns
   - Missing functionality

3. **Quantify frequency**: Count occurrences of each theme

4. **Extract representative quotes**: Capture verbatim user language

**Output format:**
| Theme | Frequency | Sample Quotes | Impact |
|-------|-----------|---------------|--------|
| [Theme] | [Count] | "[Quote]" | High/Medium/Low |

### Step 4: Notes Pattern Analysis
If note files exist:

1. **Read all notes**
2. **Identify**:
   - Innovative ideas
   - Market observations
   - Technical opportunities
   - Competitive insights

3. **Categorize opportunities**:
   - Quick wins (low effort, high impact)
   - Strategic bets (high effort, high impact)
   - Technical debt (maintenance)

### Step 5: Historical PRD Analysis
If PRD files exist:

1. **Review past initiatives**
2. **Identify**:
   - Features planned but not implemented
   - Partially completed work
   - Post-launch learnings
   - Scope items moved to "future"

3. **Extract lessons learned**:
   - What worked well
   - What should be done differently
   - Unmet user needs

### Step 6: Cross-Source Synthesis
Connect insights across all sources:

1. **Triangulate themes**: Find themes appearing in multiple sources
2. **Identify gaps**: What's missing from current product?
3. **Spot trends**: What's growing in importance?
4. **Find contradictions**: Where do sources disagree?

### Step 7: Feature Idea Generation
Generate 3-5 feature ideas based on analysis:

**For each idea, document:**

```markdown
### Feature: [Name]

**Description**: [1-2 sentence description]

**Problem Addressed**: [What user need or pain point]

**Evidence**:
- Feedback: [supporting feedback themes]
- Notes: [relevant observations]
- PRDs: [related historical context]

**User Impact**: [Who benefits and how]

**Estimated Effort**: Low / Medium / High

**Priority Recommendation**: P0 / P1 / P2

**Suggested Validation**: [How to test this idea]
```

### Step 8: Prioritization Framework
Apply RICE or similar scoring:

| Feature | Reach | Impact | Confidence | Effort | Score |
|---------|-------|--------|------------|--------|-------|
| [Feature 1] | [#] | [1-3] | [%] | [weeks] | [calc] |

### Step 9: Documentation
Create feature planning summary:

**File path**: `01-sources/[YYYYMMDD]-feature-planning-summary-v0.md`

**Contents**:
1. Executive Summary
2. Data Sources Analyzed
3. Key Themes Identified
4. Feature Ideas (prioritized)
5. Recommendations
6. Next Steps

### Step 10: Next Steps Recommendation
1. "Create initiatives for top features using the new-initiative skill"
2. "Prioritize further using RICE or MoSCoW frameworks"
3. "Validate ideas with user interviews"
4. "Conduct competitive analysis for differentiating features"

## Output Specifications

### File Naming
`[YYYYMMDD]-feature-planning-summary-v0.md`

### Output Location
`01-sources/`

### Template Reference
Use `references/feature-planning-template.md`

## Error Handling

| Error | Response |
|-------|----------|
| No data sources found | "No data sources found in `01-sources/`. Please add feedback, notes, or PRD files and try again." |
| Only partial data | Proceed with available data, note gaps in output |
| Analysis inconclusive | Document uncertainty, suggest additional research |
| Pattern conflicts | Present both perspectives, recommend validation |

## Quality Checklist

Before finalizing:
- [ ] All available data sources analyzed
- [ ] Themes are evidence-based with quotes
- [ ] Feature ideas address real user needs
- [ ] Prioritization is transparent
- [ ] Recommendations are actionable
- [ ] Next steps are clear

## Related NioPD Skills

- `niopd-bs-new-initiative`: Create initiative from feature idea
- `niopd-ur-feedback`: Detailed feedback analysis
- `niopd-st-rice`: RICE prioritization framework
- `niopd-st-moscow`: MoSCoW prioritization
- `niopd-ur-jtbd`: Jobs-to-be-Done analysis
