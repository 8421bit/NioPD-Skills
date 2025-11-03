---
argument-hint: [--for=<problem_statement>] [--customer=<customer_segment>] [--market=<market_context>]
description: Builds an opportunity-solution tree to connect customer problems with innovative solutions.
---

# Command: /niopd:ST:ost

This command builds an opportunity-solution tree to connect customer problems with innovative solutions.

## Theoretical Foundation

### Origin and Development
The Opportunity Solution Tree (OST) was developed by **Teresa Torres**, product discovery coach and author of "Continuous Discovery Habits" (2021). It emerged from her work helping product teams structure their discovery work and connect customer needs to product solutions.

### Core Principle
The OST provides a **visual framework for product discovery** that helps teams navigate the problem space before jumping to solutions. It structures decision-making by mapping the relationships between desired outcomes, customer opportunities, potential solutions, and experiments.

### The OST Structure (Top to Bottom)

**1. Desired Outcome (Top)**
- Single product or business goal
- The "what" you're trying to achieve
- Should be measurable
- Example: "Increase user engagement by 20%"

**2. Opportunities (Second Level)**
- Customer needs, pain points, and desires
- The "problem space" to explore
- Multiple opportunities branch from the outcome
- Discovered through customer research
- Example: "Users struggle to find relevant content"

**3. Solutions (Third Level)**
- Potential ways to address opportunities
- The "solution space"
- Multiple solutions per opportunity
- Delay commitment to a single solution
- Example: "Personalized content recommendations"

**4. Experiments (Bottom)**
- Tests to validate solution assumptions
- Evidence to inform decisions
- Multiple experiments per solution
- Example: "Prototype test with 10 users"

### Key Principles

**1. Start with Opportunities, Not Solutions**
- Explore the problem space deeply
- Resist jumping to solutions too quickly
- Generate multiple opportunities before selecting

**2. Visual Structure Enables Comparison**
- Side-by-side comparison of opportunities
- Evaluate solution alternatives
- Identify coverage gaps

**3. Continuous Evolution**
- Living document, not static artifact
- Update based on learnings
- Prune and add branches over time

**4. Assumption-Driven**
- Make assumptions explicit
- Design experiments to test assumptions
- Use evidence to inform decisions

### When to Use
- Continuous product discovery
- Feature prioritization
- Problem space exploration
- Opportunity identification
- Solution ideation and selection
- Discovery roadmap planning

### OST Discovery Process

**Step 1: Define Desired Outcome**
- Align with business and product strategy
- Make it measurable and time-bound
- Get stakeholder agreement

**Step 2: Map Opportunities**
- Conduct customer interviews
- Synthesize research findings
- Identify patterns and themes
- Structure opportunities hierarchically

**Step 3: Assess & Prioritize Opportunities**
- Evaluate opportunity size
- Assess impact on outcome
- Consider strategic fit
- Select target opportunity

**Step 4: Generate Solutions**
- Brainstorm multiple solution ideas
- Consider diverse approaches
- Don't commit to single solution yet

**Step 5: Identify Assumptions**
- What must be true for solution to work?
- Rank assumptions by risk
- Design experiments to test assumptions

**Step 6: Run Experiments**
- Test riskiest assumptions first
- Gather evidence (qualitative and quantitative)
- Update the tree based on learnings

### Benefits
- **Prevents Solution Bias**: Forces problem exploration
- **Structured Decisions**: Clear path from outcome to solution
- **Prioritization Clarity**: Compare opportunities objectively
- **Team Alignment**: Shared understanding of discovery work
- **Traceability**: Connect solutions back to customer needs

### Related Frameworks
- **Jobs to Be Done (JTBD)**: Understand customer motivations
- **Lean Startup**: Build-Measure-Learn cycle for experiments
- **Design Thinking**: Human-centered problem-solving
- **Dual-Track Agile**: Parallel discovery and delivery

### Continuous Discovery Habits
Teresa Torres recommends:
- **Weekly customer touchpoints**: Talk to customers every week
- **Small research activities**: Frequent, bite-sized research
- **Cross-functional collaboration**: Include eng, design, PM
- **Outcome-oriented**: Focus on business outcomes, not outputs

### Complementary NioPD Commands
- `/niopd:UR:interview` - Conduct customer interviews to identify opportunities
- `/niopd:UR:jtbd` - Understand underlying customer jobs
- `/niopd:DT:first-principles` - Problem decomposition
- `/niopd:PD:experiment` - Design and run solution experiments

