---
name: figma-diagram-design
description: Apply professional color theming to Figma diagrams (flowcharts, decision trees, sequence diagrams, state diagrams, gantt charts). Use this skill whenever creating diagrams with the Figma:generate_diagram tool. Automatically assigns distinct colors to top-level branches, with child nodes inheriting their parent branch's color family for clear visual hierarchy.
---

# Figma Diagram Design

Apply hierarchy-based color theming to diagrams. Each top-level branch gets a distinct color; all descendants inherit that color, creating instant visual grouping.

## Color Application Rules

1. **Identify top-level branches** — nodes directly connected to the root/start
2. **Assign distinct colors** — one color per top-level branch from the palette
3. **Inherit downward** — all child nodes match their ancestor's branch color
4. **Root stays neutral** — use the neutral color for entry points and shared nodes

## Mermaid Styling Syntax

Define classes and apply them to nodes:

```mermaid
flowchart LR
    classDef branch1 fill:#E8F4FD,stroke:#1E88E5,color:#1565C0
    classDef branch2 fill:#F3E5F5,stroke:#8E24AA,color:#6A1B9A
    classDef branch3 fill:#E8F5E9,stroke:#43A047,color:#2E7D32
    classDef neutral fill:#F5F5F5,stroke:#757575,color:#424242

    Start["Start"]:::neutral
    A["Branch A"]:::branch1
    A1["A Child"]:::branch1
    B["Branch B"]:::branch2
    B1["B Child"]:::branch2
    
    Start --> A --> A1
    Start --> B --> B1
```

## Curated Palettes

### Modern Professional (Default)
| Branch | Fill | Stroke | Text |
|--------|------|--------|------|
| 1 - Blue | #E8F4FD | #1E88E5 | #1565C0 |
| 2 - Purple | #F3E5F5 | #8E24AA | #6A1B9A |
| 3 - Green | #E8F5E9 | #43A047 | #2E7D32 |
| 4 - Orange | #FFF3E0 | #FB8C00 | #E65100 |
| 5 - Teal | #E0F2F1 | #00897B | #00695C |
| 6 - Red | #FFEBEE | #E53935 | #C62828 |
| Neutral | #F5F5F5 | #757575 | #424242 |

### Soft Pastel
| Branch | Fill | Stroke | Text |
|--------|------|--------|------|
| 1 - Rose | #FCE4EC | #F06292 | #C2185B |
| 2 - Sky | #E1F5FE | #4FC3F7 | #0277BD |
| 3 - Mint | #E0F7FA | #4DD0E1 | #00838F |
| 4 - Peach | #FFF8E1 | #FFD54F | #F57F17 |
| 5 - Lavender | #EDE7F6 | #B39DDB | #5E35B1 |
| 6 - Sage | #F1F8E9 | #AED581 | #558B2F |
| Neutral | #FAFAFA | #BDBDBD | #616161 |

### Bold Vibrant
| Branch | Fill | Stroke | Text |
|--------|------|--------|------|
| 1 - Electric Blue | #BBDEFB | #2196F3 | #0D47A1 |
| 2 - Hot Pink | #F8BBD9 | #E91E63 | #880E4F |
| 3 - Lime | #DCEDC8 | #8BC34A | #33691E |
| 4 - Amber | #FFECB3 | #FFC107 | #FF6F00 |
| 5 - Deep Purple | #D1C4E9 | #673AB7 | #311B92 |
| 6 - Cyan | #B2EBF2 | #00BCD4 | #006064 |
| Neutral | #ECEFF1 | #607D8B | #37474F |

## Workflow

1. Parse the diagram structure to identify hierarchy
2. Count top-level branches and select palette
3. Generate classDef statements for each branch + neutral
4. Apply classes to all nodes based on their branch ancestry
5. Ensure root/shared nodes use neutral styling

## Notes

- For diagrams with >6 branches, cycle through the palette or select a subset
- Gantt charts: color by task group/section rather than hierarchy
- Sequence diagrams: color by participant/actor
- State diagrams: color by state category or region
