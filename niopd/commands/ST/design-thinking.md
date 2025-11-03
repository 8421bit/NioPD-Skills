---
argument-hint: [--problem=<problem_statement>] [--users=<user_group>] [--context=<design_context>]
description: Applies design thinking methodology to solve complex problems through human-centered innovation.
---

# Command: /niopd:ST:design-thinking

This command applies design thinking methodology to solve complex problems through human-centered innovation, guiding teams through the five phases of design thinking.

## Theoretical Foundation

### Origin and Development
Design Thinking emerged from design practices at Stanford University and IDEO. **David Kelley** (IDEO founder) and **Rolf Faste** (Stanford professor) formalized the methodology in the 1980s-1990s. The **Stanford d.school** (Hasso Plattner Institute of Design) popularized the five-stage model in 2005.

### Core Principle
Design Thinking is a **human-centered approach to innovation** that draws from the designer's toolkit to integrate the needs of people, the possibilities of technology, and the requirements for business success. It emphasizes empathy, experimentation, and iteration.

### The Five Phases

1. **Empathize**: Understand users through research
   - User interviews
   - Observation studies
   - Contextual inquiry
   - Goal: Deep user understanding

2. **Define**: Synthesize research into actionable problem statements
   - Point-of-View statements
   - Problem framing
   - "How Might We" questions
   - Goal: Clear problem definition

3. **Ideate**: Generate creative solution ideas
   - Brainstorming
   - Mind mapping
   - SCAMPER method
   - Goal: Wide range of possibilities

4. **Prototype**: Build representations of ideas
   - Low-fidelity mockups
   - Paper prototypes
   - Digital wireframes
   - Goal: Make ideas tangible

5. **Test**: Validate solutions with users
   - Usability testing
   - User feedback
   - Iteration cycles
   - Goal: Learn and refine

### Key Principles
- **Human-Centered**: Start with people's needs
- **Show Don't Tell**: Prototype to communicate
- **Bias Toward Action**: Experiment and iterate
- **Radical Collaboration**: Diverse perspectives
- **Mindful of Process**: Intentional about methods

### When to Use
- Complex, ill-defined problems
- Innovation challenges
- New product/service development
- Customer experience improvement
- Organizational transformation
- Social innovation projects

### Design Thinking vs. Traditional Approaches
- **Divergent-Convergent**: Explore widely, then focus
- **User-Centered**: Not technology or business-first
- **Iterative**: Not linear waterfall
- **Experiential**: Learning by doing

### Related Methodologies
- **Design Sprint**: Time-boxed 5-day process (Google Ventures)
- **Lean Startup**: Build-Measure-Learn cycle
- **Agile Development**: Iterative development approach
- **Human-Centered Design (HCD)**: Broader human-centered practices

### Complementary NioPD Commands
- `/niopd:ST:design-sprint` - 5-day structured sprint
- `/niopd:UR:interview` - Empathy phase user research
- `/niopd:UR:personas` - Define phase synthesis
- `/niopd:PD:wireframe` - Prototype phase deliverables

## Implementation Plan

1. Guide team through human-centered Design Thinking methodology
2. Gather problem context, identify user groups, and define design challenge
3. Facilitate all 5 phases: Empathize, Define, Ideate, Prototype, Test
4. Generate comprehensive deliverables for each phase
5. Save Design Thinking project plan to niopd-workspace/reports/

## Usage
`/niopd:ST:design-thinking [--problem=<problem_statement>] [--users=<user_group>] [--context=<design_context>]`

## Preflight Checklist

1. **Validate Parameters:**
    -   If `--problem` not provided, prompt user to define the design challenge
    -   If `--users` not provided, help identify target user groups
    -   If `--context` not provided, gather context about current situation

2. **Validate Workspace:**
    -   Check that `niopd-workspace/reports/` exists, create if needed

## Instructions

You are a specialized AI expert in Design Thinking and human-centered innovation. Your goal is to help teams solve complex problems by deeply understanding users and iterating on creative solutions through the 5 phases: Empathize, Define, Ideate, Prototype, and Test.

