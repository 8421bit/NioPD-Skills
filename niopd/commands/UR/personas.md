---
argument-hint: --from=<feedback_summary>
description: Generates user personas from a feedback summary report.
---

# Command: /niopd:UR:personas

This command generates a set of user personas based on a feedback summary report.

## Theoretical Foundation

### Origin and Development
Persona development originated from:

1. **Goal-Directed Design** - **Alan Cooper** introduced personas in "The Inmates Are Running the Asylum" (1999)
2. **User-Centered Design** - Focus on understanding and designing for specific user types
3. **Empathy Mapping** - Visual tool for understanding user perspectives

### Core Principle
Personas are **archetypal representations of actual users** based on research data, not assumptions. They help teams build empathy and make user-focused decisions by creating vivid, realistic characters that represent key user segments.

### Key Persona Elements
1. **Demographics**: Age, occupation, location, education
2. **Psychographics**: Values, attitudes, motivations, personality
3. **Behaviors**: Usage patterns, workflows, preferences
4. **Goals**: What they want to accomplish
5. **Pain Points**: Frustrations and challenges
6. **Needs**: Requirements and desired outcomes

### Persona Types
- **Primary Personas**: Main target users (2-3 personas)
- **Secondary Personas**: Additional important segments
- **Negative Personas**: Who you're NOT building for
- **Provisional Personas**: Assumption-based (to be validated)

### When to Use
- After gathering substantial user research data
- Starting new product initiatives
- Aligning teams on target users
- Prioritizing features and design decisions
- Creating user-centered documentation

### Benefits
- **Empathy Building**: Humanizes data and statistics
- **Decision Making**: Provides clear user reference for choices
- **Communication**: Shared language about users across teams
- **Focus**: Prevents designing for everyone (and no one)

### Related Methodologies
- **Jobs to Be Done**: Complementary user understanding framework
- **Customer Journey Mapping**: Understanding persona experiences over time
- **Empathy Mapping**: Says-Thinks-Does-Feels framework
- **Proto-Personas**: Quick assumption-based personas for validation

## Usage
`/niopd:UR:personas --from=<feedback_summary>`

## Preflight Checklist

1.  **Validate File:**
    -   Ensure the user has provided a `--from` file.
    -   Check that the file exists in the `niopd-workspace/reports/` directory. If not, inform the user.

## Instructions

You are a specialized AI expert in user research and product marketing. Your goal is to transform analytical feedback summaries into vivid, actionable user personas that guide product decisions.

### Step 1: Acknowledge and Prepare
-   Acknowledge the request: "This is a great way to build empathy! I'll create some user personas based on the feedback in `[YYYYMMDD]-[initiative_slug]-feedback-summary-v[version].md`."

### Step 2: Feedback Summary Analysis
- Read and analyze the provided feedback summary file.
- Identify key themes, pain points, feature requests, and user behaviors.
- Extract demographic information and user characteristics.
- Note emotional language and sentiment indicators.

### Step 3: Persona Identification & Clustering
- Group similar user characteristics and behaviors into distinct archetypes.
- Identify 2-4 primary personas that represent key user segments.
- Ensure each persona has a unique value proposition and set of needs.
- Validate that personas are distinct and not overlapping.

### Step 4: Persona Detail Development
- For each persona, develop detailed demographic and psychographic profiles.
- Create descriptive names and background stories that reflect their characteristics.
- Define their roles, experience levels, and technical proficiencies.
- Identify their core values, motivations, and decision-making styles.

### Step 5: Empathy Map Creation
- For each persona, create a comprehensive empathy map with Says, Thinks, Does, and Feels sections.
- Extract representative quotes that demonstrate their perspectives.
- Identify emotional triggers and pain points.
- Capture their goals and aspirations.

### Step 6: Behavioral Pattern Analysis
- Identify typical daily routines and workflows for each persona.
- Analyze their product usage patterns and preferences.
- Understand their decision journey and evaluation criteria.
- Note their preferred devices, platforms, and interaction methods.

### Step 7: Goal & Need Identification
- Define primary and secondary goals for each persona.
- Identify explicit and implicit needs.
- Categorize pain points and frustrations.
- Note aspirational goals and long-term objectives.

### Step 8: Scenario Development
- Create success and challenge scenarios for each persona.
- Develop detailed narratives that illustrate how they interact with the product.
- Identify key touchpoints and moments of truth.
- Highlight potential obstacles and how they might overcome them.

### Step 9: Product Implication Analysis
- Analyze how each persona's needs should influence product design.
- Identify feature priorities and requirements for each persona.
- Determine appropriate communication approaches and messaging.
- Note support needs and documentation preferences.

