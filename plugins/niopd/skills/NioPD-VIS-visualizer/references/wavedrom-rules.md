# WaveDrom Ultra SOTA Rules & Reference

WaveDrom is the gold standard for **Digital Timing Diagrams** (JSON → SVG). Use it for API latencies, hardware interrupts, or complex parallel workflows.

## 1. Signal Syntax (The Wave String)

The `wave` string determines the signal shape over time steps.

| Character | Meaning | Visual |
|-----------|---------|--------|
| `p` | Positive edge (Clock) | 📈 Rise |
| `n` | Negative edge (Clock) | 📉 Fall |
| `0` | Low Level | ＿ |
| `1` | High Level | ￣ |
| `.` | Continuation (Hold) | ＿/￣ |
| `z` | High Impedance | ― (Middle) |
| `x` | Undefined | ░ (Hatch) |
| `=` | Data Bus (Value) | ▱ (Box) |

## 2. Advanced Features

### 2.1 Grouping Signals
Group related signals (like Input/Output buses).

```json
{ "signal": [
   ["Input Group",
      { "name": "clk", "wave": "p.." },
      { "name": "ctrl", "wave": "01." }
   ],
   {},  // Spacer
   ["Output Group",
      { "name": "data", "wave": "x.=", "data": "Valid" }
   ]
]}
```

### 2.2 Edges & Arrows (Causality)
Draw arrows to show that Signal A triggers Signal B.

```json
{ "signal": [
  { "name": "A", "node": "..a..b.." }, 
  { "name": "B", "node": "....c..." }
],
  "edge": [
    "a~>c Trigger", 
    "c-~>b Ack"
  ]
}
```
- `a`: Node name (arbitrary char in `node` string).
- `~>`: Spline arrow.
- `-~>`: Sharp arrow.

### 2.3 Head/Foot Text
Add context to the diagram.
```json
{ "signal": [...],
  "head": { "text": "API Response Timeline v1.0", "tick": 0 },
  "foot": { "text": "Time (ms)", "tock": 1 }
}
```

## 3. Ultra SOTA Config

### 3.1 Scaling
Use `config` to ensure long diagrams fit.
```json
"config": { "hscale": 2 }
```

### 3.2 Period/Phase
Adjust the starting phase or period of a signal.
```json
{ "name": "Delayed", "wave": "p..", "period": 2, "phase": 0.5 }
```

## 4. Use Cases
- **Protocol Handshake**: TCP SYN/ACK visualization.
- **Bus Timing**: Showing Address vs Data lines validity windows.
- **Race Guidelines**: Visualizing thread locking/unlocking overlaps.
