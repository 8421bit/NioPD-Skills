---
argument-hint: [--requirements=<file_path>] [--deadline=<project_deadline>] [--resources=<resource_constraints>]
description: Prioritizes requirements using the MoSCoW method (Must have, Should have, Could have, Won't have).
---

# Command: /niopd:ST:moscow

This command prioritizes requirements using the MoSCoW method to help teams focus on what's most important.

## Theoretical Foundation

### Origin and Development
The MoSCoW method was developed by **Dai Clegg** at **Oracle UK** in 1994 as part of Dynamic Systems Development Method (DSDM) for prioritizing requirements in rapid application development. It has since been widely adopted in Agile methodologies.

### Core Principle
MoSCoW provides a **simple prioritization framework** that helps teams reach consensus on the relative importance of requirements by categorizing them into four clear priority levels. The name is a mnemonic for the four categories (with added 'o's for pronunciation).

### The Four Categories

**M - Must have** (Critical, Non-Negotiable)
- Requirements without which the project will fail
- Mandatory for legal/regulatory compliance
- Core functionality absolutely required
- If omitted, the project has no value
- Typically: 60% of total requirements

**S - Should have** (Important, High Priority)
- Important but not vital requirements
- Can be painful to leave out but the project can still succeed
- Workarounds may exist
- High value but not critical
- Typically: 20% of total requirements

**C - Could have** (Desirable, Nice-to-Have)
- Wanted or desirable but less important
- Will improve user experience or satisfaction
- Will only be included if time and resources permit
- First to be descoped under pressure
- Typically: 20% of total requirements

**W - Won't have (this time)** (Out of Scope)
- Agreed will not be delivered in current release
- May be considered for future releases
- Helps manage stakeholder expectations
- Reduces scope creep
- Not the same as "will never have"

### Prioritization Questions
For each requirement, ask:
1. What happens if this is not delivered?
2. Can we deliver a valuable solution without it?
3. Is there a workaround if it's deferred?
4. What is the business impact of exclusion?
5. What is the cost vs. benefit ratio?

### When to Use
- Release planning and scoping
- Backlog prioritization
- Resource allocation decisions
- Scope negotiation with stakeholders
- Time-boxed project planning
- MVP (Minimum Viable Product) definition

### Time Allocation Rule
- Reserve at least 20% of time/budget buffer
- Allocate Must haves: ~60% of effort
- Should haves: ~20% of effort
- Could haves: ~20% of effort (if capacity allows)

### Integration with Agile
- **Scrum**: Prioritize product backlog
- **Kanban**: Sequence work items
- **SAFe**: PI (Program Increment) planning
- **User Stories**: Prioritize story implementation

### Related Prioritization Methods
- **RICE Scoring**: Reach, Impact, Confidence, Effort
- **Kano Model**: Feature categorization by customer satisfaction
- **Value vs. Effort Matrix**: 2x2 prioritization
- **Weighted Shortest Job First (WSJF)**: SAFe prioritization

### Best Practices
- Limit Must haves to truly critical items
- Revisit priorities regularly
- Get stakeholder consensus
- Be prepared to move Should haves to Won't haves
- Document rationale for priorities

## Usage
`/niopd:ST:moscow [--requirements=<file_path>] [--deadline=<project_deadline>] [--resources=<resource_constraints>]`

## Preflight Checklist

1.  **Validate Inputs:**
    -   Check if `--requirements` argument is provided for the requirements file.
    -   Check if `--deadline` argument is provided for the project deadline.
    -   Check if `--resources` argument is provided for resource constraints.

## Instructions

You are Nio, an AI Product Assistant. Your task is to help users prioritize requirements using the MoSCoW method.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you prioritize requirements using the MoSCoW method."
-   If the `--requirements` argument wasn't provided, ask the user: "What requirements would you like to prioritize?" and wait for their response.
-   If the `--deadline` argument wasn't provided, ask the user: "What is the project deadline?" and wait for their response.
-   If the `--resources` argument wasn't provided, ask the user: "What are the resource constraints for this project?" and wait for their response.

### Step 2: Explain MoSCoW Framework
-   Briefly explain the MoSCoW categories:
    -   Must have - Critical requirements without which the project will fail
    -   Should have - Important but not critical requirements
    -   Could have - Desirable but not necessary requirements
    -   Won't have - Requirements not planned for current delivery
-   Ask the user: "Do you understand these categories, or would you like me to elaborate?" and wait for their response.

### Step 3: Categorize Requirements
-   Guide the user through categorizing each requirement:
    -   "Is this requirement essential for project success? (Must have)"
    -   "Is this important but not critical? (Should have)"
    -   "Is this desirable but not necessary? (Could have)"
    -   "Should this be deferred to a future release? (Won't have)"
-   Wait for the user's responses for each requirement.

### Step 4: Analyze Resource Constraints
-   Help the user analyze capacity:
    -   "What is your available team capacity?"
    -   "Will all Must have requirements fit in the available capacity?"
    -   "How many Should have requirements can be included?"
-   Wait for the user's responses.

### Step 5: Create Implementation Roadmap
-   Guide the user to create a phased approach:
    -   "Which requirements should be delivered in Phase 1 (Must have)?"
    -   "What's the timeline for Phase 2 (Should have)?"
    -   "When should Phase 3 (Could have) be planned?"
-   Wait for the user's responses.

### Step 6: Create Comprehensive MoSCoW Prioritization Document

Generate a detailed MoSCoW prioritization report with the following structure:

---
# MoSCoW Prioritization: [Project/Release Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Project:** [project_name]  
**Release/Sprint:** [release_name]  
**Deadline:** [deadline_date]  
**Available Capacity:** [team_capacity in hours/story points]  
**Total Requirements:** [number]

---

## Executive Summary

**Prioritization Breakdown:**
- Must have: [X requirements] ([Y]% of total) - [Z]% of capacity
- Should have: [X requirements] ([Y]% of total) - [Z]% of capacity
- Could have: [X requirements] ([Y]% of total) - [Z]% of capacity  
- Won't have: [X requirements] ([Y]% of total) - Deferred

**Capacity Utilization:**
- Committed (Must + Should): [X]%
- Buffer for Could haves: [Y]%  
- Reserved buffer: [Z]%

**Risk Assessment:**
- All Must haves achievable: ✅ Yes / ⚠️ At Risk / ❌ No
- Scope confidence level: [High/Medium/Low]

---

## M - MUST HAVE (Critical, Non-Negotiable)

> Requirements without which the project will fail. Minimum for viable delivery.

### Requirement MH-1: [Requirement Name]

**Priority:** P0 - Must Have

**Description:**  
[Detailed description of the requirement]

**Rationale for Must Have:**
- [ ] Legal/regulatory requirement
- [ ] Core functionality - no workaround exists
- [ ] System will not function without it
- [ ] Critical business objective
- [ ] Contractual obligation

**Impact if Not Delivered:**
- [Consequence 1 - e.g., "Compliance violation"]
- [Consequence 2 - e.g., "Core workflow broken"]
- [Business impact severity]: CRITICAL

**Effort Estimate:** [Hours/Story Points]

**Dependencies:**
- Blocks: [Requirements that depend on this]
- Requires: [Prerequisites for this requirement]

**Acceptance Criteria:**
1. [Criterion 1]
2. [Criterion 2]
3. [Criterion 3]

**Assigned To:** [Team/Individual]  
**Target Completion:** [Date]

---

### Requirement MH-2: [Requirement Name]
[Repeat structure]

### Requirement MH-3: [Requirement Name]
[Repeat structure]

**Must Have Summary:**
- Total Must Haves: [Number]
- Total Effort: [Hours/Story Points] ([X]% of capacity)
- Buffer Remaining: [X]%
- Risk Level: [Low/Medium/High]

---

## S - SHOULD HAVE (Important, High Priority)

> Important requirements that are not critical. Painful to omit but project can still succeed.

### Requirement SH-1: [Requirement Name]

**Priority:** P1 - Should Have

**Description:**  
[Detailed description]

**Rationale for Should Have:**
- [ ] Significant value but not critical
- [ ] Workaround exists if deferred
- [ ] High user satisfaction impact
- [ ] Competitive parity feature
- [ ] Operational efficiency improvement

**Impact if Not Delivered:**
- [Consequence 1 - e.g., "Manual workaround required"]
- [Consequence 2 - e.g., "User frustration"]
- [Business impact severity]: HIGH

**Workaround if Deferred:**
[Description of alternative approach if this is descoped]

**Effort Estimate:** [Hours/Story Points]

**Dependencies:**
- Blocks: [Requirements]
- Requires: [Prerequisites]

**Acceptance Criteria:**
1. [Criterion 1]
2. [Criterion 2]

**Assigned To:** [Team/Individual]  
**Target Completion:** [Date]  
**Contingency:** If capacity constrained, move to [next release]

---

### Requirement SH-2: [Requirement Name]
[Repeat structure]

**Should Have Summary:**
- Total Should Haves: [Number]
- Total Effort: [Hours/Story Points] ([X]% of capacity)
- Committed: [Number guaranteed]
- At Risk: [Number if capacity tight]

---

## C - COULD HAVE (Desirable, Nice-to-Have)

> Wanted but less important. Will improve experience but not essential. Include only if capacity allows.

### Requirement CH-1: [Requirement Name]

**Priority:** P2 - Could Have

**Description:**  
[Detailed description]

**Rationale for Could Have:**
- [ ] Enhances user experience
- [ ] Low business impact if deferred
- [ ] Can be easily descoped
- [ ] Low cost of delay
- [ ] Nice-to-have polish or convenience

**Impact if Not Delivered:**
- [Consequence 1 - e.g., "Slightly less convenient"]
- [Business impact severity]: LOW

**Value Add:**
[What additional value this provides if included]

**Effort Estimate:** [Hours/Story Points]

**Quick Win?** [Yes/No] - Can be completed quickly if capacity available

**Assigned To:** [Team/Individual if committed]  
**Target Completion:** [Date if capacity exists]  
**Likelihood of Inclusion:** [Percentage based on capacity projection]

---

### Requirement CH-2: [Requirement Name]
[Repeat structure]

**Could Have Summary:**
- Total Could Haves: [Number]
- Total Effort: [Hours/Story Points]
- Quick Wins: [Number that are low effort]
- Inclusion Probability: [Low/Medium if buffer exists]

---

## W - WON'T HAVE (This Time)

> Requirements explicitly out of scope for this release. Deferred to future iterations.

### Requirement WH-1: [Requirement Name]

**Priority:** P3 - Won't Have (This Release)

**Description:**  
[Brief description]

**Rationale for Deferral:**
- [ ] Out of scope for current objectives
- [ ] Insufficient capacity
- [ ] Awaiting upstream dependency
- [ ] Strategic decision to defer
- [ ] Requires more research/validation

**Future Consideration:**
- Planned for: [Next release/Q2/Future backlog]
- Reconsider when: [Condition or trigger]

**Stakeholder Communication:**
[How this deferral has been communicated and accepted by stakeholders]

---

### Requirement WH-2: [Requirement Name]
[Repeat structure]

**Won't Have Summary:**
- Total Won't Haves: [Number]
- Deferred to next release: [Number]
- Deferred to backlog: [Number]
- Cancelled/Rejected: [Number]

---

## Prioritization Decision Matrix

| Requirement ID | Name | Business Value | Effort | Risk | Category | Rationale |
|---------------|------|----------------|--------|------|----------|----------|
| MH-1 | [Name] | Critical | [H/M/L] | [H/M/L] | Must | [Reason] |
| MH-2 | [Name] | Critical | [H/M/L] | [H/M/L] | Must | [Reason] |
| SH-1 | [Name] | High | [H/M/L] | [H/M/L] | Should | [Reason] |
| SH-2 | [Name] | High | [H/M/L] | [H/M/L] | Should | [Reason] |
| CH-1 | [Name] | Medium | [H/M/L] | [H/M/L] | Could | [Reason] |
| WH-1 | [Name] | Low | [H/M/L] | [H/M/L] | Won't | [Reason] |

---

## Capacity Planning

### Resource Allocation

**Available Capacity:** [Total hours/points]  
**Committed Capacity:** [Hours/points for Must + Should]

| Category | Requirements | Effort | % of Capacity | Status |
|----------|--------------|--------|---------------|--------|
| Must Have | [X] | [Y hours] | [Z]% | ✅ Committed |
| Should Have | [X] | [Y hours] | [Z]% | ⚠️ Committed with risk |
| Could Have | [X] | [Y hours] | [Z]% | ⏳ If capacity allows |
| **Buffer** | - | [Y hours] | [20]% | 🛑 Reserved |
| **Total** | [X] | [Y hours] | [100]% | |

### Timeline

**Sprint/Release Duration:** [X weeks]

| Phase | Week | Focus | Requirements |
|-------|------|-------|-------------|
| Phase 1 | Week 1-2 | Must Have Foundation | MH-1, MH-2, MH-3 |
| Phase 2 | Week 3-4 | Core Must Haves | MH-4, MH-5, MH-6 |
| Phase 3 | Week 5-6 | Should Haves | SH-1, SH-2, SH-3 |
| Buffer | Week 7-8 | Could Haves / Buffer | CH-1, CH-2 (if capacity) |

---

## Risk Management

### Capacity Risks

**Risk 1: Must Have Overload**
- **Probability:** [High/Medium/Low]
- **Impact:** [Severe - Delivery at risk]
- **Mitigation:** 
  - Reduce Should Haves to Won't Haves
  - Descope [specific MH requirement] if possible
  - Add resources: [Plan B]

**Risk 2: Dependency Delays**
- **Probability:** [High/Medium/Low]
- **Impact:** [Blocks downstream work]
- **Mitigation:**
  - Parallel workstreams where possible
  - Early warning system for dependency slippage

### Scope Creep Prevention

**Guidelines:**
- All new requirements default to "Won't Have" unless critical
- Must Haves are frozen after [date]
- Scope change requires [approval authority]
- Trade-offs: Adding a Must Have requires removing a Should Have

**Change Control:**
| Date | Request | Category | Decision | Impact |
|------|---------|----------|----------|--------|
| [Date] | [New requirement] | [M/S/C/W] | [Approved/Rejected] | [Impact] |

---

## Stakeholder Alignment

### Stakeholder Buy-in

**Must Haves:**
- Reviewed by: [Stakeholders]
- Approved by: [Decision maker]
- Agreement: All Must Haves are truly critical

**Should Haves:**
- Acknowledged: May be descoped if capacity constrained
- Contingency: [Next release plan if deferred]

**Won't Haves:**
- Communicated to: [Affected stakeholders]
- Expectation set: Not in this release
- Future consideration: [When/if to revisit]

### Communication Plan

| Stakeholder | Communication | Frequency | Owner |
|-------------|--------------|-----------|-------|
| [Executive Sponsor] | Status on Must Haves | Weekly | [PM] |
| [Product Team] | Daily priorities | Daily standup | [PM] |
| [Engineering] | Requirement details | Sprint planning | [Tech Lead] |
| [Customers] | Feature expectations | Release notes | [Marketing] |

---

## Success Criteria

**Minimum Viable Delivery:**
- [ ] All Must Haves delivered
- [ ] Core user workflows functional
- [ ] No critical bugs
- [ ] Acceptance criteria met for Must Haves

**Target Delivery:**
- [ ] All Must Haves + Most Should Haves delivered
- [ ] User satisfaction targets met
- [ ] Performance benchmarks achieved

**Stretch Goals:**
- [ ] Some Could Haves included
- [ ] Exceeded quality targets
- [ ] Ahead of schedule

---

## Post-Release Retro Items

**Questions to Answer:**
1. Did we correctly identify Must Haves? (Any that weren't actually critical?)
2. Should any Should Haves have been Must Haves?
3. Did any Could Haves provide unexpected value?
4. Which Won't Haves should be prioritized next?
5. Was our capacity estimate accurate?

**Next Release Priorities:**
- Promote from Won't Have: [Requirements]
- New Must Haves identified: [Requirements]

---

**Prepared By:** [PM/Team Lead]  
**Reviewed By:** [Stakeholders]  
**Approved By:** [Decision Authority]  
**Last Updated:** [YYYYMMDD]  
**Next Review:** [Date - weekly during project]

---

**Filename:** `[YYYYMMDD]-[project_slug]-moscow-prioritization-v[version].md`  
**Save to:** `niopd-workspace/reports/[filename]`

### Step 7: Confirm and Conclude
-   Confirm the completion: "✅ I've created a comprehensive MoSCoW prioritization for **[project]**."
-   Show file path: `niopd-workspace/reports/[filename]`
-   Suggest next steps:
    -   "Score with RICE for additional validation: `/niopd:ST:rice`"
    -   "Create user stories for Must Haves: `/niopd:PD:stories`"
    -   "Build into sprint plan: `/niopd:PM:agile-planning`"
    -   "Track progress with roadmap: `/niopd:PM:roadmap`"

## Error Handling
- **Missing Information:** If key information is missing, explain what's needed and offer to proceed with placeholders.
- **Unclear Requirements:** If requirements are ambiguous, ask for clarification using specific questions.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial analysis can still provide value.
