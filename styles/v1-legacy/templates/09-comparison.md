# Two-Column Comparison Slide

Side-by-side comparison of two concepts, options, or approaches.

## When to Use
- Before/after comparisons
- Pros/cons
- Option evaluation
- Feature comparisons
- API vs MCP, Manual vs Automated, etc.

## Layout Pattern
- Title at top (128px)
- Two equal white cards
- Each card: icon, title, list of items
- Full height utilization

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Comparison - Langdock</title>
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
    .comparison-container {
      position: absolute;
      top: 280px;
      left: 64px;
      right: 64px;
      bottom: 64px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 48px;
    }
    .comparison-column {
      background: #ffffff;
      border-radius: 20px;
      padding: 40px;
      display: flex;
      flex-direction: column;
      gap: 32px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
    }
    .column-header {
      display: flex;
      align-items: center;
      gap: 16px;
      padding-bottom: 24px;
      border-bottom: 2px solid #f8f8f9;
    }
    .column-title {
      font-size: 36px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -1.44px;
    }
    .column-list {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    .list-item {
      display: flex;
      align-items: flex-start;
      gap: 16px;
    }
    .list-item-text {
      font-size: 24px;
      font-weight: 500;
      color: #121420;
      line-height: 1.4;
      letter-spacing: -0.36px;
    }
    .list-item-text span {
      color: #717279;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Integrations</span>
    </div>
    <span class="slide-number">8</span>
  </div>

  <h1 class="main-title">API vs MCP Integrations</h1>

  <div class="comparison-container">
    <div class="comparison-column">
      <div class="column-header">
        <i class="ti ti-api" style="font-size: 48px; color: #456AFC;"></i>
        <h2 class="column-title">API Integration</h2>
      </div>
      <div class="column-list">
        <div class="list-item">
          <i class="ti ti-check" style="font-size: 24px; color: #456AFC; flex-shrink: 0;"></i>
          <p class="list-item-text">Manual endpoint configuration</p>
        </div>
        <div class="list-item">
          <i class="ti ti-check" style="font-size: 24px; color: #456AFC; flex-shrink: 0;"></i>
          <p class="list-item-text">Full control over parameters</p>
        </div>
        <div class="list-item">
          <i class="ti ti-check" style="font-size: 24px; color: #456AFC; flex-shrink: 0;"></i>
          <p class="list-item-text">Works with any REST API</p>
        </div>
        <div class="list-item">
          <i class="ti ti-check" style="font-size: 24px; color: #456AFC; flex-shrink: 0;"></i>
          <p class="list-item-text">Best for: <span>Custom internal tools</span></p>
        </div>
      </div>
    </div>
    <div class="comparison-column">
      <div class="column-header">
        <i class="ti ti-plug-connected" style="font-size: 48px; color: #456AFC;"></i>
        <h2 class="column-title">MCP Integration</h2>
      </div>
      <div class="column-list">
        <div class="list-item">
          <i class="ti ti-check" style="font-size: 24px; color: #456AFC; flex-shrink: 0;"></i>
          <p class="list-item-text">Auto-discovery of tools</p>
        </div>
        <div class="list-item">
          <i class="ti ti-check" style="font-size: 24px; color: #456AFC; flex-shrink: 0;"></i>
          <p class="list-item-text">Standardized protocol</p>
        </div>
        <div class="list-item">
          <i class="ti ti-check" style="font-size: 24px; color: #456AFC; flex-shrink: 0;"></i>
          <p class="list-item-text">Quick setup with MCP servers</p>
        </div>
        <div class="list-item">
          <i class="ti ti-check" style="font-size: 24px; color: #456AFC; flex-shrink: 0;"></i>
          <p class="list-item-text">Best for: <span>Tools with MCP support</span></p>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
```

## Variations

### Pros/Cons (Different Icons)
Use `ti-check` for pros and `ti-x` with `color: #ef4444` for cons.

### Three Columns
```css
.comparison-container {
  grid-template-columns: 1fr 1fr 1fr;
  gap: 32px;
}
```

### Without Icons in List
Remove the icon from `.list-item` and use bullet points:
```css
.list-item::before {
  content: "•";
  color: #456AFC;
  font-size: 24px;
  margin-right: 12px;
}
```

### Highlighted Winner
Add accent border to winning column:
```css
.comparison-column.winner {
  border: 3px solid #456AFC;
}
```
