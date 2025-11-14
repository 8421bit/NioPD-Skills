---
argument-hint: [--for=<initiative_name>] [--reports=<report_types>]
description: Generates a comprehensive Product Strategy Document (PSD) that bridges strategic analysis and product execution by integrating insights from MR, UR, and ST analysis reports. Auto-detects initiative name from current directory if not specified.
---

# Command: /niopd:PD:draft-psd

This command generates a **Product Strategy Document (PSD)** - a critical bridge document that connects strategic analysis with product execution. The PSD synthesizes insights from Market Research (MR), User Research (UR), and Strategic Analysis (ST) to provide unified strategic guidance for product and operations teams.

## Theoretical Foundation

### Origin and Development
The Product Strategy Document concept evolved from strategic planning frameworks in the 1990s-2000s as product organizations grew more complex. It bridges **strategic planning** (Henderson, Porter, Mintzberg) with **product execution** (Lean, Agile methodologies), creating a unified strategic layer.

### Core Principle
The PSD serves as the **strategic bridge** between high-level market analysis (MRD) and detailed execution specifications (PRD). It translates strategic intent into prioritized product objectives, ensuring alignment across all teams while maintaining strategic flexibility.

### The Three-Document Strategy

In NioPD's documentation architecture:

**MRD → PSD → PRD**

1. **MRD**: Market opportunity (external view)
2. **PSD**: Product strategy (strategic choices)
3. **PRD**: Product execution (implementation details)

### PSD's Unique Role

**Strategic Synthesis**:
- Integrates insights from multiple analysis reports
- Resolves conflicts between market, user, and strategic data
- Creates coherent strategic narrative

**Priority Setting**:
- Translates market opportunities into product priorities
- Makes explicit trade-offs (what to build vs. defer)
- Allocates resources strategically

**Team Alignment**:
- Provides shared strategic context
- Aligns product, engineering, operations, marketing
- Creates decision-making framework

### Essential PSD Components

**Strategic Context**:
- Market landscape summary
- Competitive positioning
- SWOT synthesis
- Strategic opportunities

**User Insights**:
- Target segment prioritization
- Core user needs
- Satisfaction drivers
- Behavioral patterns

**Strategic Objectives**:
- Vision and mission alignment
- 3-5 strategic goals
- Success metrics (KPIs)
- Value proposition

**Product Strategy**:
- Strategic priorities (P0/P1/P2/P3)
- Feature strategy direction
- Technical strategy considerations
- Resource allocation

**Implementation Roadmap**:
- Phased approach
- Timeline and milestones
- Dependencies
- Success criteria per phase

### Strategic Frameworks Integrated

**Porter's Generic Strategies**:
- Cost Leadership vs. Differentiation
- Broad vs. Narrow (Focus) strategies
- Guides positioning decisions

**Blue Ocean vs. Red Ocean**:
- Compete in existing markets (Red)
- Create new market space (Blue)
- Shapes innovation strategy

**Product-Market Fit** (Marc Andreessen):
- Evidence of market pull
- Validates strategy
- Guides pivots

**Strategic Trade-offs**:
- Good-Better-Best positioning
- Feature breadth vs. depth
- Speed to market vs. quality

### Priority Framework (MoSCoW Applied)

**P0 - Must Have**: Launch blockers
- Core value proposition
- Competitive parity features
- Technical foundation

**P1 - Should Have**: High value
- Differentiation features
- User delight factors
- Strategic investments

**P2 - Could Have**: Future consideration
- Nice-to-have enhancements
- Long-term opportunities
- Experimental features

**P3 - Won't Have**: Explicitly out of scope
- Deprioritized requests
- Future phase candidates
- Strategic "no's"

### When to Create a PSD

- After completing strategic analysis (SWOT, competitive, market)
- Before detailed PRD development
- Annual strategic planning cycles
- Major product pivots
- New product initiatives
- Portfolio prioritization

### PSD Best Practices

