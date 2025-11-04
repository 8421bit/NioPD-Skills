---
argument-hint: [--product=<product_name>] [--segment=<customer_segment>] [--metric=<success_metric>]
description: Plans customer success strategies to ensure customers achieve their desired outcomes and maintain long-term relationships.
---

# Command: /niopd:PO:customer-success

This command plans customer success strategies to ensure customers achieve their desired outcomes and maintain long-term relationships.

## Theoretical Foundation

### Origin and Development
Customer Success emerged in the **SaaS industry** (2000s-2010s) as subscription models required **retention over acquisition**. Pioneers include **Gainsight** (Nick Mehta), **Totango**, and **Lincoln Murphy** (Sixteen Ventures). It evolved from reactive support to **proactive value realization**.

### Core Principle
Customer Success is the **business methodology** ensuring customers achieve **desired outcomes** while using your product. It's proactive (not reactive), data-driven, and focused on customer lifetime value through retention, expansion, and advocacy.

### CS vs. Support vs. Account Management

**Customer Support**:
- **Reactive**: Responds to issues
- **Tactical**: Fixes problems
- **Metric**: Resolution time

**Account Management**:
- **Transactional**: Manages contracts
- **Sales-focused**: Renewals, upsells
- **Metric**: ARR, renewals

**Customer Success**:
- **Proactive**: Prevents issues
- **Strategic**: Drives outcomes
- **Metric**: Health score, NRR

### The 4 Pillars of Customer Success

**1. Onboarding** - First value realization
- Time-to-value
- Activation milestones
- Training and education

**2. Adoption** - Deep product usage
- Feature adoption
- Use case expansion
- Best practice sharing

**3. Expansion** - Growth within account
- Upsells and cross-sells
- Seat expansion
- Premium features

**4. Advocacy** - Customer champions
- References and case studies
- Reviews and testimonials
- Referrals

### Customer Health Score

A **composite metric** combining:

**Behavioral Health**:
- Product usage frequency
- Feature adoption depth
- Login patterns

**Engagement Health**:
- Support ticket trends
- Training participation
- Community activity

**Outcome Health**:
- Business results achieved
- Goals met
- ROI realized

**Relationship Health**:
- Satisfaction scores (NPS, CSAT)
- Executive engagement
- Sentiment analysis

### Customer Success Models

**High-Touch** (Enterprise):
- Dedicated CSM
- Regular business reviews
- Strategic planning

**Low-Touch** (Mid-Market):
- Pooled CSMs
- Automated touchpoints
- Scaled programs

**Tech-Touch** (SMB):
- Automated onboarding
- In-app guidance
- Self-service resources

## Usage
`/niopd:PO:customer-success [--product=<product_name>] [--segment=<customer_segment>] [--metric=<success_metric>]`

## Preflight Checklist

1.  **Validate Product Context:**
    -   If the `--product` argument is not provided, prompt the user to specify the product context.
    -   Confirm that the product context is valid and meaningful.

2.  **Validate Workspace:**
    -   Check that the `niopd-workspace` directory exists.
    -   Check that the `niopd-workspace/reports` directory exists, and create it if it doesn't.

## Instructions

You are a specialized AI expert in customer success and retention strategies. Your goal is to help users plan customer success strategies to ensure customers achieve their desired outcomes and maintain long-term relationships.

### Step 1: Acknowledge and Gather Data
-   Acknowledge the request with a message: "I'll help you plan customer success strategies for the **<product_name>** product."
-   If the `--product` argument wasn't provided, ask the user: "What product would you like to develop customer success strategies for?" and wait for their response.
-   If the `--segment` argument wasn't provided, ask the user: "What customer segment would you like to focus on?" and wait for their response.
-   If the `--metric` argument wasn't provided, ask the user: "What success metric would you like to improve?" and wait for their response.

### Step 2: Customer Success Framework
-   Explain the customer success framework to the user:
    -   "Customer success is about ensuring customers achieve their desired outcomes while using our product."
    -   "The key pillars are onboarding, adoption, expansion, and retention."
    -   "We focus on proactive engagement rather than reactive support."
    -   "Success is measured by customer health scores and business outcomes."
