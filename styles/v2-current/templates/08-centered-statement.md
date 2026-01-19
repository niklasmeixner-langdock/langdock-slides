# 08 - Centered Statement

Display powerful quotes, key takeaways, or important statements with visual impact.

## Use Cases
- Key takeaways
- Memorable quotes
- Important statistics
- Call-to-action moments
- Transition statements
- Summary points

## Layout Options

### Option A: Large Centered Quote

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
      padding: 64px 120px;
      position: relative;
    }

    .quote-mark {
      font-size: 120px;
      font-weight: 700;
      color: rgba(68, 105, 252, 0.15);
      line-height: 1;
      margin-bottom: -40px;
    }

    .statement {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      line-height: 1.3;
      color: #1a1c21;
      text-align: center;
      max-width: 1200px;
    }

    .highlight {
      color: #4469fc;
    }

    .attribution {
      margin-top: 48px;
      font-size: 18px;
      font-weight: 500;
      color: rgba(26,28,33,0.5);
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
    <div class="quote-mark">"</div>
    <p class="statement">AI adoption isn't about replacing people—it's about <span class="highlight">amplifying their capabilities</span> and freeing them to do their best work.</p>
    <p class="attribution">— The Langdock Philosophy</p>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Big Statistic

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
      background: #1a1c21;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 64px;
      position: relative;
    }

    .stat-number {
      font-size: 200px;
      font-weight: 700;
      letter-spacing: -8px;
      color: #4469fc;
      line-height: 1;
      margin-bottom: 24px;
    }

    .stat-label {
      font-size: 32px;
      font-weight: 600;
      letter-spacing: -0.64px;
      color: #FFFFFF;
      text-align: center;
      margin-bottom: 16px;
    }

    .stat-description {
      font-size: 20px;
      font-weight: 400;
      color: rgba(255,255,255,0.6);
      text-align: center;
      max-width: 600px;
    }

    .logo {
      position: absolute;
      bottom: 64px;
      left: 64px;
      height: 24px;
      width: auto;
      filter: brightness(0) invert(1);
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="stat-number">85%</div>
    <div class="stat-label">of employees want AI tools at work</div>
    <p class="stat-description">But only 25% of organizations have a secure, managed solution in place.</p>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option C: Key Takeaway Card

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
      justify-content: center;
      align-items: center;
      padding: 64px;
      position: relative;
    }

    .takeaway-card {
      background: #FFFFFF;
      border-radius: 24px;
      padding: 64px 80px;
      max-width: 1000px;
      text-align: center;
      box-shadow: 0px 8px 40px rgba(0, 0, 0, 0.08);
    }

    .icon-container {
      width: 72px;
      height: 72px;
      background: rgba(68, 105, 252, 0.1);
      border-radius: 18px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 32px;
    }

    .icon-container svg {
      width: 36px;
      height: 36px;
      color: #4469fc;
    }

    .label {
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 20px;
    }

    .statement {
      font-size: 36px;
      font-weight: 600;
      letter-spacing: -0.72px;
      line-height: 1.35;
      color: #1a1c21;
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
    <div class="takeaway-card">
      <div class="icon-container">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <line x1="9" y1="18" x2="15" y2="18"/>
          <line x1="10" y1="22" x2="14" y2="22"/>
          <path d="M15.09 14c.18-.98.65-1.74 1.41-2.5A4.65 4.65 0 0 0 18 8 6 6 0 0 0 6 8c0 1 .23 2.23 1.5 3.5A4.61 4.61 0 0 1 8.91 14"/>
        </svg>
      </div>
      <div class="label">Key Takeaway</div>
      <p class="statement">The best AI strategy isn't about choosing one model—it's about having access to the right model for each task.</p>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option D: Simple Bold Statement

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
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 64px 160px;
      position: relative;
    }

    .statement {
      font-size: 64px;
      font-weight: 600;
      letter-spacing: -1.28px;
      line-height: 1.2;
      color: #1a1c21;
      text-align: center;
    }

    .underline {
      display: inline;
      background: linear-gradient(to top, rgba(68, 105, 252, 0.2) 30%, transparent 30%);
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
    <p class="statement">Your employees are already using AI.<br>The question is whether <span class="underline">you're in control</span>.</p>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Text Emphasis Styles

```css
/* Blue highlight */
.highlight { color: #4469fc; }

/* Underline highlight */
.underline {
  background: linear-gradient(to top, rgba(68, 105, 252, 0.2) 30%, transparent 30%);
}

/* Bold emphasis */
.emphasis { font-weight: 700; }

/* Teal accent */
.accent { color: #96D7D2; }
```

## Font Size Guidelines

| Content Type | Size | Use When |
|-------------|------|----------|
| Short statement (3-8 words) | 64-72px | Punchy one-liners |
| Medium statement (10-20 words) | 48-56px | Key messages |
| Long quote (20+ words) | 36-44px | Full quotes with context |
| Statistics | 150-200px | Numbers that need impact |