1. **Synthesis Over Aggregation**: Create insights, don't just summarize
2. **Make Trade-offs Explicit**: Document what you're NOT doing and why
3. **Quantify Where Possible**: Use data to support strategic choices
4. **Align to Vision**: Connect strategy to overarching product vision
5. **Stakeholder Review**: Get buy-in from cross-functional leaders
6. **Living Document**: Update quarterly as strategy evolves

### Related Strategic Frameworks

- **OKRs (Objectives and Key Results)**: John Doerr (Google, Intel)
- **Balanced Scorecard**: Kaplan & Norton (strategic performance)
- **Strategic Roadmapping**: Product strategy visualization
- **GOST Framework**: Goals, Objectives, Strategies, Tactics
- **North Star Metric**: Sean Ellis (focus metric)

### Complementary NioPD Commands

- `/niopd:ST:swot` - Strategic SWOT analysis foundation
- `/niopd:MR:competitor` - Competitive intelligence
- `/niopd:UR:feedback` - User insights synthesis
- `/niopd:PD:draft-mrd` - Market requirements foundation
- `/niopd:PD:draft-prd` - Execution specification
- `/niopd:ST:balanced-scorecard` - Strategic performance framework

## Usage
`/niopd:PD:draft-psd [--for=<initiative_name>] [--reports=<report_types>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative name.

**Examples:**
```bash
# Explicit initiative name with specific reports
/niopd:PD:draft-psd --for=dark-mode-feature --reports=swot,competitor

# Auto-detect initiative name, all reports
cd dark-mode-feature
/niopd:PD:draft-psd  # Uses "dark-mode-feature"

# Auto-detect initiative name, specific reports
cd dark-mode-feature
/niopd:PD:draft-psd --reports=feedback,behavior
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

3.  **Validate Initiative (Optional):**
    -   Check if initiative file exists in `niopd-workspace/docs/` (optional reference)
    -   Check if PRD exists in `niopd-workspace/docs/` (optional reference)
    -   These are helpful context but not required for PSD generation

4.  **Identify Analysis Reports:**
    -   Search for relevant analysis reports in `niopd-workspace/reports/`:
        -   SWOT analysis reports: `niopd-workspace/reports/[YYYYMMDD]-*-swot-v[version].md`
        -   Competitor comparison reports: `niopd-workspace/reports/[YYYYMMDD]-*-competitor-comparison-v[version].md`
        -   User feedback summary reports: `niopd-workspace/reports/[YYYYMMDD]-<initiative_slug>-feedback-summary-v[version].md`
        -   User behavior reports: `niopd-workspace/reports/[YYYYMMDD]-*-behavior-summary-v[version].md`
        -   User journey reports: `niopd-workspace/reports/[YYYYMMDD]-*-user-journey-v[version].md`
        -   Satisfaction analysis reports: `niopd-workspace/reports/[YYYYMMDD]-*-satisfaction-v[version].md`
    -   If `--reports` argument is provided, filter reports by specified types.
    -   If no reports are found, inform the user and suggest running relevant MR, UR, or ST commands first.

## Instructions

You are Nio, a strategic product AI assistant specializing in bridging strategic analysis and product execution. Your goal is to synthesize insights from multiple analysis reports into a unified Product Strategy Document that provides actionable strategic guidance for product and operations teams.

**Core Principle:** The PSD should be created in the primary language used by the user and serve as the strategic foundation for product development and operations. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Strategic Data
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将帮您为 **<initiative_name>** 倡议创建一份产品战略文档，综合来自可用分析报告的见解。"
    -   If English: "I'll help you create a Product Strategy Document for **<initiative_name>** by synthesizing insights from available analysis reports."
    -   For other languages, use an appropriate translation based on user's language preference
