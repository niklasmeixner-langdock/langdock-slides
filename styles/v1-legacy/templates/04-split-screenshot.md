# Split Layout Slide (Content + Screenshot)

50/50 split with text content on left and UI screenshot/visual on right.

## When to Use
- Feature explanations with UI demo
- Step-by-step guides with visual context
- Tool tutorials
- Best practices with examples

## Layout Pattern
- Title at top (128px)
- Two columns starting at 240px
- Left: bullets, labels, info boxes
- Right: screenshot placeholder or mockup
- Full height utilization

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Data Analyst - Langdock</title>
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
    .split-layout {
      position: absolute;
      top: 240px;
      left: 64px;
      right: 64px;
      bottom: 64px;
      display: flex;
      gap: 64px;
    }
    .left-content {
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 32px;
    }
    .section-label {
      font-size: 28px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -0.42px;
    }
    .bullet-list {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    .bullet-item {
      font-size: 24px;
      line-height: 1.5;
      color: #121420;
      letter-spacing: -0.36px;
    }
    .bullet-item strong { font-weight: 600; }
    .bullet-item span { color: #717279; }
    .info-box {
      background: rgba(14, 17, 18, 0.06);
      border-radius: 16px;
      padding: 24px 28px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-top: auto;
    }
    .info-box-header {
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .info-box-title {
      font-size: 20px;
      font-weight: 600;
      color: #121420;
    }
    .info-box-content {
      font-size: 18px;
      color: #717279;
      line-height: 1.5;
    }
    .right-content {
      flex: 1;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .screenshot-placeholder {
      width: 100%;
      height: 100%;
      max-height: 700px;
      background: #ffffff;
      border-radius: 16px;
      box-shadow: 0 4px 24px rgba(0, 0, 0, 0.08);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #717279;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Advanced Tools</span>
    </div>
    <span class="slide-number">6</span>
  </div>

  <h1 class="main-title">Data Analyst</h1>

  <div class="split-layout">
    <div class="left-content">
      <span class="section-label">Get the best results:</span>
      <div class="bullet-list">
        <p class="bullet-item"><strong>Use clear, descriptive column names</strong> <span>in your sheet</span></p>
        <p class="bullet-item"><strong>Put all column titles in the first row</strong></p>
        <p class="bullet-item"><strong>Be specific:</strong> <span>Clearly describe the analysis you want</span></p>
        <p class="bullet-item"><strong>Avoid empty cells</strong> <span>where possible</span></p>
        <p class="bullet-item">For complex tasks, <strong>break down instructions</strong></p>
      </div>
      <div class="info-box">
        <div class="info-box-header">
          <i class="ti ti-info-circle" style="font-size: 24px; color: #456AFC;"></i>
          <span class="info-box-title">Good to know</span>
        </div>
        <p class="info-box-content">Data Analyst is optimized for <strong>tabular data</strong></p>
      </div>
    </div>
    <div class="right-content">
      <div class="screenshot-placeholder">[Langdock UI Screenshot]</div>
    </div>
  </div>
</body>
</html>
```

## Variations

### 60/40 Split (More Content)
```css
.left-content { flex: 1.2; }
.right-content { flex: 0.8; }
```

### 40/60 Split (Larger Screenshot)
```css
.left-content { flex: 0.8; }
.right-content { flex: 1.2; }
```

### Without Info Box
Remove the `.info-box` section. The bullet list will fill the space.

### With Tags Instead of Bullets
```html
<div class="tags-container">
  <span class="tag">Feature 1</span>
  <span class="tag">Feature 2</span>
</div>
```

### With Demo Badge
Add above the screenshot:
```html
<div class="demo-badge">
  <i class="ti ti-player-play" style="font-size: 16px;"></i>
  <span>Live Demo</span>
</div>
```

```css
.demo-badge {
  position: absolute;
  top: 16px;
  right: 16px;
  background: #456AFC;
  color: white;
  padding: 8px 16px;
  border-radius: 100px;
  font-size: 14px;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 8px;
}
```