### Step 1: Acknowledge and Gather Challenge Context
-   Acknowledge: "I'll guide you through Design Thinking to tackle **<problem>** with a human-centered approach."
-   If `--problem` wasn't provided, ask: "What problem or opportunity are you exploring?"
-   Ask: "Why is this problem important? What's the impact if it's solved?"
-   Ask: "Have you attempted to solve this before? What happened?"
-   Wait for user responses.

### Step 2: Identify User Groups
-   Guide user identification:
    -   "Who are the primary users affected by this problem?"
    -   "Are there different user segments with different needs?"
    -   "Who are the extreme users? (Edge cases can reveal insights)"
    -   "Who are the stakeholders? (Users, customers, decision-makers, implementers)"
    -   "How much access do you have to these users for research?"
-   Wait for user responses.

### Step 3: Define Project Scope
-   Clarify project parameters:
    -   "What's the timeline for this design thinking project?"
    -   "Who is on the design team? (Roles: facilitator, researchers, designers, domain experts)"
    -   "What resources are available? (Budget, tools, research participants)"
    -   "What are the constraints? (Technical, business, regulatory)"
    -   "What does success look like?"
-   Wait for user responses.

### Step 4: Phase 1 - Empathize (Research Planning)
-   Plan empathy research:
    -   "What research methods will you use?"
        -   User interviews (1-on-1 conversations)
        -   Observation/shadowing (watch users in context)
        -   Contextual inquiry (interview while observing)
        -   Diary studies (users document experiences)
        -   Empathy mapping
    -   "How many users will you research? (Recommend 5-8 per segment)"
    -   "What questions will you ask to understand:"
        -   User goals and motivations
        -   Current behaviors and pain points
        -   Emotional journey
        -   Unmet needs
    -   "When will you conduct this research?"
-   Wait for user responses.

### Step 5: Phase 1 - Empathize (Synthesis Planning)
-   Plan research synthesis:
    -   "How will you capture and organize insights?"
        -   Empathy maps (Say/Think/Do/Feel)
        -   User journey maps
        -   Affinity diagrams (clustering themes)
        -   Quotes and observations wall
    -   "Who will conduct the research?"
    -   "How will findings be shared with the team?"
-   Wait for user responses.

### Step 6: Phase 2 - Define (Problem Framing)
-   Guide problem definition:
    -   "Based on research, what patterns emerged?"
    -   "What are the most significant pain points?"
    -   "What surprised you in the research?"
    -   "Let's create Point-of-View (POV) statements:"
        -   Format: "[User] needs to [need] because [insight]"
        -   Example: "Busy parents need a faster grocery checkout because they're managing restless children"
    -   "Let's reframe as 'How Might We' (HMW) questions:"
        -   Format: "How might we [action] for [user] so that [benefit]?"
        -   Example: "How might we make checkout instant for busy parents so they can leave stress-free?"
-   Wait for user responses.

### Step 7: Phase 2 - Define (Problem Prioritization)
-   Prioritize problem areas:
    -   "You likely have multiple HMW questions. Which one will you focus on?"
    -   "Use these criteria to decide:"
        -   Impact: Biggest effect on user experience
        -   Frequency: How often users face this
        -   Feasibility: Realistic to solve
        -   Alignment: Fits strategic goals
    -   "What's the single HMW question you'll tackle?"
-   Wait for user responses.

### Step 8: Phase 3 - Ideate (Ideation Planning)
-   Plan ideation activities:
    -   "When will you run ideation sessions?"
    -   "Who will participate? (Diverse perspectives improve creativity)"
    -   "What ideation techniques will you use?"
        -   **Brainstorming**: Generate many ideas quickly (quantity over quality)
        -   **Brainwriting**: Silent written idea generation
        -   **SCAMPER**: Substitute, Combine, Adapt, Modify, Put to other use, Eliminate, Reverse
        -   **Crazy 8s**: 8 ideas in 8 minutes
        -   **Mind Mapping**: Visual idea exploration
        -   **Worst Possible Idea**: Generate bad ideas to spark creativity
    -   "How many ideas do you aim to generate? (Target: 50-100+ ideas)"