-   Search for and read relevant analysis reports in `niopd-workspace/reports/`:
    -   **Strategic Analysis Reports:**
        -   SWOT analysis: `[YYYYMMDD]-*-swot-v[version].md`
        -   Competitor comparison: `[YYYYMMDD]-*-competitor-comparison-v[version].md`
        -   Business model canvas: `[YYYYMMDD]-*-canvas-v[version].md`
    -   **User Research Reports:**
        -   User feedback summary: `[YYYYMMDD]-<initiative_slug>-feedback-summary-v[version].md`
        -   User behavior analysis: `[YYYYMMDD]-*-behavior-summary-v[version].md`
        -   User journey maps: `[YYYYMMDD]-*-user-journey-v[version].md`
        -   Satisfaction analysis: `[YYYYMMDD]-*-satisfaction-v[version].md`
    -   **Market Research Reports:**
        -   Market segmentation: `[YYYYMMDD]-*-segmentation-v[version].md`
        -   Market trends: `[YYYYMMDD]-*-trends-v[version].md`
-   If `--reports` argument is provided, filter reports by specified types.
-   Read initiative file (if exists) for context: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-initiative-v[version].md`
-   Read existing PRD (if exists) for alignment: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-prd-v[version].md`
-   Ensure you're reading the most recent versions by checking dates and version numbers.

### Step 2: Strategic Analysis & Synthesis
-   Analyze each identified report to extract strategic insights:
    -   **Strategic Opportunities:** From SWOT, competitor analysis, market trends
    -   **Market Positioning:** From competitor comparison, market segmentation
    -   **User Needs & Pain Points:** From feedback, behavior, satisfaction reports
    -   **Competitive Advantages:** From SWOT strengths, competitor gaps
    -   **Risks & Threats:** From SWOT threats, market analysis
-   Synthesize insights across reports:
    -   Identify patterns and themes
    -   Resolve conflicting findings through prioritization
    -   Connect strategic opportunities with user needs
    -   Align market positioning with competitive advantages
-   Prepare strategic recommendations based on synthesis.

### Step 3: Product Strategy Formulation
-   Define strategic priorities based on synthesized insights:
    -   **Vision & Mission Alignment:** How initiative supports overall product vision
    -   **Strategic Objectives:** 3-5 key objectives derived from analysis
    -   **Target User Segments:** Prioritized based on user research and market data
    -   **Value Proposition:** Unique value based on competitive analysis and user needs
    -   **Differentiation Strategy:** How to stand out based on competitor gaps
-   Develop strategic trade-offs and decisions:
    -   What to prioritize and why
    -   What to defer and rationale
    -   Resource allocation recommendations
-   Create success criteria aligned with strategic objectives.

### Step 4: Product Strategy Document Structure

**Important:** Generate a comprehensive Product Strategy Document using the following structure:

---
# Product Strategy Document: {{initiative_name}}

## 1. Executive Summary
*A concise overview (2-3 paragraphs) of the strategic direction, key objectives, and expected impact*

## 2. Strategic Context
### 2.1 Market Landscape
- Current market trends and dynamics
- Key market opportunities identified
- Market size and growth potential

### 2.2 Competitive Positioning
- Competitive landscape overview
- Our competitive advantages
- Competitor gaps and opportunities
- Differentiation strategy

### 2.3 SWOT Analysis Summary
- **Strengths:** Internal capabilities to leverage
- **Weaknesses:** Areas requiring improvement
- **Opportunities:** External opportunities to capture
- **Threats:** External risks to mitigate

## 3. User Insights & Needs
### 3.1 Target User Segments
- Primary user segment definition
- Secondary user segments
- Segment prioritization rationale

### 3.2 Core User Needs
- Key pain points to address
- Feature requests and expectations
- User behavior patterns

### 3.3 User Satisfaction Drivers
- Current satisfaction levels
- Key drivers of satisfaction
- Areas for improvement

## 4. Strategic Objectives
### 4.1 Vision & Mission Alignment
*How this initiative supports overall product vision*

### 4.2 Strategic Goals (3-5 goals)
1. **Goal 1:** {{goal_description}}
   - Success Metrics: {{metrics}}
   - Timeline: {{timeline}}
   - Impact: {{expected_impact}}

2. **Goal 2:** {{goal_description}}
   [Same structure]

### 4.3 Value Proposition
*Unique value we deliver to users based on insights*

## 5. Product Strategy & Priorities
### 5.1 Strategic Priorities
**P0 - Must Have (Launch Blockers):**
- {{priority_item}} - Rationale: {{reason}}

