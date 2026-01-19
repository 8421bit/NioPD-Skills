---
name: niopd-vis-visualizer
description: A universal visualization engine supporting Flowcharts, Sequence Diagrams, C4 Architecture, Mindmaps, Timing Diagrams, Entity-Relationship (ER) Diagrams, Gantt Charts, and Freeform Sketches. Intelligently selects between Mermaid, Excalidraw, PlantUML, D2, Markmap, and WaveDrom.
---

# Universal Visualizer Skill (Ultra SOTA)

This skill is the **Central Visualization Engine** for NioPD. It intelligently selects the best diagramming tool based on user intent and content type, then generates industry-standard visualizations with strict syntax validation and semantic styling.

## 1. Engine Selection Logic (The "Brain")

**Analyze the user's request and content to select the best engine:**

| Engine | Primary Strength | Use Case |
| :--- | :--- | :--- |
| **Excalidraw** | Creative/Presentation | High-end reports, Pitch decks, UI/UX, hierarchies, "Visual First" |
| **Mermaid** | Logic/Workflow | PRD flows, Sequence maps, State diagrams, Quick technical docs |
| **PlantUML** | Architecture (C4) | **C4 Models** (System/Container), Complex Enterprise UML |
| **D2** | Modern Clarity | Cloud Architecture, Entity Relationship, complex layouts (`tala`) |
| **Markmap** | Rapid Hierarchy | Brainstorming, Taxonomy, Content breakdown |
| **WaveDrom** | Timing/Hardware | API Latency, Protocol Handshake, Hardware flows |

**Selection Heuristics:**
1. **"Story/Pitch/Concept"** OR **"Excalidraw"** → **Excalidraw**
2. **"Architecture/C4/System"** → **PlantUML** (or Mermaid C4 if simple)
3. **"Workflow/Logic/Sequence"** → **Mermaid**
4. **"Brainstorming/Structure"** → **Markmap**
5. **"Timing/Latency"** → **WaveDrom**
6. **"Complex Topology"** → **D2**

---

## 2. Mermaid Workflow (Logic & Process)

**Reference**: [mermaid-rules.md](references/mermaid-rules.md)

### 2.1 Diagram Types & Configuration
**Choose diagram type based on content:**

| Type | Best For | Configuration Options |
|:--- |:--- |:--- |
| **Process Flow** (`graph TB/LR`) | Workflows, decision trees, sequential steps | `layout`: "vertical" (TB) or "horizontal" (LR)<br>`style`: "professional" |
| **Circular Flow** (`graph TD`) | Cyclic processes, feedback loops | Use curved connection lines |
| **Comparison** (`graph TB`) | A vs B analysis, before/after | Parallel subgraphs |
| **Mindmap** (`mindmap`) | Hierarchical breakdowns | Radial layout |
| **Sequence** (`sequenceDiagram`) | Interactions over time, API calls | `autonumber` |
| **State** (`stateDiagram`) | Lifecycle stages, status transitions | State nodes |

**Configuration Parameters:**
- **Layout**: `direction` (TB/LR/RL/BT), `aspect` (portrait/landscape).
- **Detail Level**: `simple` (core steps), `standard` (balanced), `detailed` (full annotations).
- **Style**: `professional` (Semantic colors), `minimal` (Monochrome), `colorful` (Vibrant).

### 2.2 Critical Syntax Rules (Error Prevention)
**Always follow these rules to prevent parsing errors:**
1. **List Syntax Conflict**: `[1. Perception]` triggers list parser. 
   - ✅ RIGHT: `[1.Perception]`, `[① Perception]`, `[(1) Perception]`, `[Step 1: Perception]`.
2. **Subgraph Naming**: Spaces break rendering. 
   - ✅ RIGHT: `subgraph agent["AI Agent Core"]`.
3. **Node References**: ALWAYS use IDs. 
   - ✅ RIGHT: `A --> B`. ❌ WRONG: `"Start" --> "End"`.
4. **Special Characters**: 
   - Quotes: `『』`. Parentheses: `「」`.

