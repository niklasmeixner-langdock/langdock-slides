# 00 - Base Structure

The foundational HTML structure for all v2-current slides.

## HTML Boilerplate

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <style>
    /* ========== CSS RESET ========== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* ========== GOOGLE FONTS ========== */
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

    /* ========== DESIGN TOKENS ========== */
    :root {
      /* Colors */
      --color-primary-dark: #1a1c21;
      --color-primary-blue: #4469fc;
      --color-bg-light: #F8F8FC;
      --color-bg-elevated: #ECECF4;
      --color-bg-white: #FFFFFF;
      --color-dark-warm: #4d473c;
      --color-text-primary: #1a1c21;
      --color-text-secondary: rgba(26,28,33,0.55);
      --color-text-muted: rgba(26,28,33,0.3);
      --color-text-on-dark: #FFFFFF;
      --color-text-on-dark-secondary: rgba(255,255,255,0.75);
      --color-accent-teal: #96D7D2;
      --color-border-light: rgba(26,28,33,0.1);

      /* Typography */
      --font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;

      /* Layout */
      --canvas-width: 1920px;
      --canvas-height: 1200px;
      --margin: 64px;
      --gap-xl: 48px;
      --gap-lg: 32px;
      --gap-md: 24px;
      --gap-sm: 16px;
      --gap-xs: 8px;

      /* Border Radius */
      --radius-xl: 24px;
      --radius-lg: 16px;
      --radius-md: 12px;
      --radius-sm: 8px;
      --radius-pill: 100px;

      /* Shadows */
      --shadow-card: 0px 4px 24px rgba(0, 0, 0, 0.08);
      --shadow-elevated: 0px 8px 32px rgba(0, 0, 0, 0.12);
    }

    /* ========== BASE STYLES ========== */
    body {
      font-family: var(--font-family);
      background: var(--color-bg-light);
      color: var(--color-text-primary);
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    /* ========== SLIDE CONTAINER ========== */
    .slide {
      width: var(--canvas-width);
      height: var(--canvas-height);
      padding: var(--margin);
      position: relative;
      overflow: hidden;
      display: flex;
      flex-direction: column;
    }

    /* Background variants */
    .slide--light { background: var(--color-bg-light); }
    .slide--white { background: var(--color-bg-white); }
    .slide--elevated { background: var(--color-bg-elevated); }
    .slide--dark { background: var(--color-dark-warm); color: var(--color-text-on-dark); }

    /* ========== TYPOGRAPHY ========== */
    .h1 {
      font-size: 56px;
      font-weight: 600;
      letter-spacing: -1.12px;
      line-height: 1.1;
      color: var(--color-text-primary);
    }
    .slide--dark .h1 { color: var(--color-text-on-dark); }

    .h2 {
      font-size: 40px;
      font-weight: 600;
      letter-spacing: -0.8px;
      line-height: 1.2;
      color: var(--color-text-primary);
    }
    .slide--dark .h2 { color: var(--color-text-on-dark); }

    .h3 {
      font-size: 24px;
      font-weight: 600;
      letter-spacing: -0.48px;
      line-height: 1.3;
      color: var(--color-text-primary);
    }
    .slide--dark .h3 { color: var(--color-text-on-dark); }

    .body {
      font-size: 20px;
      font-weight: 400;
      letter-spacing: -0.2px;
      line-height: 1.5;
      color: var(--color-text-secondary);
    }
    .slide--dark .body { color: var(--color-text-on-dark-secondary); }

    .body-small {
      font-size: 18px;
      font-weight: 400;
      letter-spacing: -0.18px;
      line-height: 1.5;
      color: var(--color-text-secondary);
    }

    .caption {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: -0.14px;
      line-height: 1.4;
      color: var(--color-text-muted);
    }

    /* ========== LAYOUT UTILITIES ========== */
    .flex { display: flex; }
    .flex-col { flex-direction: column; }
    .items-center { align-items: center; }
    .items-start { align-items: flex-start; }
    .items-end { align-items: flex-end; }
    .justify-center { justify-content: center; }
    .justify-between { justify-content: space-between; }
    .justify-start { justify-content: flex-start; }
    .justify-end { justify-content: flex-end; }
    .flex-1 { flex: 1; }
    .flex-wrap { flex-wrap: wrap; }

    .gap-xl { gap: var(--gap-xl); }
    .gap-lg { gap: var(--gap-lg); }
    .gap-md { gap: var(--gap-md); }
    .gap-sm { gap: var(--gap-sm); }
    .gap-xs { gap: var(--gap-xs); }

    .text-center { text-align: center; }
    .text-left { text-align: left; }
    .text-right { text-align: right; }

    /* ========== COMPONENT CLASSES ========== */
    /* See components/README.md for full component documentation */
  </style>
</head>
<body>
  <div class="slide slide--light">
    <!-- Slide content goes here -->
  </div>
</body>
</html>
```

## Slide Background Variants

| Class | Background | Text Color |
|-------|------------|------------|
| `.slide--light` | `#F8F8FC` (light gray) | Dark text |
| `.slide--white` | `#FFFFFF` (white) | Dark text |
| `.slide--elevated` | `#ECECF4` (elevated) | Dark text |
| `.slide--dark` | `#4d473c` (warm brown) | White text |

## Content Areas

Most slides use this basic structure:

```html
<div class="slide slide--light">
  <!-- Header area (optional) -->
  <div class="slide-header">
    <!-- Breadcrumb, slide number, etc. -->
  </div>

  <!-- Main content area -->
  <div class="slide-content flex-1 flex flex-col gap-lg">
    <!-- Title -->
    <h1 class="h1">Slide Title</h1>

    <!-- Subtitle (optional) -->
    <p class="body">Supporting description text goes here.</p>

    <!-- Main content -->
    <div class="content-area flex-1">
      <!-- Cards, lists, images, etc. -->
    </div>
  </div>

  <!-- Footer area (optional) -->
  <div class="slide-footer">
    <!-- Logo, page number, etc. -->
  </div>
</div>
```

## Typography Quick Reference

| Class | Size | Weight | Use For |
|-------|------|--------|---------|
| `.h1` | 56px | 600 | Main slide titles |
| `.h2` | 40px | 600 | Section titles, card headers |
| `.h3` | 24px | 600 | Subsections, feature titles |
| `.body` | 20px | 400 | Main content text |
| `.body-small` | 18px | 400 | Secondary content |
| `.caption` | 14px | 500 | Labels, small text |

## Logo Placement

```html
<!-- Bottom left corner (default) -->
<img
  src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png"
  alt="Langdock"
  style="position: absolute; bottom: 64px; left: 64px; height: 24px; width: auto;"
>

<!-- On dark slides, invert the logo -->
<img
  src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png"
  alt="Langdock"
  style="position: absolute; bottom: 64px; left: 64px; height: 24px; width: auto; filter: brightness(0) invert(1);"
>
```
