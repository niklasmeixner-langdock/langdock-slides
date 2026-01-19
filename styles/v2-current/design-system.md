# V2-Current Design System

This is the primary, modern brand style guide for Langdock presentations, based on the 2024/2025 website redesign.

---

## Design Tokens

### Colors

```css
/* Primary Colors */
--color-primary-dark: #1a1c21;        /* Primary text, headings */
--color-primary-blue: #4469fc;        /* Accent, CTAs, links */

/* Background Colors */
--color-bg-light: #F8F8FC;            /* Page background */
--color-bg-elevated: #ECECF4;         /* Elevated surfaces, tags */
--color-bg-white: #FFFFFF;            /* Cards, content areas */

/* Dark Theme Colors */
--color-dark-warm: #4d473c;           /* Warm dark cards (feature cards) */
--color-dark-cool: #1a1c21;           /* Cool dark (text-based dark) */

/* Text Colors */
--color-text-primary: #1a1c21;        /* Primary text */
--color-text-secondary: rgba(26,28,33,0.55);  /* Subtitles, descriptions */
--color-text-muted: rgba(26,28,33,0.3);       /* Labels, captions */
--color-text-on-dark: #FFFFFF;        /* Text on dark backgrounds */
--color-text-on-dark-secondary: rgba(255,255,255,0.75); /* Secondary on dark */

/* Accent Colors */
--color-accent-teal: #96D7D2;         /* Highlight, decorative */
--color-accent-blue-light: rgba(68,105,252,0.1); /* Blue tint backgrounds */

/* Border Colors */
--color-border-light: rgba(26,28,33,0.1);  /* Light borders */
--color-border-dark: rgba(0,0,0,0.1);      /* Subtle borders */
```

### Typography

```css
/* Font Family */
--font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;

/* Headline 1 - Main slide titles */
--h1-size: 56px;
--h1-weight: 600;           /* Semi Bold */
--h1-tracking: -1.12px;     /* -2% */
--h1-line-height: 1.1;

/* Headline 2 - Section titles, card headers */
--h2-size: 40px;
--h2-weight: 600;           /* Semi Bold */
--h2-tracking: -0.8px;      /* -2% */
--h2-line-height: 1.2;

/* Headline 3 - Subsections, feature titles */
--h3-size: 24px;
--h3-weight: 600;           /* Semi Bold */
--h3-tracking: -0.48px;     /* -2% */
--h3-line-height: 1.3;

/* Body - Main content text */
--body-size: 20px;
--body-weight: 400;         /* Regular */
--body-tracking: -0.2px;    /* -1% */
--body-line-height: 1.5;

/* Body Small - Secondary content */
--body-small-size: 18px;
--body-small-weight: 400;
--body-small-tracking: -0.18px;
--body-small-line-height: 1.5;

/* Caption - Labels, tags, small text */
--caption-size: 14px;
--caption-weight: 500;      /* Medium */
--caption-tracking: -0.14px;
--caption-line-height: 1.4;

/* Tag - Pills, badges */
--tag-size: 16px;
--tag-weight: 500;          /* Medium */
--tag-tracking: -0.16px;
--tag-line-height: 1.4;
```

### Layout

```css
/* Canvas */
--canvas-width: 1920px;
--canvas-height: 1080px;

/* Margins */
--margin: 64px;
--margin-small: 32px;

/* Gaps */
--gap-xl: 48px;
--gap-lg: 32px;
--gap-md: 24px;
--gap-sm: 16px;
--gap-xs: 8px;

/* Border Radius */
--radius-xl: 24px;          /* Large cards */
--radius-lg: 16px;          /* Medium cards */
--radius-md: 12px;          /* Small cards, containers */
--radius-sm: 8px;           /* Small elements */
--radius-pill: 100px;       /* Pills, buttons */
```

### Shadows

```css
/* Card Shadow */
--shadow-card: 0px 4px 24px rgba(0, 0, 0, 0.08);

/* Elevated Shadow */
--shadow-elevated: 0px 8px 32px rgba(0, 0, 0, 0.12);

/* Button Shadow (blue) */
--shadow-button-blue: 0px 4px 12px rgba(68, 105, 252, 0.25);
```