### Step 10: Quote Selection & Validation
- Select powerful, representative quotes that show each persona's perspective.
- Ensure quotes authentically represent the persona's voice and perspective.
- Use quotes to validate and support persona characteristics.
- Preserve original language to maintain authenticity.

### Step 11: Create Comprehensive User Personas Document

Generate a detailed user persona document with the following comprehensive structure:

---
# User Personas: [Initiative/Product Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Based on Research:** [Source documents - e.g., Feedback Summary, Interview Notes]  
**Research Date Range:** [Start date] - [End date]  
**Number of Research Participants:** [Count]

---

## Executive Summary

**Primary Personas Identified:** [Number] 

**Key Insights:**
- [Major insight 1 about user needs]
- [Major insight 2 about pain points]
- [Major insight 3 about opportunities]

**Design Implications:**
- [How personas should influence product direction]
- [Critical features for primary personas]
- [Communication and support strategies]

---

## Persona 1: [Name - First and Last]

### Quick Profile

![Photo placeholder - Describe: Age, appearance, professional setting]

**Age:** [Age or age range]  
**Location:** [City, Country or region]  
**Occupation:** [Job title and industry]  
**Income:** [Income range if relevant]  
**Education:** [Level and field]  
**Family Status:** [Relevant family context]

**Quote:** *"[A representative quote that captures their perspective]"*

---

### Background Story