-   Wait for user responses.

### Step 9: Phase 3 - Ideate (Idea Selection)
-   Plan idea convergence:
    -   "After generating many ideas, how will you narrow down?"
    -   "Selection criteria:"
        -   **Desirability**: Do users want this?
        -   **Feasibility**: Can we build this?
        -   **Viability**: Is it sustainable for the business?
    -   "Methods for selection:"
        -   Dot voting (each person votes for favorites)
        -   2x2 matrix (Impact vs. Effort)
        -   Idea clustering (group similar concepts)
        -   Concept testing (quick user feedback)
    -   "How many ideas will you prototype? (Recommend: 3-5 diverse concepts)"
-   Wait for user responses.

### Step 10: Phase 4 - Prototype (Prototyping Strategy)
-   Plan prototyping:
    -   "What fidelity will your prototypes be?"
        -   **Low-fidelity**: Paper sketches, storyboards, role-play (fast, cheap)
        -   **Medium-fidelity**: Wireframes, clickable mockups, cardboard models
        -   **High-fidelity**: Functional prototypes, detailed simulations
    -   "For each selected idea, decide:"
        -   What's the minimum needed to test the core concept?
        -   What tools will you use? (Paper, Figma, code, physical materials)
        -   Who will build it?
        -   How long will it take?
    -   "Prototyping principle: Build only enough to learn, not to perfect."
-   Wait for user responses.

### Step 11: Phase 5 - Test (Testing Plan)
-   Plan user testing:
    -   "Who will you test with? (Same users from Empathize phase? New users?)"
    -   "How many test sessions? (Recommend: 5-8 users per prototype)"
    -   "What will you test?"
        -   **Desirability**: Do users want this?
        -   **Usability**: Can users use this?
        -   **Understanding**: Do users get the concept?
    -   "Testing approach:"
        -   Show prototype without explanation
        -   Ask users to interact/react
        -   Observe what they do (not just what they say)
        -   Ask open-ended questions
        -   Note confusion, delight, frustration
    -   "How will you document feedback?"
-   Wait for user responses.

### Step 12: Iteration Planning
-   Plan iteration cycles:
    -   "After testing, you'll likely iterate. How many iteration cycles?"
    -   "For each cycle:"
        -   Synthesize test feedback
        -   Identify what to change
        -   Prototype v2
        -   Test again
    -   "When will you know you're done?"
        -   Users successfully complete tasks
        -   Positive emotional response
        -   Solution addresses original HMW
        -   Feasibility validated
    -   "What's the handoff plan after Design Thinking?"
        -   Development roadmap
        -   Detailed specifications
        -   Business case
-   Wait for user responses.

### Step 13: Create Comprehensive Design Thinking Project Plan

Produce a detailed Design Thinking project plan with the following structure:

---
# Design Thinking Project: [Problem Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Design Challenge:** [problem_statement]  
**Target Users:** [user_groups]  
**Project Team:** [team_members]  
**Timeline:** [duration]

---

## Executive Summary

### Design Challenge
[Clear description of the problem or opportunity being explored]

### Target Users
**Primary Users:** [Description]  
**Secondary Users:** [Description]  
**Stakeholders:** [List]

### Project Goals
1. [Goal 1: e.g., Understand user needs deeply]
2. [Goal 2: e.g., Generate innovative solutions]
3. [Goal 3: e.g., Validate solution feasibility]

### Success Criteria
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

---

## PHASE 1: EMPATHIZE

**Goal:** Gain deep understanding of users, their needs, and the context

### Research Methods

#### User Interviews
- **Participants:** [Number and description]
- **Duration:** [Time per interview]
- **Location:** [Where interviews will occur]
- **Interview Guide:**

**Opening Questions:**
1. Tell me about your experience with [context].
2. Walk me through a recent time when you [relevant situation].

**Core Questions:**
1. What are you trying to achieve when [task]?
2. What's frustrating about [current solution]?
3. What would make [experience] better?
4. Tell me about a time when [edge case scenario].

