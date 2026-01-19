# Reusable Components

Copy-paste these components into any slide template.

---

## Header

Standard header with breadcrumbs and slide number.

```html
<div class="header">
  <div class="breadcrumbs">
    <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
    <span class="footnote">Section Name</span>
  </div>
  <span class="slide-number">1</span>
</div>
```

```css
.header {
  position: absolute;
  top: 40px;
  left: 64px;
  right: 64px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.breadcrumbs {
  display: flex;
  align-items: center;
  gap: 12px;
}
.footnote {
  font-family: 'Inter', sans-serif;
  font-size: 18px;
  font-weight: 500;
  color: #717279;
  letter-spacing: -0.36px;
}
.slide-number {
  font-family: 'Inter', sans-serif;
  font-size: 18px;
  font-weight: 500;
  color: #717279;
}
```

### Dark Variant
For dark backgrounds, use `color: rgba(248, 248, 249, 0.5)` for text.

---

## Tags/Pills

```html
<span class="tag">Label</span>
```

### Light Tag (Default)
```css
.tag {
  display: inline-flex;
  padding: 12px 16px;
  background: rgba(14, 17, 18, 0.12);
  border-radius: 100px;
  font-family: 'Inter', sans-serif;
  font-size: 20px;
  font-weight: 500;
  color: #121420;
  white-space: nowrap;
}
```

### Dark Tag (For Dark Slides)
```css
.tag-dark {
  padding: 12px 20px;
  background: rgba(255, 255, 255, 0.04);
  border-radius: 100px;
  font-size: 20px;
  font-weight: 500;
  color: #ffffff;
}
```

### Accent Tag
```css
.tag-accent {
  padding: 12px 16px;
  background: #456AFC;
  border-radius: 100px;
  font-size: 20px;
  font-weight: 500;
  color: #ffffff;
}
```

---

## Info Box

### Solid Background (Default)
```html
<div class="info-box">
  <div class="info-box-header">
    <i class="ti ti-info-circle" style="font-size: 24px; color: #456AFC;"></i>
    <span class="info-box-title">Good to know</span>
  </div>
  <p class="info-box-content">Your informational content here.</p>
</div>
```

```css
.info-box {
  background: rgba(14, 17, 18, 0.06);
  border-radius: 16px;
  padding: 24px 28px;
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.info-box-header {
  display: flex;
  align-items: center;
  gap: 12px;
}
.info-box-title {
  font-family: 'Inter', sans-serif;
  font-size: 20px;
  font-weight: 600;
  color: #121420;
}
.info-box-content {
  font-family: 'Inter', sans-serif;
  font-size: 18px;
  color: #717279;
  line-height: 1.5;
}
```

### Dashed Border (Preferred for annotations/callouts)
Use dashed borders for info boxes, annotations, and callout content. This creates a lighter, more elegant appearance.

```html
<div class="info-box-dashed">
  <p class="info-box-content">Annotation or callout text here.</p>
</div>
```

```css
.info-box-dashed {
  border: 1.5px dashed #c0c0c0;
  border-radius: 12px;
  padding: 16px 20px;
  background: transparent;
}
.info-box-dashed .info-box-content {
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  color: #717279;
  line-height: 1.5;
}
```

### When to use each style
| Dashed Border | Solid Background |
|---------------|------------------|
| Annotations pointing to content | Important notices |
| Side notes and callouts | Tips with icons |
| Code/prompt section labels | Warnings |
| Lightweight visual grouping | Emphasis boxes |

---

## Code Block

```html
<div class="code-block">
  <div class="code-header">
    <span class="code-language">python</span>
  </div>
  <pre class="code-content"><code>import langdock
client = langdock.Client(api_key="...")</code></pre>
</div>
```

```css
.code-block {
  background: #1e1e2e;
  border-radius: 12px;
  overflow: hidden;
}
.code-header {
  background: #2a2a3e;
  padding: 8px 16px;
  border-bottom: 1px solid #3a3a4e;
}
.code-language {
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
  color: #717279;
  text-transform: uppercase;
}
.code-content {
  padding: 20px;
  margin: 0;
  overflow-x: auto;
}
.code-content code {
  font-family: 'JetBrains Mono', monospace;
  font-size: 14px;
  color: #e0e0e0;
  line-height: 1.6;
}
```

