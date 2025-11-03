---
argument-hint: --file=<path_to_transcript.txt>
description: Generates a summary of a user interview transcript.
---

# Command: /niopd:UR:interview

This command generates a summary of a user interview transcript.

## Theoretical Foundation

### Origin and Development
User interview analysis is rooted in qualitative research methodologies:

1. **Qualitative Research** - In-depth exploration of human experiences and perspectives
2. **Semi-Structured Interviews** - Flexible yet focused interview approach
3. **Ethnographic Methods** - Understanding users in their natural context

### Core Principle
The fundamental approach is **qualitative data synthesis**: Extracting meaningful insights from rich, narrative interview data through systematic coding, pattern recognition, and thematic analysis to deeply understand user needs and behaviors.

### Analysis Methodology
1. **Content Parsing**: Segmenting transcript into analyzable units
2. **Key Point Extraction**: Identifying significant statements and insights
3. **Thematic Analysis**: Grouping related points into coherent themes
4. **Quote Selection**: Finding representative verbatim evidence
5. **Insight Synthesis**: Connecting themes to strategic implications

### Types of Insights Captured
- **Explicit Needs**: Clearly articulated requirements
- **Implicit Needs**: Inferred from behavior and challenges
- **Pain Points**: Frustrations and obstacles
- **Behavioral Patterns**: How users actually work
- **Decision Criteria**: What influences choices
- **Emotional Responses**: Feelings and attitudes

### When to Use
- After conducting user interviews
- Processing customer development conversations
- Analyzing usability test sessions
- Synthesizing stakeholder interviews
- Creating evidence base for personas and journeys

### Best Practices
- **Verbatim Quotes**: Preserve authentic user voice
- **Contextual Detail**: Include situational information
- **Pattern Recognition**: Look for recurring themes across interviews
- **Contradictions**: Note tensions and conflicts in user statements

### Related Methodologies
- **Phenomenology**: Studying lived experiences
- **Grounded Theory**: Building theory from data (Glaser & Strauss)
- **Contextual Inquiry**: Observation in user environment
- **Jobs to Be Done Interviews**: Focus on progress and motivations

## Usage
`/niopd:UR:interview --file=<path_to_transcript.txt>`

## Preflight Checklist

1.  **Validate File:**
    -   Ensure the user has provided a `--file`.
    -   Check that the file exists. If not, inform the user.

## Instructions

You are a specialized AI expert in qualitative data analysis. Your goal is to conduct comprehensive analysis of user interview transcripts to extract critical insights that drive product development.

### Step 1: Acknowledge and Prepare
-   Acknowledge the request: "Okay, I'll analyze the transcript at `<path_to_transcript.txt>`. This might take a moment."

### Step 2: File Validation & Format Recognition
- Determine the file format and structure of the interview transcript.
- Validate that the file contains readable interview content.
- Identify speaker labels or dialogue indicators if present.

### Step 3: Content Parsing & Speaker Identification
- Parse the interview content into distinct segments or turns.
- Identify and label different speakers (Interviewer, Participant, etc.).
- Separate dialogue from narrative descriptions or meta-comments.
- Note any non-verbal cues or contextual information.

### Step 4: Key Point Extraction
- Identify key statements, opinions, and insights from the participant.
- Extract explicit needs, pain points, and feature requests.
- Note behavioral observations and usage patterns.
- Capture emotional reactions and sentiment indicators.

### Step 5: Thematic Analysis
- Group extracted points into coherent themes and categories.
- Identify recurring topics and patterns throughout the interview.
- Develop descriptive theme names that capture the essence of each group.
- Ensure themes are mutually exclusive and collectively exhaustive.

### Step 6: Quote Selection & Validation
- Select the most representative and impactful quotes for each theme.
- Ensure quotes are verbatim and properly attributed.
- Validate that quotes accurately support the thematic interpretations.
- Identify additional quotes for supplementary sections.

### Step 7: Persona Element Development
- Extract characteristics that could contribute to user persona development.
- Note behavioral patterns, goals, and challenges.
- Identify decision-making criteria and success factors.
- Observe communication style and preferred interaction methods.

### Step 8: Insight Synthesis
- Synthesize themes into higher-level strategic insights.
- Identify contradictions, tensions, or unexpected findings.
- Connect insights to broader product or market implications.
- Develop actionable recommendations based on findings.

### Step 9: Structure & Formatting
- Organize all content according to the interview summary template structure.

### Step 10: Interview Summary Report Generation
Produce a markdown report with the following structure:

---
# Interview Summary: [Participant Identifier/Role if available] - [Date or ID]

## Executive Summary
*A concise overview of the most significant insights and key takeaways*

