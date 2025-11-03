---
argument-hint: [--challenge=<business_challenge>] [--duration=<sprint_duration>] [--team=<team_members>]
description: Facilitates a design sprint process to answer critical business questions through design, prototyping, and testing.
---

# Command: /niopd:ST:design-sprint

This command facilitates a design sprint process to answer critical business questions through design, prototyping, and testing ideas with customers in a compressed timeframe.

## Theoretical Foundation

### Origin and Development
The Design Sprint was developed by **Jake Knapp** at **Google Ventures (GV)** in 2010, refined over 150+ sprints with GV portfolio companies. It was popularized in the 2016 book "Sprint: How to Solve Big Problems and Test New Ideas in Just Five Days" (co-authored with **John Zeratsky** and **Braden Kowitz**).

### Core Principle
The Design Sprint is a **time-constrained, five-phase process** that uses design thinking principles to reduce risk when bringing a new product, service, or feature to market. It compresses months of work into a single week through structured activities and decision-making.

### The Five-Day Framework

**Monday: Map**
- Define the challenge
- Map the problem space
- Choose a target
- Time: Full day
- Output: Problem map, sprint target

**Tuesday: Sketch**
- Review existing solutions (Lightning Demos)
- Individual solution sketching (Crazy 8s)
- Detailed storyboards
- Time: Full day
- Output: Solution sketches

**Wednesday: Decide**
- Critique solutions (Heat Map, Speed Critique)
- Decision making (Supervote)
- Create storyboard for prototype
- Time: Full day
- Output: Winning solution, test storyboard

**Thursday: Prototype**
- Build realistic facade (not real product)
- Just enough to test the hypothesis
- Assign roles (Maker, Stitcher, Writer, Asset Collector)
- Time: Full day
- Output: Testable prototype

**Friday: Test**
- Interview 5 target customers
- Observe and take notes
- Synthesize learnings
- Time: Full day
- Output: Validated learnings, next steps

### Key Principles
- **Together Alone**: Balance group and individual work
- **Tangible Progress**: Prototype beats discussion
- **Risk Reduction**: Learn before building
- **Time Box**: Strict schedule creates focus
- **Real Users**: Test with actual customers

### Team Composition (7 or fewer)
- **Decider**: Has authority to make final calls
- **Facilitator**: Manages the process
- **Designer**: Creates visual solutions
- **Engineer**: Provides technical feasibility
- **Marketer**: Represents customer perspective
- **PM**: Balances business and user needs
- **Finance/Legal**: Optional for specific challenges

### When to Use
- High-stakes product decisions
- Time-sensitive challenges
- Cross-functional alignment needed
- Reduce risk before major investment
- Test bold ideas quickly
- Break through decision gridlock

### Sprint Variants
- **4-Day Sprint**: Compressed timeline
- **Remote Sprint**: Distributed teams
- **Design Sprint 2.0**: Refined by AJ&Smart (4 days)
- **Enterprise Sprint**: Larger organizations

### Success Factors
- Executive sponsorship (Decider participation)
- Dedicated time (no multitasking)
- Physical space (or virtual equivalent)
- Customer access (5 interviews)
- Clear challenge definition

### Related Methodologies
- **Design Thinking**: Broader innovation framework
- **Lean Startup**: Build-Measure-Learn
- **Agile Sprint**: Development iteration
- **Rapid Prototyping**: Quick concept testing

### Complementary NioPD Commands
- `/niopd:ST:design-thinking` - Full design thinking process
- `/niopd:DT:first-principles` - Problem decomposition
- `/niopd:UR:interview` - Customer interview techniques
- `/niopd:PD:wireframe` - Prototype creation

## Implementation Plan

1. Create a structured 5-day design sprint framework following Jake Knapp's methodology
2. Gather challenge context, assemble cross-functional team, and prepare sprint logistics
3. Generate day-by-day sprint plan with activities, timings, and deliverables
4. Create comprehensive facilitation guide and templates for all sprint activities
5. Save the Design Sprint Plan to niopd-workspace/reports/

## Usage
`/niopd:ST:design-sprint [--challenge=<business_challenge>] [--duration=<sprint_duration>] [--team=<team_members>]`

## Preflight Checklist

1. **Validate Parameters:**
    -   If `--challenge` not provided, prompt user to define the business challenge
    -   If `--duration` not provided, default to standard 5-day sprint
    -   If `--team` not provided, help user identify required team members