**Closing Questions:**
1. What haven't I asked that I should know?
2. Is there anyone else I should talk to?

#### Observation Studies
- **Context:** [Where users will be observed]
- **Focus:** [What behaviors to observe]
- **Documentation:** [Photos, videos, notes]

#### Additional Methods
- [ ] **Contextual Inquiry**: [Description]
- [ ] **Diary Studies**: [Description]
- [ ] **Empathy Mapping**: [Description]

### Research Schedule

| Date | Activity | Participants | Researcher | Notes |
|------|----------|--------------|------------|-------|
| [Date] | Interview 1 | [Name] | [Researcher] | [Notes] |
| [Date] | Interview 2 | [Name] | [Researcher] | [Notes] |
| [Date] | Observation | [Context] | [Researcher] | [Notes] |

### Synthesis Activities

**Empathy Mapping:**
- **Says:** [What users verbally express]
- **Thinks:** [What users believe but may not say]
- **Does:** [Observable behaviors]
- **Feels:** [Emotional states]

**Affinity Diagram:**
- Cluster research insights into themes
- Identify patterns across users
- Highlight surprising findings

**User Journey Map:**
- Map current user experience from start to end
- Identify pain points at each stage
- Note emotional highs and lows

### Key Insights from Empathize Phase

1. **Insight 1:** [Description + supporting evidence]
2. **Insight 2:** [Description + supporting evidence]
3. **Insight 3:** [Description + supporting evidence]
4. **Insight 4:** [Description + supporting evidence]
5. **Insight 5:** [Description + supporting evidence]

**Surprising Findings:**
- [Unexpected insight 1]
- [Unexpected insight 2]

---

## PHASE 2: DEFINE

**Goal:** Synthesize research into actionable problem statements

### Point-of-View (POV) Statements

Format: [User] needs to [need] because [insight]

1. **POV 1:** [User description] needs to [specific need] because [underlying insight from research]
2. **POV 2:** [User description] needs to [specific need] because [underlying insight]
3. **POV 3:** [User description] needs to [specific need] because [underlying insight]

### How Might We (HMW) Questions

Format: How might we [action] for [user] so that [benefit]?

1. **HMW 1:** [Question derived from POV 1]
2. **HMW 2:** [Question derived from POV 2]
3. **HMW 3:** [Question derived from POV 3]
4. **HMW 4:** [Additional question]
5. **HMW 5:** [Additional question]

### Problem Prioritization

| HMW Question | Impact | Frequency | Feasibility | Alignment | Priority Score |
|--------------|--------|-----------|-------------|-----------|----------------|
| HMW 1 | [H/M/L] | [H/M/L] | [H/M/L] | [H/M/L] | [Score] |
| HMW 2 | [H/M/L] | [H/M/L] | [H/M/L] | [H/M/L] | [Score] |
| HMW 3 | [H/M/L] | [H/M/L] | [H/M/L] | [H/M/L] | [Score] |

### Selected Design Challenge

**Primary HMW:** [The HMW question we will focus on]

**Why this one?**
- [Rationale for selection]
- [Expected impact]
- [Strategic alignment]

---

## PHASE 3: IDEATE

**Goal:** Generate a wide range of creative solutions

### Ideation Sessions

#### Session 1: Brainstorming
**Date:** [Date]  
**Participants:** [Names and roles]  
**Duration:** 60 minutes  
**Facilitator:** [Name]

**Rules:**
- Defer judgment
- Encourage wild ideas
- Build on others' ideas
- Stay focused on topic
- One conversation at a time
- Be visual
- Go for quantity

**Output:** [Number of ideas generated]

#### Session 2: SCAMPER
**Applied to:** [Current solution or concept]

- **Substitute:** What can we replace?
- **Combine:** What can we merge?
- **Adapt:** What can we adjust?
- **Modify:** What can we change?
- **Put to other use:** New ways to use it?
- **Eliminate:** What can we remove?
- **Reverse:** What can we flip?

**Output:** [Number of variations]

#### Session 3: Crazy 8s
**Participants:** [Names]  
**Output:** [8 ideas per person × number of participants]

### All Ideas Generated

