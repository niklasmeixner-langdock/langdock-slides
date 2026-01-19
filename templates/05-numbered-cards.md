# Numbered Cards Slide (4-Column)

Process steps or features displayed as numbered white cards.

## When to Use
- Step-by-step processes
- Feature breakdowns
- How-to guides
- Sequential instructions

## Layout Pattern
- Title at top (128px)
- 4 equal-width cards starting at 280px
- Cards have number, title, description
- Full height utilization

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>How to Create - Langdock</title>
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
    .main-title {
      position: absolute;
      top: 128px;
      left: 64px;
      font-size: 64px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -3.2px;
      line-height: 1.1;
    }
    .cards-container {
      position: absolute;
      top: 280px;
      left: 64px;
      right: 64px;
      bottom: 64px;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 24px;
    }
    .numbered-card {
      background: #ffffff;
      border-radius: 16px;
      padding: 32px;
      display: flex;
      flex-direction: column;
      gap: 24px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
    }
    .card-number {
      font-size: 48px;
      font-weight: 600;
      color: #456AFC;
      line-height: 1;
    }
    .card-content {
      display: flex;
      flex-direction: column;
      gap: 12px;
      flex: 1;
    }
    .card-title {
      font-size: 28px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -0.42px;
      line-height: 1.2;
    }
    .card-description {
      font-size: 20px;
      font-weight: 500;
      color: #717279;
      line-height: 1.4;
      letter-spacing: -0.3px;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Custom Integrations</span>
    </div>
    <span class="slide-number">12</span>
  </div>

  <h1 class="main-title">How to Create Custom Integrations</h1>

  <div class="cards-container">
    <div class="numbered-card">
      <span class="card-number">01</span>
      <div class="card-content">
        <h3 class="card-title">Navigate to Settings</h3>
        <p class="card-description">Go to Admin Settings → Integrations → Custom Integrations</p>
      </div>
    </div>
    <div class="numbered-card">
      <span class="card-number">02</span>
      <div class="card-content">
        <h3 class="card-title">Create New Integration</h3>
        <p class="card-description">Click "Add Integration" and choose your authentication method</p>
      </div>
    </div>
    <div class="numbered-card">
      <span class="card-number">03</span>
      <div class="card-content">
        <h3 class="card-title">Define Actions</h3>
        <p class="card-description">Add actions with endpoints, parameters, and descriptions</p>
      </div>
    </div>
    <div class="numbered-card">
      <span class="card-number">04</span>
      <div class="card-content">
        <h3 class="card-title">Test & Deploy</h3>
        <p class="card-description">Test your integration and make it available to users</p>
      </div>
    </div>
  </div>
</body>
</html>
```

## Variations

### 3-Column Layout
```css
.cards-container {
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}
```

### With Icons Instead of Numbers
Replace `.card-number` with an icon:
```html
<div class="card-icon">
  <i class="ti ti-settings" style="font-size: 48px; color: #456AFC;"></i>
</div>
```

### Taller Cards (More Description)
Increase description font or add more padding:
```css
.card-description {
  font-size: 22px;
  line-height: 1.5;
}
```
