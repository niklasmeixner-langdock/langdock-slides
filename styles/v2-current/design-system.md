# V2-Current Design System

This is the primary, modern brand style guide for Langdock presentations, based on the 2024/2025 website redesign.

---

## Design Tokens

### Colors

```css
/* Background */
--color-bg: #FFFFFF;                  /* Always white for slide backgrounds */

/* Text Colors */
--color-text-primary: #2F2F2F;        /* Primary text, headings */
--color-text-secondary: #505655;      /* Body text, descriptions */
--color-text-muted: #66716F;          /* Labels, captions */
--color-text-on-dark: #FFFFFF;        /* Text on dark accent cards */
--color-text-on-dark-secondary: rgba(255,255,255,0.75);

/* Accent Colors (use flexibly, iterate through these for variety) */
--accent-sand: #D8D5CB;               /* Warm neutral */
--accent-teal: #144C5E;               /* Dark teal */
--accent-sage: #66716F;               /* Muted green-gray */
--accent-charcoal: #505655;           /* Dark gray */
--accent-peach: #FFDCB9;              /* Warm highlight */
--accent-mint: #C6D0CF;               /* Cool light */
--accent-dark: #2F2F2F;               /* Near black */
--accent-brown: #4D473C;              /* Warm dark brown */
```

### How to Use Accent Colors

Accent colors are **flexible** and should be used to create visual variety, similar to the Langdock website:

1. **Feature cards** - Iterate through accents (sand, mint, teal, brown, etc.)
2. **Icon backgrounds** - Use light accents (sand, mint, peach)
3. **Dark cards** - Use teal (#144C5E), brown (#4D473C), or dark (#2F2F2F)
4. **Tags/pills** - Match the card background or use contrasting accent
5. **Highlights** - Peach (#FFDCB9) for warm emphasis

**Example pattern from website:**
- Card 1: Sand background (#D8D5CB)
- Card 2: White with mint elements
- Card 3: Teal dark (#144C5E)
- Card 4: Brown warm (#4D473C)
- Card 5: Mint (#C6D0CF)
- etc.

Mix light and dark cards for visual rhythm. No strict rules - use contextually.

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

### Cards (Accent Backgrounds)

Cards can use any accent color. Common patterns:

```css
/* Light accent cards (dark text) */
.card { background: #D8D5CB; color: #2F2F2F; }  /* Sand */
.card { background: #C6D0CF; color: #2F2F2F; }  /* Mint */
.card { background: #FFDCB9; color: #2F2F2F; }  /* Peach */
.card { background: #FFFFFF; color: #2F2F2F; }  /* White */

/* Dark accent cards (white text) */
.card { background: #144C5E; color: #FFFFFF; }  /* Teal */
.card { background: #4D473C; color: #FFFFFF; }  /* Brown */
.card { background: #2F2F2F; color: #FFFFFF; }  /* Dark */
.card { background: #505655; color: #FFFFFF; }  /* Charcoal */
```

### Tags/Pills

Tags should complement their context:

```css
/* On light backgrounds */
.tag { background: #C6D0CF; color: #2F2F2F; }   /* Mint */
.tag { background: #D8D5CB; color: #2F2F2F; }   /* Sand */

/* On dark backgrounds */
.tag { background: rgba(255,255,255,0.2); color: #FFFFFF; }

/* Accent tags */
.tag { background: #FFDCB9; color: #2F2F2F; }   /* Peach highlight */
```

### Icon Containers

```css
/* On white/light slides */
.icon-box { background: #C6D0CF; }  /* Mint */
.icon-box { background: #D8D5CB; }  /* Sand */

/* On dark cards */
.icon-box { background: rgba(255,255,255,0.15); }
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
