# Markmap Ultra SOTA Rules & Reference

Markmap (Markdown Mindmaps) transforms structured Markdown into interactive, zoomable mindmaps.

## 1. Syntax Fundamentals

Markmap parses standard Markdown headers and lists.

### 1.1 The Hierarchy
```markdown
# Root Topic (Level 1)
## Main Branch A (Level 2)
### Sub-branch 1 (Level 3)
- Leaf Node 1
- Leaf Node 2
## Main Branch B
```

### 1.2 Inline Formatting
- **Bold**: `**Critical**` for Emphasis.
- *Italic*: `*Note*` for context.
- `Code`: `` `variable` `` for technical terms.
- ~~Strike~~: `~~Deprecated~~` for removed items.

## 2. Advanced Interactivity

### 2.1 Hyperlinks
Make nodes clickable to link to docs or external sites.
```markdown
- [Jira Ticket](https://jira.company.com/browse/PROJ-123)
- [Design Doc](./design.pdf)
```

### 2.2 Mathematical Formulas
Support for KaTeX logic.
```markdown
- Formula: $E=mc^2$
```

### 2.3 Multiline Nodes
Use `<br/>` HTML tags to force breaks in long text.
```markdown
- Very Long Idea<br/>Split for readability
```

## 3. Frontmatter Configuration (JSON)

Enhance the map behavior using a frontmatter block.

```yaml
---
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 2
  maxWidth: 300
---
```

- `colorFreezeLevel`: At what depth colors stop branching (keeps diagram uniform).
- `initialExpandLevel`: How many levels are open by default.
- `maxWidth`: Max width of a node text block.

## 4. Best Practices for "Ultra" Maps

### 4.1 Balance
Keep branches roughly symmetrical. A map with one huge branch and three tiny ones is hard to navigate.

### 4.2 Depth Control
- **Level 1**: The Core Problem/Topic.
- **Level 2**: The Pillars/Categories.
- **Level 3**: The Items/Arguments.
- **Level 4**: (Optional) Micro-details. *Avoid going deeper.*

### 4.3 Node Concise Rule
Keep node text strictly under **5-7 words**. If more is needed, create sub-nodes.
- ❌ "The user logs in and then we check the database for their password hash."
- ✅ "User Login"
  - "Check DB Hash"
