# Goals/Agenda Slide

Numbered list with objectives positioned in the lower third of the slide.

## When to Use
- Session openers
- Learning objectives
- Key takeaways
- Agenda lists (3-5 items)

## Layout Pattern
- Title at top (128px)
- Large whitespace in middle
- Goals list at ~664px from top
- Optional footer note at bottom

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Goals for today - Langdock</title>
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
    .breadcrumbs {
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .footnote {
      font-size: 18px;
      font-weight: 500;
      color: #717279;
      letter-spacing: -0.36px;
    }
    .slide-number {
      font-size: 18px;
      font-weight: 500;
      color: #717279;
    }
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
    .goals-list {
      position: absolute;
      top: 664px;
      left: 64px;
      display: flex;
      flex-direction: column;
      gap: 32px;
    }
    .goal-item {
      display: flex;
      align-items: baseline;
      gap: 20px;
    }
    .goal-number {
      font-size: 40px;
      font-weight: 500;
      color: #717279;
      line-height: 1.2;
      min-width: 50px;
    }
    .goal-text {
      font-size: 40px;
      font-weight: 700;
      color: #121420;
      line-height: 1.2;
      letter-spacing: -1.6px;
    }
    .footer-note {
      position: absolute;
      bottom: 64px;
      left: 64px;
      font-size: 18px;
      font-weight: 400;
      color: #717279;
      line-height: 1.5;
    }
    .footer-note a {
      color: #121420;
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Agenda</span>
    </div>
    <span class="slide-number">1</span>
  </div>

  <h1 class="main-title">Goals for today</h1>

  <div class="goals-list">
    <div class="goal-item">
      <span class="goal-number">01</span>
      <span class="goal-text">Get an Overview</span>
    </div>
    <div class="goal-item">
      <span class="goal-number">02</span>
      <span class="goal-text">Learn more about the functionalities</span>
    </div>
    <div class="goal-item">
      <span class="goal-number">03</span>
      <span class="goal-text">Build your first AI assistant</span>
    </div>
  </div>

  <p class="footer-note">We recommend to open <a href="https://app.langdock.com">app.langdock.com</a> and take notes.</p>
</body>
</html>
```

## Customization

### Number of Goals
- 3 goals: Use 32px gap (default)
- 4-5 goals: Reduce to 24px gap, move list higher (top: 580px)

### Without Footer
Remove the `.footer-note` element and CSS.

### Alternative Titles
- "Learning Objectives"
- "What we'll cover"
- "Today's Agenda"
- "Key Takeaways"