Add JetBrains Mono font:
```html
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
```

---

## Chat Messages

```html
<div class="chat-message user">
  <div class="message-bubble">
    <p>User message text</p>
  </div>
</div>
<div class="chat-message assistant">
  <div class="avatar">
    <i class="ti ti-robot" style="font-size: 20px; color: #456AFC;"></i>
  </div>
  <div class="message-bubble">
    <p>Assistant response text</p>
  </div>
</div>
```

```css
.chat-message {
  display: flex;
  gap: 12px;
  margin-bottom: 16px;
}
.chat-message.user {
  justify-content: flex-end;
}
.chat-message.user .message-bubble {
  background: #456AFC;
  color: #ffffff;
}
.chat-message.assistant .message-bubble {
  background: #f8f8f9;
  color: #121420;
}
.message-bubble {
  padding: 16px 20px;
  border-radius: 16px;
  max-width: 80%;
  font-family: 'Inter', sans-serif;
  font-size: 18px;
  line-height: 1.5;
}
.avatar {
  width: 40px;
  height: 40px;
  background: #f8f8f9;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}
```

---

## UI Mockup Container

```html
<div class="ui-mockup">
  <div class="mockup-header">
    <div class="mockup-dots">
      <span class="dot"></span>
      <span class="dot"></span>
      <span class="dot"></span>
    </div>
  </div>
  <div class="mockup-content">
    <!-- UI content here -->
  </div>
</div>
```

```css
.ui-mockup {
  background: #ffffff;
  border-radius: 16px;
  box-shadow: 0 4px 24px rgba(0, 0, 0, 0.08);
  overflow: hidden;
}
.mockup-header {
  background: #f8f8f9;
  padding: 12px 16px;
  border-bottom: 1px solid #ededee;
}
.mockup-dots {
  display: flex;
  gap: 8px;
}
.mockup-dots .dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #bebec2;
}
.mockup-content {
  padding: 24px;
}
```

---

## Numbered Card

```html
<div class="numbered-card">
  <span class="card-number">01</span>
  <div class="card-content">
    <h3 class="card-title">Card Title</h3>
    <p class="card-description">Description text.</p>
  </div>
</div>
```

```css
.numbered-card {
  background: #ffffff;
  border-radius: 16px;
  padding: 32px;
  display: flex;
  flex-direction: column;
  gap: 24px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
}
.card-number {
  font-family: 'Inter', sans-serif;
  font-size: 48px;
  font-weight: 600;
  color: #456AFC;
  line-height: 1;
}
.card-title {
  font-family: 'Inter', sans-serif;
  font-size: 28px;
  font-weight: 600;
  color: #121420;
  letter-spacing: -0.42px;
}
.card-description {
  font-family: 'Inter', sans-serif;
  font-size: 20px;
  font-weight: 500;
  color: #717279;
  line-height: 1.4;
}
```

---

## Dashed Grid Card

```html
<div class="grid-card">
  <i class="ti ti-icon-name" style="font-size: 40px; color: #456AFC;"></i>
  <div class="grid-card-content">
    <span class="grid-card-title">Title</span>
    <span class="grid-card-desc">Description</span>
  </div>
</div>
```

```css
.grid-card {
  border: 1.5px dashed #bebec2;
  padding: 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  min-height: 180px;
}
.grid-card-content {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.grid-card-title {
  font-family: 'Inter', sans-serif;
  font-size: 22px;
  font-weight: 500;
  color: #121420;
}
.grid-card-desc {
  font-family: 'Inter', sans-serif;
  font-size: 18px;
  font-weight: 500;
  color: #717279;
  line-height: 1.35;
}
```

---

## Annotation with Curved Connector

Use dashed curved lines to connect annotations to content. The annotation text sits in a dashed box, with a curved dashed line pointing to the relevant element.

