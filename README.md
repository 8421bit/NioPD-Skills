# NioPD

Agent Skills for AI-powered Product Management with Claude Code.

NioPD (Nio Product Director) transforms Claude Code into a **Virtual Product Expert Team**, giving every Product Manager instant access to 65 specialized agent skills across 10 domains—all orchestrated by an AI partner named **Nio**.

> *"User-led, Nio-coordinated, Expert-executed"*

These skills follow the [Agent Skills specification](https://agentskills.io/specification) and are designed for use with Claude Code.

## Installation

### Marketplace

```bash
/plugin marketplace add 8421bit/NioPD-Skills
/plugin install niopd@NioPD-Skills
```

### Manually

Add the contents of this repo to a `/.claude` folder in the root of your project directory. See the [official Claude Skills documentation](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) for more details.

## Quick Start

```bash
# Initialize workspace
/niopd:init

# Start a conversation with Nio
/niopd:hi

# Create a new product initiative
/niopd-BS-new-initiative

# Generate a PRD
/niopd-PD-draft-prd
```

## Skills

### Core Commands (Root)

| Command | Description |
|:---|:---|
| `/niopd:init` | Initialize NioPD workspace |
| `/niopd:hi` | Start a conversation with Nio |
| `/niopd:help` | Display help information |
| `/niopd:note` | Add a quick note |
| `/niopd:reflect` | Review workflows and suggest improvements |

### Domain Skills (10 Namespaces)

| Domain | Namespace | Skills | Examples |
|:---|:---|:---|:---|
| **Business Strategy** | `BS` | 3 | `/niopd-BS-new-initiative`, `/niopd-BS-feature-planning` |
| **Deep Thinking** | `DT` | 4 | `/niopd-DT-first-principles`, `/niopd-DT-five-whys` |
| **Market Research** | `MR` | 7 | `/niopd-MR-competitor`, `/niopd-MR-trends` |
| **User Research** | `UR` | 9 | `/niopd-UR-personas`, `/niopd-UR-feedback` |
| **Strategic Analysis** | `ST` | 11 | `/niopd-ST-swot`, `/niopd-ST-canvas` |
| **Product Development** | `PD` | 8 | `/niopd-PD-draft-prd`, `/niopd-PD-stories` |
| **Project Management** | `PM` | 10 | `/niopd-PM-roadmap`, `/niopd-PM-kpis` |
| **Product Operations** | `PO` | 5 | `/niopd-PO-faq`, `/niopd-PO-stakeholder-update` |
| **System** | `SYS` | 4 | `/niopd:SYS:update`, `/niopd:SYS:new-command` |
| **Visualization** | `VIS` | 1 | `/niopd-VIS-visualizer` |

### Recommended Workflow

```
Discovery → Strategy → Requirements → Design → Execution

1. /niopd-BS-new-initiative → /niopd-MR-* → /niopd-UR-* → /niopd-ST-*
2. /niopd-PD-draft-mrd → /niopd-PD-draft-psd
3. /niopd-PD-draft-prd → /niopd-PD-stories
4. /niopd-PD-journey → /niopd-PD-process → /niopd-PD-roadmap
5. /niopd-PM-* → /niopd-PO-*
```

## Workspace Structure

NioPD organizes your work into a standardized directory structure:

```
Project Root/
├── 01-sources/    # Brainstorming, Raw Data (BS, DT)
├── 02-reports/    # Analysis, Research (UR, MR, ST)
├── 03-docs/       # PRDs, Specs (PD, PO)
└── 04-plans/      # Roadmaps, Tracking (PM)
```

## License

MIT
