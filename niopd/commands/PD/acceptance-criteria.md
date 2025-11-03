---
argument-hint: [--story=<user_story>] [--acceptance=<acceptance_criteria>] [--feature=<feature_name>]
description: Generates detailed acceptance criteria for user stories to ensure clear implementation requirements.
---

# Command: /niopd:PD:acceptance-criteria

This command generates detailed acceptance criteria for user stories to ensure clear implementation requirements.

## Theoretical Foundation

### Origin and Development
Acceptance Criteria emerged from **Behavior-Driven Development (BDD)**, pioneered by **Dan North** in 2003. The Given-When-Then format was formalized to bridge communication between business stakeholders, developers, and testers. The concept was refined through Agile practices and **Specification by Example** (Gojko Adzic, 2011).

### Core Principle
Acceptance Criteria define the **boundaries of a user story** - the conditions that must be satisfied for the story to be considered complete. They serve as the "Confirmation" in Ron Jeffries' 3 C's model (Card, Conversation, Confirmation) and provide a shared definition of "done."

### Essential Characteristics

Good acceptance criteria are:
- **Specific**: Unambiguous and clear
- **Testable**: Can be verified objectively
- **Complete**: Cover all scenarios (happy path, alternatives, errors)
- **Concise**: Brief but comprehensive
- **Independent**: Can be tested separately
- **Agreed**: Accepted by product, development, and QA

### Given-When-Then Format

Developed by Dan North for BDD:

**Structure**:
- **Given** [precondition/context]: Initial state
- **When** [action/event]: Trigger or action
- **Then** [expected outcome]: Observable result

**Example**:
- **Given** the user is on the login page
- **When** they enter valid credentials and click "Login"
- **Then** they are redirected to the dashboard

**Multiple conditions**:
- **And**: Additional preconditions or outcomes
- **But**: Exceptions or edge cases

### Checklist Format

Alternative to Given-When-Then:

```
Acceptance Criteria:
- [ ] User can select dark mode from settings
- [ ] Dark mode persists across sessions
- [ ] All screens support dark mode
- [ ] Images have appropriate dark mode variants
- [ ] Error message: "Dark mode requires app version 2.0+"
```

### Scenarios to Cover

**1. Happy Path (Primary Flow)**:
- Expected user journey with valid inputs
- Successful completion scenario

**2. Alternative Paths**:
- Different valid ways to achieve the goal
- Optional features or workflows

**3. Error Conditions**:
- Invalid inputs
- System errors
- Network failures
- Authorization failures

**4. Edge Cases**:
- Boundary values (min/max, empty, very large)
- Special characters
- Concurrent operations
- Rare but valid scenarios

**5. Non-Functional Requirements**:
- Performance (response time < 2s)
- Security (encryption, authentication)
- Accessibility (WCAG AA compliance)
- Usability (< 3 clicks to complete)

### INVEST Applied to Acceptance Criteria

- **Independent**: Criteria can be tested separately
- **Negotiable**: Details can be refined
- **Valuable**: Each criterion adds value
- **Estimable**: Testable scope is clear
- **Small**: Atomic, single-purpose checks
- **Testable**: Can be verified pass/fail

### Definition of Done (DoD)

Acceptance criteria are part of DoD:
1. ✅ All acceptance criteria pass
2. ✅ Code reviewed
3. ✅ Unit tests written and passing
4. ✅ Integration tests passing
5. ✅ Documentation updated
6. ✅ Deployed to staging

### Specification by Example

**Gojko Adzic's approach**:
- Use concrete examples instead of abstract requirements
- Collaborate to derive examples
- Refine examples into executable specifications
- Automate validation

**Example**:
Instead of: "Search should handle special characters"
Use: "When user searches for 'café' or 'cafe', both return results for 'Café Latte'"

### When to Write Acceptance Criteria

**Three Amigos Meeting**:
- Product Owner: Business perspective
- Developer: Technical perspective
- Tester: Quality perspective
- Collaborate to define acceptance criteria before sprint

**Refinement Activities**:
- Backlog grooming
- Sprint planning
- Story elaboration sessions

### Anti-Patterns to Avoid

❌ **Too Vague**: "User can log in successfully"
✅ **Specific**: "Given valid credentials, when user clicks login, then dashboard loads within 2 seconds"

❌ **Implementation Details**: "System uses OAuth 2.0 for authentication"
✅ **Behavior**: "User can log in with Google account"

❌ **Missing Edge Cases**: Only happy path covered
✅ **Comprehensive**: Happy path + errors + edge cases

### Automation and Testing

