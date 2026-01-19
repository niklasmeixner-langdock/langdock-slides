# 12 - All-in-One Solution

Comprehensive display showing how multiple features come together as a complete solution.

## Use Cases
- Complete platform overview
- Solution architecture
- Feature ecosystem
- Value proposition summary
- Product positioning

## Layout Options

### Option A: Central Hub with Features

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
      margin-bottom: 48px;
    }

    .title {
      font-size: 48px;
      font-weight: 600;
      letter-spacing: -0.96px;
      color: #1a1c21;
      margin-bottom: 12px;
    }

    .subtitle {
      font-size: 20px;
      color: rgba(26,28,33,0.55);
    }

    .solution-layout {
      display: flex;
      flex: 1;
      gap: 32px;
      align-items: center;
    }

    .features-column {
      display: flex;
      flex-direction: column;
      gap: 20px;
      width: 380px;
    }

    .feature-item {
      background: #FFFFFF;
      border-radius: 16px;
      padding: 24px;
      display: flex;
      align-items: center;
      gap: 16px;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
    }

    .feature-icon {
      width: 48px;
      height: 48px;
      background: rgba(68, 105, 252, 0.1);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }

    .feature-icon svg {
      width: 24px;
      height: 24px;
      color: #4469fc;
    }

    .feature-content {
      flex: 1;
    }

    .feature-title {
      font-size: 18px;
      font-weight: 600;
      color: #1a1c21;
      margin-bottom: 4px;
    }

    .feature-description {
      font-size: 14px;
      color: rgba(26,28,33,0.55);
    }

    .center-hub {
      flex: 1;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .hub-circle {
      width: 400px;
      height: 400px;
      background: #1a1c21;
      border-radius: 50%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      position: relative;
    }

    .hub-logo {
      height: 32px;
      width: auto;
      margin-bottom: 24px;
      filter: brightness(0) invert(1);
    }

    .hub-title {
      font-size: 32px;
      font-weight: 600;
      color: #FFFFFF;
      margin-bottom: 12px;
    }

    .hub-subtitle {
      font-size: 16px;
      color: rgba(255,255,255,0.6);
      max-width: 280px;
    }

    /* Decorative connector lines */
    .connector {
      position: absolute;
      width: 60px;
      height: 2px;
      background: linear-gradient(to right, #ECECF4, transparent);
    }

    .connector-left { left: -60px; top: 50%; }
    .connector-right { right: -60px; top: 50%; transform: rotate(180deg); }

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
      <h1 class="title">The All-in-One AI Platform</h1>
      <p class="subtitle">Everything your organization needs to adopt AI securely and effectively</p>
    </div>

    <div class="solution-layout">
      <div class="features-column">
        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>
            </svg>
          </div>
          <div class="feature-content">
            <div class="feature-title">Chat</div>
            <div class="feature-description">Multi-model AI conversations</div>
          </div>
        </div>

        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="12" cy="8" r="4"/>
              <path d="M6 21v-2a4 4 0 0 1 4-4h4a4 4 0 0 1 4 4v2"/>
            </svg>
          </div>
          <div class="feature-content">
            <div class="feature-title">Assistants</div>
            <div class="feature-description">Custom AI agents for your team</div>
          </div>
        </div>

        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <ellipse cx="12" cy="5" rx="9" ry="3"/>
              <path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/>
            </svg>
          </div>
          <div class="feature-content">
            <div class="feature-title">Knowledge Base</div>
            <div class="feature-description">Connect your company data</div>
          </div>
        </div>
      </div>

      <div class="center-hub">
        <div class="hub-circle">
          <div class="connector connector-left"></div>
          <div class="connector connector-right"></div>
          <img class="hub-logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
          <div class="hub-title">Langdock</div>
          <div class="hub-subtitle">One platform for all your AI needs</div>
        </div>
      </div>

      <div class="features-column">
        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
              <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
            </svg>
          </div>
          <div class="feature-content">
            <div class="feature-title">Security</div>
            <div class="feature-description">EU hosting, SOC 2, enterprise SSO</div>
          </div>
        </div>

        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <line x1="18" y1="20" x2="18" y2="10"/>
              <line x1="12" y1="20" x2="12" y2="4"/>
              <line x1="6" y1="20" x2="6" y2="14"/>
            </svg>
          </div>
          <div class="feature-content">
            <div class="feature-title">Analytics</div>
            <div class="feature-description">Usage insights and reporting</div>
          </div>
        </div>

        <div class="feature-item">
          <div class="feature-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/>
              <circle cx="9" cy="7" r="4"/>
              <path d="M23 21v-2a4 4 0 0 0-3-3.87"/>
              <path d="M16 3.13a4 4 0 0 1 0 7.75"/>
            </svg>
          </div>
          <div class="feature-content">
            <div class="feature-title">Admin Controls</div>
            <div class="feature-description">Permissions and governance</div>
          </div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Stacked Benefits

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
      padding: 64px;
      display: flex;
      gap: 64px;
      position: relative;
    }

    .left {
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
      margin-bottom: 20px;
    }

    .title {
      font-size: 52px;
      font-weight: 600;
      letter-spacing: -1.04px;
      line-height: 1.1;
      color: #FFFFFF;
      margin-bottom: 24px;
    }

    .description {
      font-size: 20px;
      line-height: 1.6;
      color: rgba(255,255,255,0.6);
    }

    .right {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      gap: 20px;
    }

    .benefit-row {
      display: flex;
      gap: 20px;
    }

    .benefit-card {
      background: rgba(255,255,255,0.05);
      border-radius: 16px;
      padding: 28px;
      flex: 1;
      border: 1px solid rgba(255,255,255,0.08);
    }

    .benefit-icon {
      width: 40px;
      height: 40px;
      background: rgba(68, 105, 252, 0.2);
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 16px;
    }

    .benefit-icon svg {
      width: 20px;
      height: 20px;
      color: #4469fc;
    }

    .benefit-title {
      font-size: 18px;
      font-weight: 600;
      color: #FFFFFF;
      margin-bottom: 8px;
    }

    .benefit-text {
      font-size: 14px;
      color: rgba(255,255,255,0.5);
      line-height: 1.4;
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
      <div class="label">Why Langdock</div>
      <h1 class="title">One Platform. Unlimited Possibilities.</h1>
      <p class="description">Stop juggling multiple AI tools. Langdock brings everything together in one secure, enterprise-ready platform.</p>
    </div>

    <div class="right">
      <div class="benefit-row">
        <div class="benefit-card">
          <div class="benefit-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M12 2L2 7l10 5 10-5-10-5z"/>
              <path d="M2 17l10 5 10-5"/>
              <path d="M2 12l10 5 10-5"/>
            </svg>
          </div>
          <div class="benefit-title">Multi-Model Access</div>
          <div class="benefit-text">GPT-4, Claude, Gemini, and more</div>
        </div>
        <div class="benefit-card">
          <div class="benefit-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <rect x="3" y="11" width="18" height="11" rx="2"/>
              <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
            </svg>
          </div>
          <div class="benefit-title">Enterprise Security</div>
          <div class="benefit-text">EU hosting, SOC 2, SSO</div>
        </div>
      </div>

      <div class="benefit-row">
        <div class="benefit-card">
          <div class="benefit-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <ellipse cx="12" cy="5" rx="9" ry="3"/>
              <path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/>
            </svg>
          </div>
          <div class="benefit-title">Knowledge Integration</div>
          <div class="benefit-text">Connect your company data</div>
        </div>
        <div class="benefit-card">
          <div class="benefit-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="12" cy="12" r="3"/>
              <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4"/>
            </svg>
          </div>
          <div class="benefit-title">Admin Controls</div>
          <div class="benefit-text">Full visibility and governance</div>
        </div>
      </div>

      <div class="benefit-row">
        <div class="benefit-card">
          <div class="benefit-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <circle cx="12" cy="8" r="4"/>
              <path d="M6 21v-2a4 4 0 0 1 4-4h4a4 4 0 0 1 4 4v2"/>
            </svg>
          </div>
          <div class="benefit-title">Custom Assistants</div>
          <div class="benefit-text">Build AI agents for your workflows</div>
        </div>
        <div class="benefit-card">
          <div class="benefit-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <line x1="18" y1="20" x2="18" y2="10"/>
              <line x1="12" y1="20" x2="12" y2="4"/>
              <line x1="6" y1="20" x2="6" y2="14"/>
            </svg>
          </div>
          <div class="benefit-title">Usage Analytics</div>
          <div class="benefit-text">Insights and ROI tracking</div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Layout Variations

| Elements | Layout |
|----------|--------|
| 4-6 features | Central hub with sides |
| 6-8 features | Stacked benefits grid |
| 3-4 pillars | Large cards with icons |
