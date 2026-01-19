# 10 - Customer Logos

Display customer logos, partner brands, or trust indicators for social proof.

## Use Cases
- Customer showcase
- Partner logos
- Trust indicators
- "Trusted by" sections
- Integration partners
- Media mentions

## Layout Options

### Option A: Logo Grid with Header

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
      text-align: center;
      margin-bottom: 64px;
    }

    .label {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      color: rgba(26,28,33,0.4);
      margin-bottom: 16px;
    }

    .title {
      font-size: 40px;
      font-weight: 600;
      letter-spacing: -0.8px;
      color: #1a1c21;
    }

    .logos-grid {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 32px;
      flex: 1;
      align-content: center;
      padding: 0 64px;
    }

    .logo-item {
      background: #F8F8FC;
      border-radius: 16px;
      padding: 32px;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 120px;
    }

    .logo-item img {
      max-width: 140px;
      max-height: 50px;
      object-fit: contain;
      filter: grayscale(100%);
      opacity: 0.7;
      transition: all 0.2s;
    }

    .logo-item:hover img {
      filter: grayscale(0%);
      opacity: 1;
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
      <div class="label">Trusted by leading companies</div>
      <h1 class="title">Join 3,000+ organizations using Langdock</h1>
    </div>

    <div class="logos-grid">
      <div class="logo-item">
        <img src="[LOGO_URL_1]" alt="Company 1">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_2]" alt="Company 2">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_3]" alt="Company 3">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_4]" alt="Company 4">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_5]" alt="Company 5">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_6]" alt="Company 6">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_7]" alt="Company 7">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_8]" alt="Company 8">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_9]" alt="Company 9">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_10]" alt="Company 10">
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option B: Minimal Logo Row

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
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 64px;
      position: relative;
    }

    .label {
      font-size: 16px;
      font-weight: 500;
      color: rgba(26,28,33,0.4);
      margin-bottom: 48px;
    }

    .logos-row {
      display: flex;
      align-items: center;
      gap: 80px;
    }

    .logo-item img {
      height: 40px;
      width: auto;
      object-fit: contain;
      filter: grayscale(100%);
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
    <div class="label">Trusted by</div>

    <div class="logos-row">
      <div class="logo-item">
        <img src="[LOGO_URL_1]" alt="Company 1">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_2]" alt="Company 2">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_3]" alt="Company 3">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_4]" alt="Company 4">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_5]" alt="Company 5">
      </div>
      <div class="logo-item">
        <img src="[LOGO_URL_6]" alt="Company 6">
      </div>
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

### Option C: Integration Partners

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

    .integrations-grid {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 24px;
      flex: 1;
      align-content: center;
    }

    .integration-card {
      background: #F8F8FC;
      border-radius: 16px;
      padding: 24px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 16px;
      text-align: center;
    }

    .integration-icon {
      width: 48px;
      height: 48px;
      object-fit: contain;
    }

    .integration-name {
      font-size: 14px;
      font-weight: 500;
      color: #1a1c21;
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
      <h1 class="title">50+ Integrations</h1>
      <p class="subtitle">Connect Langdock to your existing tools and workflows</p>
    </div>

    <div class="integrations-grid">
      <div class="integration-card">
        <img class="integration-icon" src="../../shared/assets/integration-icons/slack-icon.png" alt="Slack">
        <span class="integration-name">Slack</span>
      </div>
      <div class="integration-card">
        <img class="integration-icon" src="../../shared/assets/integration-icons/notion-icon.png" alt="Notion">
        <span class="integration-name">Notion</span>
      </div>
      <div class="integration-card">
        <img class="integration-icon" src="../../shared/assets/integration-icons/confluence-icon.png" alt="Confluence">
        <span class="integration-name">Confluence</span>
      </div>
      <div class="integration-card">
        <img class="integration-icon" src="../../shared/assets/integration-icons/google-drive-icon.png" alt="Google Drive">
        <span class="integration-name">Google Drive</span>
      </div>
      <div class="integration-card">
        <img class="integration-icon" src="../../shared/assets/integration-icons/microsoft-sharepoint-icon.png" alt="SharePoint">
        <span class="integration-name">SharePoint</span>
      </div>
      <div class="integration-card">
        <img class="integration-icon" src="../../shared/assets/integration-icons/jira-icon.png" alt="Jira">
        <span class="integration-name">Jira</span>
      </div>
      <!-- Add more integrations as needed -->
    </div>

    <img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">
  </div>
</body>
</html>
```

## Logo Styling

```css
/* Grayscale (default for customer logos) */
.logo-item img {
  filter: grayscale(100%);
  opacity: 0.6;
}

/* Color logos (for integrations) */
.logo-item img {
  filter: none;
  opacity: 1;
}

/* Monochrome dark */
.logo-item img {
  filter: grayscale(100%) brightness(0.3);
}
```

## Grid Configurations

| Logos | Columns | Rows |
|-------|---------|------|
| 4-6 | Single row | - |
| 8-10 | 5 | 2 |
| 12-15 | 5 | 3 |
| 16-20 | 5 | 4 |

## Integration Icons Path

Use icons from the shared assets:
```
../../shared/assets/integration-icons/[service]-icon.png
```

Available integrations include: Slack, Notion, Confluence, Google Drive, SharePoint, Jira, Salesforce, HubSpot, and many more.
