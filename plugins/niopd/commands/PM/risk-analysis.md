---
argument-hint: [--project=<project_name>] [--scope=<analysis_scope>] [--method=<analysis_method>]
description: Conducts systematic risk analysis to identify, assess, and mitigate risks that may impact project success.
---

# Command: /niopd:PM:risk-analysis

This command conducts systematic risk analysis to identify, assess, and mitigate risks that may impact project success or business objectives.

## Theoretical Foundation

### Origin and Development
Project risk management was formalized by **PMI's PMBOK** (1987) and **PRINCE2**. Modern approaches include **Risk Management Framework (NIST)** and **Enterprise Risk Management (COSO, 2004)**.

### Core Principle
Risk management is **proactive identification and mitigation** of threats and opportunities. It follows: Identify → Assess → Respond → Monitor. The goal is not to eliminate risk but to manage it intelligently.

### Risk Assessment Matrix

**Probability × Impact = Risk Score**

| Impact →      | Low (1) | Med (2) | High (3) | Very High (4) |
|-------------|---------|---------|----------|---------------|
| **Very High (90%)** | 9    | 18   | 27    | 36          |
| **High (70%)**      | 7    | 14   | 21    | 28          |
| **Medium (50%)**    | 5    | 10   | 15    | 20          |
| **Low (30%)**       | 3    | 6    | 9     | 12          |
| **Very Low (10%)**  | 1    | 2    | 3     | 4           |

### Risk Response Strategies

1. **Avoid**: Eliminate threat (change plan)
2. **Mitigate**: Reduce probability or impact
3. **Transfer**: Shift to third party (insurance)
4. **Accept**: Acknowledge and monitor
5. **Exploit**: Capitalize on opportunities

### Risk Categories

- **Technical**: Technology failures, complexity
- **Schedule**: Delays, dependencies
- **Resource**: Budget, personnel
- **External**: Market, regulatory, vendors
- **Quality**: Performance, reliability

## Usage
`/niopd:PM:risk-analysis [--project=<project_name>] [--scope=<analysis_scope>] [--method=<analysis_method>]`

## Preflight Checklist

1.  **Validate Project Name:**
    -   If the `--project` argument is not provided, prompt the user to specify the project name.
    -   Confirm that the project name is valid and meaningful.

