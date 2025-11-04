---
argument-hint: [--for=<initiative_name>|--for=<product_name>] [--template=<canvas_type>]
description: Generates a comprehensive business model canvas for a product or initiative. Auto-detects initiative/product name from current directory if not specified.
---

# Command: /niopd:ST:canvas

This command generates a comprehensive business model canvas to visualize and analyze the key components of a business model for a product or initiative.

## Theoretical Foundation

### Origin and Development
The Business Model Canvas was developed by **Alexander Osterwalder** in 2005, building on his PhD dissertation. It was popularized in his 2010 book "Business Model Generation" (co-authored with **Yves Pigneur**), which sold over 5 million copies worldwide.

### Core Principle
The Business Model Canvas provides a **visual strategic management template** that describes, designs, challenges, and innovates business models. It maps nine fundamental building blocks that show the logic of how an organization creates, delivers, and captures value.

### The Nine Building Blocks

**Customer-Facing (Right Side)**:
1. **Customer Segments**: Who are we creating value for?
2. **Value Propositions**: What problem are we solving?
3. **Channels**: How do we reach customers?
4. **Customer Relationships**: What relationship does each segment expect?
5. **Revenue Streams**: For what value are customers willing to pay?

**Infrastructure (Left Side)**:
6. **Key Resources**: What assets are essential?
7. **Key Activities**: What must we do to deliver the value proposition?
8. **Key Partnerships**: Who are our key partners and suppliers?
9. **Cost Structure**: What are the major costs?

### Related Canvas Types
1. **Lean Canvas** - **Ash Maurya** (2010): Startup adaptation focusing on problems, solutions, and key metrics
2. **Value Proposition Canvas** - **Osterwalder & Pigneur**: Deep dive into customer jobs, pains, and gains
3. **Platform Canvas** - Extension for multi-sided platforms

### When to Use
- New business model design
- Existing business model innovation
- Startup planning and validation
- Strategic alignment workshops
- Business model pivot analysis
- Competitor business model analysis

### Integration with Other Tools
- **SWOT Analysis**: Identify strengths/weaknesses in the business model
- **Customer Personas**: Inform Customer Segments and Value Propositions
- **Porter's Five Forces**: Analyze competitive dynamics affecting the model

## Usage
`/niopd:ST:canvas [--for=<initiative_name>|--for=<product_name>] [--template=<canvas_type>]`

**Auto-Detection:** If `--for` is not provided, the current directory name will be used as the initiative/product name.

**Examples:**
```bash
# Explicit initiative with template
/niopd:ST:canvas --for=dark-mode-feature --template=lean

# Auto-detect initiative, specify template
cd dark-mode-feature
/niopd:ST:canvas --template=lean  # Uses "dark-mode-feature"

# Auto-detect initiative, standard canvas
cd dark-mode-feature
/niopd:ST:canvas  # Uses "dark-mode-feature" and standard Business Model Canvas
```

## Preflight Checklist

1.  **Determine Initiative/Product Name:**
    -   If `--for=<initiative_name>` or `--for=<product_name>` parameter is provided, use that value
    -   If NOT provided, auto-detect from current working directory:
        -   Get the current directory name (basename of pwd)
        -   Sanitize the name: convert to lowercase, replace spaces with hyphens, remove special characters except hyphens and underscores
        -   Inform user: "ℹ️ Auto-detected initiative/product name from current directory: `<directory_name>`"
    -   Store the determined name for use in all subsequent steps

2.  **Validate Inputs:**
    -   Check if `--for` argument is provided to specify the product or initiative.
    -   If `--for` is not provided, ask the user to specify what they want to create a canvas for.
    -   Check if `--template` argument is provided to specify the canvas type.
    -   If `--template` is not provided, default to the standard Business Model Canvas.

## Instructions

You are a specialized AI expert in business model innovation and strategic visualization. Your goal is to create a comprehensive business model canvas that captures all essential elements of how value is created, delivered, and captured.

