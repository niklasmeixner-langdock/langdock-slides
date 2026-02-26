# Langdock Slide Generator

Create professional presentation slides for Langdock training sessions. Slides are HTML, imported to Figma via MCP.

## Session Start

**Always run at the beginning of every session:**
```bash
git pull
```
This ensures you have the latest templates, styles, and knowledge base.

## Making Changes

When modifying templates, styles, or other shared resources:

1. **Create a branch** for your changes:
   ```bash
   git switch -c <descriptive-branch-name>
   ```

2. **Make your changes** (edit templates, add styles, etc.)

3. **Commit and push:**
   ```bash
   git add -A && git commit -m "Description of changes" && git push -u origin HEAD
   ```

4. **Create a PR:**
   ```bash
   gh pr create --title "Title" --body "Description"
   ```

This keeps the main branch clean and allows review before merging.

---

## Skills

| Skill | Use Case |
|-------|----------|
| **`/slides`** | Generate slides using existing templates. Give it a topic or schedule, it picks templates and fills content. |
| **`/design-slide`** | Design a custom one-off slide when no template fits. Same style system, unique layout. |

---

## Session Workflow

### 1. Setup (do once at session start)

Collect from user:
- **Project name** → Creates `slides/<project-name>/` folder
- **Figma destination** → Get the Figma file key from the user

Start infrastructure:
```bash
npx http-server . -p 8080 &   # Background, no confirmation needed
```

### 2. Planning (for `/slides` with multiple slides)

When user provides a topic, schedule, or brief:

1. **Analyze the input** - Identify sections, topics, key points
2. **Propose a deck structure** - Show the user:

```
Proposed Deck: <project-name> (X slides)
─────────────────────────────────────────
1. [section-divider]     Title / Intro
2. [goals-agenda]        Session objectives
3. [platform-overview]   What is Langdock?
4. [comparison-grid]     Key features
5. [exercise-dark]       Hands-on: First chat
6. [split-screenshot]    Deep dive: Assistants
...
─────────────────────────────────────────
Proceed? Or adjust?
```

3. **Get approval** - User confirms or requests changes
4. **Execute** - Create all slides, import to Figma

### 3. Execution

For each slide:
1. Select/create HTML based on template or custom design
2. Save to `slides/<project-name>/XX-slide-name.html`
3. Capture to Figma (see Technical section below)

### 4. Cleanup

```javascript
mcp__playwright__browser_close()
```

Optionally ask: "Keep `slides/<project-name>/` for future edits, or delete?"

---

## Project Structure

```
templates/               # HTML slide templates (reusable layouts)
slides/                  # Generated slides (gitignored, per-client)
  <project-name>/        # e.g., slides/bechtle/, slides/acme-training/

assets/
  langdock-logo.png      # Brand logo
  tabler-icons/          # SVG icon library
  integration-icons/     # Third-party logos (Slack, Notion, etc.)
  workflow-icons/        # Workflow node icons

knowledge/
  index.md               # Product knowledge → docs.langdock.com

styleguide.md            # Full design system reference
```

---

## Technical: Figma Import

Slides are captured via headless browser and imported to Figma using the `generate_figma_design` tool from the **remote Figma MCP server**.

Docs: https://developers.figma.com/docs/figma-mcp-server/tools-and-prompts/#generate_figma_design

**Important**: All generated slides must include the Figma capture script in `<head>`:
```html
<script src="https://mcp.figma.com/mcp/html-to-design/capture.js" async></script>
```

### Per-slide Capture

```javascript
// 1. Generate capture ID
const { captureId } = generate_figma_design({
  outputMode: "existingFile",
  fileKey: "<file-key>"
})

// 2. Navigate to slide
mcp__playwright__browser_navigate({
  url: "http://localhost:8080/slides/<project>/slide.html"
})

// 3. Trigger capture (fire-and-forget, do NOT await the result)
mcp__playwright__browser_run_code({
  code: `async (page) => {
    await page.evaluate(() => {
      window.figma.captureForDesign({
        captureId: '<capture-id>',
        endpoint: 'https://mcp.figma.com/mcp/capture/<capture-id>/submit',
        selector: 'body'
      });
    });
    return 'triggered';
  }`
})

// 4. Poll for completion
generate_figma_design({
  captureId: "<capture-id>",
  outputMode: "existingFile",
  fileKey: "<file-key>"
})
```

---

## Design Tokens (Quick Reference)

**The 3-Meter Rule**: All slides must be readable from 3 meters away. No text below 18px.

```css
/* Typography - minimum sizes for presentations */
Display:     72-80px, 700 weight  /* Hero statements */
Headline 1:  56-64px, 700 weight  /* Slide titles */
Headline 2:  40-48px, 600 weight  /* Section headers */
Headline 3:  32-36px, 600 weight  /* Card titles */
Body Large:  24-28px, 500 weight  /* Primary content */
Body:        20-24px, 500 weight  /* Standard text */
Label:       18-20px, 600 weight  /* Tags, badges */
Caption:     16-18px (minimal use)

/* Colors */
Background: #F4F4F5    Text Primary: #111827
Surface:    #FFFFFF    Text Secondary: #6B7280
Accent:     #456AFC    Border: #E5E7EB

/* Layout */
Canvas: 1920 x 1080px
Margins: 64px all sides
```

Full reference: `styleguide.md`

---

## Assets

### Icons
Read `assets/tabler-icons/index.md` for available SVGs. Use inline:
```html
<svg style="width: 48px; height: 48px; color: #456AFC;">...</svg>
```

### Logo
```html
<img src="assets/brand-assets/langdock-logo.png" height="24" alt="Langdock">
```
Position: bottom-left (64px from edges). Dark backgrounds: `filter: brightness(0) invert(1);`

### Integration Icons
`assets/integration-icons/` - Slack, Notion, Google Drive, etc.

### Workflow Icons
`assets/workflow-icons/` - Agent, code, condition nodes, etc.

---

## Product Knowledge

For accurate feature information:
1. Read `knowledge/index.md` to find relevant docs
2. Fetch from `https://docs.langdock.com` + path
3. Extract only what's needed for the current slide