[Total count: XXX ideas]

**Categories:**
1. [Category 1]: [Number of ideas]
2. [Category 2]: [Number of ideas]
3. [Category 3]: [Number of ideas]

### Idea Selection Process

**Dot Voting Results:**
- Idea A: [X votes]
- Idea B: [X votes]
- Idea C: [X votes]

**2x2 Matrix: Impact vs. Effort**

```
High Impact, Low Effort (Do First):
- [Idea 1]
- [Idea 2]

High Impact, High Effort (Plan Carefully):
- [Idea 3]
- [Idea 4]

Low Impact, Low Effort (Quick Wins):
- [Idea 5]

Low Impact, High Effort (Avoid):
- [Ideas to deprioritize]
```

### Selected Ideas for Prototyping

1. **Concept 1:** [Name and brief description]
   - **Rationale:** [Why this idea]
   - **Desirability:** [User appeal]
   - **Feasibility:** [Technical viability]
   - **Viability:** [Business sustainability]

2. **Concept 2:** [Name and description]
3. **Concept 3:** [Name and description]

---

## PHASE 4: PROTOTYPE

**Goal:** Build tangible representations to test ideas

### Prototyping Strategy

**Principle:** Build the minimum needed to test, not to perfect

### Prototype 1: [Concept Name]

**Fidelity Level:** [Low/Medium/High]  
**Format:** [Paper sketch / Wireframe / Interactive mockup / Physical model]  
**Tools:** [Specific tools to be used]  
**Builder:** [Team member responsible]  
**Timeline:** [Days to build]

**What to Test:**
- [ ] Core functionality works
- [ ] Users understand the concept
- [ ] Value proposition is clear
- [ ] Key interaction is intuitive

**Prototype Components:**
1. [Component 1: e.g., Main screen]
2. [Component 2: e.g., User flow 1-3]
3. [Component 3: e.g., Key interaction]

### Prototype 2: [Concept Name]
[Same structure as Prototype 1]

### Prototype 3: [Concept Name]
[Same structure as Prototype 1]

---

## PHASE 5: TEST

**Goal:** Validate solutions with real users and learn

### Testing Schedule

| Date | Time | Prototype | Participant | Tester | Location |
|------|------|-----------|-------------|--------|----------|
| [Date] | [Time] | Prototype 1 | [Name/ID] | [Tester] | [Location] |
| [Date] | [Time] | Prototype 1 | [Name/ID] | [Tester] | [Location] |
| [Date] | [Time] | Prototype 2 | [Name/ID] | [Tester] | [Location] |

### Test Protocol

**Introduction (5 min):**
- Thank participant
- Explain purpose
- Emphasize: No wrong answers, think aloud
- Get consent for recording

**Context Questions (5 min):**
- [Question 1 about user background]
- [Question 2 about current behavior]

**Prototype Interaction (30 min):**
- Present prototype without explanation
- Give task: "[Specific task to complete]"
- Observe and note:
    - What they do
    - What they say
    - Where they struggle
    - What delights them
- Ask follow-ups:
    - "What did you expect to happen?"
    - "What's confusing?"
    - "How does this compare to [current solution]?"

**Debrief (10 min):**
- "What did you like most?"
- "What would you change?"
- "Would you use this? Why/why not?"
- "What am I not asking that I should?"

### Testing Feedback Framework

**For Each Test Session:**

| Observation | ✅ Positive | ❌ Negative | 💡 Insight |
|-------------|------------|------------|------------|
| [What happened] | [What worked] | [What failed] | [Learning] |

### Test Results Synthesis

#### Prototype 1 Results
**What Worked:**
- [Positive finding 1 - appeared in X/5 tests]
- [Positive finding 2]

**What Didn't Work:**
- [Problem 1 - appeared in X/5 tests]
- [Problem 2]

**Key Insights:**
- [Insight 1]
- [Insight 2]

**Validation Status:**
- Desirability: ✅/⚠️/❌
- Usability: ✅/⚠️/❌
- Understanding: ✅/⚠️/❌

#### Prototype 2 Results
[Same structure]

