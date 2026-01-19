# 01 - Section Divider / Title Slide

A bold, full-screen slide for chapter transitions and section introductions.

## Use Cases
- Session title slides
- Chapter/module transitions
- Major section breaks
- Topic introductions

## Layout Options

### Option A: Centered Title (Light Background)

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
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 64px;
      position: relative;
    }

    .content {
      text-align: center;
      max-width: 1200px;
    }

    .section-label {
      font-size: 16px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 24px;
    }

    .title {
      font-size: 72px;
      font-weight: 600;
      letter-spacing: -1.44px;
      line-height: 1.1;
      color: #1a1c21;
      margin-bottom: 24px;
    }

    .subtitle {
      font-size: 24px;
      font-weight: 400;
      letter-spacing: -0.24px;
      line-height: 1.4;
      color: rgba(26,28,33,0.55);
      max-width: 700px;
      margin: 0 auto;
    }

    .logo {
      position: absolute;
      bottom: 64px;
      left: 64px;
      height: 24px;
      width: auto;
    }

    .slide-number {
      position: absolute;
      bottom: 64px;
      right: 64px;
      font-size: 14px;
      font-weight: 500;
      color: rgba(26,28,33,0.3);
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="content">
      <div class="section-label">Module 1</div>
      <h1 class="title">Getting Started with Langdock</h1>
      <p class="subtitle">Learn the fundamentals of the platform and how to navigate the interface effectively.</p>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
    <div class="slide-number">01</div>
  </div>
</body>
</html>
```

### Option B: Dark Background with Accent

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
      background: #4d473c;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 64px;
      position: relative;
      overflow: hidden;
    }

    /* Decorative accent circle */
    .accent-circle {
      position: absolute;
      width: 600px;
      height: 600px;
      border-radius: 50%;
      background: rgba(150, 215, 210, 0.15);
      filter: blur(100px);
      top: -200px;
      right: -100px;
    }

    .content {
      text-align: center;
      max-width: 1200px;
      position: relative;
      z-index: 1;
    }

    .section-label {
      font-size: 16px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #96D7D2;
      margin-bottom: 24px;
    }

    .title {
      font-size: 72px;
      font-weight: 600;
      letter-spacing: -1.44px;
      line-height: 1.1;
      color: #FFFFFF;
      margin-bottom: 24px;
    }

    .subtitle {
      font-size: 24px;
      font-weight: 400;
      letter-spacing: -0.24px;
      line-height: 1.4;
      color: rgba(255,255,255,0.75);
      max-width: 700px;
      margin: 0 auto;
    }

    .logo {
      position: absolute;
      bottom: 64px;
      left: 64px;
      height: 24px;
      width: auto;
      filter: brightness(0) invert(1);
    }

    .slide-number {
      position: absolute;
      bottom: 64px;
      right: 64px;
      font-size: 14px;
      font-weight: 500;
      color: rgba(255,255,255,0.4);
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="accent-circle"></div>

    <div class="content">
      <div class="section-label">Module 2</div>
      <h1 class="title">Advanced Features</h1>
      <p class="subtitle">Explore powerful capabilities that help you get the most out of AI in your workflow.</p>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
    <div class="slide-number">02</div>
  </div>
</body>
</html>
```

### Option C: Left-Aligned with Large Number

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
      display: flex;
      align-items: center;
      padding: 64px 120px;
      position: relative;
    }

    .big-number {
      font-size: 400px;
      font-weight: 700;
      color: rgba(26,28,33,0.04);
      position: absolute;
      right: 80px;
      top: 50%;
      transform: translateY(-50%);
      line-height: 1;
    }

    .content {
      max-width: 900px;
      position: relative;
      z-index: 1;
    }

    .section-label {
      font-size: 16px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 24px;
    }

    .title {
      font-size: 64px;
      font-weight: 600;
      letter-spacing: -1.28px;
      line-height: 1.1;
      color: #1a1c21;
      margin-bottom: 24px;
    }

    .subtitle {
      font-size: 24px;
      font-weight: 400;
      letter-spacing: -0.24px;
      line-height: 1.5;
      color: rgba(26,28,33,0.55);
    }

    .logo {
      position: absolute;
      bottom: 64px;
      left: 120px;
      height: 24px;
      width: auto;
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="big-number">01</div>

    <div class="content">
      <div class="section-label">Chapter One</div>
      <h1 class="title">Introduction to AI-Powered Workflows</h1>
      <p class="subtitle">Understanding how artificial intelligence can transform your daily tasks and boost productivity across your organization.</p>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Customization

### Section Labels
- Use for module numbers, chapter names, or topic categories
- Always uppercase with letter-spacing
- Accent blue (`#4469fc`) on light backgrounds
- Teal (`#96D7D2`) on dark backgrounds

### Title Sizes
| Context | Size | Use When |
|---------|------|----------|
| Short title (1-3 words) | 80-96px | "Chat", "Agents" |
| Medium title (4-8 words) | 64-72px | "Getting Started with Langdock" |
| Long title (9+ words) | 48-56px | Full sentences |

### Background Choices
| Style | When to Use |
|-------|-------------|
| Light (`#F8F8FC`) | Standard sections, informational content |
| Dark (`#4d473c`) | Key transitions, emphasis moments |
| White (`#FFFFFF`) | Clean, minimal sections |