**BDD Tools**:
- **Cucumber**: Gherkin syntax (Given-When-Then)
- **SpecFlow**: .NET BDD framework
- **JBehave**: Java BDD framework

**Test-Driven Development (TDD)**:
1. Write test based on acceptance criteria
2. Run test (should fail)
3. Write code to pass test
4. Refactor code
5. Repeat

### Related Frameworks
- **Behavior-Driven Development (BDD)**: Dan North, 2003
- **Test-Driven Development (TDD)**: Kent Beck, 1990s
- **Specification by Example**: Gojko Adzic, 2011
- **ATDD (Acceptance Test-Driven Development)**: Collaborative testing approach

### Complementary NioPD Commands
- `/niopd:PD:stories` - Generate user stories
- `/niopd:PD:draft-prd` - PRD documentation
- `/niopd:PD:experiment` - Test assumptions
- `/niopd:UR:usability` - Validate with users

## Usage
`/niopd:PD:acceptance-criteria [--story=<user_story>] [--acceptance=<acceptance_criteria>] [--feature=<feature_name>]`

## Preflight Checklist

1.  **Validate Inputs:**
    -   Check if `--story` argument is provided for the user story.
    -   If `--story` is not provided, ask the user to specify the user story.
    -   Check if `--feature` argument is provided for the feature name.

## Instructions

You are Nio, an AI Product Assistant. Your task is to help users generate detailed acceptance criteria for user stories.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you generate detailed acceptance criteria for your user story."
-   If the `--story` argument wasn't provided, ask the user: "What user story would you like to define acceptance criteria for?" and wait for their response.
-   If the `--feature` argument wasn't provided, ask the user: "Which feature does this story relate to?" and wait for their response.

### Step 2: Understand the User Story
-   Help the user break down the user story:
    -   "Who is the user persona for this story?"
    -   "What action do they want to take?"
    -   "What benefit or outcome do they expect?"
-   Confirm the story format: "As a [persona], I want to [action], so that [benefit]."
-   Wait for the user's responses.

### Step 3: Explain Acceptance Criteria
-   Briefly explain what good acceptance criteria should include:
    -   Specific and testable conditions
    -   Clear pass/fail conditions
    -   Covering both happy path and edge cases
    -   Independent and atomic
-   Ask the user: "Do you understand what we're aiming for with the acceptance criteria, or would you like me to elaborate?" and wait for their response.

### Step 4: Identify Happy Path Scenarios
-   Guide the user to identify the main success scenario:
    -   "What is the primary flow that should work for this story?"
    -   "What conditions must be true for this scenario to succeed?"
-   Wait for the user's responses.

### Step 5: Identify Edge Cases and Error Conditions
-   Help the user identify alternative flows and error conditions:
    -   "What could go wrong in this scenario?"
    -   "What edge cases should we consider?"
    -   "What invalid inputs or states might occur?"
-   Wait for the user's responses.

### Step 6: Define Preconditions and Assumptions
-   Guide the user to identify what must be true before the story can be executed:
    -   "What preconditions must be met?"
    -   "What assumptions are we making?"
-   Wait for the user's responses.

### Step 7: Define Postconditions and Outcomes
-   Help the user identify what should be true after the story is completed:
    -   "What should be the system state after this story?"
    -   "What outcomes should be observable?"
-   Wait for the user's responses.

### Step 8: Format Acceptance Criteria
-   Structure the acceptance criteria using the Given-When-Then format:
    -   Given [precondition]
    -   When [action]
    -   Then [expected outcome]
-   Create criteria for each scenario identified.

### Step 9: Review and Refine
-   Present the acceptance criteria to the user: "Here are the acceptance criteria I've drafted. Do they adequately cover the requirements?"
-   Wait for the user's feedback and make adjustments as needed.

### Step 10: Save to PRD or Story File
-   Ask the user: "Would you like me to add these acceptance criteria to your PRD or user story file? If so, please provide the filename." and wait for their response.
-   If the user provides a filename, append the acceptance criteria to that file.

### Step 11: Confirm and Conclude
-   Confirm the completion: "✅ I've generated detailed acceptance criteria for your user story."
-   Suggest next steps: "Consider using /niopd:PD:stories to create more user stories, /niopd:PD:integrate to incorporate insights from user feedback reports, or /niopd:PM:kpis to define success metrics for your feature. For a complete PRD workflow, use /niopd:PD:workflow to guide you through the next steps."

## Error Handling
- **Missing Information:** If key information is missing, explain what's needed and offer to proceed with placeholders.
- **Unclear Requirements:** If requirements are ambiguous, ask for clarification using specific questions.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial criteria creation can still provide value.