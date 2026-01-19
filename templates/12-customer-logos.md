# Customer Logos / Stats Slide

Left column with key statistics, right side with logo grid. Great for social proof and company credibility.

## When to Use
- Customer testimonials section
- "Who uses us" slides
- Trust/credibility slides
- Partnership announcements

## Layout Pattern
- Title at top-left (128px)
- Left column: 3 key stats with labels (width ~320px)
- Right side: 5x5 logo grid
- Stats separated by subtle dividers

## Full Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=1920, height=1080">
  <title>Our Customers - Langdock</title>
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
      top: 100px;
      left: 64px;
      font-size: 64px;
      font-weight: 600;
      color: #121420;
      letter-spacing: -3.2px;
      line-height: 1.1;
    }
    .content-layout {
      position: absolute;
      top: 240px;
      left: 64px;
      right: 64px;
      bottom: 64px;
      display: flex;
      gap: 80px;
    }
    .stats-column {
      width: 320px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      gap: 0;
    }
    .stat-item {
      padding: 40px 0;
      border-top: 1px solid #e0e0e0;
    }
    .stat-item:first-child {
      border-top: none;
      padding-top: 0;
    }
    .stat-item:last-child {
      padding-bottom: 0;
    }
    .stat-number {
      font-size: 72px;
      font-weight: 700;
      color: #121420;
      letter-spacing: -2.88px;
      line-height: 1;
      margin-bottom: 12px;
    }
    .stat-label {
      font-size: 22px;
      font-weight: 500;
      color: #717279;
      letter-spacing: -0.33px;
      line-height: 1.3;
    }
    .logos-grid {
      flex: 1;
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      grid-template-rows: repeat(5, 1fr);
      gap: 24px;
      align-content: center;
    }
    .logo-item {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 60px;
    }
    .logo-item img {
      max-width: 140px;
      max-height: 48px;
      object-fit: contain;
      filter: grayscale(100%);
      opacity: 0.7;
    }
    /* Color logos variant */
    .logos-grid.color .logo-item img {
      filter: none;
      opacity: 1;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="breadcrumbs">
      <i class="ti ti-chevron-right" style="font-size: 18px; color: #717279;"></i>
      <span class="footnote">Langdock</span>
    </div>
    <span class="slide-number">8</span>
  </div>

  <h1 class="main-title">Our Customers</h1>

  <div class="content-layout">
    <div class="stats-column">
      <div class="stat-item">
        <div class="stat-number">3.500+</div>
        <div class="stat-label">Companies trust Langdock</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">100+</div>
        <div class="stat-label">Successful large rollouts</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">17%</div>
        <div class="stat-label">Month-over-month growth<br>and profitable</div>
      </div>
    </div>

    <div class="logos-grid color">
      <!-- Row 1 -->
      <div class="logo-item"><img src="logos/merck.png" alt="Merck"></div>
      <div class="logo-item"><img src="logos/personio.png" alt="Personio"></div>
      <div class="logo-item"><img src="logos/der-spiegel.png" alt="Der Spiegel"></div>
      <div class="logo-item"><img src="logos/lavera.png" alt="Lavera"></div>
      <div class="logo-item"><img src="logos/babbel.png" alt="Babbel"></div>
      <div class="logo-item"><img src="logos/getyourguide.png" alt="GetYourGuide"></div>
      <!-- Row 2 -->
      <div class="logo-item"><img src="logos/forto.png" alt="Forto"></div>
      <div class="logo-item"><img src="logos/blinkist.png" alt="Blinkist"></div>
      <div class="logo-item"><img src="logos/adelphi.png" alt="Adelphi"></div>
      <div class="logo-item"><img src="logos/heyjobs.png" alt="HeyJobs"></div>
      <div class="logo-item"><img src="logos/hofmann.png" alt="Hofmann"></div>
      <div class="logo-item"><img src="logos/ibb.png" alt="IBB"></div>
      <!-- Row 3 -->
      <div class="logo-item"><img src="logos/leipfinger-bader.png" alt="Leipfinger Bader"></div>
      <div class="logo-item"><img src="logos/mondu.png" alt="Mondu"></div>
      <div class="logo-item"><img src="logos/accso.png" alt="Accso"></div>
      <div class="logo-item"><img src="logos/palmerhargreaves.png" alt="Palmer Hargreaves"></div>
      <div class="logo-item"><img src="logos/porta.png" alt="Porta"></div>
      <div class="logo-item"><img src="logos/razor-group.png" alt="Razor Group"></div>
      <!-- Row 4 -->
      <div class="logo-item"><img src="logos/piper.png" alt="Piper"></div>
      <div class="logo-item"><img src="logos/intershop.png" alt="Intershop"></div>
      <div class="logo-item"><img src="logos/lanch.png" alt="Lanch"></div>
      <div class="logo-item"><img src="logos/mobilede.png" alt="Mobile.de"></div>
      <div class="logo-item"><img src="logos/statworx.png" alt="Statworx"></div>
      <div class="logo-item"><img src="logos/flensburger.png" alt="Flensburger"></div>
      <!-- Row 5 -->
      <div class="logo-item"><img src="logos/justaddsugar.png" alt="JustAddSugar"></div>
      <div class="logo-item"><img src="logos/turbine-kreuzberg.png" alt="Turbine Kreuzberg"></div>
      <div class="logo-item"><img src="logos/i-like-visuals.png" alt="I Like Visuals"></div>
      <div class="logo-item"><img src="logos/odaline.png" alt="Odaline"></div>
      <div class="logo-item"><img src="logos/floy.png" alt="Floy"></div>
      <div class="logo-item"><img src="logos/kombo.png" alt="Kombo"></div>
    </div>
  </div>
</body>
</html>
```

## Variations

### Grayscale Logos
Remove the `.color` class from `.logos-grid`:
```html
<div class="logos-grid">
```

### Fewer Logos (4x4)
```css
.logos-grid {
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(4, 1fr);
}
```

### Stats on Right
Swap the order in HTML and adjust flex:
```css
.content-layout {
  flex-direction: row-reverse;
}
```

### With Integration Icons Instead of Logos
Use integration icons for "Integrations" slide:
```html
<div class="integration-grid">
  <div class="integration-icon">
    <img src="integration-icons/slack-icon.png" alt="Slack">
  </div>
  <!-- ... more icons -->
</div>
```

```css
.integration-grid {
  flex: 1;
  display: grid;
  grid-template-columns: repeat(5, 80px);
  grid-template-rows: repeat(4, 80px);
  gap: 20px;
  align-content: center;
  justify-content: center;
}
.integration-icon {
  width: 80px;
  height: 80px;
  background: #ffffff;
  border-radius: 16px;
  padding: 16px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  display: flex;
  align-items: center;
  justify-content: center;
}
.integration-icon img {
  width: 48px;
  height: 48px;
  object-fit: contain;
}
```

### Dark Variant
```css
body { background: #242631; }
.main-title { color: #f8f8f9; }
.stat-number { color: #f8f8f9; }
.stat-label { color: rgba(248, 248, 249, 0.6); }
.stat-item { border-top-color: rgba(255, 255, 255, 0.1); }
.logo-item img { filter: brightness(0) invert(1); opacity: 0.7; }
```