2.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/reports` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in project risk management. Your goal is to conduct systematic risk analysis to identify, assess, and mitigate risks that may impact project success or business objectives.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you conduct a systematic risk analysis for the **<project_name>** project."
-   If the `--project` argument wasn't provided, ask the user: "What project would you like to analyze for risks?" and wait for their response.
-   If the `--scope` argument wasn't provided, ask the user: "What is the scope of this risk analysis?" and wait for their response.
-   If the `--method` argument wasn't provided, ask the user: "What risk analysis method would you prefer to use?" and wait for their response.

### Step 2: Project Context Analysis
-   Help the user define the project context:
    -   "What are the main objectives of the **<project_name>** project?"
    -   "What are the key deliverables expected from this project?"
    -   "What is the project timeline?"
    -   "What is the budget allocated for this project?"
-   Wait for the user's responses.

### Step 3: Stakeholder Analysis
-   Guide the user to identify key stakeholders:
    -   "Who is the project sponsor and what is their role?"
    -   "Who is the project manager and what are their responsibilities?"
    -   "Who are the key team members and what expertise do they bring?"
    -   "Are there any external stakeholders such as customers, vendors, or regulators?"
-   Wait for the user's responses.

### Step 4: Assumptions and Constraints
-   Help the user identify key assumptions and constraints:
    -   "What assumptions are you making for this project planning?"
    -   "What constraints might impact the project execution?"
-   Wait for the user's responses.

### Step 5: Risk Identification
-   Guide the user through risk identification by category:
    -   "Let's identify technical risks. What technical challenges or uncertainties do you foresee?"
    -   "Let's identify schedule risks. What timeline or milestone threats do you see?"
    -   "Let's identify resource risks. What personnel, budget, or material constraints might arise?"
    -   "Let's identify external risks. What market, regulatory, or environmental factors could impact the project?"
    -   "Let's identify quality risks. What performance, reliability, or satisfaction threats do you anticipate?"
-   Wait for the user's responses for each category.

### Step 6: Risk Assessment Framework
-   Explain the risk assessment framework to the user:
    -   "We'll assess each risk by probability and impact."
    -   "Probability scale: Very High (90-100%), High (70-89%), Medium (30-69%), Low (10-29%), Very Low (0-9%)."
    -   "Impact scale: Very High (4), High (3), Medium (2), Low (1)."
    -   "Risk Score = Probability × Impact."
-   Ask the user: "Do you understand this framework, or would you like me to explain any part in more detail?" and wait for their response.

### Step 7: Risk Prioritization
-   Help the user assess probability and impact for each identified risk:
    -   For each risk, ask: "What is the probability of this risk occurring?" and "What would be the impact if it occurred?"
    -   Calculate the risk score for each risk.
    -   Categorize risks by priority:
        -   Very High Risk: Score 28-40 (Immediate action required)
        -   High Risk: Score 18-27 (Management attention needed)
        -   Medium Risk: Score 8-17 (Monitor and review regularly)
        -   Low Risk: Score 1-7 (Accept and monitor passively)
-   Wait for the user's responses.

### Step 8: Risk Response Planning
-   Guide the user through developing response strategies for high and medium priority risks:
    -   "For each high priority risk, let's determine the best response strategy: Avoidance, Mitigation, Transfer, or Acceptance."
    -   For each selected strategy, ask: "What specific actions will you take to address this risk?" and "What resources will be required?"
-   Wait for the user's responses.

### Step 9: Contingency Planning
-   Help the user develop contingency plans for high priority risks:
    -   "For each high priority risk, let's define trigger conditions for fallback plans."
    -   "What specific response actions will be taken when these triggers occur?"
    -   "What resources will be required to execute these fallback plans?"
-   Wait for the user's responses.

### Step 10: Risk Monitoring and Control
-   Guide the user in establishing monitoring mechanisms:
    -   "How often should each risk category be reviewed?"
    -   "Who will be responsible for monitoring each risk?"
    -   "What reporting format will be used for each risk category?"
-   Wait for the user's responses.

### Step 11: Roles and Responsibilities
-   Help the user define roles and responsibilities:
    -   "Who will be the overall risk manager for this project?"
    -   "Who will be responsible for managing each identified risk?"
    -   "How will risk status be communicated to stakeholders?"
-   Wait for the user's responses.

### Step 12: Create Risk Analysis Report
Produce a markdown report with the following structure:

---
# Risk Analysis Report: [Project Name]

## Executive Summary
*A brief overview of key risks and recommended actions*

## Project Context
### Objectives
[Project objectives identified in Step 2]

### Deliverables
[Key deliverables identified in Step 2]

### Timeline
[Project timeline identified in Step 2]

### Budget
[Budget identified in Step 2]

## Stakeholder Analysis
### Key Stakeholders
[Stakeholders identified in Step 3]

## Assumptions and Constraints
### Assumptions
[Assumptions identified in Step 4]

### Constraints
[Constraints identified in Step 4]

## Risk Register
### High Priority Risks (Score 18+)
1. **[Risk Name]:** [Description, Probability, Impact, Score, Owner]
2. **[Risk Name]:** [Description, Probability, Impact, Score, Owner]

### Medium Priority Risks (Score 8-17)
1. **[Risk Name]:** [Description, Probability, Impact, Score, Owner]
2. **[Risk Name]:** [Description, Probability, Impact, Score, Owner]

### Low Priority Risks (Score 1-7)
1. **[Risk Name]:** [Description, Probability, Impact, Score, Owner]
2. **[Risk Name]:** [Description, Probability, Impact, Score, Owner]

## Risk Response Plans
### High Priority Risk Responses
1. **[Risk Name]:** [Strategy, Actions, Resources, Timeline]
2. **[Risk Name]:** [Strategy, Actions, Resources, Timeline]

### Medium Priority Risk Responses
1. **[Risk Name]:** [Strategy, Actions, Resources, Timeline]
2. **[Risk Name]:** [Strategy, Actions, Resources, Timeline]

## Contingency Plans
### High Priority Risk Fallback Plans
1. **[Risk Name]:** [Trigger Conditions, Response Actions, Resource Requirements]
2. **[Risk Name]:** [Trigger Conditions, Response Actions, Resource Requirements]

## Monitoring and Control
### Review Schedule
[Review schedule identified in Step 10]

### Roles and Responsibilities
[Roles and responsibilities identified in Step 11]

## Success Metrics
- **Risk Identification Rate:** [Percentage of risks identified before impact]
- **Response Effectiveness:** [How well risk responses mitigate threats]
- **Cost of Risk Management:** [Resources spent on risk activities]

---

### Step 13: Save the Report
- Generate a filename for the risk analysis report following the NioPD naming convention: `[YYYYMMDD]-[project_slug]-risk-analysis-v[version].md`.
- Save the risk analysis report to: `niopd-workspace/plans/[filename]`

### Step 14: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the risk analysis for the **<project_name>** project."
- Provide the path to the file: "You can view the detailed risk analysis report at: `niopd-workspace/plans/[YYYYMMDD]-[project_slug]-risk-analysis-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PM:risk-analysis` to update this analysis as the project progresses, or `/niopd:PM:kpis` to track project performance against identified risks."

## Error Handling
- **Missing Project Name:** If no project name is specified, explain that a project name is required and ask for one.
- **Incomplete Risk Assessment:** If the user doesn't provide sufficient information for risk assessment, explain what's needed and offer to proceed with partial analysis.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial risk analysis can still provide value.
```

This command generates a comprehensive Risk Analysis report to identify, assess, and mitigate risks that may impact project success. The report includes risk identification, assessment, prioritization, response planning, and monitoring mechanisms.