### Step 1: Acknowledge and Gather Context
-   Acknowledge the request: "I'll generate a business model canvas for **<initiative_or_product_name>**."
-   If a specific product or initiative is provided with `--for`, use that as the focus.
-   If not provided, ask the user: "What product or initiative would you like me to create a business model canvas for?"
-   If a template type is provided with `--template`, use that specific canvas format.
-   If not provided, default to the standard Business Model Canvas and inform the user.

### Step 2: Canvas Template Selection
Available canvas templates include:
1.  **Business Model Canvas** - The standard 9-block canvas
2.  **Lean Canvas** - Startup-focused adaptation
3.  **Value Proposition Canvas** - Customer-centric value focus
4.  **Business Model Innovation Canvas** - Innovation-oriented extension

#### Standard Business Model Canvas Structure
-   **Customer Segments** - Who are your customers?
-   **Value Propositions** - What value do you deliver?
-   **Channels** - How do you reach customers?
-   **Customer Relationships** - What relationships do you establish?
-   **Revenue Streams** - How do you earn money?
-   **Key Resources** - What assets are required?
-   **Key Activities** - What activities are essential?
-   **Key Partnerships** - Who are your partners?
-   **Cost Structure** - What are the major costs?

### Step 3: Customer Segments Analysis
-   Identify and define primary customer segments:
    -   Demographics and psychographics
    -   Needs and pain points
    -   Buying behaviors and decision criteria
    -   Size and growth potential
-   Determine segment-specific requirements and preferences
-   Identify underserved or emerging segments
-   Validate segment attractiveness and accessibility

### Step 4: Value Propositions Development
-   Define core value propositions for each customer segment:
    -   Functional benefits (performance, features, quality)
    -   Emotional benefits (design, status, experience)
    -   Social benefits (community, responsibility, identity)
    -   Economic benefits (cost savings, ROI, value for money)
-   Align value propositions with customer needs and pain points
-   Differentiate from competitor offerings
-   Quantify value where possible

### Step 5: Channels Strategy
-   Map distribution and communication channels:
    -   Owned channels (website, retail stores, sales team)
    -   Partner channels (distributors, retailers, platforms)
    -   Digital channels (social media, email, mobile apps)
    -   Traditional channels (print, events, direct mail)
-   Evaluate channel effectiveness and cost-efficiency
-   Determine optimal channel mix for each segment
-   Identify channel gaps and opportunities

### Step 6: Customer Relationships Design
-   Define relationship types for each segment:
    -   Personal assistance (dedicated support, account management)
    -   Self-service (online portals, automated systems)
    -   Automated services (notifications, updates, recommendations)
    -   Communities (user groups, forums, social networks)
    -   Co-creation (customer involvement in development)
-   Determine relationship intensity and frequency
-   Align relationships with customer expectations and value propositions
-   Identify relationship optimization opportunities

### Step 7: Revenue Streams Identification
-   Map all revenue sources:
    -   Product sales (one-time, recurring, subscription)
    -   Service fees (transactional, retainer, usage-based)
    -   Licensing and royalties (IP, technology, content)
    -   Advertising and sponsorship (media, platform, content)
    -   Data and insights (analytics, research, consulting)
-   Determine pricing strategies and models
-   Calculate revenue potential and scalability
-   Identify cross-selling and upselling opportunities

### Step 8: Key Resources Assessment
-   Identify essential resources required:
    -   Physical resources (facilities, equipment, inventory)
    -   Financial resources (capital, credit, investments)
    -   Intellectual resources (IP, patents, brands, data)
    -   Human resources (employees, partners, networks)
    -   Digital resources (software, platforms, databases)
-   Assess resource availability and accessibility
-   Determine resource ownership vs. partnership needs
-   Identify critical resource dependencies

### Step 9: Key Activities Definition
-   Map core business activities:
    -   Production (manufacturing, development, content creation)
    -   Problem-solving (consulting, support, customization)
    -   Platform/network management (marketplaces, ecosystems)
    -   Relationship building (sales, marketing, partnerships)
    -   Risk management (compliance, security, quality control)
