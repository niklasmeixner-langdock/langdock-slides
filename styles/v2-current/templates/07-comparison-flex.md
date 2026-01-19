# 07 - Comparison Flex

Flexible two-column comparison layout for before/after, pros/cons, or side-by-side content.

## Use Cases
- Before/after comparisons
- Pros/cons analysis
- Two approaches side-by-side
- Problem/solution pairs
- With/without scenarios

## Layout Options

### Option A: Before & After Cards

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

    .comparison-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 32px;
      flex: 1;
    }

    .comparison-card {
      background: #FFFFFF;
      border-radius: 20px;
      padding: 40px;
      display: flex;
      flex-direction: column;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
    }

    .comparison-card.negative {
      background: #FFFFFF;
      border: 2px solid rgba(239, 68, 68, 0.15);
    }

    .comparison-card.positive {
      background: #FFFFFF;
      border: 2px solid rgba(34, 197, 94, 0.15);
    }

    .card-header {
      display: flex;
      align-items: center;
      gap: 16px;
      margin-bottom: 32px;
    }

    .card-icon {
      width: 48px;
      height: 48px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .negative .card-icon {
      background: rgba(239, 68, 68, 0.1);
    }

    .negative .card-icon svg {
      color: #ef4444;
    }

    .positive .card-icon {
      background: rgba(34, 197, 94, 0.1);
    }

    .positive .card-icon svg {
      color: #22c55e;
    }

    .card-icon svg {
      width: 24px;
      height: 24px;
    }

    .card-label {
      font-size: 24px;
      font-weight: 600;
      letter-spacing: -0.48px;
      color: #1a1c21;
    }

    .card-content {
      display: flex;
      flex-direction: column;
      gap: 20px;
      flex: 1;
    }

    .item {
      display: flex;
      align-items: flex-start;
      gap: 16px;
    }

    .item-icon {
      width: 24px;
      height: 24px;
      flex-shrink: 0;
      margin-top: 2px;
    }

    .negative .item-icon svg {
      color: #ef4444;
    }

    .positive .item-icon svg {
      color: #22c55e;
    }

    .item-text {
      font-size: 18px;
      font-weight: 400;
      line-height: 1.5;
      color: rgba(26,28,33,0.7);
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
      <h1 class="title">Managing AI Without vs. With Langdock</h1>
    </div>

    <div class="comparison-container">
      <div class="comparison-card negative">
        <div class="card-header">
          <div class="card-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="12" cy="12" r="10"/>
              <line x1="15" y1="9" x2="9" y2="15"/>
              <line x1="9" y1="9" x2="15" y2="15"/>
            </svg>
          </div>
          <span class="card-label">Without Langdock</span>
        </div>
        <div class="card-content">
          <div class="item">
            <div class="item-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <line x1="18" y1="6" x2="6" y2="18"/>
                <line x1="6" y1="6" x2="18" y2="18"/>
              </svg>
            </div>
            <span class="item-text">Multiple accounts across different AI tools</span>
          </div>
          <div class="item">
            <div class="item-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <line x1="18" y1="6" x2="6" y2="18"/>
                <line x1="6" y1="6" x2="18" y2="18"/>
              </svg>
            </div>
            <span class="item-text">Data scattered with no central oversight</span>
          </div>
          <div class="item">
            <div class="item-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <line x1="18" y1="6" x2="6" y2="18"/>
                <line x1="6" y1="6" x2="18" y2="18"/>
              </svg>
            </div>
            <span class="item-text">Security and compliance risks</span>
          </div>
          <div class="item">
            <div class="item-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <line x1="18" y1="6" x2="6" y2="18"/>
                <line x1="6" y1="6" x2="18" y2="18"/>
              </svg>
            </div>
            <span class="item-text">No visibility into AI usage</span>
          </div>
        </div>
      </div>

      <div class="comparison-card positive">
        <div class="card-header">
          <div class="card-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/>
              <polyline points="22 4 12 14.01 9 11.01"/>
            </svg>
          </div>
          <span class="card-label">With Langdock</span>
        </div>
        <div class="card-content">
          <div class="item">
            <div class="item-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="item-text">One platform for all AI models and tools</span>
          </div>
          <div class="item">
            <div class="item-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="item-text">Centralized knowledge and conversations</span>
          </div>
          <div class="item">
            <div class="item-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="item-text">Enterprise security and EU hosting</span>
          </div>
          <div class="item">
            <div class="item-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="item-text">Full admin controls and analytics</span>
          </div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Problem & Solution

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
      position: relative;
    }

    .left-panel {
      width: 50%;
      background: #F8F8FC;
      padding: 64px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .right-panel {
      width: 50%;
      background: #1a1c21;
      padding: 64px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .panel-label {
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      margin-bottom: 16px;
    }

    .left-panel .panel-label {
      color: rgba(26,28,33,0.4);
    }

    .right-panel .panel-label {
      color: #4469fc;
    }

    .panel-title {
      font-size: 40px;
      font-weight: 600;
      letter-spacing: -0.8px;
      line-height: 1.2;
      margin-bottom: 32px;
    }

    .left-panel .panel-title {
      color: #1a1c21;
    }

    .right-panel .panel-title {
      color: #FFFFFF;
    }

    .panel-content {
      display: flex;
      flex-direction: column;
      gap: 24px;
    }

    .content-item {
      font-size: 18px;
      line-height: 1.6;
    }

    .left-panel .content-item {
      color: rgba(26,28,33,0.6);
    }

    .right-panel .content-item {
      color: rgba(255,255,255,0.8);
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
    <div class="left-panel">
      <div class="panel-label">The Problem</div>
      <h2 class="panel-title">Shadow AI is creating risk</h2>
      <div class="panel-content">
        <p class="content-item">Employees are using consumer AI tools without IT oversight, creating security blind spots.</p>
        <p class="content-item">Sensitive company data is being shared with unvetted services.</p>
        <p class="content-item">No way to enforce policies or track usage across the organization.</p>
      </div>
    </div>

    <div class="right-panel">
      <div class="panel-label">The Solution</div>
      <h2 class="panel-title">Secure, managed AI access</h2>
      <div class="panel-content">
        <p class="content-item">Provide employees with a compliant alternative that meets their needs.</p>
        <p class="content-item">EU-hosted data processing with enterprise-grade security.</p>
        <p class="content-item">Full visibility and control over AI usage across your organization.</p>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option C: Visual Arrow Comparison

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
      padding: 64px;
      display: flex;
      flex-direction: column;
      position: relative;
    }

    .header {
      text-align: center;
      margin-bottom: 64px;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      color: #1a1c21;
    }

    .comparison-visual {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 48px;
      flex: 1;
    }

    .state-box {
      background: #FFFFFF;
      border-radius: 20px;
      padding: 48px;
      width: 600px;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
    }

    .state-label {
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: rgba(26,28,33,0.4);
      margin-bottom: 16px;
    }

    .state-title {
      font-size: 28px;
      font-weight: 600;
      letter-spacing: -0.56px;
      color: #1a1c21;
      margin-bottom: 24px;
    }

    .state-description {
      font-size: 18px;
      line-height: 1.6;
      color: rgba(26,28,33,0.6);
    }

    .arrow {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 12px;
    }

    .arrow-icon {
      width: 64px;
      height: 64px;
      background: #4469fc;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0px 4px 12px rgba(68, 105, 252, 0.3);
    }

    .arrow-icon svg {
      width: 28px;
      height: 28px;
      color: #FFFFFF;
    }

    .arrow-label {
      font-size: 14px;
      font-weight: 600;
      color: #4469fc;
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
      <h1 class="title">Transform Your AI Workflow</h1>
    </div>

    <div class="comparison-visual">
      <div class="state-box">
        <div class="state-label">Before</div>
        <div class="state-title">Fragmented AI Tools</div>
        <div class="state-description">Multiple subscriptions, inconsistent experiences, and data scattered across various platforms with no central management.</div>
      </div>

      <div class="arrow">
        <div class="arrow-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
            <line x1="5" y1="12" x2="19" y2="12"/>
            <polyline points="12 5 19 12 12 19"/>
          </svg>
        </div>
        <span class="arrow-label">Langdock</span>
      </div>

      <div class="state-box">
        <div class="state-label">After</div>
        <div class="state-title">Unified AI Platform</div>
        <div class="state-description">One secure workspace with all models, shared knowledge, and complete admin visibility across your organization.</div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Color Coding

| State | Border Color | Icon Background |
|-------|-------------|-----------------|
| Negative/Before | `rgba(239, 68, 68, 0.15)` | `rgba(239, 68, 68, 0.1)` |
| Positive/After | `rgba(34, 197, 94, 0.15)` | `rgba(34, 197, 94, 0.1)` |
| Neutral | None | `#ECECF4` |
