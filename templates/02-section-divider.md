# Section Divider Slide

Big title with gradient background to introduce new sections.

## When to Use
- Chapter transitions
- Major section breaks
- Visual breathing room
- Topic introductions

## Layout Pattern
- Organic gradient background (radial gradients, NOT linear)
- Logo placeholder top-left (add Langdock logo manually in Figma)
- Large title bottom-left
- Optional subtitle below title in secondary color
- No header/slide number

## IMPORTANT: Gradient Positioning
- Use `bottom: -120px` to ensure gradient touches the canvas edge (html-to-design adds padding)
- Use radial gradients with `at X% 100%` to anchor to bottom
- Height should be ~820px to create good coverage
- Avoid linear gradients - they look flat and boring

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@700&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Inter', sans-serif;
      width: 1920px;
      height: 1080px;
      position: relative;
      background: #f8f8f9;
    }
    .gradient-bg {
      position: absolute;
      bottom: -120px;
      left: 0;
      width: 1920px;
      height: 820px;
      background: radial-gradient(ellipse 120% 120% at 85% 100%, rgba(170,160,255,0.5) 0%, transparent 50%),
                  radial-gradient(ellipse 100% 100% at 50% 100%, rgba(150,190,255,0.4) 0%, transparent 45%),
                  radial-gradient(ellipse 80% 80% at 15% 100%, rgba(130,180,255,0.3) 0%, transparent 40%);
    }
    .logo-placeholder {
      position: absolute;
      top: 80px;
      left: 64px;
      font-size: 14px;
      color: #717279;
      background: #ededee;
      padding: 8px 12px;
      border-radius: 4px;
    }
    .section-title {
      position: absolute;
      bottom: 120px;
      left: 64px;
      font-size: 96px;
      font-weight: 700;
      color: #121420;
      letter-spacing: -4.8px;
    }
    .section-subtitle {
      position: absolute;
      bottom: 40px;
      left: 64px;
      font-size: 96px;
      font-weight: 700;
      color: #717279;
      letter-spacing: -4.8px;
    }
  </style>
</head>
<body>
  <div class="gradient-bg"></div>
  <div class="logo-placeholder">[Add Langdock logo]</div>
  <h1 class="section-title">Section Title</h1>
  <p class="section-subtitle">Subtitle Text</p>
</body>
</html>
```

## Key Learnings

### Logo
- Cannot use local file paths with html-to-design MCP
- Use a placeholder `[Add Langdock logo]` and add the logo manually in Figma after import
- Logo position: top 80px, left 64px

### Gradient
- **DO NOT use linear gradients** - they look flat and boring
- Use multiple overlapping radial gradients for an organic, cloud-like effect
- Anchor gradients to bottom with `at X% 100%` positioning
- Use `bottom: -120px` to compensate for html-to-design padding
- Colors: purple/violet (`rgba(170,160,255,0.5)`), light blue (`rgba(150,190,255,0.4)`), cyan (`rgba(130,180,255,0.3)`)
- Spread across the entire bottom, not just one corner

### Typography
- Title: 96px, font-weight 700, color #121420, letter-spacing -4.8px
- Subtitle: 96px, font-weight 700, color #717279 (secondary text color from design system)
- Both positioned at bottom-left with 64px left margin
- Title at bottom: 120px, Subtitle at bottom: 40px

## Variations

### Title Only (No Subtitle)
Simply remove the subtitle element.

### Different Gradient Colors

**Warmer purple/pink:**
```css
background: radial-gradient(ellipse 120% 120% at 85% 100%, rgba(200,150,255,0.5) 0%, transparent 50%),
            radial-gradient(ellipse 100% 100% at 50% 100%, rgba(180,160,255,0.4) 0%, transparent 45%),
            radial-gradient(ellipse 80% 80% at 15% 100%, rgba(160,140,255,0.3) 0%, transparent 40%);
```

**More blue/cyan:**
```css
background: radial-gradient(ellipse 120% 120% at 85% 100%, rgba(130,180,255,0.5) 0%, transparent 50%),
            radial-gradient(ellipse 100% 100% at 50% 100%, rgba(120,200,255,0.4) 0%, transparent 45%),
            radial-gradient(ellipse 80% 80% at 15% 100%, rgba(100,220,255,0.3) 0%, transparent 40%);
```