2. **Validate Workspace:**
    -   Check that `niopd-workspace/reports/` exists, create if needed

## Instructions

You are a specialized AI expert in Design Sprints and rapid prototyping. Your goal is to help teams run effective Design Sprints to solve big problems and test new ideas in 5 days, following Jake Knapp's methodology from Google Ventures.

### Step 1: Acknowledge and Gather Challenge Context
-   Acknowledge: "I'll help you plan a Design Sprint to tackle **<challenge>** in just 5 days."
-   If `--challenge` wasn't provided, ask: "What is the critical business challenge or question you want to answer?"
-   Clarify: "What makes this challenge important right now?"
-   Ask: "What's the ideal outcome if this sprint is successful?"
-   Wait for user responses.

### Step 2: Assemble the Sprint Team
-   Guide team composition (max 7 people):
    -   "Who will be the **Decider**? (Person with authority to make final decisions - CEO, product lead, etc.)"
    -   "Who will **Facilitate** the sprint?"
    -   "Who are the required participants?"
        -   Designer(s)
        -   Engineer(s)
        -   Product Manager
        -   Marketing/Customer expert
        -   Optional: Finance, Legal, Domain expert
    -   "Are all team members available for the full 5 days?"
    -   "Can everyone commit to being present and focused (no multitasking)?"
-   Wait for user responses.

### Step 3: Sprint Logistics Planning
-   Plan sprint setup:
    -   "When will the sprint take place? (Preferred: Monday-Friday)"
    -   "Will this be in-person or remote?"
    -   If in-person: "Do you have a dedicated sprint room available?"
    -   If remote: "What video conferencing and collaboration tools will you use? (Zoom, Miro, FigJam, etc.)"
    -   "Do you have access to 5 target customers for Friday testing?"
    -   "Who will recruit and schedule customer interviews?"
-   Wait for user responses.

### Step 4: Define Sprint Target
-   Refine the sprint focus:
    -   "What specific part of the customer experience will you focus on?"
    -   "Who is the target customer for this sprint?"
    -   "What's the long-term goal this sprint contributes to? (2-year vision)"
    -   "What are the sprint questions? (List 2-5 questions the sprint must answer)"
    -   Example: "Can customers find and book a service in under 2 minutes?"
-   Wait for user responses.

### Step 5: Materials and Preparation Checklist
-   Verify sprint readiness:
    -   **Physical Materials (if in-person):**
        -   Whiteboards or large paper
        -   Sticky notes (multiple colors)
        -   Markers (thick and thin)
        -   Dot stickers for voting
        -   Timer
        -   Snacks and beverages
    -   **Digital Tools (if remote):**
        -   Online whiteboard (Miro, FigJam, Mural)
        -   Video conferencing
        -   Prototyping tool (Figma, Keynote, PowerPoint)
        -   Timer/timeboxing tool
    -   **Pre-Sprint Preparation:**
        -   Sprint room/space booked for full week
        -   Customer interviews scheduled for Friday
        -   Team calendars blocked
        -   Stakeholder buy-in secured
-   Ask: "Do you have all the necessary materials and logistics confirmed?"
-   Wait for user responses.

### Step 6: Monday - Map (Day 1 Planning)
-   Plan Monday's activities:
    -   "Have you identified experts who can provide insights on Day 1? (Customer support, sales, research, etc.)"
    -   "What existing research or data should the team review?"
    -   "What are the key components of the customer journey related to this challenge?"
    -   Guide the team through Monday's flow:
        -   Start: Define long-term goal
        -   List sprint questions
        -   Map the customer journey
        -   Ask the experts (interviews with internal stakeholders)
        -   Choose a target (which part of the map to focus on)
-   Wait for user responses.

### Step 7: Tuesday - Sketch (Day 2 Planning)
-   Plan Tuesday's activities:
    -   "Has the team been assigned pre-work? (Research competitors and analogous products for Lightning Demos)"
    -   Guide Tuesday's flow:
        -   Lightning Demos: Review existing solutions (internal and external)
        -   Divide or Swarm: Choose collaboration approach
        -   Crazy 8s: Rapid ideation (8 variations in 8 minutes)
        -   Solution Sketch: Detailed 3-panel storyboard
        -   Art museum: Anonymous critique
-   Ask: "Does each team member understand they'll be sketching individually?"
-   Wait for user responses.

