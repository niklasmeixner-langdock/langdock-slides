# All-in-One Solution / Product Platform Slide

Comprehensive view of the Langdock platform showing the blue product box with features, plus a dark foundation layer with integrations, connectors, models, and infrastructure.

## When to Use
- Product overview presentations
- Enterprise sales decks
- "Your Company GPT" positioning
- Full platform capability showcase
- Technical architecture overview

## Layout Pattern
- Top: "Rolled out to all your employees" label
- Main area with dashed border containing:
  - Left label: "Single entry-point" + "Your Company GPT"
  - Blue product platform box (Chat, Agents, Workflows, Mobile App)
  - Right: Compliance badges + Admin controls
- Bottom: Dark foundation bar with 4 sections (Integrations, Connectors, Model-agnostic, Infrastructure)
- Customer logo in bottom-left corner

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>All-in-one Company GPT - Langdock</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Inter', sans-serif;
      background: #f8f8f9;
      width: 1920px;
      height: 1080px;
      position: relative;
      overflow: hidden;
    }
    .header {
      position: absolute;
      top: 40px;
      left: 64px;
      right: 64px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .breadcrumbs { display: flex; align-items: center; gap: 12px; }
    .footnote { font-size: 18px; font-weight: 500; color: #717279; letter-spacing: -0.36px; }
    .slide-number { font-size: 18px; font-weight: 500; color: #717279; }

    /* Top Label */
    .top-label {
      position: absolute;
      top: 100px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 24px;
      font-weight: 500;
      color: #717279;
    }

    /* Main Container with Dashed Border */
    .main-container {
      position: absolute;
      top: 160px;
      left: 64px;
      right: 64px;
      bottom: 64px;
      border: 2px dashed #22c55e;
      border-radius: 24px;
      padding: 32px;
      display: flex;
      flex-direction: column;
    }

    /* Content Area */
    .content-area {
      flex: 1;
      display: flex;
      gap: 32px;
      align-items: stretch;
    }

    /* Left Labels */
    .left-labels {
      width: 200px;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      padding: 40px 0;
    }
    .left-label {
      font-size: 22px;
      font-weight: 600;
      color: #121420;
      line-height: 1.3;
    }
    .left-label-sub {
      font-size: 18px;
      font-weight: 500;
      color: #717279;
    }

    /* Blue Product Platform */
    .product-platform {
      flex: 1;
      background: #456AFC;
      border-radius: 20px;
      padding: 32px;
      display: flex;
      flex-direction: column;
    }
    .platform-logo-row {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 24px;
    }
    .platform-logo-icon {
      width: 32px;
      height: 32px;
      background: #ffffff;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .platform-tiles-grid {
      flex: 1;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr;
      gap: 16px;
    }
    .platform-tile {
      background: rgba(255, 255, 255, 0.15);
      border-radius: 16px;
      padding: 24px;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      gap: 12px;
    }
    .tile-icon-box {
      width: 56px;
      height: 56px;
      background: rgba(255, 255, 255, 0.2);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .tile-icon-box i {
      font-size: 28px;
      color: #ffffff;
    }
    .tile-label {
      font-size: 22px;
      font-weight: 600;
      color: #ffffff;
    }
    .platform-footer {
      margin-top: 24px;
      display: flex;
      flex-direction: column;
      gap: 4px;
    }
    .platform-footer-title {
      font-size: 20px;
      font-weight: 600;
      color: #ffffff;
    }
    .platform-footer-sub {
      font-size: 16px;
      color: rgba(255, 255, 255, 0.7);
    }

    /* Right Section (Badges + Controls) */
    .right-section {
      width: 320px;
      display: flex;
      flex-direction: column;
      gap: 24px;
      padding: 40px 0;
    }
    .badges-row {
      display: flex;
      gap: 16px;
      align-items: center;
    }
    .badge {
      height: 56px;
      object-fit: contain;
    }
    .control-item {
      background: rgba(69, 106, 252, 0.08);
      border-radius: 12px;
      padding: 20px 24px;
      font-size: 20px;
      font-weight: 500;
      color: #456AFC;
    }

    /* Foundation Bar (Dark) */
    .foundation-bar {
      background: #242631;
      border-radius: 16px;
      margin-top: 24px;
      padding: 24px 32px;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 24px;
    }
    .foundation-section {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .foundation-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .foundation-title {
      font-size: 18px;
      font-weight: 600;
      color: #ffffff;
    }
    .foundation-count {
      font-size: 16px;
      font-weight: 500;
      color: rgba(255, 255, 255, 0.5);
    }
    .foundation-items {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
    }
    .foundation-icon {
      width: 40px;
      height: 40px;
      background: rgba(255, 255, 255, 0.08);
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .foundation-icon img {
      width: 24px;
      height: 24px;
      object-fit: contain;
    }
    .foundation-tag {
      background: rgba(255, 255, 255, 0.08);
      border-radius: 8px;
      padding: 10px 16px;
      font-size: 15px;
      font-weight: 500;
      color: #ffffff;
    }
    .foundation-tag.highlight {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.2);
    }

    /* Customer Logo */
    .customer-logo {
      position: absolute;
      bottom: 96px;
      left: 96px;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .customer-logo img {
      height: 48px;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Langdock</span>
    </div>
    <span class="slide-number">6</span>
  </div>

  <div class="top-label">Rolled out to all your employees</div>

  <div class="main-container">
    <div class="content-area">
      <!-- Left Labels -->
      <div class="left-labels">
        <div>
          <div class="left-label">Single entry-point</div>
          <div class="left-label-sub">for AI related tasks</div>
        </div>
        <div>
          <div class="left-label">Your</div>
          <div class="left-label">Company GPT</div>
        </div>
      </div>

      <!-- Blue Product Platform -->
      <div class="product-platform">
        <div class="platform-logo-row">
          <div class="platform-logo-icon">
            <img src="assets/langdock-logo.png" alt="Langdock" style="width: 20px; height: 20px;">
          </div>
        </div>
        <div class="platform-tiles-grid">
          <div class="platform-tile">
            <div class="tile-icon-box">
              <i class="ti ti-message"></i>
            </div>
            <span class="tile-label">Chat</span>
          </div>
          <div class="platform-tile">
            <div class="tile-icon-box">
              <i class="ti ti-robot"></i>
            </div>
            <span class="tile-label">Agents</span>
          </div>
          <div class="platform-tile">
            <div class="tile-icon-box">
              <i class="ti ti-git-branch"></i>
            </div>
            <span class="tile-label">Workflows</span>
          </div>
          <div class="platform-tile">
            <div class="tile-icon-box">
              <i class="ti ti-device-mobile"></i>
            </div>
            <span class="tile-label">Mobile App</span>
          </div>
        </div>
        <div class="platform-footer">
          <span class="platform-footer-title">Langdock</span>
          <span class="platform-footer-sub">Product Platform</span>
        </div>
      </div>

      <!-- Right Section -->
      <div class="right-section">
        <div class="badges-row">
          <img src="badges/iso-27001.png" alt="ISO 27001" class="badge">
          <img src="badges/soc2.png" alt="SOC 2" class="badge">
          <img src="badges/gdpr.png" alt="GDPR" class="badge">
          <img src="badges/made-in-germany.png" alt="Made in Germany" class="badge">
        </div>
        <div class="control-item">Admin controls</div>
        <div class="control-item">Branding & Customizations</div>
      </div>
    </div>

    <!-- Foundation Bar -->
    <div class="foundation-bar">
      <div class="foundation-section">
        <div class="foundation-header">
          <span class="foundation-title">Integrations</span>
          <span class="foundation-count">50+</span>
        </div>
        <div class="foundation-items">
          <div class="foundation-icon">
            <img src="assets/integration-icons/slack-icon.png" alt="Slack">
          </div>
          <div class="foundation-icon">
            <img src="assets/integration-icons/jira-icon.png" alt="Jira">
          </div>
          <div class="foundation-icon">
            <img src="assets/integration-icons/hubspot-icon.png" alt="HubSpot">
          </div>
          <span class="foundation-tag highlight">Yours</span>
        </div>
      </div>

      <div class="foundation-section">
        <div class="foundation-header">
          <span class="foundation-title">Connectors</span>
        </div>
        <div class="foundation-items">
          <span class="foundation-tag">API</span>
          <span class="foundation-tag">MCP</span>
          <span class="foundation-tag">A2A</span>
        </div>
      </div>

      <div class="foundation-section">
        <div class="foundation-header">
          <span class="foundation-title">Model-agnostic</span>
          <span class="foundation-count">30+</span>
        </div>
        <div class="foundation-items">
          <div class="foundation-icon">
            <i class="ti ti-brand-openai" style="font-size: 20px; color: #ffffff;"></i>
          </div>
          <div class="foundation-icon">
            <span style="font-size: 16px; font-weight: 600; color: #ffffff;">A</span>
          </div>
          <div class="foundation-icon">
            <i class="ti ti-diamond" style="font-size: 20px; color: #ffffff;"></i>
          </div>
          <div class="foundation-icon">
            <i class="ti ti-brand-amazon" style="font-size: 20px; color: #ffffff;"></i>
          </div>
          <span class="foundation-tag highlight">Yours</span>
        </div>
      </div>

      <div class="foundation-section">
        <div class="foundation-header">
          <span class="foundation-title">Infrastructure</span>
        </div>
        <div class="foundation-items">
          <span class="foundation-tag highlight">Your Infrastructure</span>
        </div>
      </div>
    </div>
  </div>

  <!-- Customer Logo -->
  <div class="customer-logo">
    <img src="logos/dekra.png" alt="DEKRA">
  </div>
</body>
</html>
```

## Key Visual Elements

### Dashed Green Border
Creates a visual container suggesting customization/ownership:
```css
border: 2px dashed #22c55e;
```

### Blue Product Platform
Core product in vibrant blue (#456AFC) with semi-transparent tiles:
```css
background: rgba(255, 255, 255, 0.15);
```

### Foundation Bar
Dark bar showing technical foundation with integration icons:
- Uses integration icons from `/integration-icons/`
- Mix of icons and text tags
- "Yours" tags with border-only style

### Compliance Badges
Row of trust badges (ISO, SOC2, GDPR, Made in Germany)

## Variations

### Without Customer Logo
Remove for generic presentations.

### Simplified Foundation
Show only 2 sections:
```css
.foundation-bar {
  grid-template-columns: 1fr 1fr;
}
```

### More Integrations
Expand integration icons in foundation:
```html
<div class="foundation-items">
  <div class="foundation-icon"><img src="assets/integration-icons/slack-icon.png"></div>
  <div class="foundation-icon"><img src="assets/integration-icons/microsoft-teams-icon.png"></div>
  <div class="foundation-icon"><img src="assets/integration-icons/jira-icon.png"></div>
  <div class="foundation-icon"><img src="assets/integration-icons/salesforce-icon.png"></div>
  <div class="foundation-icon"><img src="assets/integration-icons/hubspot-icon.png"></div>
  <span class="foundation-tag highlight">+45</span>
</div>
```

### Different Product Tiles
Adjust tiles for different focus:
- Chat + Agents + Workflows + API (developer focus)
- Chat + Agents + Knowledge + Analytics (enterprise focus)
