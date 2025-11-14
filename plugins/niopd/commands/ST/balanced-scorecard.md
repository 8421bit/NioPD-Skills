---
argument-hint: [--organization=<org_name>] [--strategy=<strategic_objective>] [--perspective=<perspective_filter>]
description: Develops a balanced scorecard to align business activities with strategic goals across four perspectives.
---
# Command: /niopd:ST:balanced-scorecard

This command develops a balanced scorecard to align business activities with strategic goals across four perspectives: financial, customer, internal processes, and learning & growth.

## Theoretical Foundation

### Origin and Development
The Balanced Scorecard was developed by **Robert Kaplan** and **David Norton** in 1992 through research with 12 companies. Their seminal Harvard Business Review article "The Balanced Scorecard—Measures that Drive Performance" revolutionized performance management.

### Core Principle
The Balanced Scorecard translates an organization's **vision and strategy into a comprehensive set of performance measures** that provides the framework for strategic measurement and management. It balances financial measures with operational measures on customer satisfaction, internal processes, and innovation.

### The Four Perspectives

1. **Financial Perspective**: "How do we look to shareholders?"
   - Revenue growth
   - Profitability metrics (ROI, EBITDA)
   - Cost reduction
   - Asset utilization

2. **Customer Perspective**: "How do customers see us?"
   - Customer satisfaction (CSAT, NPS)
   - Customer retention
   - Market share
   - Customer acquisition

3. **Internal Processes Perspective**: "What must we excel at?"
   - Process efficiency
   - Quality metrics
   - Innovation processes
   - Operational excellence

4. **Learning & Growth Perspective**: "Can we continue to improve and create value?"
   - Employee satisfaction
   - Skills development
   - Information systems capabilities
   - Organizational culture

### Strategy Maps
Introduced by Kaplan & Norton in 2001, **Strategy Maps** visually represent cause-and-effect relationships between objectives across the four perspectives, showing how learning & growth enables better processes, which drive customer satisfaction, leading to financial success.

### When to Use
- Strategic planning implementation
- Performance management systems
- Organizational alignment
- Change management initiatives
- M&A integration
- Annual goal setting

### Four-Step Process
1. **Translate the Vision**: Define strategic objectives for each perspective
2. **Communicate and Link**: Cascade objectives throughout organization
3. **Business Planning**: Set targets and allocate resources
4. **Feedback and Learning**: Monitor, review, and adjust strategy

### Related Frameworks
- **OKRs (Objectives and Key Results)**: Modern implementation approach
- **KPI Management**: Metric selection and tracking
- **Strategy Maps**: Visual representation of strategic logic
- **Performance Prism**: Stakeholder-focused alternative

### Best Practices
- Limit to 15-25 measures total (4-7 per perspective)
- Ensure measures link to strategy (not just operational metrics)
- Include leading indicators (predictive) and lagging indicators (outcomes)
- Review quarterly and update annually
- Create clear cause-and-effect linkages

## Implementation Plan

1. Create a structured balanced scorecard framework:
   - Financial perspective
   - Customer perspective
   - Internal processes perspective
   - Learning & growth perspective

2. Gather input data about the organization, strategic objectives, and perspective focus

3. Generate detailed KPIs and targets for each perspective

4. Create cause-and-effect relationships between perspectives

## Usage
`/niopd:ST:balanced-scorecard [--organization=<org_name>] [--strategy=<strategy>] [--perspective=<perspective>]`

## Preflight Checklist

1.  **Check User's Configuration Files:**
    -   Read and parse the .{{IDE_TYPE}}/{{IDE_TYPE}}.md file for user preferences and project settings
    -   Read and parse the {{IDE_TYPE}}.md file for project background and context
    -   Extract user's preferred communication language from configuration
    -   Extract other relevant settings (project context, team preferences, etc.)
    -   Store all configuration settings for use throughout the command execution

2. **Validate Parameters:** If `--organization` is not provided, prompt the user.
3. **Validate Workspace:** Check `niopd-workspace/reports/` exists, create if needed.

## Instructions