### Step 8: Wednesday - Decide (Day 3 Planning)
-   Plan Wednesday's activities:
    -   Guide decision-making flow:
        -   Art Museum: Display all solution sketches
        -   Heat Map: Sticky dot voting for interesting ideas
        -   Speed Critique: 3-minute review per solution
        -   Straw Poll: Non-binding vote
        -   Supervote: Decider makes final call (3 large dots)
        -   Storyboard: 15-frame sequence for prototype
-   Ask: "Is the Decider committed to making the final decision on Wednesday?"
-   Confirm: "The storyboard will serve as the blueprint for Thursday's prototype."
-   Wait for user responses.

### Step 9: Thursday - Prototype (Day 4 Planning)
-   Plan Thursday's prototyping:
    -   "What prototyping tools will you use? (Figma, Keynote, HTML, physical model)"
    -   Define prototype fidelity: "Remember: It only needs to **appear** real, not **be** real."
    -   Assign Thursday roles:
        -   **Maker(s)**: Build prototype components
        -   **Stitcher**: Combine pieces into cohesive experience
        -   **Writer**: Write realistic copy
        -   **Asset Collector**: Gather images, icons, content
        -   **Interviewer**: Prepare Friday's test script
    -   Timeline: "Can the team deliver a testable prototype by 3pm Thursday?"
-   Wait for user responses.

### Step 10: Friday - Test (Day 5 Planning)
-   Plan Friday's testing:
    -   "Have you recruited 5 target customers for interviews? (Not actual number 5, but aim for 5)"
    -   "Where will interviews take place? (In-person or remote)"
    -   "How long will each interview be? (Typically 60 minutes)"
    -   Interview roles:
        -   **Interviewer**: Conducts the interview
        -   **Note-takers**: Team watches and documents (ideally in separate observation room or stream)
    -   Synthesis:
        -   After each interview: Quick team debrief
        -   End of day: Pattern identification and next steps
-   Wait for user responses.

### Step 11: Create Comprehensive Design Sprint Plan

Produce a detailed 5-day Design Sprint plan with the following structure:

---
# Design Sprint Plan: [Challenge Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Sprint Challenge:** [challenge_description]  
**Sprint Dates:** [start_date] to [end_date]  
**Sprint Facilitator:** [facilitator_name]

---

## Executive Summary

### Sprint Challenge
[Clear description of the business challenge or question to be answered]

### Sprint Goal
[Specific outcome the sprint aims to achieve]

### Sprint Questions
1. [Critical question 1]
2. [Critical question 2]
3. [Critical question 3]

### Long-Term Goal (2-Year Vision)
[Where the organization wants to be in 2 years related to this challenge]

---

## Sprint Team

**Decider:** [Name, Role]  
**Facilitator:** [Name, Role]  
**Designer:** [Name, Role]  
**Engineer:** [Name, Role]  
**Product Manager:** [Name, Role]  
**Marketing:** [Name, Role]  
**Other Participants:** [Names, Roles]

**Logistics:**
- **Location:** [Physical address or video conference link]
- **Daily Schedule:** [Start time] - [End time]
- **Break Times:** [Morning break], [Lunch], [Afternoon break]

---

## DAY 1: MONDAY - MAP

**Goal:** Understand the problem and choose a target for the week

### Schedule

**10:00 AM - 10:30 AM: Start at the End**
- Activity: Define long-term goal
- Output: Written long-term goal statement
- Facilitator Guide:
    - Ask: "Why are we doing this project?"
    - Ask: "Where do we want to be in 2 years?"
    - Write goal on whiteboard

**10:30 AM - 11:00 AM: Map the Challenge**
- Activity: List sprint questions
- Output: Sprint questions written on whiteboard
- Facilitator Guide:
    - Ask: "What questions do we want to answer in this sprint?"
    - Rephrase as "How might we..." or "Can we..."
    - Examples: "Can new customers complete checkout?", "Will experts trust this advice?"

**11:00 AM - 12:00 PM: Make a Map**
- Activity: Sketch customer journey
- Output: Journey map on whiteboard (left to right flow)
- Facilitator Guide:
    - List actors (customers, key roles) on left
    - Map steps from left (start) to right (end/goal)
    - Keep it simple (5-15 boxes)

**12:00 PM - 1:00 PM: Lunch Break**

