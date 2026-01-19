# Exercise Slide (Dark)

Call-to-action slide with dark background for hands-on activities.

## When to Use
- Hands-on exercises
- Practice moments
- Interactive breaks
- Activity prompts

## Layout Pattern
- Dark background (#242631)
- All content centered vertically and horizontally
- Label → Title → Duration → Tags
- Light text on dark

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Exercise - Langdock</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Inter', sans-serif;
      background: #242631;
      width: 1920px;
      height: 1080px;
      position: relative;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
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
    .footnote { font-size: 18px; font-weight: 500; color: rgba(248, 248, 249, 0.5); letter-spacing: -0.36px; }
    .slide-number { font-size: 18px; font-weight: 500; color: rgba(248, 248, 249, 0.5); }
    .exercise-label {
      font-size: 28px;
      font-weight: 600;
      color: #456AFC;
      margin-bottom: 24px;
    }
    .exercise-title {
      font-size: 64px;
      font-weight: 700;
      color: #ffffff;
      text-align: center;
      line-height: 1.2;
      max-width: 1000px;
      margin-bottom: 16px;
      letter-spacing: -3.2px;
    }
    .exercise-duration {
      font-size: 28px;
      font-weight: 500;
      color: #456AFC;
      margin-bottom: 64px;
    }
    .exercise-tags {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 16px;
      max-width: 1200px;
    }
    .tag-dark {
      padding: 12px 20px;
      background: rgba(255, 255, 255, 0.04);
      border-radius: 100px;
      font-size: 20px;
      font-weight: 500;
      color: #ffffff;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: rgba(248, 248, 249, 0.5);"></i>
      <span class="footnote">Assistants</span>
    </div>
    <span class="slide-number">27</span>
  </div>

  <span class="exercise-label">It's your turn!</span>
  <h1 class="exercise-title">Let's build an assistant with the prompt from earlier today</h1>
  <span class="exercise-duration">(5 min)</span>

  <div class="exercise-tags">
    <span class="tag-dark">Some ideas</span>
    <span class="tag-dark">Email writing Assistant</span>
    <span class="tag-dark">Grammar Checker</span>
    <span class="tag-dark">Translator, English ↔ German</span>
  </div>
</body>
</html>
```

## Variations

### Without Tags
Remove the `.exercise-tags` section for simpler exercises.

### Alternative Labels
- "It's your turn!"
- "Try it yourself"
- "Practice time"
- "Let's explore"
- "Hands-on exercise"

### Q&A Variant
```html
<span class="exercise-label">Questions?</span>
<h1 class="exercise-title">Let's discuss what we've learned</h1>
<span class="exercise-duration">(Open discussion)</span>
```

### Break Slide
```html
<span class="exercise-label">Take a break</span>
<h1 class="exercise-title">We'll continue in 10 minutes</h1>
```

## Dark Theme Colors

| Element | Color |
|---------|-------|
| Background | #242631 |
| Primary text | #ffffff |
| Accent | #456AFC |
| Secondary text | rgba(248, 248, 249, 0.5) |
| Tag background | rgba(255, 255, 255, 0.04) |