You are a specialized AI expert in strategic planning and the Balanced Scorecard framework. Your goal is to help organizations translate vision and strategy into a comprehensive set of performance measures across four balanced perspectives.

**Core Principle:** The final output should be created in the primary language used by the user. Follow all user preferences and project settings defined in the .{{IDE_TYPE}}/{{IDE_TYPE}}.md and {{IDE_TYPE}}.md configuration files.

### Step 1: Acknowledge and Gather Context
-   Read and parse configuration files:
    -   Load .{{IDE_TYPE}}/{{IDE_TYPE}}.md for user preferences and communication settings
    -   Load {{IDE_TYPE}}.md for project background and context information
    -   Extract communication language, project context, and other relevant settings
-   Acknowledge the request in the user's preferred language:
    -   If Chinese: "我将帮您创建一个平衡计分卡，以使 **<organization>** 的活动与战略目标保持一致。"
    -   If English: "I'll help you create a Balanced Scorecard to align **<organization>**'s activities with strategic goals."
    -   For other languages, use an appropriate translation based on user's language preference
-   If `--organization` wasn't provided, ask in the user's preferred language: "What is your organization's name?"
-   If `--strategy` wasn't provided, ask in the user's preferred language: "What is your organization's primary strategic objective or vision?"
-   If `--perspective` is provided, note it in the user's preferred language: "I'll focus primarily on the **<perspective>** perspective while maintaining balance."
-   Wait for user responses.

### Step 2: Understand Strategic Vision
-   Guide the user through strategic context:
    -   "What is your organization's vision statement?"
    -   "What are the top 3-5 strategic goals for the next 1-3 years?"
    -   "What does success look like for your organization?"
    -   "What are the key challenges or obstacles to achieving this vision?"
-   Wait for user responses.

### Step 3: Financial Perspective - Define Objectives
-   Explore the Financial Perspective ("How do we look to shareholders?"):
    -   "What are your financial goals? (e.g., revenue growth, profitability, cost reduction)"
    -   "What financial metrics currently matter most to your stakeholders?"
    -   "What is your target revenue growth rate?"
    -   "What profitability targets do you have? (ROI, EBITDA margin, net profit margin)"
-   Wait for user responses.

### Step 4: Financial Perspective - Define KPIs
-   Help identify Financial KPIs:
    -   For each financial objective, ask:
        -   "What specific KPI will measure this? (e.g., Annual Revenue Growth %, ROI %, Operating Margin %)"
        -   "What is the current value?"
        -   "What is the target value and by when?"
        -   "How often will this be measured? (Monthly/Quarterly/Annually)"
        -   "Who is responsible for this metric?"
-   Suggest 4-6 balanced financial metrics covering growth, profitability, and efficiency.
-   Wait for user responses.

### Step 5: Customer Perspective - Define Objectives
-   Explore the Customer Perspective ("How do customers see us?"):
    -   "Who are your primary customer segments?"
    -   "What value proposition do you offer to customers?"
    -   "What are your customer satisfaction goals?"
    -   "What market share or customer acquisition targets do you have?"
    -   "How do you want to differentiate from competitors in customers' eyes?"
-   Wait for user responses.

### Step 6: Customer Perspective - Define KPIs
-   Help identify Customer KPIs:
    -   For each customer objective, ask:
        -   "What KPI will measure customer satisfaction? (e.g., NPS, CSAT score, Customer Retention Rate)"
        -   "What is the current value?"
        -   "What is the target?"
        -   "How will you measure this?"
    -   Suggest metrics like:
        -   Customer satisfaction scores (NPS, CSAT)
        -   Customer retention/churn rate
        -   Market share
        -   Customer acquisition cost (CAC)
        -   Customer lifetime value (CLV)
-   Wait for user responses.

### Step 7: Internal Processes Perspective - Define Objectives
-   Explore the Internal Processes Perspective ("What must we excel at?"):
    -   "What core processes create value for customers?"
    -   "What operational improvements would most impact customer satisfaction?"
    -   "What innovation processes do you need to develop?"
    -   "Where do you need to improve efficiency or quality?"
    -   "What are your process excellence goals?"
