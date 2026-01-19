# Platform Overview / Architecture Slide

Shows the Langdock platform as a central hub connecting data sources to a unified frontend. Features visual flow with icons, the platform box, and output elements.

## When to Use
- Platform architecture explanation
- "How it works" slides
- Data flow visualization
- Enterprise deployment overview
- Single-entry-point messaging

## Layout Pattern
- Title with subtitle at top
- Left: scattered document/data source icons with connecting lines
- Center: dark Langdock platform box with 4 capability tiles
- Right: curved "Unified Web Frontend" banner
- Bottom: "Operated by you" annotation with customer logo

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Single-entry point - Langdock</title>
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
      top: 100px;
      left: 64px;
      font-size: 56px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -2.8px;
      line-height: 1.1;
    }
    .subtitle {
      position: absolute;
      top: 170px;
      left: 64px;
      font-size: 28px;
      font-weight: 500;
      color: #717279;
      letter-spacing: -0.42px;
    }

    /* Data Sources (Left Side) */
    .data-sources {
      position: absolute;
      top: 280px;
      left: 64px;
      width: 400px;
      height: 600px;
    }
    .data-icon {
      position: absolute;
      width: 48px;
      height: 48px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .data-icon img {
      width: 40px;
      height: 40px;
      object-fit: contain;
    }
    .data-icon.doc {
      background: #ffffff;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    }
    .data-icon.shape {
      background: #22c55e;
      border-radius: 8px;
    }

    /* Connection Lines */
    .connection-lines {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }
    .connection-lines path {
      stroke: #d0d0d0;
      stroke-width: 1;
      fill: none;
    }

    /* Platform Box (Center) */
    .platform-box {
      position: absolute;
      top: 280px;
      left: 520px;
      width: 480px;
      background: #242631;
      border-radius: 24px;
      padding: 32px;
    }
    .platform-header {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 24px;
    }
    .platform-logo {
      width: 24px;
      height: 24px;
    }
    .platform-name {
      font-size: 20px;
      font-weight: 600;
      color: #ffffff;
    }
    .platform-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }
    .platform-tile {
      background: rgba(255, 255, 255, 0.06);
      border-radius: 12px;
      padding: 20px;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .platform-tile-icon {
      width: 48px;
      height: 48px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .platform-tile-icon img {
      width: 32px;
      height: 32px;
    }
    .platform-tile-label {
      font-size: 16px;
      font-weight: 500;
      color: #ffffff;
    }
    .platform-tile-sub {
      font-size: 13px;
      color: rgba(255, 255, 255, 0.5);
    }

    /* Unified Frontend Banner (Right) */
    .unified-banner {
      position: absolute;
      top: 240px;
      right: 64px;
      width: 180px;
      height: 500px;
    }
    .unified-banner-inner {
      width: 100%;
      height: 100%;
      background: linear-gradient(180deg, #456AFC 0%, #8B9FD9 50%, #E8E8EA 100%);
      border-radius: 100px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
    }
    .unified-banner-text {
      writing-mode: vertical-rl;
      text-orientation: mixed;
      transform: rotate(180deg);
      font-size: 18px;
      font-weight: 600;
      color: #ffffff;
      letter-spacing: 2px;
      text-transform: uppercase;
    }
    .unified-banner-logo {
      position: absolute;
      top: 24px;
      width: 32px;
      height: 32px;
    }

    /* Bottom Annotation */
    .bottom-annotation {
      position: absolute;
      bottom: 100px;
      left: 520px;
      display: flex;
      align-items: center;
      gap: 24px;
    }
    .annotation-box {
      border: 1.5px dashed #22c55e;
      border-radius: 12px;
      padding: 16px 24px;
      display: flex;
      align-items: center;
      gap: 16px;
    }
    .annotation-text {
      font-size: 18px;
      font-weight: 500;
      color: #717279;
    }
    .customer-logo {
      height: 40px;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Langdock</span>
    </div>
    <span class="slide-number">5</span>
  </div>

  <h1 class="main-title">Single-entry point for all AI related tasks</h1>
  <p class="subtitle">Unifying previously fragmented internal and external solutions</p>

  <!-- Connection Lines SVG -->
  <svg class="connection-lines" viewBox="0 0 1920 1080">
    <!-- Curved lines from data sources to platform -->
    <path d="M 180 340 C 280 340, 400 400, 520 420"/>
    <path d="M 200 400 C 300 400, 400 450, 520 470"/>
    <path d="M 160 480 C 280 480, 400 500, 520 520"/>
    <path d="M 220 560 C 320 540, 420 540, 520 550"/>
    <path d="M 180 640 C 300 620, 420 580, 520 580"/>
    <path d="M 240 720 C 340 680, 440 620, 520 600"/>
    <!-- More lines... -->
  </svg>

  <!-- Data Sources -->
  <div class="data-sources">
    <div class="data-icon doc" style="top: 40px; left: 100px;">
      <i class="ti ti-file-text" style="font-size: 24px; color: #717279;"></i>
    </div>
    <div class="data-icon shape" style="top: 80px; left: 180px;"></div>
    <div class="data-icon doc" style="top: 140px; left: 60px;">
      <i class="ti ti-file-spreadsheet" style="font-size: 24px; color: #22c55e;"></i>
    </div>
    <div class="data-icon doc" style="top: 200px; left: 140px;">
      <i class="ti ti-file-analytics" style="font-size: 24px; color: #717279;"></i>
    </div>
    <div class="data-icon shape" style="top: 260px; left: 200px;"></div>
    <div class="data-icon doc" style="top: 320px; left: 80px;">
      <i class="ti ti-chart-bar" style="font-size: 24px; color: #22c55e;"></i>
    </div>
    <div class="data-icon doc" style="top: 380px; left: 160px;">
      <i class="ti ti-file-text" style="font-size: 24px; color: #717279;"></i>
    </div>
    <div class="data-icon shape" style="top: 440px; left: 100px;"></div>
  </div>

  <!-- Platform Box -->
  <div class="platform-box">
    <div class="platform-header">
      <img src="assets/langdock-logo.png" alt="Langdock" class="platform-logo">
      <span class="platform-name">Langdock</span>
    </div>
    <div class="platform-grid">
      <div class="platform-tile">
        <div class="platform-tile-icon">
          <i class="ti ti-message" style="font-size: 24px; color: #ffffff;"></i>
        </div>
        <span class="platform-tile-label">Chat</span>
      </div>
      <div class="platform-tile">
        <div class="platform-tile-icon">
          <i class="ti ti-robot" style="font-size: 24px; color: #ffffff;"></i>
        </div>
        <span class="platform-tile-label">Agents</span>
      </div>
      <div class="platform-tile">
        <div class="platform-tile-icon">
          <i class="ti ti-plug-connected" style="font-size: 24px; color: #ffffff;"></i>
        </div>
        <span class="platform-tile-label">Integrations</span>
        <span class="platform-tile-sub">API, MCP, A2A</span>
      </div>
      <div class="platform-tile">
        <div class="platform-tile-icon">
          <i class="ti ti-git-branch" style="font-size: 24px; color: #ffffff;"></i>
        </div>
        <span class="platform-tile-label">Workflows</span>
      </div>
    </div>
  </div>

  <!-- Unified Frontend Banner -->
  <div class="unified-banner">
    <div class="unified-banner-inner">
      <img src="assets/langdock-logo.png" alt="Langdock" class="unified-banner-logo">
      <span class="unified-banner-text">Langdock - Unified Web Frontend</span>
    </div>
  </div>

  <!-- Bottom Annotation -->
  <div class="bottom-annotation">
    <div class="annotation-box">
      <span class="annotation-text">Operated & managed<br>by you</span>
      <img src="logos/dekra.png" alt="DEKRA" class="customer-logo">
    </div>
  </div>
</body>
</html>
```

## Key Visual Elements

### Data Source Icons
Mix of document icons and colored shapes to represent diverse data sources:
```html
<!-- Document icon -->
<div class="data-icon doc">
  <i class="ti ti-file-text" style="font-size: 24px; color: #717279;"></i>
</div>

<!-- Colored shape -->
<div class="data-icon shape"></div>
```

### Connection Lines
Use SVG cubic bezier curves for organic flow:
```html
<path d="M startX startY C controlX1 controlY1, controlX2 controlY2, endX endY"/>
```

### Platform Tiles
4 core capabilities in a 2x2 grid:
- Chat
- Agents
- Integrations (with subtitle)
- Workflows

## Variations

### Without Customer Logo
Remove the bottom annotation for generic presentations.

### With More Platform Features
Expand grid to 3x2 for additional capabilities:
```css
.platform-grid {
  grid-template-columns: repeat(3, 1fr);
}
```

### Horizontal Banner
Replace vertical banner with horizontal bottom banner:
```css
.unified-banner {
  position: absolute;
  bottom: 140px;
  right: 64px;
  width: 400px;
  height: 80px;
}
.unified-banner-inner {
  border-radius: 40px;
}
.unified-banner-text {
  writing-mode: horizontal-tb;
  transform: none;
}
```