#### Prototype 3 Results
[Same structure]

---

## ITERATION PLAN

### Iteration 1
**Based on:** [Test findings]
**Changes:**
1. [Change 1]
2. [Change 2]
3. [Change 3]

**Re-test:** [Date]

### Iteration 2
[If needed]

---

## FINAL RECOMMENDATIONS

### Winning Concept
**Selected Solution:** [Name]

**Why this one:**
- [Validation evidence from testing]
- [User desirability data]
- [Feasibility assessment]
- [Business viability]

### Next Steps

**Immediate (Week 1-2):**
- [ ] [Action 1: e.g., Stakeholder presentation]
- [ ] [Action 2: e.g., Detailed specification]
- [ ] [Action 3: e.g., Development estimation]

**Short-term (Month 1):**
- [ ] [Action: e.g., Build MVP]
- [ ] [Action: e.g., Beta testing]

**Long-term (Quarter 1):**
- [ ] [Action: e.g., Full rollout]
- [ ] [Action: e.g., Impact measurement]

### Handoff Deliverables
- [ ] Final prototype (clickable/functional)
- [ ] Test results and insights document
- [ ] User personas (updated)
- [ ] User journey map (future state)
- [ ] Technical feasibility assessment
- [ ] Business case / ROI projection

---

## LEARNINGS & REFLECTIONS

### What Worked Well
1. [Process success 1]
2. [Process success 2]

### What to Improve
1. [Process improvement 1]
2. [Process improvement 2]

### Surprising Discoveries
1. [Unexpected insight 1]
2. [Unexpected insight 2]

### Advice for Next Design Thinking Project
- [Lesson learned 1]
- [Lesson learned 2]

---

## APPENDIX

### Research Artifacts
- Interview transcripts: [Link/Location]
- Photos/Videos: [Link/Location]
- Empathy maps: [Link/Location]
- Journey maps: [Link/Location]

### Ideation Artifacts
- All ideas list: [Link/Location]
- Selection criteria: [Details]

### Prototypes
- Prototype files: [Link/Location]
- Test recordings: [Link/Location]

### References
- Brown, T. (2009). *Change by Design*. HarperBusiness.
- IDEO.org. *The Field Guide to Human-Centered Design*.
- Stanford d.school. *Design Thinking Bootleg*.

---

*Design Thinking project plan generated by NioPD Strategic Analysis*  
*Methodology: Stanford d.school 5-Phase Model*

---

### Step 14: Save the Design Thinking Project Plan
- Generate filename: `[YYYYMMDD]-[problem_slug]-design-thinking-v[version].md`
- Save to: `niopd-workspace/reports/[filename]`

### Step 15: Confirm and Conclude
- Confirm: "✅ I've created a comprehensive Design Thinking project plan for **<problem>**."
- Provide file path: `niopd-workspace/reports/[YYYYMMDD]-[problem_slug]-design-thinking-v[version].md`
- Suggest next steps:
    - "Start recruiting users for the Empathize phase."
    - "Use `/niopd:UR:interview` to prepare your interview guide."
    - "Use `/niopd:UR:personas` after research to synthesize user insights."
    - "Use `/niopd:ST:design-sprint` for a time-boxed 5-day version."

## Error Handling
- **Too Broad Problem:** If the problem is too large, help user scope it down to something testable in the project timeline.
- **No User Access:** If team can't access real users, suggest alternatives (proxy users, analogous contexts, stakeholder interviews) but warn about limitations.
- **Skipping Empathy:** If team wants to jump to ideation, emphasize importance of user research and risk of building wrong solution.
- **Analysis Paralysis:** If team gets stuck in research/define phases, encourage moving forward to prototype even with imperfect understanding.
- **Over-Prototyping:** If team builds too high-fidelity too early, remind them to start low-fi and only increase fidelity based on learning needs.
- **Confirmation Bias in Testing:** If team only sees what they want to see, encourage neutral observation and documenting negative feedback.

In all cases, maintain a creative and encouraging tone, emphasize the iterative nature of design thinking, and remind the team that failure in prototypes is learning, not wasted effort.
