# v2-current Reusable Components

This directory contains reusable UI components for the v2-current slide design system. These components can be combined and customized to create new slide layouts.

## Quick Reference

| Component | Use For |
|-----------|---------|
| [Buttons](#buttons) | CTAs, actions, links |
| [Tags & Badges](#tags--badges) | Labels, categories, status |
| [Cards](#cards) | Content containers |
| [Icons](#icons) | Visual indicators |
| [Lists](#lists) | Bullet points, checklists |
| [Typography](#typography) | Headings, body text |
| [Callouts](#callouts) | Highlights, tips, warnings |
| [Progress & Steps](#progress--steps) | Numbered sequences |
| [Logo Placement](#logo-placement) | Branding |
| [Decorative Elements](#decorative-elements) | Visual accents |

---

## Buttons

### Primary Button (Dark)
```html
<a href="#" class="btn-primary">
  Get Started
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
    <line x1="5" y1="12" x2="19" y2="12"/>
    <polyline points="12 5 19 12 12 19"/>
  </svg>
</a>

<style>
.btn-primary {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: #1a1c21;
  color: #FFFFFF;
  padding: 14px 28px;
  border-radius: 100px;
  font-size: 16px;
  font-weight: 500;
  text-decoration: none;
}

.btn-primary svg {
  width: 18px;
  height: 18px;
}
</style>
```

### Primary Button (Blue)
```html
<a href="#" class="btn-blue">
  Learn More
</a>

<style>
.btn-blue {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: #4469fc;
  color: #FFFFFF;
  padding: 14px 28px;
  border-radius: 100px;
  font-size: 16px;
  font-weight: 500;
  text-decoration: none;
}
</style>
```

### Secondary Button (Outline)
```html
<a href="#" class="btn-secondary">
  View Demo
</a>

<style>
.btn-secondary {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: transparent;
  border: 2px solid #1a1c21;
  color: #1a1c21;
  padding: 12px 26px;
  border-radius: 100px;
  font-size: 16px;
  font-weight: 500;
  text-decoration: none;
}

/* Light version for dark backgrounds */
.btn-secondary-light {
  border-color: rgba(255,255,255,0.3);
  color: #FFFFFF;
}
</style>
```

### Ghost Button
```html
<a href="#" class="btn-ghost">
  Skip for now
</a>

<style>
.btn-ghost {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: transparent;
  color: rgba(26,28,33,0.55);
  padding: 12px 20px;
  font-size: 16px;
  font-weight: 500;
  text-decoration: none;
}

.btn-ghost:hover {
  color: #1a1c21;
}
</style>
```

---

## Tags & Badges

### Label Tag (Blue)
```html
<span class="tag-label">Module 1</span>

<style>
.tag-label {
  font-size: 14px;
  font-weight: 500;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  color: #4469fc;
}
</style>
```

### Label Tag (Teal - for dark backgrounds)
```html
<span class="tag-label-teal">Advanced</span>

<style>
.tag-label-teal {
  font-size: 14px;
  font-weight: 500;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  color: #96D7D2;
}
</style>
```

### Pill Tag
```html
<span class="tag-pill">GPT-4</span>

<style>
.tag-pill {
  background: #ECECF4;
  padding: 6px 12px;
  border-radius: 100px;
  font-size: 13px;
  font-weight: 500;
  color: rgba(26,28,33,0.6);
}

/* Filled variant */
.tag-pill-filled {
  background: rgba(68, 105, 252, 0.1);
  color: #4469fc;
}

/* Dark background variant */
.tag-pill-dark {
  background: rgba(255,255,255,0.15);
  color: #FFFFFF;
}
</style>
```

### Badge with Icon
```html
<div class="badge-icon">
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
    <polygon points="5 3 19 12 5 21 5 3"/>
  </svg>
  <span>Hands-On Exercise</span>
</div>

<style>
.badge-icon {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(255,255,255,0.15);
  padding: 10px 20px;
  border-radius: 100px;
}

.badge-icon svg {
  width: 18px;
  height: 18px;
  color: #96D7D2;
}

.badge-icon span {
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  color: #FFFFFF;
}
</style>
```

### Status Badge
```html
<span class="badge-status badge-success">Active</span>
<span class="badge-status badge-warning">Pending</span>
<span class="badge-status badge-neutral">Draft</span>

<style>
.badge-status {
  padding: 4px 10px;
  border-radius: 100px;
  font-size: 12px;
  font-weight: 500;
}

.badge-success {
  background: rgba(34, 197, 94, 0.1);
  color: #16a34a;
}

.badge-warning {
  background: rgba(234, 179, 8, 0.1);
  color: #ca8a04;
}

.badge-neutral {
  background: #ECECF4;
  color: rgba(26,28,33,0.6);
}
</style>
```

---

## Cards

### Basic Card
```html
<div class="card">
  <h3 class="card-title">Card Title</h3>
  <p class="card-text">Card description text goes here.</p>
</div>

<style>
.card {
  background: #FFFFFF;
  border-radius: 16px;
  padding: 32px;
  box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
}

.card-title {
  font-size: 22px;
  font-weight: 600;
  letter-spacing: -0.44px;
  color: #1a1c21;
  margin-bottom: 12px;
}

.card-text {
  font-size: 16px;
  font-weight: 400;
  line-height: 1.5;
  color: rgba(26,28,33,0.55);
}
</style>
```

### Card with Icon
```html
<div class="card-icon">
  <div class="card-icon-wrapper">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
      <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>
    </svg>
  </div>
  <h3 class="card-title">Chat Feature</h3>
  <p class="card-text">Description of the feature.</p>
</div>

<style>
.card-icon-wrapper {
  width: 56px;
  height: 56px;
  background: rgba(68, 105, 252, 0.1);
  border-radius: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 24px;
}

.card-icon-wrapper svg {
  width: 28px;
  height: 28px;
  color: #4469fc;
}
</style>
```

### Dark Card
```html
<div class="card-dark">
  <div class="card-dark-content">
    <h3 class="card-dark-title">Feature Name</h3>
    <p class="card-dark-text">Feature description goes here.</p>
  </div>
</div>

<style>
.card-dark {
  background: #4d473c;
  border-radius: 16px;
  padding: 40px;
  position: relative;
  overflow: hidden;
}

.card-dark-content {
  position: relative;
  z-index: 1;
}

.card-dark-title {
  font-size: 24px;
  font-weight: 600;
  letter-spacing: -0.48px;
  color: #FFFFFF;
  margin-bottom: 8px;
}

.card-dark-text {
  font-size: 16px;
  font-weight: 400;
  line-height: 1.5;
  color: rgba(255,255,255,0.7);
}
</style>
```

### Numbered Card
```html
<div class="card-numbered">
  <div class="card-number">01</div>
  <h3 class="card-title">Step Title</h3>
  <p class="card-text">Step description.</p>
</div>

<style>
.card-numbered {
  background: #FFFFFF;
  border-radius: 16px;
  padding: 32px;
  box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.06);
}

.card-number {
  font-size: 48px;
  font-weight: 700;
  color: rgba(68, 105, 252, 0.15);
  margin-bottom: 16px;
  line-height: 1;
}
</style>
```

---

## Icons

### Icon Container (Light Background)
```html
<div class="icon-container">
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
    <!-- icon path -->
  </svg>
</div>

<style>
.icon-container {
  width: 56px;
  height: 56px;
  background: rgba(68, 105, 252, 0.1);
  border-radius: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.icon-container svg {
  width: 28px;
  height: 28px;
  color: #4469fc;
}

/* Small variant */
.icon-container-sm {
  width: 40px;
  height: 40px;
  border-radius: 10px;
}

.icon-container-sm svg {
  width: 20px;
  height: 20px;
}

/* Large variant */
.icon-container-lg {
  width: 80px;
  height: 80px;
  border-radius: 20px;
}

.icon-container-lg svg {
  width: 40px;
  height: 40px;
}
</style>
```

### Icon Container (Dark Background)
```html
<div class="icon-container-dark">
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
    <!-- icon path -->
  </svg>
</div>

<style>
.icon-container-dark {
  width: 56px;
  height: 56px;
  background: rgba(150, 215, 210, 0.15);
  border-radius: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.icon-container-dark svg {
  width: 28px;
  height: 28px;
  color: #96D7D2;
}
</style>
```

### Common Icons
```html
<!-- Checkmark -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <polyline points="20 6 9 17 4 12"/>
</svg>

<!-- Arrow Right -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <line x1="5" y1="12" x2="19" y2="12"/>
  <polyline points="12 5 19 12 12 19"/>
</svg>

<!-- Chat/Message -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>
</svg>

<!-- Lock/Security -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
  <path d="M7 11V7a5 5 0 0 1 10 0v4"/>
</svg>

<!-- Database -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <ellipse cx="12" cy="5" rx="9" ry="3"/>
  <path d="M21 12c0 1.66-4 3-9 3s-9-1.34-9-3"/>
  <path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/>
</svg>

<!-- Chart/Analytics -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <line x1="18" y1="20" x2="18" y2="10"/>
  <line x1="12" y1="20" x2="12" y2="4"/>
  <line x1="6" y1="20" x2="6" y2="14"/>
</svg>

<!-- Settings/Gear -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <circle cx="12" cy="12" r="3"/>
  <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"/>
</svg>

<!-- Play -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <polygon points="5 3 19 12 5 21 5 3"/>
</svg>

<!-- Clock -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <circle cx="12" cy="12" r="10"/>
  <polyline points="12 6 12 12 16 14"/>
</svg>

<!-- Users -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/>
  <circle cx="9" cy="7" r="4"/>
  <path d="M23 21v-2a4 4 0 0 0-3-3.87"/>
  <path d="M16 3.13a4 4 0 0 1 0 7.75"/>
</svg>

<!-- X/Close -->
<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
  <line x1="18" y1="6" x2="6" y2="18"/>
  <line x1="6" y1="6" x2="18" y2="18"/>
</svg>
```

---

## Lists

### Bullet List
```html
<ul class="list-bullet">
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ul>

<style>
.list-bullet {
  list-style: none;
}

.list-bullet li {
  position: relative;
  padding-left: 24px;
  font-size: 18px;
  color: rgba(26,28,33,0.7);
  line-height: 1.6;
  margin-bottom: 12px;
}

.list-bullet li::before {
  content: '';
  position: absolute;
  left: 0;
  top: 10px;
  width: 6px;
  height: 6px;
  background: #4469fc;
  border-radius: 50%;
}
</style>
```

### Check List
```html
<ul class="list-check">
  <li>
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
      <polyline points="20 6 9 17 4 12"/>
    </svg>
    <span>Completed item</span>
  </li>
</ul>

<style>
.list-check {
  list-style: none;
}

.list-check li {
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 18px;
  color: #1a1c21;
  margin-bottom: 16px;
}

.list-check svg {
  width: 20px;
  height: 20px;
  color: #4469fc;
  flex-shrink: 0;
}
</style>
```

### Numbered List
```html
<ol class="list-numbered">
  <li>First step</li>
  <li>Second step</li>
  <li>Third step</li>
</ol>

<style>
.list-numbered {
  list-style: none;
  counter-reset: item;
}

.list-numbered li {
  counter-increment: item;
  display: flex;
  align-items: flex-start;
  gap: 16px;
  font-size: 18px;
  color: rgba(26,28,33,0.7);
  margin-bottom: 20px;
}

.list-numbered li::before {
  content: counter(item);
  width: 32px;
  height: 32px;
  background: rgba(68, 105, 252, 0.1);
  color: #4469fc;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  font-weight: 600;
  flex-shrink: 0;
}
</style>
```

---

## Typography

### Heading Utilities
```html
<h1 class="h1">Headline 1</h1>
<h2 class="h2">Headline 2</h2>
<h3 class="h3">Headline 3</h3>
<p class="body">Body text</p>
<p class="body-sm">Small body text</p>

<style>
.h1 {
  font-size: 56px;
  font-weight: 600;
  letter-spacing: -1.12px;
  line-height: 1.1;
  color: #1a1c21;
}

.h2 {
  font-size: 40px;
  font-weight: 600;
  letter-spacing: -0.8px;
  line-height: 1.2;
  color: #1a1c21;
}

.h3 {
  font-size: 28px;
  font-weight: 600;
  letter-spacing: -0.56px;
  line-height: 1.3;
  color: #1a1c21;
}

.body {
  font-size: 18px;
  font-weight: 400;
  line-height: 1.6;
  color: rgba(26,28,33,0.55);
}

.body-sm {
  font-size: 16px;
  font-weight: 400;
  line-height: 1.5;
  color: rgba(26,28,33,0.55);
}

/* Light variants for dark backgrounds */
.h1-light { color: #FFFFFF; }
.h2-light { color: #FFFFFF; }
.h3-light { color: #FFFFFF; }
.body-light { color: rgba(255,255,255,0.7); }
</style>
```

### Text Highlight
```html
<span class="highlight">highlighted text</span>
<span class="highlight-teal">teal highlight</span>

<style>
.highlight {
  background: linear-gradient(180deg, transparent 60%, rgba(68, 105, 252, 0.2) 60%);
  padding: 0 4px;
}

.highlight-teal {
  background: rgba(150, 215, 210, 0.2);
  color: #96D7D2;
  padding: 2px 8px;
  border-radius: 4px;
}
</style>
```

---

## Callouts

### Info Callout
```html
<div class="callout callout-info">
  <div class="callout-icon">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
      <circle cx="12" cy="12" r="10"/>
      <line x1="12" y1="16" x2="12" y2="12"/>
      <line x1="12" y1="8" x2="12.01" y2="8"/>
    </svg>
  </div>
  <div class="callout-content">
    <div class="callout-title">Note</div>
    <div class="callout-text">This is important information.</div>
  </div>
</div>

<style>
.callout {
  display: flex;
  gap: 16px;
  padding: 20px 24px;
  border-radius: 12px;
}

.callout-info {
  background: rgba(68, 105, 252, 0.08);
  border-left: 3px solid #4469fc;
}

.callout-icon svg {
  width: 24px;
  height: 24px;
  color: #4469fc;
}

.callout-title {
  font-size: 16px;
  font-weight: 600;
  color: #1a1c21;
  margin-bottom: 4px;
}

.callout-text {
  font-size: 15px;
  color: rgba(26,28,33,0.7);
  line-height: 1.5;
}
</style>
```

### Tip Callout
```html
<div class="callout callout-tip">
  <!-- same structure -->
</div>

<style>
.callout-tip {
  background: rgba(150, 215, 210, 0.1);
  border-left: 3px solid #96D7D2;
}

.callout-tip .callout-icon svg {
  color: #5ba8a3;
}
</style>
```

### Warning Callout
```html
<div class="callout callout-warning">
  <!-- same structure -->
</div>

<style>
.callout-warning {
  background: rgba(234, 179, 8, 0.1);
  border-left: 3px solid #eab308;
}

.callout-warning .callout-icon svg {
  color: #ca8a04;
}
</style>
```

---

## Progress & Steps

### Step Indicator
```html
<div class="step-indicator">
  <div class="step active">
    <div class="step-number">1</div>
    <div class="step-label">Setup</div>
  </div>
  <div class="step-line"></div>
  <div class="step">
    <div class="step-number">2</div>
    <div class="step-label">Configure</div>
  </div>
  <div class="step-line"></div>
  <div class="step">
    <div class="step-number">3</div>
    <div class="step-label">Launch</div>
  </div>
</div>

<style>
.step-indicator {
  display: flex;
  align-items: center;
  gap: 0;
}

.step {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}

.step-number {
  width: 40px;
  height: 40px;
  background: #ECECF4;
  color: rgba(26,28,33,0.4);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 16px;
  font-weight: 600;
}

.step.active .step-number {
  background: #4469fc;
  color: #FFFFFF;
}

.step-label {
  font-size: 14px;
  font-weight: 500;
  color: rgba(26,28,33,0.55);
}

.step.active .step-label {
  color: #1a1c21;
}

.step-line {
  width: 60px;
  height: 2px;
  background: #ECECF4;
  margin: 0 8px;
  margin-bottom: 24px;
}
</style>
```

### Progress Bar
```html
<div class="progress-bar">
  <div class="progress-fill" style="width: 65%"></div>
</div>

<style>
.progress-bar {
  width: 100%;
  height: 8px;
  background: #ECECF4;
  border-radius: 100px;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background: #4469fc;
  border-radius: 100px;
}
</style>
```

---

## Logo Placement

### Standard Logo (Light Background)
```html
<img class="logo" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">

<style>
.logo {
  position: absolute;
  bottom: 64px;
  left: 64px;
  height: 24px;
  width: auto;
}
</style>
```

### Logo (Dark Background)
```html
<img class="logo logo-light" src="https://raw.githubusercontent.com/niklasmeixner-langdock/langdock-slides/main/assets/langdock-logo.png" alt="Langdock">

<style>
.logo-light {
  filter: brightness(0) invert(1);
}
</style>
```

### Logo Positions
```css
/* Bottom left (default) */
.logo { bottom: 64px; left: 64px; }

/* Bottom right */
.logo-right { bottom: 64px; right: 64px; left: auto; }

/* Top left */
.logo-top { top: 64px; left: 64px; bottom: auto; }

/* Top right */
.logo-top-right { top: 64px; right: 64px; bottom: auto; left: auto; }
```

---

## Decorative Elements

### Accent Circle (Blur)
```html
<div class="accent-circle"></div>

<style>
.accent-circle {
  position: absolute;
  width: 500px;
  height: 500px;
  border-radius: 50%;
  background: rgba(150, 215, 210, 0.15);
  filter: blur(100px);
}

/* Positioning variants */
.accent-top-right {
  top: -200px;
  right: -100px;
}

.accent-bottom-left {
  bottom: -200px;
  left: -100px;
}
</style>
```

### Decorative Grid
```html
<div class="deco-grid"></div>

<style>
.deco-grid {
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(rgba(68, 105, 252, 0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(68, 105, 252, 0.03) 1px, transparent 1px);
  background-size: 40px 40px;
  pointer-events: none;
}
</style>
```

### Browser Chrome Mockup
```html
<div class="browser-chrome">
  <div class="browser-dots">
    <div class="browser-dot"></div>
    <div class="browser-dot"></div>
    <div class="browser-dot"></div>
  </div>
</div>

<style>
.browser-chrome {
  background: #ECECF4;
  padding: 12px 16px;
  display: flex;
  align-items: center;
  gap: 8px;
  border-radius: 12px 12px 0 0;
}

.browser-dots {
  display: flex;
  gap: 6px;
}

.browser-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: rgba(26,28,33,0.15);
}
</style>
```

### Divider Line
```html
<div class="divider"></div>
<div class="divider-vertical"></div>

<style>
.divider {
  width: 100%;
  height: 1px;
  background: #ECECF4;
}

.divider-vertical {
  width: 1px;
  height: 100%;
  background: #ECECF4;
}

/* Dark variant */
.divider-dark {
  background: rgba(255,255,255,0.1);
}
</style>
```

---

## Usage Guidelines

1. **Consistency**: Always use components from this library rather than creating custom one-off styles
2. **Color Mode**: Match components to slide background (light/dark variants)
3. **Spacing**: Maintain 64px margins and 24-32px gaps between elements
4. **Typography**: Use the heading hierarchy consistently
5. **Icons**: Use stroke-based SVG icons at 2px stroke width
6. **Shadows**: Use subtle shadows only on light backgrounds

## Component Combinations

### Feature Card with Icon and Tags
```html
<div class="card">
  <div class="icon-container">
    <svg><!-- icon --></svg>
  </div>
  <h3 class="card-title">Feature Name</h3>
  <p class="card-text">Feature description.</p>
  <div class="tag-group">
    <span class="tag-pill">Tag 1</span>
    <span class="tag-pill">Tag 2</span>
  </div>
</div>
```

### CTA Section
```html
<div class="cta-section">
  <h2 class="h2">Ready to get started?</h2>
  <p class="body">Start your free trial today.</p>
  <div class="btn-group">
    <a href="#" class="btn-primary">Start Free Trial</a>
    <a href="#" class="btn-secondary">Learn More</a>
  </div>
</div>
```