-   Wait for user responses.

### Step 8: Internal Processes Perspective - Define KPIs
-   Help identify Internal Process KPIs:
    -   For each process objective, ask:
        -   "What KPI measures this process? (e.g., Cycle Time, Defect Rate, On-Time Delivery %)"
        -   "Current performance?"
        -   "Target performance?"
    -   Suggest process categories:
        -   **Operations Management**: Process efficiency, quality, cost
        -   **Customer Management**: Response time, service quality
        -   **Innovation**: New product development cycle, R&D productivity
        -   **Regulatory/Social**: Compliance, safety, environmental
-   Wait for user responses.

### Step 9: Learning & Growth Perspective - Define Objectives
-   Explore the Learning & Growth Perspective ("Can we continue to improve?"):
    -   "What capabilities must employees develop to execute your strategy?"
    -   "What technology or systems investments are needed?"
    -   "How do you want to develop organizational culture?"
    -   "What employee engagement or retention goals do you have?"
    -   "What knowledge management or innovation capabilities need improvement?"
-   Wait for user responses.

### Step 10: Learning & Growth Perspective - Define KPIs
-   Help identify Learning & Growth KPIs:
    -   For each L&G objective, ask:
        -   "What KPI measures capability development? (e.g., Employee Engagement Score, Training Hours per Employee)"
        -   "Current state?"
        -   "Target state?"
    -   Suggest metrics covering:
        -   **Human Capital**: Employee satisfaction, turnover rate, skills coverage
        -   **Information Capital**: System availability, data quality
        -   **Organization Capital**: Culture alignment, strategic readiness
-   Wait for user responses.

### Step 11: Define Strategic Linkages
-   Create cause-and-effect relationships:
    -   "Let's link the perspectives. For example:"
        -   "If we improve **[L&G objective]**, how does that enable **[Internal Process objective]**?"
        -   "If we excel at **[Process objective]**, how does that improve **[Customer objective]**?"
        -   "If we achieve **[Customer objective]**, how does that drive **[Financial objective]**?"
    -   "What are the 3-5 most critical linkages in your strategy?"
-   Help user create a strategy map showing causal relationships.
-   Wait for user responses.

### Step 12: Define Initiatives
-   Identify strategic initiatives for each perspective:
    -   "What major initiatives will you launch to achieve these objectives?"
    -   For each initiative:
        -   "Which objective(s) does this support?"
        -   "Who will lead it?"
        -   "What is the timeline?"
        -   "What budget is allocated?"
    -   Ensure initiatives are prioritized and resourced.
-   Wait for user responses.

### Step 13: Create Balanced Scorecard Document

Produce a comprehensive markdown Balanced Scorecard with the following structure:

---
# Balanced Scorecard: [Organization Name]

**Document Version:** v[version]  
**Date:** [YYYYMMDD]  
**Organization:** [organization_name]  
**Strategic Vision:** [vision_statement]

---

## Executive Summary

