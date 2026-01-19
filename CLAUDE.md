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

## Project Structure

```
.claude/commands/
  create-slides.md    # Skill definition for slide creation

templates/
  title-slide.html       # Session title/opener slides
  comparison-slide.html  # 3-column comparison layouts
  process-flow-slide.html # Step-by-step process diagrams
  feature-deep-dive-slide.html # Detailed feature exploration

design-system.css     # CSS variables and component styles
langdock-knowledge.md # Product knowledge base
icons.svg             # SVG icon library
developer-capabilities-slide.html # Example completed slide
```

## MCP Servers

This project uses two MCP servers:

1. **figma-desktop** (`http://127.0.0.1:3845/mcp`)
   - Read existing Figma designs for reference
   - Get design context and styles

2. **html-to-design** (`https://h2d-mcp.divriots.com/.../mcp`)
   - Import HTML slides directly to Figma
   - Convert HTML/CSS to Figma layers

## Workflow for Creating Slides

1. **Read inspiration slides** from Figma using `mcp__figma-desktop__get_design_context`
2. **Parse the training schedule** to identify modules and topics
3. **Research content** using the knowledge base in `langdock-knowledge.md`
4. **Generate HTML** for each slide using the design system
5. **Import to Figma** using `mcp__html-to-design__import-html`

## Design System Quick Reference

### Colors
- Background: `#f8f8f9`
- Elevated: `#ededee`
- Primary text: `#121420`
- Secondary text: `#717279`
- Accent: `#456AFC`

### Typography
- Headline 1: Inter Semi Bold, 64px, -3.2px tracking
- Headline 2: Inter Bold, 40px, -1.6px tracking
- Body: Inter Regular, 18px
- Tags: Inter Medium, 16-20px

### Slide Dimensions
- 1920 x 1080 pixels (16:9)
- Margins: 64px
- Element gaps: 32px

## Best Practices

1. **Keep slides visual** - Use icons, diagrams, and tags rather than dense text
2. **One concept per slide** - Don't overload slides with multiple topics
3. **Consistent styling** - Use the design system variables for all colors and fonts
4. **Demo badges** - Mark slides that include live demonstrations
5. **Clear hierarchy** - Use Headline 1 for main title, Headline 2 for sections