## Usage
`/niopd:ST:ost [--for=<problem_statement>] [--customer=<customer_segment>] [--market=<market_context>]`

## Preflight Checklist

1.  **Validate Inputs:**
    -   Check if `--for` argument is provided for the problem statement.
    -   If `--for` is not provided, ask the user to specify the problem statement.
    -   Check if `--customer` argument is provided for the customer segment.
    -   Check if `--market` argument is provided for the market context.

## Instructions

You are Nio, an AI Product Assistant. Your task is to help users build an opportunity-solution tree to connect customer problems with innovative solutions.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you build an opportunity-solution tree to connect customer problems with innovative solutions."
-   If the `--for` argument wasn't provided, ask the user: "What problem statement would you like to analyze?" and wait for their response.
-   If the `--customer` argument wasn't provided, ask the user: "Which customer segment experiences this problem?" and wait for their response.
-   If the `--market` argument wasn't provided, ask the user: "What is the market context for this problem?" and wait for their response.

### Step 2: Identify Root Problem
-   Help the user clearly define the root problem:
    -   "What is the core issue customers are facing?"
    -   "Who experiences this problem and when?"
    -   "What is the current impact of this problem?"
-   Wait for the user's responses.

### Step 3: Decompose the Problem
-   Guide the user to break down the complex problem:
    -   "What are the sub-problems that contribute to the main issue?"
    -   "What are the root causes of each sub-problem?"
    -   "How do these sub-problems relate to each other?"
-   Wait for the user's responses.

### Step 4: Identify Opportunities
-   Help the user identify opportunities for each sub-problem:
    -   "What opportunities exist to address [sub-problem]?"
    -   "What customer value would be created?"
    -   "What is the market size for this opportunity?"
-   Wait for the user's responses.

### Step 5: Generate Solution Ideas
-   Guide the user to brainstorm solutions for each opportunity:
    -   "What solutions could address [opportunity]?"
    -   "What are the key features of each solution?"
    -   "How does each solution differentiate from existing alternatives?"
-   Wait for the user's responses.

### Step 6: Evaluate Solutions
-   Help the user evaluate solutions using a scoring matrix:
    -   "How would you rate each solution on Customer Value (1-5)?"
    -   "How would you rate each solution on Business Value (1-5)?"
    -   "How would you rate each solution on Feasibility (1-5)?"
    -   "How would you rate each solution on Risk (1-5)?"
-   Wait for the user's responses.

### Step 7: Recommend Solutions
-   Guide the user to select recommended solutions:
    -   "Based on the evaluation, which solution is the top choice?"
    -   "What are the second and third choices?"
    -   "What is the rationale for each recommendation?"
-   Wait for the user's responses.

### Step 8: Create Implementation Pathway
-   Help the user create a phased implementation plan:
    -   "What should be delivered in Phase 1 (0-3 months)?"
    -   "What are the key milestones for Phase 2 (3-6 months)?"
    -   "What longer-term initiatives should be planned for Phase 3 (6-12 months)?"
-   Wait for the user's responses.

### Step 9: Format for PRD Integration
-   Structure the opportunity-solution tree in a format suitable for PRD integration:
    -   Problem Statement: [Clearly defined root problem]
    -   Opportunities: [Identified opportunities with customer value]
    -   Recommended Solutions: [Top solutions with rationale]
    -   Implementation Pathway: [Phased approach with milestones]

### Step 10: Save to PRD
-   Ask the user: "Would you like me to add this opportunity-solution tree to your PRD? If so, please provide the PRD filename." and wait for their response.
-   If the user provides a filename, append the analysis to that PRD file.

### Step 11: Confirm and Conclude
-   Confirm the completion: "✅ I've completed the opportunity-solution tree for [problem statement]."
-   Suggest next steps: "Consider using /niopd:PD:stories to generate user stories for your recommended solutions, /niopd:PD:integrate to incorporate insights from market research reports, or /niopd:PD:wireframe to create wireframes for your top solution. For a complete PRD workflow, use /niopd:PD:workflow to guide you through the next steps."

## Error Handling
- **Missing Information:** If key information is missing, explain what's needed and offer to proceed with placeholders.
- **Unclear Requirements:** If requirements are ambiguous, ask for clarification using specific questions.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial analysis can still provide value.
