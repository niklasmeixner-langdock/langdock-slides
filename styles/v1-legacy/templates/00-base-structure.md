# Base Slide Structure

Every slide follows this base HTML structure. Use this as a starting point for custom slides.

## HTML Boilerplate

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Slide Title - Langdock</title>
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

    /* === HEADER === */
    .header {
      position: absolute;
      top: 40px;
      left: 64px;
      right: 64px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .breadcrumbs {
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .footnote {
      font-size: 18px;
      font-weight: 500;
      color: #717279;
      letter-spacing: -0.36px;
    }
    .slide-number {
      font-size: 18px;
      font-weight: 500;
      color: #717279;
    }

    /* === TITLE === */
    .main-title {
      position: absolute;
      top: 128px;
      left: 64px;
      font-size: 64px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -3.2px;
      line-height: 1.1;
      max-width: 1400px;
    }

    /* === CONTENT AREA === */
    /* Full height content: starts at 240px */
    /* Lower third content: starts at ~600px */
    .content {
      position: absolute;
      top: 240px;
      left: 64px;
      right: 64px;
      bottom: 64px;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Section Name</span>
    </div>
    <span class="slide-number">1</span>
  </div>

  <h1 class="main-title">Slide Title</h1>

  <div class="content">
    <!-- Main content goes here -->
  </div>
</body>
</html>
```

## Layout Zones

```
┌─────────────────────────────────────────────────┐
│  40px   HEADER: breadcrumbs + slide number      │
├─────────────────────────────────────────────────┤
│  128px  TITLE: main headline                    │
├─────────────────────────────────────────────────┤
│  240px+ CONTENT ZONE                            │
│         - Full height: top: 240px               │
│         - Lower third: top: 600px               │
│         - Centered: use flexbox centering       │
├─────────────────────────────────────────────────┤
│  64px   FOOTER MARGIN                           │
└─────────────────────────────────────────────────┘
```

## Typography Reference

| Element | Size | Weight | Color | Tracking |
|---------|------|--------|-------|----------|
| Headline 1 | 64px | 600 | #121420 | -3.2px |
| Headline 2 | 40px | 700 | #121420 | -1.6px |
| Headline 3 | 36px | 600 | #121420 | -1.44px |
| Body Large | 28px | 500 | #121420 | -0.42px |
| Body | 24px | 500 | #121420 | -0.36px |
| Body Small | 20px | 500 | varies | -0.3px |
| Footnote | 18px | 500 | #717279 | -0.36px |

## Color Tokens

```css
--background: #f8f8f9;
--text-primary: #121420;
--text-secondary: #717279;
--accent: #456AFC;
--border: #bebec2;
--surface-white: #ffffff;
--surface-dark: #242631;
--overlay-subtle: rgba(14, 17, 18, 0.12);  /* Tags */
--overlay-dark: rgba(14, 17, 18, 0.06);    /* Info boxes */
```