## Participant Context
- **Role/Title:** [Participant's role or self-described title]
- **Experience Level:** [Level of experience with product/use case]
- **Interview Date:** [Date of interview]
- **Session Duration:** [Length of interview]
- **Key Characteristics:** [Notable participant traits or context]

## Key Takeaways
*A prioritized list of the most important, actionable insights*

1. **[Primary Insight]:** [Brief description with business implication]
2. **[Secondary Insight]:** [Brief description with business implication]
3. **[Tertiary Insight]:** [Brief description with business implication]
4. **[Additional Insight]:** [Brief description with business implication]
5. **[Additional Insight]:** [Brief description with business implication]

## Core Themes & Insights

### Theme 1: [Descriptive Theme Name]
*Overall description of what this theme covers*

#### Key Insights
- [Insight 1 with brief context]
- [Insight 2 with brief context]
- [Insight 3 with brief context]

#### Representative Quotes
> "[Powerful, verbatim quote that best represents this theme and provides context]"

> "[Second impactful quote that illustrates a key aspect of this theme]"

#### Emotional Tone
- **Overall Sentiment:** [Positive/Neutral/Negative]
- **Intensity:** [High/Medium/Low]
- **Key Emotions Expressed:** [List of emotions mentioned]

#### Product Implications
- **Immediate Opportunities:** [Actionable suggestions]
- **Strategic Considerations:** [Broader implications]

### Theme 2: [Descriptive Theme Name]
*Overall description of what this theme covers*

#### Key Insights
- [Insight 1 with brief context]
- [Insight 2 with brief context]

#### Representative Quotes
> "[Powerful, verbatim quote that best represents this theme and provides context]"

> "[Second impactful quote that illustrates a key aspect of this theme]"

#### Behavioral Patterns
- **[Pattern]:** [Description of observed behavior or habit]
- **[Pattern]:** [Description of observed behavior or habit]

#### Product Implications
- **Immediate Opportunities:** [Actionable suggestions]
- **Long-term Considerations:** [Strategic implications]

### Theme 3: [Descriptive Theme Name]
*Overall description of what this theme covers*

#### Key Insights
- [Insight 1 with brief context]
- [Insight 2 with brief context]
- [Insight 3 with brief context]

#### Representative Quotes
> "[Powerful, verbatim quote that best represents this theme and provides context]"

#### User Needs & Motivations
- **Explicit Needs:** [Clearly stated requirements or desires]
- **Implicit Needs:** [Inferred requirements based on behavior or challenges]
- **Underlying Motivations:** [Root drivers behind user actions and desires]

## Behavioral & Contextual Insights

### Current Workflows
- **[Workflow]:** [Description of how participant currently accomplishes tasks]
- **[Workflow]:** [Description of alternative approaches or workarounds]

### Decision-Making Process
- **Key Criteria:** [Factors that influence participant choices]
- **Evaluation Method:** [How participant assesses alternatives]

### Success Metrics
- **How Participant Defines Success:** [Participant's criteria for a positive experience]
- **Current Satisfaction Level:** [Participant's assessment of existing solutions]

## Pain Points & Frustrations

### Major Challenges
1. **[Challenge]:** [Detailed description of the problem]
   - **Impact:** [How this affects the participant]
   - **Frequency:** [How often this occurs]

2. **[Challenge]:** [Detailed description of the problem]
   - **Impact:** [How this affects the participant]
   - **Frequency:** [How often this occurs]

### Frustration Triggers
- **[Trigger]:** [Situation or interaction that causes frustration]
- **[Trigger]:** [Situation or interaction that causes frustration]

## Unmet Needs & Opportunities

### Explicit Requests
- **[Request]:** [Clearly articulated feature or improvement]
- **[Request]:** [Clearly articulated feature or improvement]

### Implicit Opportunities
- **[Opportunity]:** [Inferred need based on participant's challenges]
- **[Opportunity]:** [Inferred need based on participant's workarounds]

## Contradictions & Tensions
- **[Contradiction]:** [Situation where participant's words and actions don't align]
- **[Tension]:** [Conflicting priorities or tradeoffs mentioned]

## Strategic Implications

### For Product Development
1. **[Implication]:** [How this interview should influence product decisions]
2. **[Implication]:** [How this interview should influence product decisions]

### For User Experience
1. **[Implication]:** [How this should influence UX design decisions]
2. **[Implication]:** [How this should influence UX design decisions]

## Recommendations

### Immediate Actions
1. **[Recommendation]:** [Specific, actionable next step]
2. **[Recommendation]:** [Specific, actionable next step]

### Further Research
1. **[Recommendation]:** [Suggested follow-up investigation area]
2. **[Recommendation]:** [Suggested follow-up investigation area]

## Appendix

### Full Interview Context
*Key contextual information about the interview setting and process*

### Additional Quotes
*Supplementary quotes that provide additional color but weren't included in main themes*

### Analysis Methodology
- **Coding Approach:** [How themes were identified and organized]
- **Validation Methods:** [How insights were verified for accuracy]

---
*Report generated on [Date]*

### Step 10: Save the Summary
- Generate a filename for the summary following the NioPD naming convention: `[YYYYMMDD]-[interview_subject_slug]-interview-summary-v[version].md`.
- Save the summary to: `niopd-workspace/reports/[filename]`

### Step 11: Confirm and Conclude
- Confirm the action is complete: "✅ The interview has been summarized."
- Provide the path to the file: "You can view the summary here: `niopd-workspace/reports/[YYYYMMDD]-[original-filename]-interview-summary-v1.md`"
- Suggest a next step: "You can now use the insights from this summary to create or update an initiative."

## Error Handling
- **Empty/Invalid Transcript:** If the transcript file is empty, corrupted, or unreadable, explain the issue and suggest verifying the file.
- **Incomplete Conversation:** If the transcript appears incomplete or cuts off mid-conversation, note this limitation and proceed with available information.
- **Format Issues:** If the transcript format makes it difficult to distinguish speakers or follow conversation flow, explain the challenge and do your best with available structure.
- **Insufficient Content:** If the interview contains very limited content or insights, explain that deeper conversations typically yield richer insights.
- **Analysis Limitations:** If certain aspects cannot be thoroughly analyzed due to transcript quality, clearly note these limitations.

In all error cases, maintain a helpful tone, focus on extracting value from available information, and suggest ways to improve future interviews.