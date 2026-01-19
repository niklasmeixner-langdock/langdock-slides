# V2-Current Design System

This is the primary, modern brand style guide for Langdock presentations, based on the 2024/2025 website redesign.

---

## Design Tokens

### Colors

```css
/* Brand Palette */
--color-sand: #D8D5CB;                /* Light warm background, cards */
--color-teal-dark: #144C5E;           /* Primary accent, CTAs, icons */
--color-sage: #66716F;                /* Secondary text, muted elements */
--color-charcoal: #505655;            /* Body text on light backgrounds */
--color-peach: #FFDCB9;               /* Highlight, warm accent */
--color-mint: #C6D0CF;                /* Light accent, tags, borders */
--color-dark: #2F2F2F;                /* Primary text, headings */
--color-brown-warm: #4D473C;          /* Warm dark cards, feature sections */

/* Background Colors */
--color-bg-light: #D8D5CB;            /* Page background (sand) */
--color-bg-white: #FFFFFF;            /* Cards, content areas */
--color-bg-elevated: #C6D0CF;         /* Elevated surfaces, tags (mint) */

/* Dark Theme Colors */
--color-dark-warm: #4D473C;           /* Warm dark cards (brown) */
--color-dark-cool: #2F2F2F;           /* Cool dark backgrounds */

/* Text Colors */
--color-text-primary: #2F2F2F;        /* Primary text, headings */
--color-text-secondary: #505655;      /* Body text, descriptions */
--color-text-muted: #66716F;          /* Labels, captions (sage) */
--color-text-on-dark: #FFFFFF;        /* Text on dark backgrounds */
--color-text-on-dark-secondary: rgba(255,255,255,0.75); /* Secondary on dark */

/* Accent Colors */
--color-accent-primary: #144C5E;      /* Primary accent (teal) */
--color-accent-warm: #FFDCB9;         /* Warm accent (peach) */
--color-accent-light: #C6D0CF;        /* Light accent (mint) */

/* Border Colors */
--color-border-light: rgba(47,47,47,0.1);   /* Light borders */
--color-border-dark: rgba(0,0,0,0.1);       /* Subtle borders */
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
/* Primary Button (Teal) */
.button-primary {
  background: #144C5E;
  color: #FFFFFF;
  padding: 12px 24px;
  border-radius: 100px;
  font-size: 16px;
  font-weight: 500;
}

/* Secondary Button (Outline) */
.button-secondary {
  background: transparent;
  border: 1.5px solid #66716F;
  color: #2F2F2F;
  padding: 12px 24px;
  border-radius: 100px;
}

/* Accent Button (Dark) */
.button-accent {
  background: #2F2F2F;
  color: #FFFFFF;
  padding: 12px 24px;
  border-radius: 100px;
}
```

### Tags/Pills

```css
/* Light Tag (Mint) */
.tag-light {
  background: #C6D0CF;
  color: #2F2F2F;
  padding: 8px 16px;
  border-radius: 100px;
  font-size: 16px;
  font-weight: 500;
}

/* Peach Tag */
.tag-peach {
  background: #FFDCB9;
  color: #2F2F2F;
  padding: 8px 16px;
  border-radius: 100px;
}

/* Teal Tag */
.tag-teal {
  background: rgba(20,76,94,0.15);
  color: #144C5E;
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

/* Sand Card */
.card-sand {
  background: #D8D5CB;
  border-radius: 16px;
  padding: 32px;
}

/* Mint Card */
.card-mint {
  background: #C6D0CF;
  border-radius: 16px;
  padding: 32px;
}

/* Dark Card (Warm Brown) */
.card-dark {
  background: #4D473C;
  border-radius: 16px;
  padding: 32px;
  color: #FFFFFF;
}

/* Dark Card (Charcoal) */
.card-charcoal {
  background: #2F2F2F;
  border-radius: 16px;
  padding: 32px;
  color: #FFFFFF;
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
