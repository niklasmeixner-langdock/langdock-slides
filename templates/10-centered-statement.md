# Centered Statement Slide

Single impactful message or quote with maximum visual focus.

## When to Use
- Key takeaways
- Powerful quotes
- Transition moments
- Core principles
- Summary statements

## Layout Pattern
- Light background
- All content vertically and horizontally centered
- Large bold text
- Optional subtitle below

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Key Message - Langdock</title>
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
    .footnote { font-size: 18px; font-weight: 500; color: #717279; letter-spacing: -0.36px; }
    .slide-number { font-size: 18px; font-weight: 500; color: #717279; }
    .centered-message {
      font-size: 72px;
      font-weight: 700;
      color: #121420;
      text-align: center;
      line-height: 1.2;
      max-width: 1400px;
      letter-spacing: -3.6px;
    }
    .centered-message .highlight {
      color: #456AFC;
    }
    .subtitle {
      font-size: 28px;
      font-weight: 500;
      color: #717279;
      text-align: center;
      margin-top: 32px;
      letter-spacing: -0.42px;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <span class="footnote">Key Insight</span>
    </div>
    <span class="slide-number">20</span>
  </div>

  <h1 class="centered-message">The best prompts are <span class="highlight">specific</span>, <span class="highlight">contextual</span>, and <span class="highlight">iterative</span></h1>
  <p class="subtitle">Good prompting is a conversation, not a command</p>
</body>
</html>
```

## Variations

### Without Subtitle
Remove the `.subtitle` element for pure focus on the message.

### With Icon
Add icon above the message:
```html
<i class="ti ti-bulb" style="font-size: 80px; color: #456AFC; margin-bottom: 40px;"></i>
<h1 class="centered-message">...</h1>
```

### Quote Style
```html
<h1 class="centered-message">"Your quote here"</h1>
<p class="subtitle">— Attribution Name</p>
```

### Smaller Text for Longer Messages
```css
.centered-message {
  font-size: 56px;
  letter-spacing: -2.8px;
}
```

### Multiple Highlighted Words
Use `<span class="highlight">` for each word you want in accent color.

### All Caps Variant
```css
.centered-message {
  text-transform: uppercase;
  letter-spacing: 4px;
  font-size: 48px;
}
```

## Examples

**Learning moment:**
```html
<h1 class="centered-message">AI is your <span class="highlight">copilot</span>, not your replacement</h1>
```

**Summary:**
```html
<h1 class="centered-message">Three things to remember: <span class="highlight">Context</span>, <span class="highlight">Clarity</span>, <span class="highlight">Iteration</span></h1>
```

**Transition:**
```html
<h1 class="centered-message">Now let's put this into <span class="highlight">practice</span></h1>
```
