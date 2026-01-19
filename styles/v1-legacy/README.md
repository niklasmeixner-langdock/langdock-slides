# V1-Legacy Style Guide

This is the original training slide style, preserved for consistency with existing materials.

## Usage

To use this style when creating slides, add `--style=v1-legacy` to your request:

```
/create-slides --style=v1-legacy
[Your slide content]
```

## Design Tokens

### Colors
```css
--background: #f8f8f9;
--background-elevated: #ededee;
--text-primary: #121420;
--text-secondary: #717279;
--accent: #456AFC;
--surface-white: #ffffff;
--surface-dark: #242631;
```

### Typography
```css
/* Inter font */
Headline 1: 64px, 600 weight, -3.2px tracking
Headline 2: 40px, 700 weight, -1.6px tracking
Body: 20px, 500 weight, -0.2px tracking
Small: 18px, 500 weight, -0.36px tracking
```

### Layout
```css
Canvas: 1920 x 1080px
Margins: 64px all sides
```

## Templates

See `templates/` folder for all available slide types:

- 01-goals-agenda.md
- 02-section-divider.md
- 03-capability-grid.md
- 04-split-screenshot.md
- 05-numbered-cards.md
- 07-exercise-dark.md
- 09-comparison.md
- 10-centered-statement.md
- 11-split-code.md
- 12-customer-logos.md
- 13-platform-overview.md
- 14-all-in-one-solution.md
- 15-capability-network.md
- 16-annotated-content.md

## Components

See `components/README.md` for reusable UI patterns.

## Shared Resources

These resources are shared with v2-current:

- **Icons**: `../../shared/assets/tabler-icons/`
- **Integration logos**: `../../shared/assets/integration-icons/`
- **Langdock logo**: `../../shared/assets/langdock-logo.png`
- **Product knowledge**: `../../shared/knowledge/index.md`
