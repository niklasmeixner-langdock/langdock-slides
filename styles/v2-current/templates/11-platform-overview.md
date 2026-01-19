# 11 - Platform Overview

Display product features, capabilities, or platform highlights in a visual grid.

## Use Cases
- Product feature overview
- Platform capabilities
- Feature highlights
- Product tour summaries
- Capability showcase

## Layout Options

### Option A: Feature Cards Grid

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

    .features-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
      flex: 1;
    }

    .feature-card {
      background: #FFFFFF;
      border-radius: 16px;
      padding: 32px;
      display: flex;
      flex-direction: column;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
    }

    .feature-icon {
      width: 56px;
      height: 56px;
      background: rgba(68, 105, 252, 0.1);
      border-radius: 14px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 24px;
    }

    .feature-icon svg {
      width: 28px;
      height: 28px;
      color: #4469fc;
    }

    .feature-title {
      font-size: 22px;
      font-weight: 600;
      letter-spacing: -0.44px;
      color: #1a1c21;
      margin-bottom: 12px;
    }

    .feature-description {
      font-size: 16px;
      font-weight: 400;
      line-height: 1.5;
      color: rgba(26,28,33,0.55);
      flex: 1;
    }

    .feature-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 20px;
    }

    .tag {
      background: #ECECF4;
      padding: 6px 12px;
      border-radius: 100px;
      font-size: 13px;
      font-weight: 500;
      color: rgba(26,28,33,0.6);
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
      <div class="label">Platform Overview</div>
      <h1 class="title">Everything You Need for Enterprise AI</h1>
    </div>

    <div class="features-grid">
      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>
          </svg>
        </div>
        <div class="feature-title">Multi-Model Chat</div>
        <div class="feature-description">Access GPT-4, Claude, Gemini, and more from one unified interface. Switch models mid-conversation.</div>
        <div class="feature-tags">
          <span class="tag">GPT-4</span>
          <span class="tag">Claude</span>
          <span class="tag">Gemini</span>
        </div>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M12 2L2 7l10 5 10-5-10-5z"/>
            <path d="M2 17l10 5 10-5"/>
            <path d="M2 12l10 5 10-5"/>
          </svg>
        </div>
        <div class="feature-title">Custom Assistants</div>
        <div class="feature-description">Build specialized AI assistants with custom instructions, knowledge bases, and capabilities.</div>
        <div class="feature-tags">
          <span class="tag">Templates</span>
          <span class="tag">Sharing</span>
        </div>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <ellipse cx="12" cy="5" rx="9" ry="3"/>
            <path d="M21 12c0 1.66-4 3-9 3s-9-1.34-9-3"/>
            <path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/>
          </svg>
        </div>
        <div class="feature-title">Knowledge Base</div>
        <div class="feature-description">Connect your company data from Notion, Confluence, Google Drive, and more for context-aware AI.</div>
        <div class="feature-tags">
          <span class="tag">50+ Integrations</span>
        </div>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
            <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
          </svg>
        </div>
        <div class="feature-title">Enterprise Security</div>
        <div class="feature-description">EU data hosting, SOC 2 compliance, SSO, and enterprise-grade security controls.</div>
        <div class="feature-tags">
          <span class="tag">EU Hosted</span>
          <span class="tag">SOC 2</span>
        </div>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <line x1="18" y1="20" x2="18" y2="10"/>
            <line x1="12" y1="20" x2="12" y2="4"/>
            <line x1="6" y1="20" x2="6" y2="14"/>
          </svg>
        </div>
        <div class="feature-title">Admin Analytics</div>
        <div class="feature-description">Full visibility into AI usage across your organization with detailed analytics and reporting.</div>
        <div class="feature-tags">
          <span class="tag">Dashboard</span>
          <span class="tag">Reports</span>
        </div>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <circle cx="12" cy="12" r="3"/>
            <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"/>
          </svg>
        </div>
        <div class="feature-title">Workflows</div>
        <div class="feature-description">Automate repetitive tasks with AI-powered workflows and custom automations.</div>
        <div class="feature-tags">
          <span class="tag">Automation</span>
          <span class="tag">No-Code</span>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Dark Feature Cards (Website Style)

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
      margin-bottom: 16px;
    }

    .subtitle {
      font-size: 20px;
      color: rgba(26,28,33,0.55);
    }

    .features-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 24px;
      flex: 1;
    }

    .feature-card {
      background: #4d473c;
      border-radius: 16px;
      padding: 40px;
      display: flex;
      flex-direction: column;
      position: relative;
      overflow: hidden;
    }

    .feature-content {
      position: relative;
      z-index: 1;
    }

    .feature-title {
      font-size: 24px;
      font-weight: 600;
      letter-spacing: -0.48px;
      color: #FFFFFF;
      margin-bottom: 8px;
    }

    .feature-description {
      font-size: 16px;
      font-weight: 400;
      line-height: 1.5;
      color: rgba(255,255,255,0.7);
      margin-bottom: 24px;
    }

    .feature-arrow {
      width: 36px;
      height: 36px;
      background: rgba(255,255,255,0.15);
      border-radius: 100px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .feature-arrow svg {
      width: 18px;
      height: 18px;
      color: #FFFFFF;
    }

    /* Decorative UI preview area */
    .feature-visual {
      position: absolute;
      bottom: -20px;
      right: -20px;
      width: 300px;
      height: 200px;
      background: rgba(255,255,255,0.08);
      border-radius: 12px;
      opacity: 0.5;
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
      <h1 class="title">The All-in-One AI Platform</h1>
      <p class="subtitle">Everything your team needs to work smarter with AI</p>
    </div>

    <div class="features-grid">
      <div class="feature-card">
        <div class="feature-content">
          <div class="feature-title">Chat</div>
          <div class="feature-description">Model agnostic, intuitive to use. Access all leading AI models from one place.</div>
          <div class="feature-arrow">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <line x1="5" y1="12" x2="19" y2="12"/>
              <polyline points="12 5 19 12 12 19"/>
            </svg>
          </div>
        </div>
        <div class="feature-visual"></div>
      </div>

      <div class="feature-card">
        <div class="feature-content">
          <div class="feature-title">Assistants</div>
          <div class="feature-description">Custom AI agents tailored to your specific workflows and use cases.</div>
          <div class="feature-arrow">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <line x1="5" y1="12" x2="19" y2="12"/>
              <polyline points="12 5 19 12 12 19"/>
            </svg>
          </div>
        </div>
        <div class="feature-visual"></div>
      </div>

      <div class="feature-card">
        <div class="feature-content">
          <div class="feature-title">Knowledge</div>
          <div class="feature-description">Connect your data sources for context-aware, accurate responses.</div>
          <div class="feature-arrow">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <line x1="5" y1="12" x2="19" y2="12"/>
              <polyline points="12 5 19 12 12 19"/>
            </svg>
          </div>
        </div>
        <div class="feature-visual"></div>
      </div>

      <div class="feature-card">
        <div class="feature-content">
          <div class="feature-title">Admin</div>
          <div class="feature-description">Full control over permissions, analytics, and organizational settings.</div>
          <div class="feature-arrow">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <line x1="5" y1="12" x2="19" y2="12"/>
              <polyline points="12 5 19 12 12 19"/>
            </svg>
          </div>
        </div>
        <div class="feature-visual"></div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Icon Suggestions

Use Tabler icons from: `../../shared/assets/tabler-icons/`

| Feature | Icon |
|---------|------|
| Chat | message, sparkles |
| Assistants | robot, users |
| Knowledge | database, folder |
| Security | shield-check, key |
| Analytics | chart-bar |
| Settings | settings |
| Integrations | plug-connected |
| Workflows | git-branch |
