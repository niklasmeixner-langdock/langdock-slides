# Langdock Slide Generator

This project creates professional presentation slides for Langdock training sessions. Slides are generated as HTML and imported into Figma using the html.to.design MCP.

## Available Commands

### `/create-slides`
Generate presentation slides from a training schedule. Parses the input schedule and creates HTML slides for each module/topic.

**Usage:**
```
/create-slides
[Paste your training schedule here]
```

By default, uses the **v2-current** style guide (modern brand). Add `--style=v1-legacy` to use the legacy style.

## Project Structure

```
styles/
  v2-current/              # PRIMARY - Current brand style guide
    templates/             # Slide templates
    components/            # Reusable components
    design-system.md       # Design tokens & guidelines

  v1-legacy/               # SECONDARY - Legacy style guide
    templates/             # Original templates
    components/            # Original components

shared/
  assets/
    langdock-logo.png      # Brand logo
    tabler-icons/          # SVG icon library
    integration-icons/     # Third-party integration logos
  knowledge/
    index.md               # Product knowledge base

.claude/commands/
  create-slides.md         # Skill definition for slide creation
```

## Style Guides

### v2-current (Default)
The primary, modern brand style. Use this for all new presentations unless specifically requested otherwise.

### v1-legacy
The original training slide style. Available as a secondary option for consistency with existing materials.

## MCP Servers

This project uses two MCP servers:

1. **figma-desktop** (`http://127.0.0.1:3845/mcp`)
   - Read existing Figma designs for reference
   - Get design context and styles

2. **html-to-design** (`https://h2d-mcp.divriots.com/.../mcp`)
   - Import HTML slides directly to Figma
   - Convert HTML/CSS to Figma layers

## Workflow for Creating Slides

1. **Select style guide** - v2-current (default) or v1-legacy
2. **Read inspiration slides** from Figma using `mcp__figma-desktop__get_design_context`
3. **Parse the training schedule** to identify modules and topics
4. **Research content** using the knowledge base in `shared/knowledge/index.md`
5. **Generate HTML** for each slide using the appropriate design system
6. **Import to Figma** using `mcp__html-to-design__import-html`

## Shared Resources

### Assets (shared/assets/)
- `langdock-logo.png` - Brand logo
- `tabler-icons/` - SVG icon library with index
- `integration-icons/` - Third-party service logos

### Knowledge (shared/knowledge/)
- `index.md` - Topic-to-URL mapping for all Langdock documentation

## Best Practices

1. **Keep slides visual** - Use icons, diagrams, and tags rather than dense text
2. **One concept per slide** - Don't overload slides with multiple topics
3. **Consistent styling** - Use the design system variables from the selected style guide
4. **Demo badges** - Mark slides that include live demonstrations
5. **Clear hierarchy** - Use appropriate heading levels for visual hierarchy
