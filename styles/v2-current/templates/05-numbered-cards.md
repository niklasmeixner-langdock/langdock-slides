# 05 - Numbered Cards

Display step-by-step processes, sequential instructions, or numbered features in card format.

## Use Cases
- How-to guides
- Process flows
- Step-by-step instructions
- Numbered feature highlights
- Workflow explanations

## Layout Options

### Option A: 4-Column Horizontal Cards

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
      flex-direction: column;
      position: relative;
    }

    .header {
      text-align: center;
      margin-bottom: 64px;
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
      color: #1a1c21;
    }

    .cards-container {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 24px;
      flex: 1;
    }

    .card {
      background: #FFFFFF;
      border-radius: 16px;
      padding: 32px;
      display: flex;
      flex-direction: column;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
    }

    .card-number {
      width: 48px;
      height: 48px;
      background: #1a1c21;
      color: #FFFFFF;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      font-weight: 600;
      margin-bottom: 24px;
    }

    .card-title {
      font-size: 22px;
      font-weight: 600;
      letter-spacing: -0.44px;
      color: #1a1c21;
      margin-bottom: 12px;
    }

    .card-description {
      font-size: 16px;
      font-weight: 400;
      line-height: 1.5;
      color: rgba(26,28,33,0.55);
      flex: 1;
    }

    .card-icon {
      margin-top: auto;
      padding-top: 24px;
    }

    .card-icon svg {
      width: 32px;
      height: 32px;
      color: rgba(26,28,33,0.2);
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
      <div class="label">Getting Started</div>
      <h1 class="title">Four Steps to AI-Powered Productivity</h1>
    </div>

    <div class="cards-container">
      <div class="card">
        <div class="card-number">1</div>
        <div class="card-title">Sign Up & Log In</div>
        <div class="card-description">Create your account using your company email and SSO credentials.</div>
        <div class="card-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
            <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/>
            <circle cx="12" cy="7" r="4"/>
          </svg>
        </div>
      </div>

      <div class="card">
        <div class="card-number">2</div>
        <div class="card-title">Explore the Chat</div>
        <div class="card-description">Start a conversation with any AI model. Try different models for different tasks.</div>
        <div class="card-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
            <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>
          </svg>
        </div>
      </div>

      <div class="card">
        <div class="card-number">3</div>
        <div class="card-title">Connect Knowledge</div>
        <div class="card-description">Link your documents and data sources for context-aware responses.</div>
        <div class="card-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
            <ellipse cx="12" cy="5" rx="9" ry="3"/>
            <path d="M21 12c0 1.66-4 3-9 3s-9-1.34-9-3"/>
            <path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/>
          </svg>
        </div>
      </div>

      <div class="card">
        <div class="card-number">4</div>
        <div class="card-title">Build Assistants</div>
        <div class="card-description">Create custom AI assistants tailored to your specific workflows.</div>
        <div class="card-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
            <rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
            <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
          </svg>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: 3-Column with Connector Lines

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
      flex-direction: column;
      position: relative;
    }

    .header {
      text-align: center;
      margin-bottom: 80px;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      color: #1a1c21;
    }

    .steps-container {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      gap: 48px;
      flex: 1;
      padding: 0 48px;
      position: relative;
    }

    /* Connector line */
    .connector-line {
      position: absolute;
      top: 32px;
      left: 50%;
      transform: translateX(-50%);
      width: 800px;
      height: 2px;
      background: #ECECF4;
      z-index: 0;
    }

    .step {
      flex: 1;
      max-width: 400px;
      text-align: center;
      position: relative;
      z-index: 1;
    }

    .step-number {
      width: 64px;
      height: 64px;
      background: #4469fc;
      color: #FFFFFF;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 24px;
      font-weight: 600;
      margin: 0 auto 32px;
      box-shadow: 0px 4px 12px rgba(68, 105, 252, 0.25);
    }

    .step-title {
      font-size: 24px;
      font-weight: 600;
      letter-spacing: -0.48px;
      color: #1a1c21;
      margin-bottom: 16px;
    }

    .step-description {
      font-size: 18px;
      font-weight: 400;
      line-height: 1.6;
      color: rgba(26,28,33,0.55);
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
      <h1 class="title">How It Works</h1>
    </div>

    <div class="steps-container">
      <div class="connector-line"></div>

      <div class="step">
        <div class="step-number">1</div>
        <div class="step-title">Ask a Question</div>
        <div class="step-description">Type your question or request in natural language. No special syntax required.</div>
      </div>

      <div class="step">
        <div class="step-number">2</div>
        <div class="step-title">AI Processes</div>
        <div class="step-description">Langdock routes your request to the best model and retrieves relevant context.</div>
      </div>

      <div class="step">
        <div class="step-number">3</div>
        <div class="step-title">Get Results</div>
        <div class="step-description">Receive accurate, context-aware responses you can trust and act on.</div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option C: Vertical Steps (Left-Aligned)

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
      gap: 80px;
      position: relative;
    }

    .content {
      width: 500px;
      display: flex;
      flex-direction: column;
      justify-content: center;
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
    }

    .steps-container {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      gap: 32px;
    }

    .step {
      display: flex;
      align-items: flex-start;
      gap: 24px;
      background: #FFFFFF;
      border-radius: 16px;
      padding: 28px 32px;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
    }

    .step-number {
      width: 40px;
      height: 40px;
      background: #ECECF4;
      color: #1a1c21;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 18px;
      font-weight: 600;
      flex-shrink: 0;
    }

    .step-content {
      flex: 1;
    }

    .step-title {
      font-size: 20px;
      font-weight: 600;
      letter-spacing: -0.4px;
      color: #1a1c21;
      margin-bottom: 6px;
    }

    .step-description {
      font-size: 16px;
      font-weight: 400;
      line-height: 1.5;
      color: rgba(26,28,33,0.55);
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
      <h1 class="title">Creating Your First Assistant</h1>
      <p class="description">Follow these simple steps to build a custom AI assistant tailored to your team's needs.</p>
    </div>

    <div class="steps-container">
      <div class="step">
        <div class="step-number">1</div>
        <div class="step-content">
          <div class="step-title">Navigate to Assistants</div>
          <div class="step-description">Click on the Assistants tab in the left sidebar to access the assistant builder.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-number">2</div>
        <div class="step-content">
          <div class="step-title">Click "Create New"</div>
          <div class="step-description">Start from scratch or choose from pre-built templates for common use cases.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-number">3</div>
        <div class="step-content">
          <div class="step-title">Configure Instructions</div>
          <div class="step-description">Define your assistant's personality, capabilities, and knowledge sources.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-number">4</div>
        <div class="step-content">
          <div class="step-title">Test & Deploy</div>
          <div class="step-description">Try your assistant, refine as needed, then share with your team.</div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Number Style Variants

```css
/* Dark square (default) */
.card-number {
  background: #1a1c21;
  color: #FFFFFF;
  border-radius: 12px;
}

/* Blue circle */
.card-number {
  background: #4469fc;
  color: #FFFFFF;
  border-radius: 50%;
  box-shadow: 0px 4px 12px rgba(68, 105, 252, 0.25);
}

/* Light square */
.card-number {
  background: #ECECF4;
  color: #1a1c21;
  border-radius: 12px;
}

/* Outline circle */
.card-number {
  background: transparent;
  border: 2px solid #4469fc;
  color: #4469fc;
  border-radius: 50%;
}
```

## Layout Guidelines

| Steps | Recommended Layout |
|-------|-------------------|
| 2-3 | Horizontal with connector lines |
| 3-4 | 3-4 column cards |
| 4-6 | Vertical list format |
| 6+ | Consider splitting across multiple slides |