[2-3 paragraph narrative describing this persona's background, daily life, career journey, and how they came to need your product]

Example:
> [Name] works as a [occupation] at [type of company]. They've been in their role for [timeframe] and are responsible for [key responsibilities]. On a typical day, they [describe typical workflow]. They discovered your product/service when [discovery story]. 

---

### Demographics & Characteristics

**Professional:**
- **Role:** [Job title]
- **Experience Level:** [Entry / Mid / Senior / Expert]
- **Industry:** [Industry sector]
- **Company Size:** [Startup / SMB / Mid-market / Enterprise]
- **Team Size:** [Number of reports/team members]
- **Technical Proficiency:** [Low / Medium / High]

**Psychographics:**
- **Values:** [What matters most to them]
- **Personality Traits:** [Key characteristics]
- **Decision Style:** [Analytical / Intuitive / Collaborative / Quick]
- **Risk Tolerance:** [Conservative / Moderate / Adventurous]
- **Communication Preference:** [Email / Phone / Chat / Video]

---

### Goals & Motivations

**Primary Goals:**
1. **[Goal 1]:** [Description of what they want to achieve]
   - Success metric: [How they measure success]
   - Timeframe: [When they need it]

2. **[Goal 2]:** [Description]
   - Success metric: [Measurement]
   - Timeframe: [When]

3. **[Goal 3]:** [Description]
   - Success metric: [Measurement]
   - Timeframe: [When]

**Secondary Goals:**
- [Additional goal 1]
- [Additional goal 2]

**Motivations:**
- **Career:** [Career-related motivations]
- **Personal:** [Personal achievement motivations]
- **Team/Organization:** [Organizational motivations]

---

### Pain Points & Frustrations

**Critical Pain Points:**

1. **[Pain Point 1 - Title]**
   - **Description:** [Detailed description]
   - **Impact:** [How it affects their work/life]
   - **Current Workaround:** [How they currently deal with it]
   - **Severity:** High / Medium / Low

2. **[Pain Point 2 - Title]**
   - **Description:** [Detailed description]
   - **Impact:** [How it affects their work/life]
   - **Current Workaround:** [How they currently deal with it]
   - **Severity:** High / Medium / Low

3. **[Pain Point 3 - Title]**
   - **Description:** [Detailed description]
   - **Impact:** [How it affects their work/life]
   - **Current Workaround:** [How they currently deal with it]
   - **Severity:** High / Medium / Low

**Frustrations:**
- [Specific frustration with current tools/processes]
- [Specific frustration with alternatives]
- [Specific frustration with workflow]

---

### Empathy Map

**SAYS** (What they say out loud):
- *"[Quote 1 from research]"*
- *"[Quote 2 from research]"*
- *"[Quote 3 from research]"*

**THINKS** (What they're thinking):
- [Internal thought 1 - worries, aspirations]
- [Internal thought 2 - concerns]
- [Internal thought 3 - hopes]

**DOES** (Observable behaviors):
- [Behavior 1 - daily routines]
- [Behavior 2 - work habits]
- [Behavior 3 - problem-solving approach]

**FEELS** (Emotional states):
- [Emotion 1 - when things go well]
- [Emotion 2 - when facing challenges]
- [Emotion 3 - about current solutions]

---

### Behaviors & Patterns

**Daily Workflow:**

```
08:00 - [Morning routine]
09:00 - [Key morning activities]
12:00 - [Midday activities]
15:00 - [Afternoon focus]
18:00 - [End of day routine]
```

**Product Usage Patterns:**
- **Frequency:** [Daily / Weekly / Monthly]
- **Duration:** [Typical session length]
- **Primary Use Cases:** [Top 3 use cases]
- **Devices:** [Desktop / Mobile / Tablet preferences]
- **Time of Day:** [When they're most active]

**Decision-Making Journey:**
1. **Awareness:** [How they discover solutions]
2. **Consideration:** [How they evaluate options]
3. **Decision:** [What drives final choice]
4. **Adoption:** [How they onboard]
5. **Advocacy:** [When they recommend to others]

**Information Preferences:**
- **Learning Style:** [Visual / Textual / Hands-on / Video]
- **Content Preferences:** [Tutorials / Documentation / Examples / Live support]
- **Research Approach:** [Thorough / Quick / Peer-driven / Expert-driven]

---

### Needs & Requirements

**Must-Have Features:**
1. [Essential feature 1] - [Why it's critical]
2. [Essential feature 2] - [Why it's critical]
3. [Essential feature 3] - [Why it's critical]

**Nice-to-Have Features:**
1. [Desired feature 1] - [Value it would add]
2. [Desired feature 2] - [Value it would add]
3. [Desired feature 3] - [Value it would add]

**Deal-Breakers:**
- [What would cause them to reject the product]
- [What would cause them to churn]
- [What would prevent recommendation]

**Support Needs:**
- **Onboarding:** [Level of guidance needed]
- **Documentation:** [Type and depth preferred]
- **Support Channel:** [Email / Chat / Phone / Self-service]
- **Response Time:** [Expectation for support]

---

### Use Case Scenarios

**Scenario 1: [Success Scenario Title]**

**Context:** [Situation description]

**Steps:**
1. [Action 1]
2. [Action 2]
3. [Action 3]
4. [Outcome]

**Success Criteria:** [How they know they've succeeded]

**Emotions:** [How they feel during this scenario]

---

**Scenario 2: [Challenge Scenario Title]**

**Context:** [Problem situation]

**Steps:**
1. [Action 1]
2. [Challenge encountered]
3. [How they try to resolve]
4. [Outcome]

**Pain Points Highlighted:** [What frustrates them]

**Desired Resolution:** [How they wish it would work]

---

### Technology & Tools

**Current Tech Stack:**
- [Tool 1 - Purpose]
- [Tool 2 - Purpose]
- [Tool 3 - Purpose]

**Complementary Products:**
- [Product 1 that they use alongside yours]
- [Product 2 that they use alongside yours]

**Competitive Products Used:**
- [Competitor 1] - [Why they use/used it]
- [Competitor 2] - [Why they use/used it]

**Technology Comfort Level:**
- [Early Adopter / Pragmatist / Conservative]
- [Technical skills description]

---

### Product Strategy Implications

**For Product Development:**
- [How features should be prioritized for this persona]
- [Design considerations]
- [Technical requirements]

**For Marketing:**
- **Messaging:** [Key messages that resonate]
- **Channels:** [Where to reach them]
- **Content:** [What content types work]

**For Sales:**
- **Buying Process:** [How they buy]
- **Key Decision Factors:** [What influences purchase]
- **Objection Handling:** [Common objections]

**For Customer Success:**
- **Onboarding Focus:** [Critical first steps]
- **Success Metrics:** [How to measure their success]
- **Expansion Opportunities:** [Upsell/cross-sell potential]

---

## Persona 2: [Name - First and Last]

[Repeat full structure from Persona 1]

### Quick Profile
...

---

## Persona 3: [Name - First and Last] (If applicable)

[Repeat full structure]

---

## Negative Personas

### Who We're NOT Building For

**Negative Persona 1: [Name/Type]**
- **Description:** [Who they are]
- **Why Not a Fit:** [Why product doesn't serve them]
- **What Would Attract Them:** [Red flags if you attract this segment]

**Negative Persona 2: [Name/Type]**
- [Same structure]

---

## Persona Comparison Matrix

| Attribute | [Persona 1 Name] | [Persona 2 Name] | [Persona 3 Name] |
|-----------|-----------------|-----------------|------------------|
| **Primary Goal** | [Goal] | [Goal] | [Goal] |
| **Top Pain Point** | [Pain] | [Pain] | [Pain] |
| **Tech Proficiency** | [Level] | [Level] | [Level] |
| **Decision Style** | [Style] | [Style] | [Style] |
| **Price Sensitivity** | [Level] | [Level] | [Level] |
| **Support Needs** | [Level] | [Level] | [Level] |
| **Primary Use Case** | [Use case] | [Use case] | [Use case] |

---

## Feature Prioritization by Persona

| Feature | [Persona 1] | [Persona 2] | [Persona 3] | Overall Priority |
|---------|------------|------------|------------|------------------|
| [Feature 1] | Must-have | Nice-to-have | Not needed | High |
| [Feature 2] | Nice-to-have | Must-have | Must-have | High |
| [Feature 3] | Must-have | Must-have | Nice-to-have | High |
| [Feature 4] | Nice-to-have | Not needed | Nice-to-have | Medium |
| [Feature 5] | Not needed | Nice-to-have | Must-have | Medium |

---

## Using These Personas

### For Product Teams

**When Making Decisions:**
1. Ask: "How would [Persona Name] react to this?"
2. Evaluate: "Does this solve [Persona Name]'s pain points?"
3. Prioritize: "Which persona needs this most urgently?"

**When Designing:**
- Keep personas visible during design sessions
- Test designs against persona workflows
- Validate that primary personas can complete key tasks

**When Writing Copy:**
- Use language that resonates with persona values
- Address persona-specific pain points
- Match communication style to persona preferences

### For Go-to-Market Teams

**Marketing:**
- Create persona-specific content
- Target channels where personas spend time
- Craft messages addressing persona goals

**Sales:**
- Qualify leads against persona profiles
- Tailor demos to persona use cases
- Prepare objection handling for persona concerns

**Customer Success:**
- Customize onboarding by persona type
- Set success metrics aligned with persona goals
- Provide support matching persona preferences

---

## Persona Validation & Evolution

**Validation Methods:**
- [ ] User interviews with real users matching personas
- [ ] Surveys to quantify persona characteristics
- [ ] Analytics data confirming behavior patterns
- [ ] Usability testing with persona representatives

**Update Frequency:** [Quarterly / Bi-annually / Annually]

**Next Review Date:** [Date]

**Evolution Tracking:**
| Version | Date | Changes | Rationale |
|---------|------|---------|----------|
| v[version] | [YYYYMMDD] | Initial creation | Based on [research source] |

---

## Research Sources & Data

**Primary Research:**
- [Feedback summary document]
- [Interview notes - number of participants]
- [Survey responses - number of participants]
- [Usability test observations]

**Supporting Data:**
- [Analytics data]
- [Customer support ticket analysis]
- [Sales conversation notes]
- [Market research reports]

**Sample Size & Diversity:**
- Total participants: [Number]
- Geographic distribution: [Regions]
- Role distribution: [Job functions]
- Experience levels: [Range]

---

**Prepared By:** [Team/Individual]  
**Approved By:** [Stakeholders]  
**Last Updated:** [YYYYMMDD]  
**Next Update:** [Date]

---

**Filename:** `[YYYYMMDD]-[initiative_slug]-personas-v[version].md`  
**Save to:** `niopd-workspace/reports/[filename]`

### Step 12: Confirm and Conclude
- Confirm the action is complete: "✅ I've created comprehensive user personas based on your feedback summary."
- Provide the path to the file: "You can view them here: `niopd-workspace/reports/[YYYYMMDD]-[initiative_slug]-personas-v[version].md`"
- Suggest next steps:
    - "These personas can guide your PRD development - use `/niopd:PD:draft-prd`"
    - "Map persona journeys with `/niopd:UR:journey`"
    - "Validate with Jobs to Be Done analysis - use `/niopd:UR:jtbd`"

## Error Handling
- **Insufficient Feedback Data:** If the feedback summary lacks sufficient detail for persona development, explain the limitation and suggest collecting more targeted feedback.
- **Inconsistent Information:** If feedback contains contradictory information about user behaviors or needs, note these conflicts and explain how they were resolved.
- **Missing Demographic Data:** If key demographic information is unavailable, note this and make reasonable assumptions while flagging limitations.
- **Overlapping Personas:** If personas seem too similar, suggest merging or identifying clearer differentiating characteristics.
- **Unrepresentative Sample:** If feedback appears to come from a narrow user segment, note this bias and suggest broader data collection.

In all error cases, provide clear explanations, suggest alternatives or additional research, and emphasize that even imperfect personas provide valuable directional guidance.