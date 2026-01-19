# 14 - Annotated Content

Display content with callouts, annotations, highlights, or explanatory markers.

## Use Cases
- UI annotations with numbered callouts
- Feature highlights with explanations
- Process explanations with markers
- Diagram annotations
- Step-by-step guides with pointers

## Layout Options

### Option A: Screenshot with Numbered Callouts

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
      margin-bottom: 40px;
    }

    .label {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 12px;
    }

    .title {
      font-size: 44px;
      font-weight: 600;
      letter-spacing: -0.88px;
      color: #1a1c21;
    }

    .main-content {
      display: flex;
      gap: 48px;
      flex: 1;
    }

    .screenshot-area {
      flex: 1;
      position: relative;
    }

    .screenshot-container {
      background: #FFFFFF;
      border-radius: 16px;
      box-shadow: 0px 8px 40px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      height: 100%;
    }

    .screenshot-container img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    /* Callout markers on screenshot */
    .callout-marker {
      position: absolute;
      width: 36px;
      height: 36px;
      background: #4469fc;
      color: #FFFFFF;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 16px;
      font-weight: 600;
      box-shadow: 0 4px 12px rgba(68, 105, 252, 0.4);
      z-index: 10;
    }

    .callout-marker::after {
      content: '';
      position: absolute;
      width: 48px;
      height: 48px;
      border: 2px solid #4469fc;
      border-radius: 50%;
      opacity: 0.4;
    }

    /* Position markers - adjust based on screenshot */
    .marker-1 { top: 15%; left: 20%; }
    .marker-2 { top: 35%; left: 45%; }
    .marker-3 { top: 60%; left: 30%; }
    .marker-4 { top: 75%; left: 70%; }

    .annotations-panel {
      width: 450px;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .annotation {
      display: flex;
      gap: 16px;
      align-items: flex-start;
    }

    .annotation-number {
      width: 32px;
      height: 32px;
      background: rgba(68, 105, 252, 0.1);
      color: #4469fc;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 14px;
      font-weight: 600;
      flex-shrink: 0;
    }

    .annotation-content {
      flex: 1;
    }

    .annotation-title {
      font-size: 18px;
      font-weight: 600;
      color: #1a1c21;
      margin-bottom: 4px;
    }

    .annotation-description {
      font-size: 15px;
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
    <div class="header">
      <div class="label">Interface Guide</div>
      <h1 class="title">Understanding the Chat Interface</h1>
    </div>

    <div class="main-content">
      <div class="screenshot-area">
        <div class="screenshot-container">
          <img src="[SCREENSHOT_URL]" alt="Chat Interface">
        </div>
        <div class="callout-marker marker-1">1</div>
        <div class="callout-marker marker-2">2</div>
        <div class="callout-marker marker-3">3</div>
        <div class="callout-marker marker-4">4</div>
      </div>

      <div class="annotations-panel">
        <div class="annotation">
          <div class="annotation-number">1</div>
          <div class="annotation-content">
            <div class="annotation-title">Model Selector</div>
            <div class="annotation-description">Choose from GPT-4, Claude, Gemini, and other available AI models for your conversation.</div>
          </div>
        </div>

        <div class="annotation">
          <div class="annotation-number">2</div>
          <div class="annotation-content">
            <div class="annotation-title">Conversation History</div>
            <div class="annotation-description">Access your previous chats and continue conversations where you left off.</div>
          </div>
        </div>

        <div class="annotation">
          <div class="annotation-number">3</div>
          <div class="annotation-content">
            <div class="annotation-title">Input Area</div>
            <div class="annotation-description">Type your prompts here. Supports markdown formatting and file attachments.</div>
          </div>
        </div>

        <div class="annotation">
          <div class="annotation-number">4</div>
          <div class="annotation-content">
            <div class="annotation-title">Quick Actions</div>
            <div class="annotation-description">Access templates, save responses, and share conversations with your team.</div>
          </div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Feature Highlight Cards with Arrows

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
      margin-bottom: 48px;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      color: #1a1c21;
    }

    .content-area {
      flex: 1;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
    }

    .central-element {
      width: 700px;
      height: 500px;
      background: #F8F8FC;
      border-radius: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      z-index: 1;
    }

    .central-element img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 12px;
      box-shadow: 0 4px 24px rgba(0,0,0,0.08);
    }

    /* Annotation cards positioned around central element */
    .annotation-card {
      position: absolute;
      background: #FFFFFF;
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.08);
      width: 280px;
      z-index: 2;
    }

    .annotation-card::before {
      content: '';
      position: absolute;
      width: 60px;
      height: 2px;
      background: #4469fc;
    }

    /* Top left annotation */
    .card-top-left {
      top: 50px;
      left: 80px;
    }

    .card-top-left::before {
      bottom: -30px;
      right: -30px;
      transform: rotate(45deg);
      width: 80px;
    }

    /* Top right annotation */
    .card-top-right {
      top: 50px;
      right: 80px;
    }

    .card-top-right::before {
      bottom: -30px;
      left: -30px;
      transform: rotate(-45deg);
      width: 80px;
    }

    /* Bottom left annotation */
    .card-bottom-left {
      bottom: 80px;
      left: 80px;
    }

    .card-bottom-left::before {
      top: -30px;
      right: -30px;
      transform: rotate(-45deg);
      width: 80px;
    }

    /* Bottom right annotation */
    .card-bottom-right {
      bottom: 80px;
      right: 80px;
    }

    .card-bottom-right::before {
      top: -30px;
      left: -30px;
      transform: rotate(45deg);
      width: 80px;
    }

    .annotation-icon {
      width: 40px;
      height: 40px;
      background: rgba(68, 105, 252, 0.1);
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 12px;
    }

    .annotation-icon svg {
      width: 20px;
      height: 20px;
      color: #4469fc;
    }

    .annotation-card-title {
      font-size: 16px;
      font-weight: 600;
      color: #1a1c21;
      margin-bottom: 6px;
    }

    .annotation-card-text {
      font-size: 14px;
      color: rgba(26,28,33,0.55);
      line-height: 1.5;
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
      <h1 class="title">Key Platform Features</h1>
    </div>

    <div class="content-area">
      <div class="annotation-card card-top-left">
        <div class="annotation-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>
          </svg>
        </div>
        <div class="annotation-card-title">Smart Chat</div>
        <div class="annotation-card-text">Context-aware conversations with memory across sessions.</div>
      </div>

      <div class="annotation-card card-top-right">
        <div class="annotation-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
            <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
          </svg>
        </div>
        <div class="annotation-card-title">Enterprise Security</div>
        <div class="annotation-card-text">SOC 2 compliant with EU data hosting options.</div>
      </div>

      <div class="central-element">
        <img src="[SCREENSHOT_URL]" alt="Platform Preview">
      </div>

      <div class="annotation-card card-bottom-left">
        <div class="annotation-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <ellipse cx="12" cy="5" rx="9" ry="3"/>
            <path d="M21 12c0 1.66-4 3-9 3s-9-1.34-9-3"/>
            <path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/>
          </svg>
        </div>
        <div class="annotation-card-title">Knowledge Base</div>
        <div class="annotation-card-text">Connect your company data for accurate, context-aware responses.</div>
      </div>

      <div class="annotation-card card-bottom-right">
        <div class="annotation-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <line x1="18" y1="20" x2="18" y2="10"/>
            <line x1="12" y1="20" x2="12" y2="4"/>
            <line x1="6" y1="20" x2="6" y2="14"/>
          </svg>
        </div>
        <div class="annotation-card-title">Analytics</div>
        <div class="annotation-card-text">Track usage, costs, and productivity across your organization.</div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option C: Inline Annotations (Dark Theme)

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
      background: #4d473c;
      padding: 64px;
      display: flex;
      flex-direction: column;
      position: relative;
    }

    .header {
      margin-bottom: 48px;
    }

    .label {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #96D7D2;
      margin-bottom: 12px;
    }

    .title {
      font-size: 44px;
      font-weight: 600;
      letter-spacing: -0.88px;
      color: #FFFFFF;
    }

    .annotated-content {
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 24px;
    }

    .annotated-row {
      display: flex;
      align-items: stretch;
      gap: 24px;
    }

    .content-block {
      flex: 1;
      background: rgba(255,255,255,0.08);
      border-radius: 16px;
      padding: 32px;
      position: relative;
    }

    .content-block-large {
      flex: 2;
    }

    .annotation-badge {
      position: absolute;
      top: -12px;
      left: 24px;
      background: #96D7D2;
      color: #1a1c21;
      padding: 6px 14px;
      border-radius: 100px;
      font-size: 12px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .block-title {
      font-size: 20px;
      font-weight: 600;
      color: #FFFFFF;
      margin-bottom: 12px;
      margin-top: 8px;
    }

    .block-text {
      font-size: 16px;
      font-weight: 400;
      line-height: 1.6;
      color: rgba(255,255,255,0.7);
    }

    .block-list {
      list-style: none;
      margin-top: 16px;
    }

    .block-list li {
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 15px;
      color: rgba(255,255,255,0.8);
      padding: 8px 0;
      border-bottom: 1px solid rgba(255,255,255,0.1);
    }

    .block-list li:last-child {
      border-bottom: none;
    }

    .block-list svg {
      width: 18px;
      height: 18px;
      color: #96D7D2;
      flex-shrink: 0;
    }

    .highlight-text {
      background: rgba(150, 215, 210, 0.2);
      color: #96D7D2;
      padding: 2px 8px;
      border-radius: 4px;
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
    <div class="header">
      <div class="label">Feature Deep Dive</div>
      <h1 class="title">Custom Assistants Explained</h1>
    </div>

    <div class="annotated-content">
      <div class="annotated-row">
        <div class="content-block content-block-large">
          <div class="annotation-badge">What It Is</div>
          <div class="block-title">AI Assistants Tailored to Your Workflow</div>
          <div class="block-text">Create specialized AI agents with custom instructions, knowledge bases, and capabilities. Each assistant can be fine-tuned for specific tasks like <span class="highlight-text">writing emails</span>, <span class="highlight-text">analyzing data</span>, or <span class="highlight-text">generating reports</span>.</div>
        </div>

        <div class="content-block">
          <div class="annotation-badge">Key Benefit</div>
          <div class="block-title">Consistency at Scale</div>
          <div class="block-text">Ensure everyone on your team gets the same high-quality AI assistance, following your company's guidelines and best practices.</div>
        </div>
      </div>

      <div class="annotated-row">
        <div class="content-block">
          <div class="annotation-badge">How To Use</div>
          <div class="block-title">Getting Started</div>
          <ul class="block-list">
            <li>
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
              Navigate to Assistants
            </li>
            <li>
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
              Click "Create New"
            </li>
            <li>
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
              Define instructions
            </li>
            <li>
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
              Add knowledge sources
            </li>
          </ul>
        </div>

        <div class="content-block">
          <div class="annotation-badge">Pro Tip</div>
          <div class="block-title">Start with Templates</div>
          <div class="block-text">Use our pre-built assistant templates as a starting point. Customize them to match your specific needs and save hours of setup time.</div>
        </div>

        <div class="content-block">
          <div class="annotation-badge">Example</div>
          <div class="block-title">Meeting Summarizer</div>
          <div class="block-text">Upload meeting transcripts and get structured summaries with action items, decisions, and key discussion points automatically extracted.</div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option D: Text with Margin Annotations

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
      padding: 64px 120px;
      display: flex;
      gap: 80px;
      position: relative;
    }

    .main-content {
      flex: 1;
      max-width: 900px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      line-height: 1.2;
      color: #1a1c21;
      margin-bottom: 40px;
    }

    .paragraph {
      font-size: 20px;
      font-weight: 400;
      line-height: 1.8;
      color: rgba(26,28,33,0.7);
      margin-bottom: 32px;
      position: relative;
    }

    .highlight {
      background: linear-gradient(180deg, transparent 60%, rgba(68, 105, 252, 0.2) 60%);
      padding: 0 4px;
    }

    .margin-note {
      position: absolute;
      right: -320px;
      width: 280px;
      padding: 16px 20px;
      background: #FFFFFF;
      border-radius: 12px;
      box-shadow: 0 2px 12px rgba(0,0,0,0.06);
      border-left: 3px solid #4469fc;
    }

    .note-icon {
      width: 24px;
      height: 24px;
      color: #4469fc;
      margin-bottom: 8px;
    }

    .note-text {
      font-size: 14px;
      font-weight: 400;
      line-height: 1.5;
      color: rgba(26,28,33,0.6);
    }

    .note-label {
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 6px;
    }

    /* Connector line */
    .margin-note::before {
      content: '';
      position: absolute;
      left: -43px;
      top: 50%;
      width: 40px;
      height: 1px;
      background: rgba(68, 105, 252, 0.3);
    }

    .margin-note::after {
      content: '';
      position: absolute;
      left: -47px;
      top: 50%;
      transform: translateY(-50%);
      width: 8px;
      height: 8px;
      background: #4469fc;
      border-radius: 50%;
    }

    .sidebar {
      width: 320px;
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
    <div class="main-content">
      <h1 class="title">Why Enterprise AI Platforms Matter</h1>

      <p class="paragraph" style="margin-top: 40px;">
        Traditional AI tools lack the <span class="highlight">security and compliance</span> features that enterprises require. When employees use consumer AI products, sensitive company data may be exposed to third parties without proper safeguards.
        <div class="margin-note" style="top: 0;">
          <div class="note-label">Key Risk</div>
          <div class="note-text">Consumer AI tools often train on user data, potentially exposing proprietary information.</div>
        </div>
      </p>

      <p class="paragraph">
        An enterprise AI platform provides <span class="highlight">centralized control</span> over model access, usage policies, and data handling. Administrators can enforce guardrails while giving employees the productivity benefits of AI.
        <div class="margin-note" style="top: 0;">
          <div class="note-label">Solution</div>
          <div class="note-text">Langdock offers admin controls, SSO, and audit logs for complete visibility.</div>
        </div>
      </p>

      <p class="paragraph">
        With proper governance, organizations can achieve <span class="highlight">10x productivity gains</span> while maintaining compliance with industry regulations like GDPR and SOC 2.
        <div class="margin-note" style="top: 0;">
          <div class="note-label">Result</div>
          <div class="note-text">Companies report 40% time savings on routine tasks after implementing enterprise AI.</div>
        </div>
      </p>
    </div>

    <div class="sidebar"></div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Annotation Styles

### Numbered Callouts
```css
.callout-marker {
  width: 36px;
  height: 36px;
  background: #4469fc;
  color: #FFFFFF;
  border-radius: 50%;
  font-size: 16px;
  font-weight: 600;
  box-shadow: 0 4px 12px rgba(68, 105, 252, 0.4);
}
```

### Badge Labels
```css
.annotation-badge {
  background: #96D7D2;
  color: #1a1c21;
  padding: 6px 14px;
  border-radius: 100px;
  font-size: 12px;
  font-weight: 600;
  text-transform: uppercase;
}
```

### Highlight Text
```css
.highlight {
  background: linear-gradient(180deg, transparent 60%, rgba(68, 105, 252, 0.2) 60%);
  padding: 0 4px;
}

/* Alternative: solid background */
.highlight-solid {
  background: rgba(150, 215, 210, 0.2);
  color: #96D7D2;
  padding: 2px 8px;
  border-radius: 4px;
}
```

### Margin Notes
```css
.margin-note {
  padding: 16px 20px;
  background: #FFFFFF;
  border-radius: 12px;
  border-left: 3px solid #4469fc;
  box-shadow: 0 2px 12px rgba(0,0,0,0.06);
}
```

## Icon Suggestions

| Annotation Type | Icon |
|----------------|------|
| Tip/Pro Tip | lightbulb |
| Warning | alert-triangle |
| Note | info-circle |
| Example | file-text |
| Step | arrow-right |
| Key Point | star |
| Definition | book-open |
