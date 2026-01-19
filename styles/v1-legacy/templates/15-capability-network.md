# Capability Network Slide

Organic layout with icon + title + tags nodes, connected by subtle curved lines. Based on "What AI Can Do" reference slide.

## When to Use
- Feature/capability overviews
- "What can X do?" slides
- Technology ecosystem maps
- Related concepts visualization

## Layout Pattern
- Title at top (128px)
- 6 capability nodes in organic arrangement (not rigid grid)
- Nodes positioned absolutely for flexible placement
- Subtle curved solid lines connecting adjacent nodes
- Each node: icon (48px) → title → flowing tags

## Key Design Rules

1. **Node positioning**: Use absolute positioning, NOT flexbox grids
2. **Connectors**: SOLID light gray (`#e0e0e0`), NOT dashed
3. **Layout**: Organic/hexagonal feel - top row slightly offset from bottom row
4. **Spacing**: Generous gaps between nodes (~300-400px)

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Capability Overview - Langdock</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
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

    /* SVG connectors - SOLID lines, not dashed */
    .connectors {
      position: absolute;
      top: 0;
      left: 0;
      width: 1920px;
      height: 1080px;
      pointer-events: none;
      z-index: 0;
    }
    .connector {
      fill: none;
      stroke: #e0e0e0;
      stroke-width: 1.5;
      /* NO stroke-dasharray - solid lines */
    }

    /* Capability node */
    .capability {
      position: absolute;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 12px;
      max-width: 280px;
      z-index: 1;
    }
    .capability-icon {
      width: 48px;
      height: 48px;
      color: #456AFC;
    }
    .capability-title {
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
    .tag {
      background: #ededee;
      padding: 8px 14px;
      border-radius: 100px;
      font-size: 14px;
      font-weight: 500;
      color: #717279;
    }

    /* Organic positioning - adjust these for each slide */
    .cap-1 { top: 280px; left: 140px; }       /* Top left */
    .cap-2 { top: 260px; left: 50%; transform: translateX(-50%); }  /* Top center */
    .cap-3 { top: 280px; right: 140px; }      /* Top right */
    .cap-4 { top: 620px; left: 180px; }       /* Bottom left */
    .cap-5 { top: 640px; left: 50%; transform: translateX(-50%); }  /* Bottom center */
    .cap-6 { top: 620px; right: 180px; }      /* Bottom right */
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="color: #717279;"><path d="M9 6l6 6l-6 6" /></svg>
      <span class="footnote">Section Name</span>
    </div>
    <span class="slide-number">1</span>
  </div>

  <h1 class="main-title">Recap: What AI can do</h1>

  <!-- SVG Connectors - SOLID curved lines -->
  <svg class="connectors" viewBox="0 0 1920 1080">
    <!-- Top row: node 1 to node 2 -->
    <path class="connector" d="M 380 380 C 500 440, 700 440, 820 380" />
    <!-- Top row: node 2 to node 3 -->
    <path class="connector" d="M 1100 380 C 1220 440, 1420 440, 1540 380" />
    <!-- Left column: node 1 to node 4 -->
    <path class="connector" d="M 280 480 C 260 540, 260 580, 280 640" />
    <!-- Center column: node 2 to node 5 -->
    <path class="connector" d="M 960 460 C 960 520, 960 580, 960 640" />
    <!-- Right column: node 3 to node 6 -->
    <path class="connector" d="M 1640 480 C 1660 540, 1660 580, 1640 640" />
    <!-- Bottom row: node 4 to node 5 -->
    <path class="connector" d="M 420 720 C 540 780, 740 780, 860 720" />
    <!-- Bottom row: node 5 to node 6 -->
    <path class="connector" d="M 1060 720 C 1180 780, 1380 780, 1500 720" />
  </svg>

  <!-- Capability 1: Top Left -->
  <div class="capability cap-1">
    <svg class="capability-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M15 7l-6.5 6.5a1.5 1.5 0 0 0 3 3l6.5 -6.5a3 3 0 0 0 -6 -6l-6.5 6.5a4.5 4.5 0 0 0 9 9l6.5 -6.5" />
    </svg>
    <span class="capability-title">File Attachments</span>
    <div class="capability-tags">
      <span class="tag">Analyze contracts</span>
      <span class="tag">Summarize</span>
      <span class="tag">Answer questions about documents</span>
    </div>
  </div>

  <!-- Capability 2: Top Center -->
  <div class="capability cap-2">
    <svg class="capability-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M16 18a2 2 0 0 1 2 2a2 2 0 0 1 2 -2a2 2 0 0 1 -2 -2a2 2 0 0 1 -2 2m0 -12a2 2 0 0 1 2 2a2 2 0 0 1 2 -2a2 2 0 0 1 -2 -2a2 2 0 0 1 -2 2m-7 12a6 6 0 0 1 6 -6a6 6 0 0 1 -6 -6a6 6 0 0 1 -6 6a6 6 0 0 1 6 6" />
    </svg>
    <span class="capability-title">Plain Model</span>
    <div class="capability-tags">
      <span class="tag">Write texts</span>
      <span class="tag">Brainstorm</span>
      <span class="tag">Translate</span>
      <span class="tag">Explain concepts</span>
      <span class="tag">Code</span>
    </div>
  </div>

  <!-- Capability 3: Top Right -->
  <div class="capability cap-3">
    <svg class="capability-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M15 8h.01" />
      <path d="M3 6a3 3 0 0 1 3 -3h12a3 3 0 0 1 3 3v12a3 3 0 0 1 -3 3h-12a3 3 0 0 1 -3 -3v-12z" />
      <path d="M3 16l5 -5c.928 -.893 2.072 -.893 3 0l5 5" />
      <path d="M14 14l1 -1c.928 -.893 2.072 -.893 3 0l3 3" />
    </svg>
    <span class="capability-title">Image Generation</span>
    <div class="capability-tags">
      <span class="tag">Create mockups of products</span>
      <span class="tag">Create presentation images</span>
    </div>
  </div>

  <!-- Capability 4: Bottom Left -->
  <div class="capability cap-4">
    <svg class="capability-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M3 12a9 9 0 1 0 18 0a9 9 0 0 0 -18 0" />
      <path d="M3.6 9h16.8" />
      <path d="M3.6 15h16.8" />
      <path d="M11.5 3a17 17 0 0 0 0 18" />
      <path d="M12.5 3a17 17 0 0 1 0 18" />
    </svg>
    <span class="capability-title">Web Search</span>
    <div class="capability-tags">
      <span class="tag">Find companies online</span>
      <span class="tag">Find answers</span>
      <span class="tag">Use real-time information</span>
    </div>
  </div>

  <!-- Capability 5: Bottom Center -->
  <div class="capability cap-5">
    <svg class="capability-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M7 8l-4 4l4 4" />
      <path d="M17 8l4 4l-4 4" />
      <path d="M14 4l-4 16" />
    </svg>
    <span class="capability-title">Data Analysis</span>
    <div class="capability-tags">
      <span class="tag">Create tables</span>
      <span class="tag">Create graphs</span>
      <span class="tag">Find patterns</span>
      <span class="tag">Extract information</span>
      <span class="tag">Perform statistical analyses</span>
    </div>
  </div>

  <!-- Capability 6: Bottom Right -->
  <div class="capability cap-6">
    <svg class="capability-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M3 10a7 7 0 1 0 14 0a7 7 0 1 0 -14 0" />
      <path d="M21 21l-6 -6" />
    </svg>
    <span class="capability-title">Image Analysis</span>
    <div class="capability-tags">
      <span class="tag">Describe images</span>
      <span class="tag">Extract text</span>
      <span class="tag">Analyze graphs and tables</span>
    </div>
  </div>
</body>
</html>
```

## Variations

### 4-Node Layout
Remove 2 nodes and adjust positioning for a simpler layout.

### 3-Node Layout (Triangle)
Position 3 nodes in a triangle pattern for fewer capabilities.

### With Section Labels
Add a subtitle or category label above groups of nodes:
```html
<span class="section-label" style="position: absolute; top: 240px; left: 50%; transform: translateX(-50%);">
  Core Capabilities
</span>
```

### Without Connectors
For simpler slides, remove the SVG connector layer entirely.

## Connector Path Tips

SVG paths use Bezier curves: `M startX startY C controlX1 controlY1, controlX2 controlY2, endX endY`

- `M`: Move to start point
- `C`: Cubic Bezier curve with two control points
- Control points determine the curve shape
- Adjust coordinates based on actual node positions