**P1 - Should Have (High Value):**
- {{priority_item}} - Rationale: {{reason}}

**P2 - Nice to Have (Future Consideration):**
- {{priority_item}} - Rationale: {{reason}}

**P3 - Out of Scope:**
- {{deprioritized_item}} - Rationale: {{reason}}

### 5.2 Feature Strategy
*High-level feature direction based on user needs and strategic objectives*

### 5.3 Technical Strategy Considerations
*Key technical approaches and constraints*

## 6. Implementation Roadmap
### 6.1 Phased Approach
**Phase 1: Foundation (Timeline)**
- Objectives: {{phase_objectives}}
- Key Deliverables: {{deliverables}}
- Success Criteria: {{criteria}}

**Phase 2: Growth (Timeline)**
- Objectives: {{phase_objectives}}
- Key Deliverables: {{deliverables}}
- Success Criteria: {{criteria}}

**Phase 3: Optimization (Timeline)**
- Objectives: {{phase_objectives}}
- Key Deliverables: {{deliverables}}
- Success Criteria: {{criteria}}

### 6.2 Resource Requirements
- Engineering: {{resources}}
- Design: {{resources}}
- Product: {{resources}}
- Marketing/Operations: {{resources}}

### 6.3 Key Milestones
- Milestone 1: {{milestone}} - {{date}}
- Milestone 2: {{milestone}} - {{date}}

## 7. Risk Management & Mitigation
### 7.1 Strategic Risks
| Risk | Probability | Impact | Mitigation Strategy | Owner |
|------|-------------|--------|---------------------|-------|
| {{risk}} | {{prob}} | {{impact}} | {{mitigation}} | {{owner}} |

### 7.2 Market Risks
*Competition, market changes, user adoption*

### 7.3 Execution Risks
*Technical, resource, timeline challenges*

## 8. Success Metrics & KPIs
### 8.1 North Star Metric
*Primary metric that indicates overall success*

### 8.2 Key Performance Indicators
**Business Metrics:**
- {{metric}}: Target {{target}}, Baseline {{baseline}}

**User Metrics:**
- {{metric}}: Target {{target}}, Baseline {{baseline}}

**Product Metrics:**
- {{metric}}: Target {{target}}, Baseline {{baseline}}

### 8.3 Measurement Plan
- Data collection methods
- Analysis frequency
- Review and iteration process

## 9. Operational Strategy
### 9.1 Go-to-Market Strategy
- Launch approach: {{soft_launch/beta/full_launch}}
- Target audience: {{initial_users}}
- Marketing/communication plan

### 9.2 User Onboarding Strategy
- Onboarding flow design
- Support and documentation
- Feedback collection mechanism

### 9.3 Growth Strategy
- User acquisition channels
- Retention tactics
- Expansion opportunities

## 10. Dependencies & Assumptions
### 10.1 Key Dependencies
- Technical dependencies
- Cross-team dependencies
- External dependencies

### 10.2 Critical Assumptions
- Assumption: {{assumption}}
  - Risk if Wrong: {{risk}}
  - Validation Method: {{validation}}

## 11. Decision Framework
### 11.1 Strategic Trade-offs Made
*Decisions made and rationale*

### 11.2 Open Strategic Questions
- Question: {{question}}
  - Impact: {{impact}}
  - Decision Deadline: {{date}}
  - DRI (Directly Responsible Individual): {{owner}}

## 12. Appendix
### 12.1 Source Analysis Reports
- **SWOT Analysis:** `{{report_path}}`
- **Competitor Analysis:** `{{report_path}}`
- **User Research:** `{{report_path}}`
- **Market Analysis:** `{{report_path}}`

### 12.2 Reference Documents
- Initiative Document: `{{path}}`
- PRD (if exists): `{{path}}`

---

### Step 5: Content Generation with User Guidance
-   Guide the user through structured questioning to populate the PSD:
    -   Confirm strategic priorities identified from analysis
    -   Clarify trade-offs between competing priorities
    -   Validate resource allocation assumptions
    -   Confirm timeline and milestone feasibility
