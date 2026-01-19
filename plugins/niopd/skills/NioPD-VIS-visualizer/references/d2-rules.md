# D2 Ultra SOTA Rules & Reference

This document provides a comprehensive reference for D2 (Declarative Diagramming), optimizing for its modern layout engine and "programmer-friendly" syntax.

## 1. Global Configuration

D2 allows global styling and layout configuration.

### 1.1 Layout Engines
- `layout: dagre` (Default, good for hierarchy)
- `layout: tala` (Best for complex node graphs, minimizes crossings)
- `layout: elk` (Good for huge graphs with complex grouping)

### 1.2 Global Themes
D2 has built-in themes (0-300).
- `0`: Classic Minimal
- `100`: Neutral Grey
- `300`: Uplifting (Pop color)

Example Header:
```d2
direction: right
layout: tala
theme: 100
```

## 2. Shapes & Syntax

### 2.1 Basic Shapes
```d2
Square: {shape: square}
Circle: {shape: circle}
Cloud: {shape: cloud}
Package: {shape: package}
Cylinder: {shape: cylinder}
Queue: {shape: queue}
Person: {shape: person}
```

### 2.2 Text & Labels
Labels are optional if the ID is descriptive, unlike Mermaid.
```d2
# Simple
user -> api

# With Labels
user: "Power User"
api: "REST Endpoint"
user -> api: "Authorized Request"
```

### 2.3 Containers (Nesting)
D2's superpower is nesting.
```d2
Cloud: {
  LoadBalancer -> WebServer
  WebServer -> Database
}
User -> Cloud.LoadBalancer
```

## 3. Advanced Features

### 3.1 SQL Syntax support
D2 can render SQL table schemas.
```d2
Users: {
  shape: sql_table
  id: int {constraint: primary_key}
  email: varchar(255) {constraint: unique}
}
```

### 3.2 Classes & Code
```d2
my_class: {
  shape: class
  # Operations
  +Start()
  -Stop()
}
```

### 3.3 Markdown Blocks (SOTA Documentation)
Use `|md` for rich text descriptions inside nodes.
```d2
Service: {
  description: |md
    # Critical Service
    - **SLA**: 99.9%
    - **Owner**: @team-alpha
  |
}
```

## 4. Connections & Styling

### 4.1 Connection Types
- `->` Uni-directional
- `<->` Bi-directional
- `--` Non-directional line

### 4.2 Styling Connections
```d2
x -> y: {
  style: {
    stroke: green
    stroke-width: 4
    animated: true
  }
}
```

### 4.3 Node Styling
```d2
Server: {
  style: {
    fill: "#f4faff"
    stroke: "#1e3a8a"
    stroke-width: 2
    shadow: true
  }
}
```