```html
<div class="annotation" style="position: absolute; top: 200px; left: 100px;">
  <p class="annotation-text">The most-used technique, good to ask the model to think out loud</p>
  <!-- SVG curved connector -->
  <svg class="annotation-connector" width="150" height="80" style="position: absolute; top: 50%; right: -150px;">
    <path d="M 0 40 C 50 40, 100 80, 150 80" stroke="#c0c0c0" stroke-width="1.5" stroke-dasharray="6 4" fill="none"/>
  </svg>
</div>
```

```css
.annotation {
  position: absolute;
  max-width: 200px;
}
.annotation-text {
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  color: #717279;
  line-height: 1.5;
  text-align: right;  /* or left, depending on connector direction */
}
.annotation-connector {
  pointer-events: none;
}
```

### Connector Path Tips
- Use cubic Bezier curves: `C controlX1 controlY1, controlX2 controlY2, endX endY`
- Keep stroke: `#c0c0c0` (gray)
- Use `stroke-dasharray="6 4"` for dashed effect
- Adjust path coordinates based on annotation position relative to target

---

## Capability Node (Icon + Title + Tags)

For capability overview slides with organic layouts. Position nodes absolutely for flexible arrangement.

```html
<div class="capability-node" style="position: absolute; top: 280px; left: 140px;">
  <svg class="capability-icon" xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
    <!-- icon path here -->
  </svg>
  <span class="capability-title">File Attachments</span>
  <div class="capability-tags">
    <span class="tag-small">Analyze contracts</span>
    <span class="tag-small">Summarize</span>
  </div>
</div>
```

```css
.capability-node {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 12px;
  max-width: 280px;
}
.capability-icon {
  width: 48px;
  height: 48px;
  color: #456AFC;
}
.capability-title {
  font-family: 'Inter', sans-serif;
  font-size: 24px;
  font-weight: 700;
  color: #121420;
  letter-spacing: -0.48px;
  text-align: center;
}
.capability-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  justify-content: center;
}
.tag-small {
  background: #ededee;
  padding: 8px 14px;
  border-radius: 100px;
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  font-weight: 500;
  color: #717279;
}
```

### Connecting Capability Nodes
Use subtle curved lines (NOT dashed) between capability nodes to show relationships:

```html
<svg class="node-connectors" viewBox="0 0 1920 1080" style="position: absolute; top: 0; left: 0; pointer-events: none;">
  <!-- Curved connector between two nodes -->
  <path d="M 380 360 C 480 420, 620 420, 720 360"
        stroke="#e0e0e0"
        stroke-width="1.5"
        fill="none"/>
</svg>
```

**Important**: Node connectors use SOLID light gray lines (`#e0e0e0`), NOT dashed. Dashed lines are only for info boxes and annotations.

---

## Prompt Block (for prompting slides)

Display prompt examples with optional accent highlighting.

```html
<div class="prompt-block">
  <span class="prompt-text">Think step by step and describe your thinking process</span>
</div>

<!-- Accent variant for emphasis -->
<div class="prompt-block accent">
  <span class="prompt-text">First do task x, then do task y and finally do task z.</span>
</div>
```

```css
.prompt-block {
  display: inline-flex;
  padding: 14px 24px;
  background: #ededee;
  border-radius: 8px;
  max-width: fit-content;
}
.prompt-block.accent {
  background: #456AFC;
}
.prompt-block .prompt-text {
  font-family: 'Inter', sans-serif;
  font-size: 18px;
  font-weight: 500;
  color: #121420;
}
.prompt-block.accent .prompt-text {
  color: #ffffff;
}
```

---

## Flow Diagram Elements

### User/LLM Nodes
Circular nodes for representing user and AI in flow diagrams.

```html
<!-- User node (light) -->
<div class="flow-node user">
  <svg><!-- user icon --></svg>
  <span>User</span>
</div>

<!-- LLM node (dark) -->
<div class="flow-node llm">
  <svg><!-- sparkles icon --></svg>
  <span>LLM</span>
</div>
```

```css
.flow-node {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 8px;
}
.flow-node.user {
  background: #ededee;
}
.flow-node.user svg { color: #717279; width: 40px; height: 40px; }
.flow-node.user span { font-size: 16px; font-weight: 600; color: #717279; }

.flow-node.llm {
  background: #717279;
}
.flow-node.llm svg { color: #ffffff; width: 40px; height: 40px; }
.flow-node.llm span { font-size: 16px; font-weight: 600; color: #ffffff; }
```