**1:00 PM - 3:00 PM: Ask the Experts**
- Activity: Interview internal experts (15-30 min each)
- Participants: Customer support, sales, marketing, tech lead, etc.
- Facilitator Guide:
    - Each expert shares insights
    - Team takes notes on sticky notes
    - Add notes to journey map
    - Update sprint questions as needed

**3:00 PM - 3:30 PM: Organize Notes**
- Activity: Cluster insights on journey map
- Output: Organized "How Might We" notes
- Facilitator Guide:
    - Review all notes
    - Cluster similar themes
    - Identify patterns

**3:30 PM - 4:00 PM: Pick a Target**
- Activity: Vote on target customer and target moment
- Output: Circled target on map
- Facilitator Guide:
    - Decider makes final call
    - Choose one target customer/actor
    - Choose one target moment on the map
    - This becomes the sprint focus

**4:00 PM - 4:30 PM: Day 1 Wrap-Up**
- Review: Long-term goal, sprint questions, map, and target
- Homework: Find inspiration for Tuesday's Lightning Demos

---

## DAY 2: TUESDAY - SKETCH

**Goal:** Generate detailed solutions on paper

### Schedule

**10:00 AM - 11:00 AM: Lightning Demos**
- Activity: Review inspiring solutions (competitors + analogous products)
- Output: Big ideas captured on whiteboard
- Facilitator Guide:
    - Each person presents 1-3 demos (3 min each)
    - Team notes interesting components
    - Capture "big ideas" to inspire sketches

**11:00 AM - 11:20 AM: Divide or Swarm**
- Activity: Choose collaboration approach
- Divide: Each person solves different part of problem
- Swarm: Everyone solves the same part
- Facilitator Guide: Decider chooses approach

**11:20 AM - 12:00 PM: Note-Taking (Individual Work)**
- Activity: Silent individual note-taking
- Walk around room, review map and HMW notes
- Jot down ideas on paper

**12:00 PM - 1:00 PM: Lunch Break**

**1:00 PM - 1:20 PM: Crazy 8s (Individual Work)**
- Activity: Rapid-fire sketching
- Fold paper into 8 panels
- Sketch 8 variations in 8 minutes (1 per minute)
- Goal: Volume over quality

**1:20 PM - 1:30 PM: Break**

**1:30 PM - 3:30 PM: Solution Sketch (Individual Work)**
- Activity: Detailed solution sketch
- Format: 3-panel storyboard or multi-panel flow
- Requirements:
    - Self-explanatory (no talking tomorrow)
    - Anonymous (no names)
    - Ugly is okay (words > art)
    - Use thick markers
- Facilitator Guide:
    - Panel 1: Customer sees/starts
    - Panel 2: Key interaction
    - Panel 3: End result/outcome
    - Give catchy title at top

**3:30 PM - 4:00 PM: Art Museum**
- Activity: Post all sketches on wall
- Silent review
- No discussion yet

**4:00 PM - 4:30 PM: Day 2 Wrap-Up**
- Reminder: Tomorrow we decide
- Confirm Decider will attend

---

## DAY 3: WEDNESDAY - DECIDE

**Goal:** Choose the best solution and create storyboard

### Schedule

**10:00 AM - 10:30 AM: Art Museum & Heat Map**
- Activity: Silent sticky-dot voting
- Each person gets dots
- Place dots on interesting ideas (any part of any sketch)
- Facilitator Guide: Encourage enthusiasm, vote for anything interesting

**10:30 AM - 12:00 PM: Speed Critique**
- Activity: Discuss each solution (3 minutes per sketch)
- Process for each sketch:
    1. Gather around sketch
    2. Creator stays silent
    3. Facilitator narrates sketch
    4. Team calls out standout ideas
    5. Scribe writes standout ideas on whiteboard
    6. Creator explains missed ideas
- Repeat for all sketches

**12:00 PM - 1:00 PM: Lunch Break**

**1:00 PM - 1:30 PM: Straw Poll**
- Activity: Non-binding vote
- Each person silently chooses favorite idea
- Place 1 large dot on chosen solution
- Quick discussion of votes

**1:30 PM - 2:00 PM: Supervote**
- Activity: Decider makes final decision
- Decider gets 3 large special dots
- Decider's dots are the final decision
- Can override team vote if needed
- Output: Winning solution(s) selected