### 2.3 Semantic Color Scheme (Standard Professional Palette)
- **Green** (#d3f9d8/#2f9e44): Input, perception, start states
- **Red** (#ffe3e3/#c92a2a): Planning, decision points, risks
- **Purple** (#e5dbff/#5f3dc4): Processing, reasoning, AI logic
- **Orange** (#ffe8cc/#d9480f): Actions, tool usage
- **Blue** (#e7f5ff/#1971c2): Metadata, definitions, titles

---

## 3. Excalidraw Workflow (Visuals & Presentation)

**Reference**: [excalidraw-rules.md](references/excalidraw-rules.md)

### 3.1 Diagram Types & Selection Guide

| Type | Use Case | Implementation Strategy |
|------|---------|-------------------------|
| **Flowchart** | Workflows, Steps | Connect rectangles with arrows (Sticky mode) |
| **Mind Map** | Brainstorming, Ideas | Central ellipse with radiating lines |
| **Hierarchy** | Org Charts, Structure | Top-down tree structure |
| **Relationship** | Dependencies | Connected clusters or shapes |
| **Comparison** | A/B Analysis | Two columns (Frames) or side-by-side |
| **Timeline** | Roadmaps | Horizontal axis with milestones |
| **Matrix** | Strategy/Priority | 2x2 Quadrants (Frames) |
| **Freeform** | Sketches | Unrestricted placement |

### 3.2 Design Rules & Element Template
**Strict Design Rules:**
- **Font**: `fontFamily: 5` (Excalifont) is MANDATORY.
- **Text**: Replace `"` with `『』`, `()` with `「」`.
- **Sizes**: Title 24-28px, Subtitle 18-20px, Body 14-16px.
- **Layout**: Keep elements within 0-1200 x 0-800.

**Element Template (Required Fields):**
```json
{
  "id": "unique-id", "type": "rectangle",
  "x": 100, "y": 100, "width": 200, "height": 50,
  "strokeColor": "#1e40af", "backgroundColor": "#dbeafe",
  "fillStyle": "solid", "strokeWidth": 2, "strokeStyle": "solid",
  "roughness": 1, "opacity": 100, "groupIds": [], "roundness": {"type": 3},
  "seed": 123456789, "version": 1, "isDeleted": false, "boundElements": []
}
```

### 3.3 Strict Output Format (Obsidian Compatible)
**You MUST strictly follow this structure without modification:**

```markdown
---
excalidraw-plugin: parsed
tags: [excalidraw]
---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'

# Excalidraw Data

## Text Elements
%%
## Drawing
```json
{ ... JSON DATA ... }
```
%%
```

### 3.4 Auto-Save & User Feedback Workflow
1. **Filename**: Generate meaningful name `[Topic].[Type].md`.
2. **Save**: `write_to_file` to current directory.
3. **Notify User (Strict Template)**:
   ```markdown
   ✅ Excalidraw diagram generated!
   
   📍 Saved to:
   [Filename]
   
   🎨 Design Choice:
   I selected "[Type]" to visualize...
   
   📖 How to View:
   1. Open in Obsidian
   2. Menu -> "Switch to EXCALIDRAW VIEW"
   ```

---

## 4. Other Engines (Specialized)

### 4.1 PlantUML (C4 Architecture)
**Reference**: [plantuml-rules.md](references/plantuml-rules.md)
- **Use for**: Detailed C4 System/Container diagrams.
- **Rule**: Include C4 URLs (`!include .../C4_Context.puml`).

### 4.2 D2 (Complex Layouts)
**Reference**: [d2-rules.md](references/d2-rules.md)
- **Use for**: Auto-layout of messy graphs (`layout: tala`).
- **Rule**: Nesting with `{}`.

### 4.3 Markmap (Mindmaps)
**Reference**: [markmap-rules.md](references/markmap-rules.md)
- **Use for**: Instant text-to-map.
- **Rule**: Standard Markdown headers `#` and list items `-`.

### 4.4 WaveDrom (Timing)
**Reference**: [wavedrom-rules.md](references/wavedrom-rules.md)
- **Use for**: Hardware/API Timing.
- **Rule**: Valid JSON signal object.

---

## 5. Quality Checklist

- [ ] **Engine Selection**: Correct engine chosen for the use case?
- [ ] **Mermaid Syntax**: No "number. space" lists? IDs used for links?
- [ ] **Excalidraw Format**: Strict Markdown wrapper? `fontFamily: 5`?
- [ ] **Data Safety**: Quotes/Parentheses escaped?
- [ ] **Semantics**: Colors match the NioPD standard?