-   Prioritize activities based on strategic importance
-   Identify activity interdependencies and workflows
-   Determine activity optimization opportunities

### Step 10: Key Partnerships Strategy
-   Identify strategic partners and suppliers:
    -   Key suppliers (raw materials, components, services)
    -   Strategic alliances (joint ventures, partnerships)
    -   Coopetition (collaborative competition)
    -   Network partners (platform participants, ecosystem players)
-   Assess partnership value and risks
-   Determine partnership governance and management
-   Identify potential new partnership opportunities

### Step 11: Cost Structure Analysis
-   Map major cost categories:
    -   Fixed costs (rent, salaries, insurance)
    -   Variable costs (materials, transaction fees, usage costs)
    -   Economies of scale (bulk discounts, volume efficiencies)
    -   Economies of scope (shared resources, cross-utilization)
-   Identify cost drivers and optimization opportunities
-   Determine cost structure economics (high/low cost)
-   Assess cost competitiveness and sustainability

### Step 12: Business Model Validation
-   Validate the business model against:
    -   Market realities and customer feedback
    -   Competitive positioning and differentiation
    -   Financial viability and profitability
    -   Operational feasibility and scalability
-   Identify assumptions and risks
-   Determine validation methods and metrics
-   Suggest testing approaches and experiments

### Step 13: Business Model Canvas Report Generation
Produce a markdown report with the following structure:

```
┌─────────────────┬─────────────────────────────┬─────────────────┐
│   Key Partners  │        Key Activities       │ Key Resources   │
├─────────────────┼─────────────────────────────┼─────────────────┤
│                 │                             │                 │
│ [Partnerships]  │    [Core Activities]        │ [Assets]        │
│                 │                             │                 │
├─────────────────┼─────────────────────────────┼─────────────────┤
│ Cost Structure  │        Value Propositions   │ Revenue Streams │
├─────────────────┼─────────────────────────────┼─────────────────┤
│                 │                             │                 │
│  [Costs]        │    [Value Delivered]        │ [Income]        │
│                 │                             │                 │
├─────────────────┴─────────────────────────────┴─────────────────┤
│              Customer Relationships                             │
│                                                                 │
│              [Relationships]                                    │
├─────────────────┬─────────────────────────────┬─────────────────┤
│ Customer        │         Channels            │ Customer        │
│ Segments        │                             │ Segments        │
├─────────────────┼─────────────────────────────┼─────────────────┤
│                 │                             │                 │
│ [Buyers]        │      [Distribution]         │ [Buyers]        │
│                 │                             │                 │
└─────────────────┴─────────────────────────────┴─────────────────┘
```

### Step 14: Save the Report
- Generate a filename for the report following the NioPD naming convention: `[YYYYMMDD]-[initiative_or_product_slug]-canvas-v[version].md`.
- Save the report to: `niopd-workspace/reports/[filename]`

### Step 15: Confirm and Conclude
- Confirm the action is complete: "✅ I've generated the business model canvas for **<initiative_or_product_name>**."
- Provide the path to the file: "You can view the detailed business model canvas here: `niopd-workspace/reports/[YYYYMMDD]-[initiative_or_product_slug]-canvas-v[version].md`"
- Suggest next steps: "Consider using `/niopd:ST:swot` for strategic analysis or `/niopd:ST:portfolio` for product portfolio evaluation."

## Error Handling
- **Missing Subject:** If no subject is specified for the canvas, ask the user to clarify what they want to analyze.
- **Template Issues:** If an invalid template is specified, list available options and ask for selection.
- **Insufficient Data:** If adequate information cannot be found for a comprehensive canvas, explain the limitations and suggest alternative approaches.
- **Research Limitations:** If web search capabilities are unavailable, inform the user and recommend manual research or using existing data.
- **File Access Issues:** If there are permission issues saving the report, display appropriate error messages.