# Capability Grid Slide

Horizontal arrangement of features with icons and tags.

## When to Use
- Feature overviews
- Capability summaries
- "What AI can do" slides
- Tool comparisons

## Layout Pattern
- Title at top (128px)
- 3-4 columns of features starting at ~320px
- Each column: icon, title, tags
- Centered alignment

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>What AI can do - Langdock</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Inter', sans-serif;
      background: #f8f8f9;
      width: 1920px;
      height: 1080px;
      position: relative;
      overflow: hidden;
    }
    .header {
      position: absolute;
      top: 40px;
      left: 64px;
      right: 64px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .breadcrumbs { display: flex; align-items: center; gap: 12px; }
    .footnote { font-size: 18px; font-weight: 500; color: #717279; letter-spacing: -0.36px; }
    .slide-number { font-size: 18px; font-weight: 500; color: #717279; }
    .main-title {
      position: absolute;
      top: 128px;
      left: 64px;
      font-size: 64px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -3.2px;
      line-height: 1.1;
    }
    .capabilities-grid {
      position: absolute;
      top: 320px;
      left: 64px;
      right: 64px;
      display: flex;
      justify-content: space-between;
      gap: 48px;
    }
    .capability-card {
      flex: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 16px;
    }
    .capability-icon {
      width: 88px;
      height: 88px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .capability-title {
      font-size: 40px;
      font-weight: 500;
      color: #121420;
      letter-spacing: -1.6px;
      text-align: center;
    }
    .capability-tags {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 8px;
      max-width: 320px;
    }
    .tag {
      padding: 12px 16px;
      background: rgba(14, 17, 18, 0.12);
      border-radius: 100px;
      font-size: 20px;
      font-weight: 500;
      color: #121420;
      white-space: nowrap;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Recap: What AI can do</span>
    </div>
    <span class="slide-number">3</span>
  </div>

  <h1 class="main-title">Recap: What AI can do</h1>

  <div class="capabilities-grid">
    <div class="capability-card">
      <div class="capability-icon">
        <i class="ti ti-paperclip" style="font-size: 56px; color: #456AFC;"></i>
      </div>
      <h3 class="capability-title">File Attachments</h3>
      <div class="capability-tags">
        <span class="tag">Analyze contracts</span>
        <span class="tag">Summarize</span>
        <span class="tag">Answer questions</span>
      </div>
    </div>
    <div class="capability-card">
      <div class="capability-icon">
        <i class="ti ti-sparkles" style="font-size: 56px; color: #456AFC;"></i>
      </div>
      <h3 class="capability-title">Plain Model</h3>
      <div class="capability-tags">
        <span class="tag">Write texts</span>
        <span class="tag">Brainstorm</span>
        <span class="tag">Translate</span>
        <span class="tag">Explain concepts</span>
      </div>
    </div>
    <div class="capability-card">
      <div class="capability-icon">
        <i class="ti ti-world" style="font-size: 56px; color: #456AFC;"></i>
      </div>
      <h3 class="capability-title">Web Search</h3>
      <div class="capability-tags">
        <span class="tag">Find companies</span>
        <span class="tag">Find answers</span>
        <span class="tag">Real-time info</span>
      </div>
    </div>
  </div>
</body>
</html>
```

## Variations

### 4 Columns
Reduce tag max-width to 280px and icon size to 48px.

### Without Tags
Remove `.capability-tags` for simpler layout. Add description text instead:
```html
<p class="capability-desc">Short description of the capability</p>
```

### With Descriptions
```css
.capability-desc {
  font-size: 20px;
  color: #717279;
  text-align: center;
  line-height: 1.4;
  max-width: 300px;
}
```

### Common Icons
- `ti-paperclip` - Files
- `ti-sparkles` - AI/Model
- `ti-world` - Web search
- `ti-database` - Knowledge base
- `ti-plug-connected` - Integrations
- `ti-robot` - Assistants
- `ti-git-branch` - Workflows