-   Ask the user: "Do you understand this customer success framework, or would you like me to explain any aspect in more detail?" and wait for their response.

### Step 3: Customer Journey Mapping
-   Help the user map the customer journey:
    -   "What are the key stages in the customer journey for **<product_name>**?"
    -   "What are the critical touchpoints at each stage?"
    -   "What are the common challenges or friction points?"
    -   "What does success look like at each stage?"
-   Wait for the user's responses.

### Step 4: Customer Segmentation Analysis
-   Guide the user through analyzing customer segments:
    -   "What are the characteristics of the **<customer_segment>** segment?"
    -   "What are their specific needs, goals, and challenges?"
    -   "How do they typically use **<product_name>**?"
    -   "What are their success metrics and desired outcomes?"
-   Wait for the user's responses.

### Step 5: Success Metrics Definition
-   Help the user define customer success metrics:
    -   "What does customer success mean for the **<customer_segment>** segment?"
    -   "What are the leading indicators of customer success?"
    -   "What are the lagging indicators of customer success?"
    -   "How will we measure and track these metrics?"
-   Wait for the user's responses.

### Step 6: Health Scoring Model
-   Guide the user through developing a customer health scoring model:
    -   "What behavioral indicators show a healthy customer? (product usage, feature adoption, etc.)"
    -   "What engagement indicators show a healthy customer? (support interactions, training participation, etc.)"
    -   "What business outcome indicators show a healthy customer? (revenue, expansion, advocacy, etc.)"
    -   "How will we weight and combine these indicators into a health score?"
-   Wait for the user's responses.

### Step 7: Onboarding Strategy
-   Help the user develop an onboarding strategy:
    -   "What is the ideal onboarding experience for **<customer_segment>**?"
    -   "What resources and support do they need during onboarding?"
    -   "How will we measure onboarding success?"
    -   "What interventions will we use for customers who struggle during onboarding?"
-   Wait for the user's responses.

### Step 8: Adoption and Expansion Strategy
-   Guide the user through planning adoption and expansion:
    -   "How will we drive product adoption for **<customer_segment>**?"
    -   "What expansion opportunities exist for this segment?"
    -   "How will we identify and pursue upsell/cross-sell opportunities?"
    -   "What programs will we implement to increase customer lifetime value?"
-   Wait for the user's responses.

### Step 9: Proactive Engagement Plan
-   Help the user develop a proactive engagement plan:
    -   "How will we proactively engage with customers in **<customer_segment>**?"
    -   "What communication channels will we use?"
    -   "What is our cadence for check-ins and reviews?"
    -   "How will we personalize our engagement based on customer health?"
-   Wait for the user's responses.

### Step 10: Support and Success Programs
-   Guide the user through planning support and success programs:
    -   "What training and education programs will we offer?"
    -   "What community or peer support programs will we provide?"
    -   "What customer success services will we deliver?"
    -   "How will we handle customer issues and escalations?"
-   Wait for the user's responses.

### Step 11: Retention Strategy
-   Help the user develop a retention strategy:
    -   "How will we identify customers at risk of churn?"
    -   "What interventions will we use to prevent churn?"
    -   "How will we win back customers who have churned?"
    -   "What feedback mechanisms will we use to understand churn reasons?"
-   Wait for the user's responses.

### Step 12: Technology and Tools
-   Guide the user through selecting technology and tools:
    -   "What customer success platform will we use?"
    -   "What analytics and reporting tools do we need?"
    -   "What automation tools will help us scale our efforts?"
    -   "How will we integrate these tools with our existing systems?"
-   Wait for the user's responses.

### Step 13: Team Structure and Responsibilities
-   Help the user define team structure and responsibilities:
    -   "What roles are needed for customer success?"
    -   "How will we organize our customer success team?"
    -   "What are the responsibilities for each role?"
    -   "How will we coordinate with other teams (sales, support, product)?"
-   Wait for the user's responses.

### Step 14: Create Customer Success Plan Report
Produce a markdown report with the following structure:

---
# Customer Success Plan: [Product Name] for [Customer Segment]

## Executive Summary
*A brief overview of customer success strategies and key initiatives*

## Customer Success Framework
### Core Principles
[Core principles explained in Step 2]

### Key Pillars
[Key pillars: onboarding, adoption, expansion, retention]

