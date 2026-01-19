# Annotated Content Slide

Content with side annotations connected via dashed curved lines. Based on "Think out loud" and "Structure your prompt" reference slides.

## When to Use
- Prompting technique explanations
- Code/prompt structure breakdowns
- Visual callouts pointing to specific parts
- Side notes and explanations

## Layout Pattern
- Title at top (128px)
- Main content in center (tags, code block, or prompt example)
- Annotations positioned on sides with dashed curved connectors
- Dashed gray lines ONLY (not solid)

## Key Design Rules

1. **Annotation connectors**: DASHED gray (`#c0c0c0`, `stroke-dasharray="6 4"`)
2. **Annotation text**: Light gray `#717279`, smaller font (16px)
3. **Main content**: Can be prompt blocks, tags, or code
4. **Layout**: Annotations float around content, not in rigid columns

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Prompting Technique - Langdock</title>
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

    /* SVG connectors - DASHED lines for annotations */
    .connectors {
      position: absolute;
      top: 0;
      left: 0;
      width: 1920px;
      height: 1080px;
      pointer-events: none;
      z-index: 0;
    }
    .connector-dashed {
      fill: none;
      stroke: #c0c0c0;
      stroke-width: 1.5;
      stroke-dasharray: 6 4;
    }

    /* Annotation text */
    .annotation {
      position: absolute;
      max-width: 220px;
      z-index: 1;
    }
    .annotation-text {
      font-size: 16px;
      color: #717279;
      line-height: 1.5;
    }
    .annotation-text.right { text-align: right; }
    .annotation-text.left { text-align: left; }

    /* Main content area */
    .content-area {
      position: absolute;
      top: 300px;
      left: 300px;
      right: 300px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 16px;
      z-index: 1;
    }

    /* Prompt blocks */
    .prompt-row {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      justify-content: center;
    }
    .prompt-block {
      padding: 14px 24px;
      border-radius: 8px;
      font-size: 18px;
      font-weight: 500;
    }
    .prompt-block.neutral {
      background: #ededee;
      color: #121420;
    }
    .prompt-block.accent {
      background: #456AFC;
      color: #ffffff;
    }
    .prompt-block.outline {
      background: transparent;
      border: 1.5px dashed #c0c0c0;
      color: #717279;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="color: #717279;"><path d="M9 6l6 6l-6 6" /></svg>
      <span class="footnote">Advanced techniques</span>
    </div>
    <span class="slide-number">24</span>
  </div>

  <h1 class="main-title">Encourage the model to think out loud</h1>

  <!-- SVG Dashed Connectors -->
  <svg class="connectors" viewBox="0 0 1920 1080">
    <!-- Left annotation to first prompt block -->
    <path class="connector-dashed" d="M 220 420 C 280 420, 320 400, 380 400" />
    <!-- Right annotation from last prompt block -->
    <path class="connector-dashed" d="M 1540 680 C 1480 680, 1440 700, 1380 700" />
  </svg>

  <!-- Left Annotation -->
  <div class="annotation" style="top: 380px; left: 64px;">
    <p class="annotation-text right">The most-used technique, good to ask the model to think out loud</p>
  </div>

  <!-- Main Content -->
  <div class="content-area">
    <!-- Row 1 -->
    <div class="prompt-row">
      <div class="prompt-block accent">Think step by step and describe your thinking process</div>
      <div class="prompt-block neutral">Explain why</div>
    </div>

    <!-- Row 2 -->
    <div class="prompt-row">
      <div class="prompt-block neutral">First, let's understand the problem</div>
      <div class="prompt-block neutral">Break it into parts</div>
      <div class="prompt-block neutral">Here's what we know</div>
    </div>

    <!-- Row 3 -->
    <div class="prompt-row">
      <div class="prompt-block outline">Explain topic x for me. Include connected questions like y & z in your considerations.</div>
    </div>

    <!-- Row 4 -->
    <div class="prompt-row">
      <div class="prompt-block accent">First do task x, then do task y and finally do task z.</div>
    </div>
  </div>

  <!-- Right Annotation -->
  <div class="annotation" style="top: 660px; right: 64px;">
    <p class="annotation-text left">Example on the next slide</p>
  </div>
</body>
</html>
```

## Variations

### Split Layout with Annotations
Left side: numbered instructions
Right side: code/prompt block with annotation pointers

```html
<div class="split-layout">
  <div class="left-instructions">
    <div class="instruction">
      <span class="num">1</span>
      <span class="text">Split prompts into logical paragraphs</span>
    </div>
    <!-- More instructions... -->
  </div>
  <div class="right-content">
    <!-- Code block or prompt example -->
  </div>
</div>
```

### Code Block with Annotations
Annotations point to specific lines or sections of code.

### Dashed Info Box Variant
Use dashed border boxes instead of floating text:

```html
<div class="info-box-dashed">
  <p class="annotation-text">Use prompt elements</p>
</div>
```

```css
.info-box-dashed {
  border: 1.5px dashed #c0c0c0;
  border-radius: 12px;
  padding: 12px 16px;
  background: transparent;
}
```

## Connector Path Examples

### Left-to-right curve
```svg
<path d="M 220 420 C 280 420, 320 400, 380 400" />
```
Start at (220,420), curve right to (380,400)

### Right-to-left curve
```svg
<path d="M 1540 680 C 1480 680, 1440 700, 1380 700" />
```
Start at (1540,680), curve left to (1380,700)

### Top-to-bottom curve
```svg
<path d="M 400 300 C 400 350, 420 380, 450 400" />
```

### S-curve
```svg
<path d="M 200 300 C 300 300, 250 400, 350 400" />
```