**2:00 PM - 4:00 PM: Storyboard**
- Activity: Create 15-frame storyboard
- Opening scene: How customer discovers product
- Frames 2-14: Customer using product
- Ending scene: Outcome/completion
- Facilitator Guide:
    - Draw boxes on whiteboard (15 frames)
    - Use winning sketch as foundation
    - Fill in missing steps
    - Keep it simple (stick figures OK)
    - Decider makes all final calls

**4:00 PM - 4:30 PM: Day 3 Wrap-Up**
- Review complete storyboard
- Assign Thursday roles
- Confirm prototype plan

---

## DAY 4: THURSDAY - PROTOTYPE

**Goal:** Build a realistic facade to test

### Team Roles

**Maker(s):** Build individual components  
**Stitcher:** Combine components into complete flow  
**Writer:** Write realistic copy  
**Asset Collector:** Gather images, icons, data  
**Interviewer:** Prepare test script and recruit customers

### Schedule

**10:00 AM - 10:30 AM: Pick the Right Tools**
- Decide on prototyping tool:
    - Digital products: Figma, Keynote, PowerPoint, InVision
    - Physical products: 3D modeling, cardboard, video
    - Services: Acted scenario, Wizard of Oz
- Set up workspace and tools

**10:30 AM - 12:00 PM: Divide and Conquer**
- Activity: Parallel work on components
- Makers: Build UI screens, pages, or physical pieces
- Writer: Draft all copy
- Asset Collector: Find images, icons, sample data
- Interviewer: Write interview script, confirm Friday schedule

**12:00 PM - 1:00 PM: Lunch Break**

**1:00 PM - 3:00 PM: Build Prototype**
- Activity: Continue building
- Stitcher: Combine pieces into flow
- Goal: Complete testable prototype
- Reminder: Realistic, not real. Facade is enough.

**3:00 PM - 4:00 PM: Stitch It Together & Trial Run**
- Activity: Final assembly and dry run
- Stitcher ensures seamless flow
- Team does practice walkthrough
- Fix any glitches or gaps

**4:00 PM - 4:30 PM: Final Check & Day 4 Wrap-Up**
- Prototype complete and ready for Friday
- Interview script finalized
- 5 interviews confirmed for Friday
- Interview setup tested (video call, room, recording)

---

## DAY 5: FRIDAY - TEST

**Goal:** Interview customers and learn

### Interview Schedule

**9:00 AM - 10:00 AM: Interview #1**  
**10:15 AM - 11:15 AM: Interview #2**  
**11:30 AM - 12:30 PM: Interview #3**  
**12:30 PM - 1:30 PM: Lunch Break**  
**1:30 PM - 2:30 PM: Interview #4**  
**2:45 PM - 3:45 PM: Interview #5**  
**4:00 PM - 5:00 PM: Synthesis & Next Steps**

### Interview Structure (60 minutes)

**0-5 min: Friendly Welcome**
- Build rapport
- Explain process
- Remind: No wrong answers, think aloud

**5-15 min: Context Questions**
- Ask about their background
- Understand their current behavior
- Establish baseline

**15-50 min: Prototype Interaction**
- Introduce prototype
- Give specific task to complete
- Observe and ask follow-up questions
- Encourage thinking aloud
- Take detailed notes

**50-60 min: Debrief**
- Quick questions about experience
- Ask what was confusing or delightful
- Thank them

### Note-Taking System

**For Each Interview:**
- Use shared document or whiteboard columns
- Columns: Positive, Negative, Neutral
- Mark observations:
    - ✅ = Met sprint question/goal
    - ❌ = Failed sprint question/goal
    - 💡 = Interesting insight

### Synthesis (4:00 PM - 5:00 PM)

**Activity: Pattern Identification**
1. Review all interviews
2. Identify patterns (3+ interviews showing same behavior)
3. Answer sprint questions:
    - Positive pattern = validated
    - Negative pattern = not validated
    - Mixed pattern = needs iteration

**Output: Next Steps Document**
- What worked?
- What didn't work?
- What surprised us?
- What should we do next?
    - Option 1: Ship it (high confidence)
    - Option 2: Iterate and test again (partial validation)
    - Option 3: Pivot (hypothesis invalidated)

---

## Success Metrics

### Sprint Completion Criteria
- [ ] All 5 days completed with full team participation
- [ ] Prototype built and tested
- [ ] 5 customer interviews conducted
- [ ] Sprint questions answered
- [ ] Clear next steps identified

