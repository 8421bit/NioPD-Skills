# NioPD (Nio Product Director) System

> **Next-Generation AI Product Management Toolkit**
> _"User-led, Nio-coordinated, Expert-executed"_

**NioPD** is a Claude Code Plugin designed to transform Claude Code into a **Virtual Product Expert Team**. It provides every Product Manager with instant access to 67 specialized agent skills, 10 expert domains, and a dedicated AI partner named **Nio**.

---

## 🚀 Core Capabilities (v1.1)

### 1. The Virtual Expert Team
NioPD is not just a collection of prompts; it's a structured organization:
- **Product Manager (You)**: The leader and decision-maker.
- **Nio (Core Agent)**: Your Virtual Head of Product, orchestrating workflows and guiding strategy.
- **Domain Experts (Sub-agents)**: Specialized agents for specific tasks (User Research, Data Analysis, etc.).

### 2. Comprehensive Toolset
Everything you need to ship world-class products:
- **67 Intelligent Commands**: Structured workflows for every PM task.
- **10 Strategic Domains**: From deep thinking to execution.
- **Universal Visualizer**: SOTA diagram generation (Mermaid, Excalidraw, PlantUML, etc.).
- **Smart Templates**: Standardized document output.

---

## 📂 Command Namespaces (10 Domains)

| Domain | Namespace | Description | Commands |
| :--- | :--- | :--- | :--- |
| **System** | `SYS` | System initialization, upgrades, and evolution | 7 |
| **Business Strategy** | `BS` | Initiative planning and market opportunity | 3 |
| **Deep Thinking** | `DT` | First principles, 5-Whys, Socratic reasoning | 4 |
| **Market Research** | `MR` | Competitor analysis, pricing, trends | 7 |
| **User Research** | `UR` | Personas, JTBD, interviews, surveys | 9 |
| **Strategic Analysis** | `ST` | SWOT, Business Canvas, RICE, Porter's 5 | 11 |
| **Product Dev** | `PD` | PRD/MRD drafts, user stories, roadmaps | 10 |
| **Project Mgmt** | `PM` | Agile planning, release tracking, KPIs | 10 |
| **Product Ops** | `PO` | AARRR metrics, Customer Success, FAQ | 5 |
| **Visualization** | `VIS` | **[NEW]** Universal Diagram Generator | 1 |

**👉 Usage**: `/niopd:<NAMESPACE>:<command>`  
*(Example: `/niopd:UR:personas` or `/niopd:VIS:visualizer`)*

---

## 🏗️ Workspace Structure (v1.1)

NioPD uses a standardized, clean directory structure to keep your thinking and execution organized:

```bash
Project Root/
├── 01-sources/    # Brainstorming, Raw Data, Strategic Inputs (BS, DT)
├── 02-reports/    # Analysis, Research Findings, Market Studies (UR, MR, ST)
├── 03-docs/       # Official Documents, PRDs, Specs (PD, PO)
└── 04-plans/      # Execution Plans, Roadmaps, Tracking (PM)
```

> **Note**: This structure is automatically maintained by Nio. Files are named using the `[YYYYMMDD]-<identifier>-<type>-v[Ver].md` convention.

---

## 🛠️ Quick Start

1. **Initialize**:
   Run the initialization command to set up your workspace:
   ```bash
   /niopd:SYS:init
   ```

2. **Start a Task**:
   Example - Create a new feature initiative:
   ```bash
   /niopd:BS:new-initiative
   ```

3. **Visualize Ideas**:
   Example - Draw a flowchart:
   ```bash
   /niopd:VIS:visualizer "User login flow with 2FA"
   ```

---

## 🧠 Core Philosophy

1.  **Document-Driven**: Every thought should lead to a traceable artifact.
2.  **Think First**: Use Deep Thinking (DT) tools before jumping to solutions.
3.  **Data-Centric**: Decisions should be backed by research (UR/MR) and metrics.
4.  **Evolutionary**: NioPD grows with you—create new agents and commands as you need them.

---

*Powered by NioPD Plugin for Claude Code*