### Flow Arrows
Solid arrows for flow direction (not dashed).

```html
<svg width="100" height="50">
  <!-- Downward arrow -->
  <path d="M 50 0 L 50 40" stroke="#456AFC" stroke-width="2" fill="none"/>
  <polygon points="50,50 45,40 55,40" fill="#456AFC"/>
</svg>
```

### Context Stack
Stacked items showing accumulated context.

```html
<div class="context-stack">
  <div class="context-item primary">Prompt: "Summarize attached files"</div>
  <div class="context-item">Uploaded files</div>
  <div class="context-item">Previous messages from chat</div>
</div>
```

```css
.context-stack {
  display: flex;
  flex-direction: column;
  gap: 4px;
}
.context-item {
  background: #ededee;
  padding: 12px 20px;
  border-radius: 6px;
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  color: #717279;
}
.context-item.primary {
  background: transparent;
  border: 2px solid #456AFC;
  color: #456AFC;
}
```

---

## Integration Icons

Display integration logos from the `/assets/integration-icons/` folder. See `/assets/integration-icons/index.md` for complete list of available icons.

### Single Integration Icon
```html
<div class="integration-icon">
  <img src="assets/integration-icons/slack-icon.png" alt="Slack">
</div>
```

```css
.integration-icon {
  width: 64px;
  height: 64px;
  background: #ffffff;
  border-radius: 12px;
  padding: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  display: flex;
  align-items: center;
  justify-content: center;
}
.integration-icon img {
  width: 40px;
  height: 40px;
  object-fit: contain;
}
```

### Integration Icon Grid
For displaying multiple integrations in a grid layout.

```html
<div class="integration-grid">
  <div class="integration-icon"><img src="assets/integration-icons/slack-icon.png" alt="Slack"></div>
  <div class="integration-icon"><img src="assets/integration-icons/microsoft-teams-icon.png" alt="Teams"></div>
  <div class="integration-icon"><img src="assets/integration-icons/jira-icon.png" alt="Jira"></div>
  <div class="integration-icon"><img src="assets/integration-icons/salesforce-icon.png" alt="Salesforce"></div>
  <div class="integration-icon"><img src="assets/integration-icons/notion-icon.png" alt="Notion"></div>
  <div class="integration-icon"><img src="assets/integration-icons/gmail-icon.png" alt="Gmail"></div>
</div>
```

```css
.integration-grid {
  display: grid;
  grid-template-columns: repeat(4, 64px);
  gap: 16px;
}
```

### Large Integration Grid (5x4)
For integration showcase slides.

```css
.integration-grid-large {
  display: grid;
  grid-template-columns: repeat(5, 80px);
  grid-template-rows: repeat(4, 80px);
  gap: 20px;
  align-content: center;
  justify-content: center;
}
.integration-grid-large .integration-icon {
  width: 80px;
  height: 80px;
  border-radius: 16px;
  padding: 16px;
}
.integration-grid-large .integration-icon img {
  width: 48px;
  height: 48px;
}
```

### Integration Icon with Label
```html
<div class="integration-item">
  <div class="integration-icon">
    <img src="assets/integration-icons/salesforce-icon.png" alt="Salesforce">
  </div>
  <span class="integration-label">Salesforce</span>
</div>
```

```css
.integration-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}
.integration-label {
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  font-weight: 500;
  color: #717279;
}
```

### Integration Icon (Dark Background)
For dark slides or foundation bars.

```css
.integration-icon-dark {
  width: 48px;
  height: 48px;
  background: rgba(255, 255, 255, 0.08);
  border-radius: 10px;
  padding: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.integration-icon-dark img {
  width: 28px;
  height: 28px;
  object-fit: contain;
}
```

### Common Integration Groupings

**Popular (Top 6):**
- `slack-icon.png`, `microsoft-teams-icon.png`, `gmail-icon.png`
- `jira-icon.png`, `notion-icon.png`, `salesforce-icon.png`

**Google Workspace:**
- `gmail-icon.png`, `google-drive-icon.png`, `google-docs-icon.png`
- `google-sheets-icon.png`, `google-calendar-icon.png`, `google-meet-icon.png`