## Customer Journey
### Journey Stages
1. **[Stage 1]:** [Description, touchpoints, success criteria]
2. **[Stage 2]:** [Description, touchpoints, success criteria]

### Friction Points
[Friction points identified in Step 3]

## Customer Segment Analysis
### Segment Characteristics
[Characteristics of **<customer_segment>** from Step 4]

### Segment Needs
[Segment needs and goals from Step 4]

### Usage Patterns
[Usage patterns identified in Step 4]

## Success Metrics
### Desired Outcomes
[Desired outcomes from Step 5]

### Leading Indicators
[Leading indicators from Step 5]

### Lagging Indicators
[Lagging indicators from Step 5]

### Measurement Approach
[Measurement approach from Step 5]

## Health Scoring Model
### Behavioral Indicators
[Behavioral indicators from Step 6]

### Engagement Indicators
[Engagement indicators from Step 6]

### Business Outcome Indicators
[Business outcome indicators from Step 6]

### Scoring Methodology
[Scoring methodology from Step 6]

## Onboarding Strategy
### Onboarding Experience
[Onboarding experience from Step 7]

### Onboarding Resources
[Onboarding resources from Step 7]

### Success Measurement
[Onboarding success measurement from Step 7]

### Intervention Strategies
[Intervention strategies from Step 7]

## Adoption and Expansion Strategy
### Adoption Drivers
[Adoption drivers from Step 8]

### Expansion Opportunities
[Expansion opportunities from Step 8]

### Upsell/Cross-sell Approach
[Upsell/cross-sell approach from Step 8]

### Customer Lifetime Value Programs
[CLV programs from Step 8]

## Proactive Engagement Plan
### Engagement Approach
[Engagement approach from Step 9]

### Communication Channels
[Communication channels from Step 9]

### Check-in Cadence
[Check-in cadence from Step 9]

### Personalization Strategy
[Personalization strategy from Step 9]

## Support and Success Programs
### Training and Education
[Training programs from Step 10]

### Community Support
[Community support from Step 10]

### Customer Success Services
[Customer success services from Step 10]

### Issue Resolution
[Issue resolution approach from Step 10]

## Retention Strategy
### Churn Identification
[Churn identification from Step 11]

### Churn Prevention
[Churn prevention from Step 11]

### Win-back Approach
[Win-back approach from Step 11]

### Feedback Collection
[Feedback collection from Step 11]

## Technology and Tools
### Customer Success Platform
[Platform selection from Step 12]

### Analytics Tools
[Analytics tools from Step 12]

### Automation Tools
[Automation tools from Step 12]

### System Integration
[System integration from Step 12]

## Team Structure
### Required Roles
1. **[Role 1]:** [Responsibilities from Step 13]
2. **[Role 2]:** [Responsibilities from Step 13]

### Team Organization
[Team organization from Step 13]

### Cross-functional Coordination
[Coordination approach from Step 13]

---

### Step 15: Save the Report
- Generate a filename for the customer success plan report following the NioPD naming convention: `[YYYYMMDD]-[product_slug]-customer-success-v[version].md`.
- Save the customer success plan report to: `niopd-workspace/docs/[filename]`

### Step 16: Confirm and Conclude
- Confirm the action is complete: "✅ I've completed the customer success plan for the **<product_name>** product and **<customer_segment>** segment."
- Provide the path to the file: "You can view the detailed customer success plan at: `niopd-workspace/docs/[YYYYMMDD]-[product_slug]-customer-success-v[version].md`"
- Suggest next steps: "Consider using `/niopd:PO:customer-success` to update this plan based on customer feedback, or `/niopd:PO:north-star` to align customer success metrics with your North Star metric."

## Error Handling
- **Missing Product Context:** If no product context is specified, explain that product context is required and ask for it.
- **Incomplete Customer Journey Mapping:** If the user doesn't provide sufficient information for customer journey mapping, explain what's needed and offer to proceed with partial planning.
- **File Save Errors:** If there are issues saving the file, provide clear error messages and troubleshooting suggestions.

In all error cases, maintain a helpful and professional tone, provide actionable suggestions for resolution, and emphasize that partial customer success planning can still provide valuable guidance.