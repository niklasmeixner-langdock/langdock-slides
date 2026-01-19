# 04 - Split Layout with Screenshot

Display content alongside a UI screenshot or visual for feature explanations.

## Use Cases
- Feature demonstrations
- UI walkthroughs
- Product screenshots with explanations
- Before/after visuals
- Step explanations with context

## Layout Options

### Option A: Left Content, Right Screenshot

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
      height: 1080px;
      background: #F8F8FC;
      padding: 64px;
      display: flex;
      gap: 64px;
      position: relative;
    }

    .content {
      width: 600px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .label {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 16px;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      line-height: 1.1;
      color: #1a1c21;
      margin-bottom: 24px;
    }

    .description {
      font-size: 20px;
      font-weight: 400;
      line-height: 1.6;
      color: rgba(26,28,33,0.55);
      margin-bottom: 40px;
    }

    .features {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .feature-item {
      display: flex;
      align-items: flex-start;
      gap: 16px;
    }

    .feature-icon {
      width: 24px;
      height: 24px;
      background: rgba(68, 105, 252, 0.1);
      border-radius: 6px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }

    .feature-icon svg {
      width: 14px;
      height: 14px;
      color: #4469fc;
    }

    .feature-text {
      font-size: 18px;
      font-weight: 500;
      color: #1a1c21;
    }

    .screenshot-container {
      flex: 1;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .screenshot {
      width: 100%;
      max-width: 1000px;
      background: #FFFFFF;
      border-radius: 16px;
      box-shadow: 0px 8px 40px rgba(0, 0, 0, 0.12);
      overflow: hidden;
    }

    .screenshot img {
      width: 100%;
      height: auto;
      display: block;
    }

    /* Browser chrome mockup */
    .browser-chrome {
      background: #ECECF4;
      padding: 12px 16px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .browser-dots {
      display: flex;
      gap: 6px;
    }

    .browser-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: rgba(26,28,33,0.15);
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
    <div class="content">
      <div class="label">Feature</div>
      <h1 class="title">Chat with Multiple AI Models</h1>
      <p class="description">Access GPT-4, Claude, Gemini, and more from a single interface. Switch models mid-conversation for different perspectives.</p>

      <div class="features">
        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
          <span class="feature-text">One interface, multiple models</span>
        </div>
        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
          <span class="feature-text">Switch models mid-conversation</span>
        </div>
        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
          <span class="feature-text">Compare outputs side-by-side</span>
        </div>
      </div>
    </div>

    <div class="screenshot-container">
      <div class="screenshot">
        <div class="browser-chrome">
          <div class="browser-dots">
            <div class="browser-dot"></div>
            <div class="browser-dot"></div>
            <div class="browser-dot"></div>
          </div>
        </div>
        <img src="[SCREENSHOT_URL]" alt="Langdock Chat Interface">
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Full-Width Screenshot with Overlay

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
      height: 1080px;
      background: #1a1c21;
      position: relative;
      overflow: hidden;
    }

    .screenshot-bg {
      position: absolute;
      inset: 0;
      opacity: 0.3;
    }

    .screenshot-bg img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .content-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      background: linear-gradient(to top, rgba(26,28,33,0.95) 0%, rgba(26,28,33,0.8) 50%, transparent 100%);
      padding: 64px;
      padding-top: 200px;
    }

    .content {
      max-width: 800px;
    }

    .label {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #96D7D2;
      margin-bottom: 16px;
    }

    .title {
      font-size: 56px;
      font-weight: 600;
      letter-spacing: -1.12px;
      line-height: 1.1;
      color: #FFFFFF;
      margin-bottom: 20px;
    }

    .description {
      font-size: 20px;
      font-weight: 400;
      line-height: 1.6;
      color: rgba(255,255,255,0.7);
    }

    .logo {
      position: absolute;
      bottom: 64px;
      right: 64px;
      height: 24px;
      width: auto;
      filter: brightness(0) invert(1);
    }
  </style>
</head>
<body>
  <div class="slide">
    <div class="screenshot-bg">
      <img src="[SCREENSHOT_URL]" alt="Background">
    </div>

    <div class="content-overlay">
      <div class="content">
        <div class="label">Live Demo</div>
        <h1 class="title">The Langdock Interface</h1>
        <p class="description">A clean, intuitive workspace designed for productivity. Access all your AI tools from one unified dashboard.</p>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option C: Right Content, Left Screenshot (Flipped)

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
      height: 1080px;
      background: #FFFFFF;
      padding: 64px;
      display: flex;
      gap: 64px;
      position: relative;
    }

    .screenshot-container {
      flex: 1;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .screenshot {
      width: 100%;
      max-width: 900px;
      background: #F8F8FC;
      border-radius: 16px;
      box-shadow: 0px 8px 40px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      padding: 24px;
    }

    .screenshot img {
      width: 100%;
      height: auto;
      display: block;
      border-radius: 8px;
    }

    .content {
      width: 550px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .title {
      font-size: 44px;
      font-weight: 600;
      letter-spacing: -0.88px;
      line-height: 1.15;
      color: #1a1c21;
      margin-bottom: 24px;
    }

    .description {
      font-size: 18px;
      font-weight: 400;
      line-height: 1.6;
      color: rgba(26,28,33,0.55);
      margin-bottom: 32px;
    }

    .cta-button {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: #1a1c21;
      color: #FFFFFF;
      padding: 14px 28px;
      border-radius: 100px;
      font-size: 16px;
      font-weight: 500;
      text-decoration: none;
      width: fit-content;
    }

    .cta-button svg {
      width: 18px;
      height: 18px;
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
    <div class="screenshot-container">
      <div class="screenshot">
        <img src="[SCREENSHOT_URL]" alt="Langdock Assistants">
      </div>
    </div>

    <div class="content">
      <h1 class="title">Build Custom Assistants for Every Team</h1>
      <p class="description">Create specialized AI assistants with custom instructions, knowledge bases, and capabilities. Share them across your organization or keep them private.</p>

      <a href="#" class="cta-button">
        Learn more
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <line x1="5" y1="12" x2="19" y2="12"/>
          <polyline points="12 5 19 12 12 19"/>
        </svg>
      </a>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Screenshot Styling

### Browser Chrome (Realistic)
```css
.browser-chrome {
  background: #ECECF4;
  padding: 12px 16px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.browser-dots {
  display: flex;
  gap: 6px;
}

.browser-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: rgba(26,28,33,0.15);
}
```

### Floating Shadow
```css
.screenshot {
  box-shadow: 0px 8px 40px rgba(0, 0, 0, 0.12);
  border-radius: 16px;
}
```

### Padded Container
```css
.screenshot {
  background: #F8F8FC;
  padding: 24px;
  border-radius: 16px;
}

.screenshot img {
  border-radius: 8px;
}
```

## Placeholder for Screenshots

When screenshot URL is not available:
```html
<div class="screenshot-placeholder" style="
  background: linear-gradient(135deg, #ECECF4 0%, #F8F8FC 100%);
  aspect-ratio: 16/10;
  display: flex;
  align-items: center;
  justify-content: center;
  color: rgba(26,28,33,0.3);
  font-size: 14px;
">
  Screenshot placeholder
</div>
```
