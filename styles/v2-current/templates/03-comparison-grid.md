# 03 - Comparison Grid

Display feature comparisons, option analysis, or structured information in a grid format.

## Use Cases
- Feature comparisons (Langdock vs. alternatives)
- Plan/tier comparisons
- Before/after states
- Option analysis
- Pros/cons tables

## Layout Options

### Option A: Feature Comparison Table

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

    .comparison-table {
      background: #FFFFFF;
      border-radius: 16px;
      overflow: hidden;
      flex: 1;
      display: flex;
      flex-direction: column;
    }

    .table-header {
      display: grid;
      grid-template-columns: 300px repeat(3, 1fr);
      background: #1a1c21;
      color: #FFFFFF;
    }

    .table-header-cell {
      padding: 24px 32px;
      font-size: 18px;
      font-weight: 600;
      text-align: center;
    }

    .table-header-cell:first-child {
      text-align: left;
    }

    .table-header-cell.highlight {
      background: #4469fc;
    }

    .table-row {
      display: grid;
      grid-template-columns: 300px repeat(3, 1fr);
      border-bottom: 1px solid rgba(26,28,33,0.08);
    }

    .table-row:last-child {
      border-bottom: none;
    }

    .table-cell {
      padding: 20px 32px;
      font-size: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .table-cell:first-child {
      font-weight: 500;
      color: #1a1c21;
      justify-content: flex-start;
    }

    .table-cell.highlight {
      background: rgba(68, 105, 252, 0.04);
    }

    .check {
      width: 24px;
      height: 24px;
      background: rgba(34, 197, 94, 0.1);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .check svg {
      width: 14px;
      height: 14px;
      color: #22c55e;
    }

    .cross {
      width: 24px;
      height: 24px;
      background: rgba(239, 68, 68, 0.1);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .cross svg {
      width: 14px;
      height: 14px;
      color: #ef4444;
    }

    .partial {
      font-size: 14px;
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
      <h1 class="title">Feature Comparison</h1>
    </div>

    <div class="comparison-table">
      <div class="table-header">
        <div class="table-header-cell">Feature</div>
        <div class="table-header-cell">ChatGPT</div>
        <div class="table-header-cell highlight">Langdock</div>
        <div class="table-header-cell">Microsoft Copilot</div>
      </div>

      <div class="table-row">
        <div class="table-cell">Multi-model support</div>
        <div class="table-cell">
          <div class="cross">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <line x1="18" y1="6" x2="6" y2="18"/>
              <line x1="6" y1="6" x2="18" y2="18"/>
            </svg>
          </div>
        </div>
        <div class="table-cell highlight">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
        <div class="table-cell">
          <div class="cross">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <line x1="18" y1="6" x2="6" y2="18"/>
              <line x1="6" y1="6" x2="18" y2="18"/>
            </svg>
          </div>
        </div>
      </div>

      <div class="table-row">
        <div class="table-cell">EU Data Hosting</div>
        <div class="table-cell">
          <div class="cross">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <line x1="18" y1="6" x2="6" y2="18"/>
              <line x1="6" y1="6" x2="18" y2="18"/>
            </svg>
          </div>
        </div>
        <div class="table-cell highlight">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
        <div class="table-cell">
          <span class="partial">Partial</span>
        </div>
      </div>

      <div class="table-row">
        <div class="table-cell">Custom Assistants</div>
        <div class="table-cell">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
        <div class="table-cell highlight">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
        <div class="table-cell">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
      </div>

      <div class="table-row">
        <div class="table-cell">Enterprise SSO</div>
        <div class="table-cell">
          <span class="partial">Enterprise only</span>
        </div>
        <div class="table-cell highlight">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
        <div class="table-cell">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
      </div>

      <div class="table-row">
        <div class="table-cell">Knowledge Base Integration</div>
        <div class="table-cell">
          <span class="partial">Limited</span>
        </div>
        <div class="table-cell highlight">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
        <div class="table-cell">
          <div class="check">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <polyline points="20 6 9 17 4 12"/>
            </svg>
          </div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Card-Based Comparison (3 columns)

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
      margin-bottom: 16px;
    }

    .subtitle {
      font-size: 20px;
      color: rgba(26,28,33,0.55);
    }

    .cards-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 32px;
      flex: 1;
    }

    .card {
      background: #FFFFFF;
      border-radius: 16px;
      padding: 40px 32px;
      display: flex;
      flex-direction: column;
      box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
    }

    .card.highlight {
      background: #1a1c21;
      color: #FFFFFF;
    }

    .card-label {
      font-size: 14px;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      color: rgba(26,28,33,0.4);
      margin-bottom: 8px;
    }

    .card.highlight .card-label {
      color: rgba(255,255,255,0.5);
    }

    .card-title {
      font-size: 28px;
      font-weight: 600;
      letter-spacing: -0.56px;
      margin-bottom: 24px;
    }

    .card-features {
      display: flex;
      flex-direction: column;
      gap: 16px;
      flex: 1;
    }

    .feature-item {
      display: flex;
      align-items: flex-start;
      gap: 12px;
    }

    .feature-icon {
      width: 20px;
      height: 20px;
      flex-shrink: 0;
      margin-top: 2px;
    }

    .feature-icon svg {
      width: 100%;
      height: 100%;
      color: #22c55e;
    }

    .card.highlight .feature-icon svg {
      color: #96D7D2;
    }

    .feature-text {
      font-size: 16px;
      line-height: 1.4;
      color: rgba(26,28,33,0.7);
    }

    .card.highlight .feature-text {
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
    <div class="header">
      <h1 class="title">Choose Your Approach</h1>
      <p class="subtitle">Compare different AI adoption strategies for your organization</p>
    </div>

    <div class="cards-grid">
      <div class="card">
        <div class="card-label">Option A</div>
        <div class="card-title">Consumer Tools</div>
        <div class="card-features">
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Quick to get started</span>
          </div>
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Low initial cost</span>
          </div>
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Familiar interfaces</span>
          </div>
        </div>
      </div>

      <div class="card highlight">
        <div class="card-label">Recommended</div>
        <div class="card-title">Langdock Platform</div>
        <div class="card-features">
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Enterprise-grade security</span>
          </div>
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Multi-model flexibility</span>
          </div>
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Knowledge integration</span>
          </div>
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Admin controls & analytics</span>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-label">Option C</div>
        <div class="card-title">Build In-House</div>
        <div class="card-features">
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Full customization</span>
          </div>
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Complete control</span>
          </div>
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
            </div>
            <span class="feature-text">Proprietary IP</span>
          </div>
        </div>
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Customization

### Table Column Variants
| Columns | Use Case |
|---------|----------|
| 2 | Before/After, Yes/No comparisons |
| 3 | Product comparison (competitor vs Langdock vs competitor) |
| 4 | Multi-tier plans, detailed feature matrix |

### Status Indicators
```css
/* Check (positive) */
.check { background: rgba(34, 197, 94, 0.1); }
.check svg { color: #22c55e; }

/* Cross (negative) */
.cross { background: rgba(239, 68, 68, 0.1); }
.cross svg { color: #ef4444; }

/* Partial/Limited */
.partial { color: rgba(26,28,33,0.55); font-size: 14px; }

/* Premium/Upgrade required */
.premium { color: #4469fc; font-size: 14px; }
```
