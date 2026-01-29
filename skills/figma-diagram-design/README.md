# figma-diagram-design

Apply professional color theming to Figma diagrams with automatic branch-based color inheritance.

## What It Does

Transforms plain gray diagrams into visually organized ones where:
- Each **top-level branch** gets a distinct color
- All **child nodes** inherit their parent's color
- **Root/shared nodes** stay neutral

This creates instant visual grouping — you can scan a complex diagram and immediately see which nodes belong together.

## Installation

```bash
npx skills add stoodiohq/agent-skills --skill figma-diagram-design
```

## Included Palettes

1. **Modern Professional** — Clean, corporate-friendly
2. **Soft Pastel** — Lighter, approachable
3. **Bold Vibrant** — High contrast, energetic

## Compatibility

| Agent | Works? |
|-------|--------|
| Claude.ai (with Figma MCP) | ✅ |
| Claude Code (with Figma MCP) | ✅ |
| Cursor | ✅ |
| Other agents | ✅ (outputs Mermaid syntax) |

**Note:** Full diagram generation requires the Figma MCP connector. Without it, agents can still output properly-styled Mermaid syntax for use in other renderers.