**Microsoft 365:**
- `microsoft-teams-icon.png`, `microsoft-outlook-email-icon.png`
- `microsoft-onedrive-icon.png`, `microsoft-sharepoint-icon.png`, `microsoft-excel-icon.png`

**Data Stack:**
- `big-query-icon.png`, `snowflake-icon.png`, `databricks-icon.png`
- `looker-icon.png`, `tableau-icon.png`

---

## Stats Display

For showing key metrics and numbers.

### Stat Item with Divider
```html
<div class="stat-item">
  <div class="stat-number">3.500+</div>
  <div class="stat-label">Companies trust Langdock</div>
</div>
```

```css
.stat-item {
  padding: 40px 0;
  border-top: 1px solid #e0e0e0;
}
.stat-item:first-child {
  border-top: none;
  padding-top: 0;
}
.stat-number {
  font-family: 'Inter', sans-serif;
  font-size: 72px;
  font-weight: 700;
  color: #121420;
  letter-spacing: -2.88px;
  line-height: 1;
  margin-bottom: 12px;
}
.stat-label {
  font-family: 'Inter', sans-serif;
  font-size: 22px;
  font-weight: 500;
  color: #717279;
  letter-spacing: -0.33px;
  line-height: 1.3;
}
```

---

## Platform Tile (Dark)

For product platform overview slides.

```html
<div class="platform-tile">
  <div class="tile-icon-box">
    <i class="ti ti-message" style="font-size: 28px; color: #ffffff;"></i>
  </div>
  <span class="tile-label">Chat</span>
</div>
```

```css
.platform-tile {
  background: rgba(255, 255, 255, 0.15);
  border-radius: 16px;
  padding: 24px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 12px;
}
.tile-icon-box {
  width: 56px;
  height: 56px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.tile-label {
  font-family: 'Inter', sans-serif;
  font-size: 22px;
  font-weight: 600;
  color: #ffffff;
}
```

---

## Foundation Bar Section

For showing platform foundation elements (integrations, connectors, models).

```html
<div class="foundation-section">
  <div class="foundation-header">
    <span class="foundation-title">Integrations</span>
    <span class="foundation-count">50+</span>
  </div>
  <div class="foundation-items">
    <div class="foundation-icon">
      <img src="assets/integration-icons/slack-icon.png" alt="Slack">
    </div>
    <div class="foundation-icon">
      <img src="assets/integration-icons/jira-icon.png" alt="Jira">
    </div>
    <span class="foundation-tag">+45</span>
  </div>
</div>
```

```css
.foundation-section {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.foundation-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.foundation-title {
  font-family: 'Inter', sans-serif;
  font-size: 18px;
  font-weight: 600;
  color: #ffffff;
}
.foundation-count {
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  font-weight: 500;
  color: rgba(255, 255, 255, 0.5);
}
.foundation-items {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
}
.foundation-icon {
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.08);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.foundation-icon img {
  width: 24px;
  height: 24px;
  object-fit: contain;
}
.foundation-tag {
  background: rgba(255, 255, 255, 0.08);
  border-radius: 8px;
  padding: 10px 16px;
  font-family: 'Inter', sans-serif;
  font-size: 15px;
  font-weight: 500;
  color: #ffffff;
}
.foundation-tag.outline {
  background: transparent;
  border: 1px solid rgba(255, 255, 255, 0.2);
}
```

---

## Customer Logo Grid

For displaying customer logos (grayscale or color).

```html
<div class="logos-grid">
  <div class="logo-item"><img src="logos/company-1.png" alt="Company 1"></div>
  <div class="logo-item"><img src="logos/company-2.png" alt="Company 2"></div>
  <!-- ... more logos -->
</div>
```

```css
.logos-grid {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-template-rows: repeat(5, 1fr);
  gap: 24px;
  align-content: center;
}
.logo-item {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 60px;
}
.logo-item img {
  max-width: 140px;
  max-height: 48px;
  object-fit: contain;
  filter: grayscale(100%);
  opacity: 0.7;
}
/* Color variant */
.logos-grid.color .logo-item img {
  filter: none;
  opacity: 1;
}
```