### Strategic Overview
[Brief summary of the organization's strategy and how the Balanced Scorecard supports it]

### Scorecard Structure
This Balanced Scorecard translates our strategy into measurable objectives across four perspectives:
- **Financial**: Sustainable financial performance
- **Customer**: Customer value and satisfaction
- **Internal Processes**: Operational excellence
- **Learning & Growth**: Organizational capability development

---

## Strategic Map

```
[Create a text-based representation of cause-and-effect relationships]

Learning & Growth → Internal Processes → Customer → Financial

Example:
"Skilled Employees" → "Efficient Processes" → "Satisfied Customers" → "Revenue Growth"
```

### Key Strategic Linkages
1. [L&G Objective] enables [Process Objective]
2. [Process Objective] drives [Customer Objective]
3. [Customer Objective] leads to [Financial Objective]

---

## Perspective 1: Financial

**Strategic Theme:** "How do we look to shareholders?"

### Objective 1.1: [Financial Objective Name]
- **Description:** [What this objective aims to achieve]
- **Strategic Rationale:** [Why this objective matters to the strategy]

**Key Performance Indicators (KPIs):**
| KPI | Current Value | Target Value | Target Date | Measurement Frequency | Owner |
|-----|---------------|--------------|-------------|----------------------|-------|
| [KPI 1] | [Value] | [Target] | [Date] | [Frequency] | [Owner] |
| [KPI 2] | [Value] | [Target] | [Date] | [Frequency] | [Owner] |

**Strategic Initiatives:**
- [ ] Initiative 1: [Name] - [Description] - Owner: [Name] - Timeline: [Date range] - Budget: [Amount]
- [ ] Initiative 2: [Name] - [Description] - Owner: [Name] - Timeline: [Date range] - Budget: [Amount]

### Objective 1.2: [Financial Objective Name]
- **Description:** [What this objective aims to achieve]
- **Strategic Rationale:** [Why this objective matters]

**Key Performance Indicators (KPIs):**
| KPI | Current Value | Target Value | Target Date | Measurement Frequency | Owner |
|-----|---------------|--------------|-------------|----------------------|-------|
| [KPI] | [Value] | [Target] | [Date] | [Frequency] | [Owner] |

**Strategic Initiatives:**
- [ ] Initiative: [Name and details]

### Objective 1.3: [Financial Objective Name]
[Repeat structure]

---

## Perspective 2: Customer

**Strategic Theme:** "How do customers see us?"

### Customer Segments
- **Primary Segment:** [Description and size]
- **Secondary Segment:** [Description and size]
- **Value Proposition:** [Unique value we offer]

### Objective 2.1: [Customer Objective Name]
- **Description:** [What this objective aims to achieve]
- **Strategic Rationale:** [Why this matters for customer value]
- **Link to Financial:** [How this drives financial objectives]

**Key Performance Indicators (KPIs):**
| KPI | Current Value | Target Value | Target Date | Measurement Frequency | Owner |
|-----|---------------|--------------|-------------|----------------------|-------|
| [KPI 1] | [Value] | [Target] | [Date] | [Frequency] | [Owner] |
| [KPI 2] | [Value] | [Target] | [Date] | [Frequency] | [Owner] |

**Strategic Initiatives:**
- [ ] Initiative: [Name and details]

### Objective 2.2: [Customer Objective Name]
[Repeat structure for each customer objective]

---

## Perspective 3: Internal Processes

**Strategic Theme:** "What must we excel at?"

### Process Categories

#### Operations Management Processes
**Objective 3.1: [Process Objective Name]**
- **Description:** [Process improvement goal]
- **Strategic Rationale:** [How this enables customer/financial objectives]
- **Process Owner:** [Department/Role]

**Key Performance Indicators (KPIs):**
| KPI | Current Value | Target Value | Target Date | Measurement Frequency | Owner |
|-----|---------------|--------------|-------------|----------------------|-------|
| [KPI] | [Value] | [Target] | [Date] | [Frequency] | [Owner] |

**Strategic Initiatives:**
- [ ] Initiative: [Name and details]

#### Customer Management Processes
**Objective 3.2: [Process Objective Name]**
[Repeat structure]

#### Innovation Processes
**Objective 3.3: [Process Objective Name]**
[Repeat structure]

#### Regulatory & Social Processes
**Objective 3.4: [Process Objective Name]**
[Repeat structure]

---

## Perspective 4: Learning & Growth

**Strategic Theme:** "Can we continue to improve and create value?"

### Human Capital
**Objective 4.1: [L&G Objective Name]**
- **Description:** [Capability development goal]
- **Strategic Rationale:** [How this enables process objectives]
- **Critical Skills:** [Skills needed]

**Key Performance Indicators (KPIs):**
| KPI | Current Value | Target Value | Target Date | Measurement Frequency | Owner |
|-----|---------------|--------------|-------------|----------------------|-------|
| [KPI] | [Value] | [Target] | [Date] | [Frequency] | [Owner] |

**Strategic Initiatives:**
- [ ] Initiative: [Training program, talent acquisition, etc.]

### Information Capital
**Objective 4.2: [L&G Objective Name]**
[Technology/systems/data capabilities]

### Organization Capital
**Objective 4.3: [L&G Objective Name]**
[Culture, leadership, teamwork, knowledge management]

---

## Implementation Roadmap

### Year 1 Priorities
**Q1:**
- [ ] Initiative 1: [Name] - [Owner]
- [ ] Initiative 2: [Name] - [Owner]

**Q2:**
- [ ] Initiative 3: [Name] - [Owner]

**Q3:**
- [ ] Initiative 4: [Name] - [Owner]

**Q4:**
- [ ] Initiative 5: [Name] - [Owner]
- [ ] Annual Scorecard Review

### Governance and Review
- **Monthly:** Operational KPI review meetings
- **Quarterly:** Strategic review with leadership team
- **Annually:** Full scorecard refresh and strategy update
- **Scorecard Owner:** [Role/Name]
- **Review Committee:** [Members]

---

## Scorecard Summary Dashboard

### Financial Perspective
| Objective | Status | Trend | Comment |
|-----------|--------|-------|----------|
| [Objective] | 🟢/🟡/🔴 | ↑/→/↓ | [Brief status] |

### Customer Perspective
| Objective | Status | Trend | Comment |
|-----------|--------|-------|----------|
| [Objective] | 🟢/🟡/🔴 | ↑/→/↓ | [Brief status] |

### Internal Processes Perspective
| Objective | Status | Trend | Comment |
|-----------|--------|-------|----------|
| [Objective] | 🟢/🟡/🔴 | ↑/→/↓ | [Brief status] |

### Learning & Growth Perspective
| Objective | Status | Trend | Comment |
|-----------|--------|-------|----------|
| [Objective] | 🟢/🟡/🔴 | ↑/→/↓ | [Brief status] |

---

## Appendix

### Methodology
- **Framework:** Kaplan & Norton Balanced Scorecard (1992)
- **Perspectives:** Financial, Customer, Internal Processes, Learning & Growth
- **Strategy Map:** Cause-and-effect relationships between objectives

### KPI Definitions
[Detailed definitions of each KPI, including calculation method, data source, and interpretation guidelines]

### References
- Kaplan, R. S., & Norton, D. P. (1992). The Balanced Scorecard—Measures that Drive Performance. *Harvard Business Review*.
- Kaplan, R. S., & Norton, D. P. (2001). *The Strategy-Focused Organization*.

---

*Balanced Scorecard generated by NioPD Strategic Analysis*

---

### Step 14: Save the Balanced Scorecard
- Generate filename: `[YYYYMMDD]-[organization_slug]-balanced-scorecard-v[version].md`
- Save to: `niopd-workspace/reports/[filename]`

### Step 15: Confirm and Conclude
- Confirm: "✅ I've created a comprehensive Balanced Scorecard for **<organization>**."
- Provide file path: `niopd-workspace/reports/[YYYYMMDD]-[organization_slug]-balanced-scorecard-v[version].md`
- Suggest next steps:
    - "Consider scheduling a quarterly review meeting to track KPI progress."
    - "Use `/niopd:ST:swot` to analyze strategic position."
    - "Use `/niopd:PM:kpis` to set up detailed KPI tracking."

## Error Handling
- **Missing Strategic Context:** If vision/strategy is unclear, guide user through strategic planning basics before creating scorecard.
- **Too Many Metrics:** If user suggests >25 total metrics, warn about scorecard bloat and help prioritize to 15-20 critical measures.
- **Weak KPIs:** If KPIs don't link to strategy, challenge user to identify metrics that truly drive strategic objectives.
- **Unbalanced Perspectives:** If one perspective dominates, remind user of the importance of balance and help identify objectives in underrepresented perspectives.
- **No Strategic Linkages:** If objectives appear disconnected, facilitate creation of strategy map to show cause-and-effect relationships.

In all cases, maintain a collaborative tone, explain Balanced Scorecard principles, and help the user create a strategically aligned performance management system.