---

## Design Principles

### 1. Clean & Minimal
- Generous whitespace
- Limited color palette
- Clear visual hierarchy

### 2. Warm & Approachable
- Warm gray-brown tones for dark elements
- Soft, rounded corners
- Friendly typography

### 3. Professional & Trustworthy
- Consistent spacing
- Balanced layouts
- Enterprise-ready aesthetic

### 4. Glassmorphism Accents
- Subtle backdrop blur effects
- Semi-transparent overlays
- Depth through layering

---

## Component Styles

### Buttons

```css
/* Primary Button (Dark) */
.button-primary {
  background: #1a1c21;
  color: #FFFFFF;
  padding: 12px 24px;
  border-radius: 100px;
  font-size: 16px;
  font-weight: 500;
}

/* Secondary Button (Outline) */
.button-secondary {
  background: transparent;
  border: 1.5px solid rgba(26,28,33,0.2);
  color: #1a1c21;
  padding: 12px 24px;
  border-radius: 100px;
}

/* Accent Button (Blue) */
.button-accent {
  background: #4469fc;
  color: #FFFFFF;
  padding: 12px 24px;
  border-radius: 100px;
  box-shadow: 0px 4px 12px rgba(68, 105, 252, 0.25);
}
```

### Tags/Pills

```css
/* Light Tag */
.tag-light {
  background: #ECECF4;
  color: rgba(26,28,33,0.7);
  padding: 8px 16px;
  border-radius: 100px;
  font-size: 16px;
  font-weight: 500;
}

/* Dark Tag */
.tag-dark {
  background: rgba(26,28,33,0.08);
  color: #1a1c21;
  padding: 8px 16px;
  border-radius: 100px;
}

/* Accent Tag */
.tag-accent {
  background: rgba(68,105,252,0.1);
  color: #4469fc;
  padding: 8px 16px;
  border-radius: 100px;
}

/* Tag on Dark Background */
.tag-on-dark {
  background: rgba(255,255,255,0.2);
  color: #FFFFFF;
  padding: 8px 16px;
  border-radius: 100px;
}
```

### Cards

```css
/* White Card */
.card-white {
  background: #FFFFFF;
  border-radius: 16px;
  padding: 32px;
  box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.08);
}

/* Elevated Card */
.card-elevated {
  background: #ECECF4;
  border-radius: 16px;
  padding: 32px;
}

/* Dark Card (Warm) */
.card-dark {
  background: #4d473c;
  border-radius: 16px;
  padding: 32px;
  color: #FFFFFF;
}

/* Glass Card */
.card-glass {
  background: rgba(255,255,255,0.16);
  backdrop-filter: blur(8px);
  border-radius: 16px;
  padding: 32px;
  border: 1px solid rgba(255,255,255,0.2);
}
```

---

## Shared Resources

These resources are shared between style guides:

- **Icons**: `../../shared/assets/tabler-icons/`
- **Integration logos**: `../../shared/assets/integration-icons/`
- **Langdock logo**: `../../shared/assets/langdock-logo.png`
- **Product knowledge**: `../../shared/knowledge/index.md`

---

## Template Catalog

See `templates/` folder for all available slide types:

| # | Template | Use Case |
|---|----------|----------|
| 00 | Base Structure | HTML boilerplate for all slides |
| 01 | Section Divider | Chapter transitions, title slides |
| 02 | Goals/Agenda | Learning objectives, session overview |
| 03 | Comparison Grid | Feature comparisons, option tables |
| 04 | Split + Screenshot | Content with UI visual |
| 05 | Numbered Cards | Step-by-step processes |
| 06 | Exercise (Dark) | Hands-on activities |
| 07 | Comparison Flex | Flexible before/after layouts |
| 08 | Centered Statement | Key quotes, takeaways |
| 09 | Split + Code | Technical examples with code |
| 10 | Customer Logos | Trust indicators, social proof |
| 11 | Platform Overview | Feature highlights |
| 12 | All-in-One Solution | Comprehensive feature display |
| 13 | Network Connection | Connected elements with lines |
| 14 | Annotated Content | Callouts and explanations |

---

## Components

See `components/README.md` for reusable UI patterns.
