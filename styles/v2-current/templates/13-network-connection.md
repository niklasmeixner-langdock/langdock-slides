# 13 - Network & Connection

Display connected elements, relationships, and network diagrams with visual lines.

## Use Cases
- System architecture
- Integration diagrams
- Feature relationships
- Data flow visualization
- Connection maps
- Ecosystem overview

## Layout Options

### Option A: Central Node with Connections

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Inter', sans-serif;
      -webkit-font-smoothing: antialiased;
    }

    .slide {
      width: 1920px;
      height: 1200px;
      background: #F8F8FC;
      padding: 64px;
      display: flex;
      flex-direction: column;
      position: relative;
    }

    .header {
      text-align: center;
      margin-bottom: 32px;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      color: #1a1c21;
    }

    .network-container {
      flex: 1;
      position: relative;
    }

    /* SVG connection lines */
    .connections-svg {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
    }

    .connection-line {
      stroke: #ECECF4;
      stroke-width: 2;
      fill: none;
    }

    /* Central node */
    .central-node {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      width: 200px;
      height: 200px;
      background: #1a1c21;
      border-radius: 50%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      z-index: 10;
    }

    .central-logo {
      height: 28px;
      width: auto;
      filter: brightness(0) invert(1);
      margin-bottom: 12px;
    }

    .central-title {
      font-size: 18px;
      font-weight: 600;
      color: #FFFFFF;
    }

    /* Outer nodes */
    .outer-node {
      position: absolute;
      background: #FFFFFF;
      border-radius: 16px;
      padding: 20px 24px;
      display: flex;
      align-items: center;
      gap: 16px;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.08);
      z-index: 5;
    }

    .node-icon {
      width: 44px;
      height: 44px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }

    .node-icon img {
      width: 28px;
      height: 28px;
      object-fit: contain;
    }

    .node-icon svg {
      width: 22px;
      height: 22px;
    }

    .node-icon.blue { background: rgba(68, 105, 252, 0.1); color: #4469fc; }
    .node-icon.green { background: rgba(34, 197, 94, 0.1); color: #22c55e; }
    .node-icon.purple { background: rgba(168, 85, 247, 0.1); color: #a855f7; }
    .node-icon.orange { background: rgba(249, 115, 22, 0.1); color: #f97316; }

    .node-content {
      display: flex;
      flex-direction: column;
    }

    .node-title {
      font-size: 16px;
      font-weight: 600;
      color: #1a1c21;
    }

    .node-subtitle {
      font-size: 13px;
      color: rgba(26,28,33,0.5);
    }

    /* Positioned nodes */
    .node-1 { top: 80px; left: 200px; }
    .node-2 { top: 80px; right: 200px; }
    .node-3 { top: 50%; left: 100px; transform: translateY(-50%); }
    .node-4 { top: 50%; right: 100px; transform: translateY(-50%); }
    .node-5 { bottom: 80px; left: 200px; }
    .node-6 { bottom: 80px; right: 200px; }

    .logo {
      position: absolute;
      bottom: 64px;
      left: 64px;
      height: 24px;
      width: auto;
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="header">
      <h1 class="title">Connected to Your Ecosystem</h1>
    </div>

    <div class="network-container">
      <!-- Connection lines SVG -->
      <svg class="connections-svg" viewBox="0 0 1792 820">
        <!-- Lines from center to each node -->
        <path class="connection-line" d="M 896 410 Q 600 300 350 120"/>
        <path class="connection-line" d="M 896 410 Q 1200 300 1450 120"/>
        <path class="connection-line" d="M 896 410 Q 500 410 200 410"/>
        <path class="connection-line" d="M 896 410 Q 1300 410 1600 410"/>
        <path class="connection-line" d="M 896 410 Q 600 520 350 700"/>
        <path class="connection-line" d="M 896 410 Q 1200 520 1450 700"/>
      </svg>

      <!-- Central Langdock node -->
      <div class="central-node">
        <img class="central-logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
        <span class="central-title">Langdock</span>
      </div>

      <!-- Outer nodes -->
      <div class="outer-node node-1">
        <div class="node-icon blue">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>
          </svg>
        </div>
        <div class="node-content">
          <span class="node-title">Slack</span>
          <span class="node-subtitle">Messaging</span>
        </div>
      </div>

      <div class="outer-node node-2">
        <div class="node-icon purple">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M14.5 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7.5L14.5 2z"/>
            <polyline points="14 2 14 8 20 8"/>
          </svg>
        </div>
        <div class="node-content">
          <span class="node-title">Notion</span>
          <span class="node-subtitle">Knowledge</span>
        </div>
      </div>

      <div class="outer-node node-3">
        <div class="node-icon green">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <ellipse cx="12" cy="5" rx="9" ry="3"/>
            <path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/>
          </svg>
        </div>
        <div class="node-content">
          <span class="node-title">Google Drive</span>
          <span class="node-subtitle">Storage</span>
        </div>
      </div>

      <div class="outer-node node-4">
        <div class="node-icon orange">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <rect x="2" y="3" width="20" height="14" rx="2" ry="2"/>
            <line x1="8" y1="21" x2="16" y2="21"/>
            <line x1="12" y1="17" x2="12" y2="21"/>
          </svg>
        </div>
        <div class="node-content">
          <span class="node-title">SharePoint</span>
          <span class="node-subtitle">Documents</span>
        </div>
      </div>

      <div class="outer-node node-5">
        <div class="node-icon blue">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/>
            <polyline points="22,6 12,13 2,6"/>
          </svg>
        </div>
        <div class="node-content">
          <span class="node-title">Outlook</span>
          <span class="node-subtitle">Email</span>
        </div>
      </div>

      <div class="outer-node node-6">
        <div class="node-icon purple">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <circle cx="12" cy="12" r="10"/>
            <line x1="2" y1="12" x2="22" y2="12"/>
            <path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/>
          </svg>
        </div>
        <div class="node-content">
          <span class="node-title">Confluence</span>
          <span class="node-subtitle">Wiki</span>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Flow Diagram (User to AI)

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Inter', sans-serif;
      -webkit-font-smoothing: antialiased;
    }

    .slide {
      width: 1920px;
      height: 1200px;
      background: #FFFFFF;
      padding: 64px;
      display: flex;
      flex-direction: column;
      position: relative;
    }

    .header {
      text-align: center;
      margin-bottom: 64px;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      color: #1a1c21;
    }

    .flow-container {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 48px;
      flex: 1;
    }

    .flow-node {
      background: #F8F8FC;
      border-radius: 20px;
      padding: 40px;
      width: 280px;
      text-align: center;
    }

    .flow-node.highlight {
      background: #1a1c21;
      color: #FFFFFF;
    }

    .flow-icon {
      width: 64px;
      height: 64px;
      background: rgba(68, 105, 252, 0.1);
      border-radius: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 20px;
    }

    .flow-node.highlight .flow-icon {
      background: rgba(255,255,255,0.1);
    }

    .flow-icon svg {
      width: 32px;
      height: 32px;
      color: #4469fc;
    }

    .flow-node.highlight .flow-icon svg {
      color: #FFFFFF;
    }

    .flow-title {
      font-size: 22px;
      font-weight: 600;
      margin-bottom: 8px;
    }

    .flow-description {
      font-size: 15px;
      color: rgba(26,28,33,0.55);
      line-height: 1.4;
    }

    .flow-node.highlight .flow-description {
      color: rgba(255,255,255,0.6);
    }

    .flow-arrow {
      width: 60px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 8px;
    }

    .arrow-line {
      width: 100%;
      height: 2px;
      background: #ECECF4;
      position: relative;
    }

    .arrow-line::after {
      content: '';
      position: absolute;
      right: 0;
      top: -4px;
      border: 5px solid transparent;
      border-left-color: #ECECF4;
    }

    .arrow-label {
      font-size: 12px;
      font-weight: 500;
      color: rgba(26,28,33,0.4);
    }

    .logo {
      position: absolute;
      bottom: 64px;
      left: 64px;
      height: 24px;
      width: auto;
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="header">
      <h1 class="title">How Langdock Works</h1>
    </div>

    <div class="flow-container">
      <div class="flow-node">
        <div class="flow-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/>
            <circle cx="12" cy="7" r="4"/>
          </svg>
        </div>
        <div class="flow-title">User</div>
        <div class="flow-description">Asks a question or gives a task</div>
      </div>

      <div class="flow-arrow">
        <span class="arrow-label">Query</span>
        <div class="arrow-line"></div>
      </div>

      <div class="flow-node highlight">
        <div class="flow-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <polygon points="12 2 2 7 12 12 22 7 12 2"/>
            <polyline points="2 17 12 22 22 17"/>
            <polyline points="2 12 12 17 22 12"/>
          </svg>
        </div>
        <div class="flow-title">Langdock</div>
        <div class="flow-description">Routes to best model, adds context</div>
      </div>

      <div class="flow-arrow">
        <span class="arrow-label">Enhanced</span>
        <div class="arrow-line"></div>
      </div>

      <div class="flow-node">
        <div class="flow-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M12 2a10 10 0 1 0 10 10H12V2z"/>
            <path d="M12 2a10 10 0 0 1 10 10"/>
          </svg>
        </div>
        <div class="flow-title">AI Models</div>
        <div class="flow-description">GPT-4, Claude, Gemini process request</div>
      </div>

      <div class="flow-arrow">
        <span class="arrow-label">Response</span>
        <div class="arrow-line"></div>
      </div>

      <div class="flow-node">
        <div class="flow-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/>
            <polyline points="22 4 12 14.01 9 11.01"/>
          </svg>
        </div>
        <div class="flow-title">Result</div>
        <div class="flow-description">Accurate, context-aware answer</div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Connection Line Styles

```css
/* Solid gray (default) */
.connection-line {
  stroke: #ECECF4;
  stroke-width: 2;
  fill: none;
}

/* Blue accent */
.connection-line {
  stroke: #4469fc;
  stroke-width: 2;
}

/* Dashed */
.connection-line {
  stroke: #ECECF4;
  stroke-width: 2;
  stroke-dasharray: 8 4;
}

/* Gradient */
.connection-line {
  stroke: url(#gradient);
}
```

## SVG Path Tips

For curved connections, use quadratic Bezier curves:
```
M startX startY Q controlX controlY endX endY
```

Example: `M 896 410 Q 600 300 350 120`
- Starts at center (896, 410)
- Control point at (600, 300)
- Ends at node position (350, 120)
