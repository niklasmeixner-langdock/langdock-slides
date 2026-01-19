# 06 - Exercise Slide (Dark)

A dark-themed slide for hands-on activities, practice moments, and interactive exercises.

## Use Cases
- Hands-on exercises
- Practice activities
- Interactive moments
- Workshop breaks
- Try-it-yourself prompts
- Demo pauses

## Layout Options

### Option A: Centered Exercise Prompt

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

    /* Decorative elements */
    .accent-circle {
      position: absolute;
      width: 500px;
      height: 500px;
      border-radius: 50%;
      background: rgba(150, 215, 210, 0.1);
      filter: blur(80px);
    }

    .accent-circle-1 {
      top: -200px;
      right: -100px;
    }

    .accent-circle-2 {
      bottom: -200px;
      left: -100px;
    }

    .content {
      text-align: center;
      max-width: 900px;
      position: relative;
      z-index: 1;
    }

    .exercise-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(255,255,255,0.15);
      padding: 10px 20px;
      border-radius: 100px;
      margin-bottom: 32px;
    }

    .exercise-badge svg {
      width: 20px;
      height: 20px;
      color: #96D7D2;
    }

    .exercise-badge span {
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #FFFFFF;
    }

    .title {
      font-size: 56px;
      font-weight: 600;
      letter-spacing: -1.12px;
      line-height: 1.15;
      color: #FFFFFF;
      margin-bottom: 24px;
    }

    .description {
      font-size: 22px;
      font-weight: 400;
      line-height: 1.6;
      color: rgba(255,255,255,0.7);
      margin-bottom: 48px;
    }

    .time-indicator {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: rgba(255,255,255,0.1);
      padding: 12px 24px;
      border-radius: 12px;
    }

    .time-indicator svg {
      width: 24px;
      height: 24px;
      color: rgba(255,255,255,0.6);
    }

    .time-indicator span {
      font-size: 18px;
      font-weight: 500;
      color: rgba(255,255,255,0.8);
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
    <div class="accent-circle accent-circle-1"></div>
    <div class="accent-circle accent-circle-2"></div>

    <div class="content">
      <div class="exercise-badge">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <polygon points="5 3 19 12 5 21 5 3"/>
        </svg>
        <span>Hands-On Exercise</span>
      </div>

      <h1 class="title">Create Your First Chat</h1>
      <p class="description">Open Langdock, start a new conversation, and ask the AI to help you draft a professional email. Experiment with different models to see how responses vary.</p>

      <div class="time-indicator">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <circle cx="12" cy="12" r="10"/>
          <polyline points="12 6 12 12 16 14"/>
        </svg>
        <span>5 minutes</span>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Exercise with Steps

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
      padding: 64px;
      display: flex;
      gap: 80px;
      position: relative;
    }

    .left {
      width: 600px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .exercise-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(150, 215, 210, 0.2);
      padding: 10px 20px;
      border-radius: 100px;
      margin-bottom: 24px;
      width: fit-content;
    }

    .exercise-badge svg {
      width: 18px;
      height: 18px;
      color: #96D7D2;
    }

    .exercise-badge span {
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #96D7D2;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      line-height: 1.15;
      color: #FFFFFF;
      margin-bottom: 20px;
    }

    .description {
      font-size: 20px;
      font-weight: 400;
      line-height: 1.6;
      color: rgba(255,255,255,0.65);
    }

    .right {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .steps {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .step {
      display: flex;
      align-items: flex-start;
      gap: 20px;
      background: rgba(255,255,255,0.08);
      border-radius: 16px;
      padding: 24px 28px;
    }

    .step-number {
      width: 36px;
      height: 36px;
      background: rgba(255,255,255,0.15);
      color: #FFFFFF;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 16px;
      font-weight: 600;
      flex-shrink: 0;
    }

    .step-content {
      flex: 1;
    }

    .step-title {
      font-size: 18px;
      font-weight: 600;
      color: #FFFFFF;
      margin-bottom: 4px;
    }

    .step-description {
      font-size: 16px;
      color: rgba(255,255,255,0.6);
      line-height: 1.4;
    }

    .time-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      margin-top: 32px;
      color: rgba(255,255,255,0.5);
    }

    .time-badge svg {
      width: 20px;
      height: 20px;
    }

    .time-badge span {
      font-size: 16px;
      font-weight: 500;
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
    <div class="left">
      <div class="exercise-badge">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <polygon points="5 3 19 12 5 21 5 3"/>
        </svg>
        <span>Exercise</span>
      </div>

      <h1 class="title">Build a Custom Assistant</h1>
      <p class="description">Follow these steps to create your first AI assistant with custom instructions and knowledge.</p>

      <div class="time-badge">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <circle cx="12" cy="12" r="10"/>
          <polyline points="12 6 12 12 16 14"/>
        </svg>
        <span>10 minutes</span>
      </div>
    </div>

    <div class="right">
      <div class="steps">
        <div class="step">
          <div class="step-number">1</div>
          <div class="step-content">
            <div class="step-title">Go to Assistants</div>
            <div class="step-description">Click the Assistants icon in the sidebar and select "Create New"</div>
          </div>
        </div>

        <div class="step">
          <div class="step-number">2</div>
          <div class="step-content">
            <div class="step-title">Name Your Assistant</div>
            <div class="step-description">Give it a descriptive name like "Meeting Summarizer" or "Email Helper"</div>
          </div>
        </div>

        <div class="step">
          <div class="step-number">3</div>
          <div class="step-content">
            <div class="step-title">Write Instructions</div>
            <div class="step-description">Define what your assistant should do, its tone, and any specific rules</div>
          </div>
        </div>

        <div class="step">
          <div class="step-number">4</div>
          <div class="step-content">
            <div class="step-title">Test It Out</div>
            <div class="step-description">Start a conversation with your assistant and refine as needed</div>
          </div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option C: Simple Prompt

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
    }

    .icon-container {
      width: 80px;
      height: 80px;
      background: rgba(150, 215, 210, 0.15);
      border-radius: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 40px;
    }

    .icon-container svg {
      width: 40px;
      height: 40px;
      color: #96D7D2;
    }

    .title {
      font-size: 64px;
      font-weight: 600;
      letter-spacing: -1.28px;
      color: #FFFFFF;
      margin-bottom: 24px;
      text-align: center;
    }

    .subtitle {
      font-size: 24px;
      font-weight: 400;
      color: rgba(255,255,255,0.6);
      text-align: center;
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
    <div class="icon-container">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <polygon points="5 3 19 12 5 21 5 3"/>
      </svg>
    </div>

    <h1 class="title">Your Turn!</h1>
    <p class="subtitle">Open Langdock and follow along with the demo</p>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Exercise Badge Variants

```css
/* Teal accent (default) */
.exercise-badge {
  background: rgba(150, 215, 210, 0.2);
  color: #96D7D2;
}

/* White on dark */
.exercise-badge {
  background: rgba(255,255,255,0.15);
  color: #FFFFFF;
}

/* Blue accent */
.exercise-badge {
  background: rgba(68, 105, 252, 0.2);
  color: #4469fc;
}
```

## Icon Options

```html
<!-- Play icon (default) -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <polygon points="5 3 19 12 5 21 5 3"/>
</svg>

<!-- Pencil/Edit icon -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"/>
  <path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"/>
</svg>

<!-- Lightbulb icon -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <line x1="9" y1="18" x2="15" y2="18"/>
  <line x1="10" y1="22" x2="14" y2="22"/>
  <path d="M15.09 14c.18-.98.65-1.74 1.41-2.5A4.65 4.65 0 0 0 18 8 6 6 0 0 0 6 8c0 1 .23 2.23 1.5 3.5A4.61 4.61 0 0 1 8.91 14"/>
</svg>
```