-   Generate content section by section, seeking user confirmation:
    -   Present each major section for review
    -   Adjust based on user feedback
    -   Ensure alignment with user's strategic vision
-   Maintain consistent language and terminology throughout.

### Step 6: Save Product Strategy Document
-   Generate filename following NioPD naming convention: `[YYYYMMDD]-<initiative_slug>-psd-v[version].md`
-   If a file with today's date exists, increment version number
-   Save the PSD to: `niopd-workspace/docs/[filename]`
-   Create the `docs/` directory if it doesn't exist

### Step 7: Generate Strategy Summary Report
-   Create an executive summary document for quick reference:
    -   1-page overview of key strategic decisions
    -   Priority matrix visualization
    -   Next steps and action items
-   Save summary as: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-psd-summary-v[version].md`

### Step 8: Confirm and Conclude
-   Confirm completion: "✅ I've created a Product Strategy Document for **<initiative_name>**."
-   Provide the path: "You can review the PSD at: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-psd-v[version].md`"
-   Provide summary path: "Executive summary available at: `niopd-workspace/docs/[YYYYMMDD]-<initiative_slug>-psd-summary-v[version].md`"
-   Suggest next steps: "This Product Strategy Document serves as the foundation for:
    - Creating or updating your PRD: `/niopd:PD:draft --for=<initiative_name>`
    - Generating user stories: `/niopd:PD:stories --for=<initiative_name>`
    - Creating implementation roadmap: `/niopd:PD:roadmap --for=<initiative_name>`
    - Developing OKRs: `/niopd:PM:kpis --for=<initiative_name>`
    - Planning releases: `/niopd:PM:release --for=<initiative_name>`"

## Error Handling
- **No Analysis Reports Found:** If no relevant analysis reports are found, inform the user: "I couldn't find analysis reports in `niopd-workspace/reports/`. To create a comprehensive Product Strategy Document, I recommend running the following commands first:
  - Strategic analysis: `/niopd:ST:swot`, `/niopd:MR:competitor`
  - User research: `/niopd:UR:feedback`, `/niopd:UR:behavior`
  - Market research: `/niopd:MR:segmentation`
  
  Alternatively, I can create a PSD template with placeholders for you to fill in manually."
- **Insufficient Data:** If limited reports are available, proceed with available data and clearly mark sections requiring additional research with `[TODO: Requires additional analysis - Run /niopd:XX:command]`
- **Conflicting Insights:** If analysis reports contain conflicting findings, present both perspectives and ask user to clarify strategic direction
- **File Save Errors:** If unable to create `strategy/` directory or save files, provide clear error messages and suggest manual directory creation
- **Report Access Issues:** If permission errors occur reading reports, suggest checking file permissions

In all error cases, maintain a helpful tone, provide actionable suggestions, and emphasize that a PSD can still be created with available information and user input.

## Next Steps After PSD Creation

The Product Strategy Document serves as the strategic foundation. Use it to drive:

### Product Development
- **Create/Update PRD:** `/niopd:PD:draft --for=<initiative_name>` - Use PSD strategic priorities to guide detailed requirements
- **Generate User Stories:** `/niopd:PD:stories --for=<initiative_name>` - Break down strategy into actionable development tasks
- **Create Roadmap:** `/niopd:PD:roadmap --for=<initiative_name>` - Visualize strategic implementation timeline

### Project Management
- **Define KPIs:** `/niopd:PM:kpis --for=<initiative_name>` - Create measurable objectives from strategic goals
- **Plan Releases:** `/niopd:PM:release --for=<initiative_name>` - Structure rollout based on strategic phases

### Stakeholder Communication
- **Stakeholder Updates:** `/niopd:PO:stakeholder-update --for=<initiative_name>` - Communicate strategic direction

### Further Analysis (if needed)
- **Additional SWOT:** `/niopd:ST:swot --for=<initiative_name>` - Refine strategic analysis
- **User Testing:** `/niopd:UR:usability --product=<name>` - Validate strategic assumptions
- **Market Validation:** `/niopd:MR:segmentation --product=<name>` - Confirm target segment strategy