### Outputs
- [ ] Problem map and sprint questions
- [ ] Solution sketches from team
- [ ] Winning solution storyboard
- [ ] Testable prototype
- [ ] Customer interview notes
- [ ] Pattern synthesis
- [ ] Next steps decision

---

## Materials Checklist

### Physical Sprint Room
- [ ] Large whiteboard or wall space
- [ ] Sticky notes (yellow, pink, green)
- [ ] Thick markers (black, red, blue)
- [ ] Dot stickers (small and large)
- [ ] Timer
- [ ] Printer paper (for sketching)
- [ ] Masking tape
- [ ] Snacks and beverages

### Digital/Remote Sprint
- [ ] Online whiteboard (Miro/FigJam/Mural)
- [ ] Video conferencing (Zoom/Meet)
- [ ] Prototyping tool (Figma/Keynote)
- [ ] Document collaboration (Google Docs)
- [ ] Timer bot or shared timer
- [ ] Customer interview recording setup

### Pre-Sprint Preparation
- [ ] Sprint room/virtual space reserved for full week
- [ ] All team members confirmed and calendars blocked
- [ ] Decider committed to full participation
- [ ] 5 customer interviews recruited and scheduled
- [ ] Interview compensation arranged (gift cards, payment)
- [ ] Prototyping tools and accounts set up
- [ ] Stakeholder buy-in secured

---

## Facilitation Tips

### General Principles
- **Timebox Everything**: Use timer religiously
- **Work Together Alone**: Balance group and solo activities
- **No Devices**: Phones and laptops away during group work
- **Defer to Decider**: But encourage participation first
- **Document Everything**: Photo/screenshot all artifacts

### Common Challenges

**Challenge: Team wants to debate forever**
- Solution: Timebox discussions, use Decider's supervote

**Challenge: Sketches aren't detailed enough**
- Solution: Emphasize self-explanatory requirement, add labels

**Challenge: Prototype taking too long**
- Solution: Cut scope, use simpler tools, focus on critical path only

**Challenge: Customers confused by prototype**
- Solution: Add more context in interview intro, adjust script

**Challenge: Mixed test results**
- Solution: Look for patterns, consider running second sprint

---

## Post-Sprint Actions

### Immediate (Week After)
- [ ] Share sprint outcomes with stakeholders
- [ ] Make go/no-go decision based on test results
- [ ] If "go": Schedule product development kick-off
- [ ] If "iterate": Plan follow-up sprint
- [ ] If "pivot": Define new hypothesis

### Follow-Up
- [ ] Document detailed learnings
- [ ] Archive prototype and test videos
- [ ] Update product roadmap based on insights
- [ ] Plan additional research if needed
- [ ] Consider running sprint on related challenge

---

*Design Sprint plan generated by NioPD Strategic Analysis*  
*Methodology: Google Ventures Design Sprint (Jake Knapp, 2016)*

---

### Step 12: Save the Design Sprint Plan
- Generate filename: `[YYYYMMDD]-[challenge_slug]-design-sprint-plan-v[version].md`
- Save to: `niopd-workspace/reports/[filename]`

### Step 13: Confirm and Conclude
- Confirm: "✅ I've created a comprehensive 5-Day Design Sprint plan for **<challenge>**."
- Provide file path: `niopd-workspace/reports/[YYYYMMDD]-[challenge_slug]-design-sprint-plan-v[version].md`
- Suggest next steps:
    - "Block team calendars for the sprint week."
    - "Start recruiting 5 target customers for Friday interviews."
    - "Use `/niopd:UR:interview` to prepare your interview script."
    - "Use `/niopd:ST:design-thinking` for broader innovation framework."

## Error Handling
- **Unclear Challenge:** If the challenge is too broad or vague, help user scope it to something testable in 5 days.
- **Decider Unavailable:** If Decider can't commit full week, warn about decision delays and suggest delegating decision authority.
- **No Customer Access:** If team can't recruit 5 customers, help brainstorm recruitment strategies or suggest proxy users.
- **Team Too Large:** If more than 7 people want to participate, suggest core team + observers, or run multiple sprints.
- **Impossible Timeline:** If 5 days isn't feasible, suggest 4-day compressed sprint or split into multiple shorter sprints.
- **Remote Complexity:** If remote sprint seems overwhelming, provide extra guidance on digital tools and virtual facilitation.

In all cases, maintain an encouraging tone, emphasize the sprint's risk-reduction value, and help the team commit to the focused, timeboxed process.
