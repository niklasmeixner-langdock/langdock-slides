# 02 - Goals / Agenda Slide

Display learning objectives, session goals, or agenda items in a clear, numbered format.

## Use Cases
- Session openers
- Learning objectives
- Meeting agendas
- Key takeaways
- Module overviews

## Layout Options

### Option A: Numbered List (Standard)

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
      font-size: 56px;
      font-weight: 600;
      letter-spacing: -1.12px;
      line-height: 1.1;
      color: #1a1c21;
    }

    .goals-list {
      display: flex;
      flex-direction: column;
      gap: 24px;
      margin-top: auto;
      margin-bottom: 120px;
    }

    .goal-item {
      display: flex;
      align-items: flex-start;
      gap: 24px;
    }

    .goal-number {
      width: 48px;
      height: 48px;
      background: #ECECF4;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      font-weight: 600;
      color: #1a1c21;
      flex-shrink: 0;
    }

    .goal-content {
      padding-top: 10px;
    }

    .goal-title {
      font-size: 24px;
      font-weight: 600;
      letter-spacing: -0.48px;
      color: #1a1c21;
      margin-bottom: 4px;
    }

    .goal-description {
      font-size: 18px;
      font-weight: 400;
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
      <div class="label">Learning Objectives</div>
      <h1 class="title">What You'll Learn Today</h1>
    </div>

    <div class="goals-list">
      <div class="goal-item">
        <div class="goal-number">1</div>
        <div class="goal-content">
          <div class="goal-title">Understand the Langdock Platform</div>
          <div class="goal-description">Navigate the interface and understand core features</div>
        </div>
      </div>

      <div class="goal-item">
        <div class="goal-number">2</div>
        <div class="goal-content">
          <div class="goal-title">Create Your First AI Assistant</div>
          <div class="goal-description">Build a custom assistant tailored to your needs</div>
        </div>
      </div>

      <div class="goal-item">
        <div class="goal-number">3</div>
        <div class="goal-content">
          <div class="goal-title">Connect Your Knowledge Base</div>
          <div class="goal-description">Integrate company data for context-aware responses</div>
        </div>
      </div>

      <div class="goal-item">
        <div class="goal-number">4</div>
        <div class="goal-content">
          <div class="goal-title">Apply Best Practices</div>
          <div class="goal-description">Learn prompting techniques and workflow optimization</div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Agenda with Time Slots

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
      padding: 64px;
      display: flex;
      flex-direction: column;
      position: relative;
    }

    .header {
      margin-bottom: 64px;
    }

    .title {
      font-size: 56px;
      font-weight: 600;
      letter-spacing: -1.12px;
      line-height: 1.1;
      color: #1a1c21;
    }

    .agenda-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 24px;
      flex: 1;
    }

    .agenda-item {
      background: #F8F8FC;
      border-radius: 16px;
      padding: 32px;
      display: flex;
      flex-direction: column;
    }

    .time {
      font-size: 14px;
      font-weight: 600;
      color: #4469fc;
      margin-bottom: 12px;
    }

    .agenda-title {
      font-size: 24px;
      font-weight: 600;
      letter-spacing: -0.48px;
      color: #1a1c21;
      margin-bottom: 8px;
    }

    .agenda-description {
      font-size: 16px;
      font-weight: 400;
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
      <h1 class="title">Today's Agenda</h1>
    </div>

    <div class="agenda-grid">
      <div class="agenda-item">
        <div class="time">09:00 - 09:30</div>
        <div class="agenda-title">Introduction & Overview</div>
        <div class="agenda-description">Welcome, introductions, and platform overview</div>
      </div>

      <div class="agenda-item">
        <div class="time">09:30 - 10:30</div>
        <div class="agenda-title">Core Features Deep Dive</div>
        <div class="agenda-description">Chat, Assistants, and Knowledge Base exploration</div>
      </div>

      <div class="agenda-item">
        <div class="time">10:45 - 11:30</div>
        <div class="agenda-title">Hands-On Workshop</div>
        <div class="agenda-description">Build your first custom assistant with guidance</div>
      </div>

      <div class="agenda-item">
        <div class="time">11:30 - 12:00</div>
        <div class="agenda-title">Q&A & Next Steps</div>
        <div class="agenda-description">Questions, best practices, and resources</div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option C: Icon-Based Goals

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

    .label {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: #4469fc;
      margin-bottom: 16px;
    }

    .title {
      font-size: 56px;
      font-weight: 600;
      letter-spacing: -1.12px;
      line-height: 1.1;
      color: #1a1c21;
    }

    .goals-grid {
      display: flex;
      gap: 32px;
      justify-content: center;
      flex: 1;
      align-items: center;
    }

    .goal-card {
      background: #FFFFFF;
      border-radius: 16px;
      padding: 40px 32px;
      width: 400px;
      text-align: center;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
    }

    .goal-icon {
      width: 64px;
      height: 64px;
      background: rgba(68, 105, 252, 0.1);
      border-radius: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 24px;
    }

    .goal-icon svg {
      width: 32px;
      height: 32px;
      color: #4469fc;
    }

    .goal-title {
      font-size: 24px;
      font-weight: 600;
      letter-spacing: -0.48px;
      color: #1a1c21;
      margin-bottom: 12px;
    }

    .goal-description {
      font-size: 16px;
      font-weight: 400;
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
      <div class="label">Session Goals</div>
      <h1 class="title">What We'll Cover</h1>
    </div>

    <div class="goals-grid">
      <div class="goal-card">
        <div class="goal-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"/>
            <polyline points="3.27 6.96 12 12.01 20.73 6.96"/>
            <line x1="12" y1="22.08" x2="12" y2="12"/>
          </svg>
        </div>
        <div class="goal-title">Platform Basics</div>
        <div class="goal-description">Navigate the interface and understand key features</div>
      </div>

      <div class="goal-card">
        <div class="goal-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <circle cx="12" cy="12" r="3"/>
            <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"/>
          </svg>
        </div>
        <div class="goal-title">Hands-On Practice</div>
        <div class="goal-description">Build and customize your own AI assistant</div>
      </div>

      <div class="goal-card">
        <div class="goal-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/>
            <polyline points="22 4 12 14.01 9 11.01"/>
          </svg>
        </div>
        <div class="goal-title">Best Practices</div>
        <div class="goal-description">Learn tips for effective AI-powered workflows</div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Customization Guidelines

### Number of Items
| Items | Recommended Layout |
|-------|-------------------|
| 2-3 | Icon cards (Option C) or simple list |
| 4-5 | Numbered list (Option A) |
| 4-6 | Agenda grid (Option B) |

### Number Style Variants
```css
/* Square with rounded corners (default) */
.goal-number { background: #ECECF4; border-radius: 12px; }

/* Circle */
.goal-number { background: #4469fc; color: #FFFFFF; border-radius: 50%; }

/* Outline */
.goal-number { background: transparent; border: 2px solid #ECECF4; }
```
