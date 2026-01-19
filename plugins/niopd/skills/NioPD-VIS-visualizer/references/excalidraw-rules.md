# Excalidraw Ultra SOTA Rules & Technical Reference

This document is the definitive guide for generating Excalidraw diagrams in NioPD. It combines the official JSON schema with NioPD's Ultra SOTA design philosophy.

## 1. Color Palette (NioPD Premium)

### Primary Colors
| Purpose | Color | Hex | Use Case |
|---------|-------|-----|----------|
| Main Title | Deep Blue | `#1e40af` | Top-level headers |
| Subtitle | Medium Blue | `#3b82f6` | Section headers, connect lines |
| Body Text | Dark Gray | `#374151` | Standard labels, notes |
| Emphasis | Orange | `#f59e0b` | Key insights, calls to action |
| Success | Green | `#10b981` | Approved states, success paths |
| Warning | Red | `#ef4444` | Errors, blockers, risks |

### Background Colors
| Purpose | Color | Hex | Use Case |
|---------|-------|-----|----------|
| Light Blue | Background | `#dbeafe` | Primary container fill |
| Light Gray | Neutral | `#f3f4f6` | Disabled/Inactive states |
| Light Orange | Highlight | `#fef3c7` | Warning containers |
| Light Green | Success | `#d1fae5` | Success containers |
| Light Purple | Accent | `#ede9fe` | Special grouping |

## 2. Element Types (JSON Templates)

### Rectangle
```json
{
  "type": "rectangle",
  "id": "unique-id",
  "x": 100,
  "y": 100,
  "width": 200,
  "height": 80,
  "strokeColor": "#1e40af",
  "backgroundColor": "#dbeafe",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "roughness": 1,
  "opacity": 100,
  "roundness": { "type": 3 },
  "seed": 123456789,
  "version": 1,
  "isDeleted": false,
  "boundElements": []
}
```

### Text (Strict Rules: `fontFamily: 5`)
```json
{
  "type": "text",
  "id": "unique-id",
  "x": 150,
  "y": 130,
  "text": "Content here",
  "fontSize": 20,
  "fontFamily": 5,
  "textAlign": "center",
  "verticalAlign": "middle",
  "strokeColor": "#1e40af",
  "backgroundColor": "transparent",
  "originalText": "Content here",
  "autoResize": true,
  "lineHeight": 1.25
}
```

### Arrow (Sticky)
```json
{
  "type": "arrow",
  "id": "unique-id",
  "x": 300,
  "y": 140,
  "width": 100,
  "height": 0,
  "points": [[0, 0], [100, 0]],
  "strokeColor": "#374151",
  "strokeWidth": 2,
  "startArrowhead": null,
  "endArrowhead": "arrow",
  "startBinding": { "elementId": "src-id", "focus": 0, "gap": 5 },
  "endBinding": { "elementId": "tgt-id", "focus": 0, "gap": 5 }
}
```

### Ellipse
```json
{
  "type": "ellipse",
  "id": "unique-id",
  "x": 100,
  "y": 100,
  "width": 120,
  "height": 120,
  "strokeColor": "#10b981",
  "backgroundColor": "#d1fae5",
  "fillStyle": "solid"
}
```

### Diamond
```json
{
  "type": "diamond",
  "id": "unique-id",
  "x": 100,
  "y": 100,
  "width": 150,
  "height": 100,
  "strokeColor": "#f59e0b",
  "backgroundColor": "#fef3c7",
  "fillStyle": "solid"
}
```

### Line
```json
{
  "type": "line",
  "id": "unique-id",
  "x": 100,
  "y": 100,
  "points": [[0, 0], [200, 100]],
  "strokeColor": "#374151",
  "strokeWidth": 2
}
```

## 3. Full JSON Structure

```json
{
  "type": "excalidraw",
  "version": 2,
  "source": "https://excalidraw.com",
  "elements": [
    // Array of elements
  ],
  "appState": {
    "gridSize": null,
    "viewBackgroundColor": "#ffffff",
    "theme": "light",
    "currentItemFontFamily": 5
  },
  "files": {}
}
```

## 4. Technical Specifications

### Font Family
| Value | Font Name | Note |
|-------|-----------|------|
| 1 | Virgil | |
| 5 | **Excalifont** | **MANDATORY for NioPD** |

### Fill Styles
- `solid` (Default), `hachure`, `cross-hatch`, `dots`.

### Roundness
- `{ "type": 3 }` (Full Rounding) is recommended for organic feel.

## 5. Advanced Logic & Bindings

### 5.1 Container Binding
Connect text to a shape so they move together:
```json
// Rectangle
{ "id": "rect-1", "boundElements": [{ "id": "text-1", "type": "text" }] }
// Text
{ "id": "text-1", "containerId": "rect-1" }
```

### 5.2 Frame & Grouping Logic (Ultra SOTA)
- **Frames (type: "frame")**: Used to create slide-like boundaries.
- **Ordering Rule**: Frame children must appear **BEFORE** the Frame element in the `elements` array.
  - `[child1, child2, frame1]` ✅
  - `[frame1, child1, child2]` ❌
- **Group Management**: Logical blocks should share `groupIds: ["grid-id-1"]`.

## 6. Diagram Types Selection

| 类型 | 英文 | 使用场景 |
|------|------|---------|
| **流程图** | Flowchart | Workflow logic |
| **思维导图** | Mind Map | Brainstorming |
| **层级图** | Hierarchy | Org charts |
| **对比图** | Comparison | A/B analysis |
| **时间线图** | Timeline | Roadmaps |
| **矩阵图** | Matrix | 2x2 Quadrants |

## 7. Design Rules

### 7.1 Text & Format
- **Strict Font**: `fontFamily: 5`.
- **Formatting**: Replace `"` with `『』`, `()` with `「」`.
- **Sizes**: Title 24-28px, Subtitle 18-20px, Body 14-16px.

### 7.2 Semantic Layering
- **Layer 0 (Background)**: Large faint shapes defining regions/frames.
- **Layer 1 (Boxes)**: Core entities.
- **Layer 2 (Connections)**: Arrows.
- **Layer 3 (Overlays)**: Post-it notes (`#fff3bf`).

### 7.3 Mathematical Alignment
- **Centering**: To center text `T` in box `B`:
  - `T.x = B.x + (B.width - T.width) / 2`
  - `T.y = B.y + (B.height - T.height) / 2`

## 8. Implementation Workflow

### Step 1: Analyze & Select
Choose diagram type based on Section 6.

### Step 2: Markdown Generation (Strict)
Must use this exact wrapper:
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
{ "... COMPLETE JSON DATA ..." }
```
%%
```

### Step 3: Validation
- Check valid JSON.
- Check `fontFamily: 5`.
- Check Frame ordering.
