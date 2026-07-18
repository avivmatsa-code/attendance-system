# AMIS Clear UI - Design Standard v0.2

## Identity

Brand: Aviv Matsa - Smart Information Systems.

AMIS Clear UI defines a clean, calm, professional information-system interface with full Hebrew/English, RTL/LTR, keyboard, and responsive support. Fluent 2 may be used as conceptual inspiration only; do not copy Microsoft branding, screens, logos, fonts, or product assets.

## Core Principles

1. Clarity before visual effect.
2. Prefer spacing and hierarchy over excessive borders and cards.
3. Keep the interface visually quiet: no gradients, glass effects, unnecessary animation, decorative backgrounds, or AI-generated temporary logos.
4. Keep components consistent.
5. Use one primary action per screen or work area.
6. Treat RTL, LTR, contrast, focus, and keyboard navigation as part of the design.
7. Mobile is a tailored layout, not a squeezed desktop.

## Typography

Default font:

```css
font-family: Arial, "Noto Sans Hebrew", sans-serif;
```

Recommended scale:

| Use | Size | Weight |
|---|---:|---:|
| Page title | 28px | 700 |
| Section title | 20px | 700 |
| Panel title | 17px | 700 |
| Body | 16px | 400 |
| Secondary text | 14px | 400-600 |
| Small text | 13px | 400-600 |

## Spacing And Sizing

Use a 4px-based spacing scale:

```text
4, 8, 12, 16, 20, 24, 32, 40, 48, 64
```

Recommended heights:

| Component | Height |
|---|---:|
| Form field | 44px |
| Button | 42-44px |
| Table row | 48-52px |
| Panel header | 52px |
| App header | 68-72px |

## Themes

Every system must support exactly six themes:

- Azure - default / כחול חי
- Turquoise / טורקיז
- Emerald / אזמרגד
- Violet / סגול
- Raspberry / פטל
- Sunset / כתום שקיעה

Theme selection changes only brand/link colors. Semantic colors for success, warning, danger, and info remain unchanged.

Persist the user's choice locally. When upgrading from v0.1, migrate `ocean` to `azure`, `forest` to `emerald`, and `plum` to `violet`. If no valid saved theme exists, use `azure`.

Theme names must be displayed only in the current interface language. Hebrew UI shows only Hebrew theme names. English UI shows only English theme names.

Theme selection should live in display settings, not as permanent header buttons.

## Header

The header may include:

- application name
- restrained BETA badge while the system is beta
- current date or system date under the application name
- Hebrew/English selection
- display settings
- About

The text under the application name must show only current/system date. Do not show contextual information such as work month, customer, case, file, or period in the header subtitle. Place contextual information in the workspace, filters, summary cards, or internal screen headings.

Do not invent a logo. The system name is text-only until a logo is supplied. Do not add Help or Report-a-problem unless real content or destinations exist.

## About Dialog

Every beta system must include an About dialog with:

- application name
- version number
- version date
- Beta status
- a warning that errors or inaccuracies may occur
- credit to Aviv Matsa
- mention of AI assistance
- copyright year

Version display examples:

```text
גרסת מערכת: 1.3.2 · 18 ביולי 2026
System version: 1.3.2 · July 18, 2026
```

Base text:

> This system is in beta. Errors, defects, or inaccurate results may occur. Important information should be checked before relying on it.
>
> The system was designed and developed by Aviv Matsa with the assistance of AI tools.
>
> Aviv Matsa - Smart Information Systems

## Primary Action On Dark Backgrounds

A primary button on a dark header or dark surface must include a visible light border or subtle inner outline, using `--header-primary-button-border` and `--header-primary-button-inner-outline` where possible.

## Direction And Language

Support Hebrew RTL and English LTR. Language switching changes all UI text, `lang`, `dir`, date/time/number formats, month/day names, directional layout and icons when relevant, printed/exported UI text, and theme names.

Use CSS logical properties where possible. Numbers, times, URLs, emails, and code should remain LTR where appropriate.

## Navigation

Single-workspace apps do not need primary navigation or tabs. Tabs are only for related views in the same context. About is a dialog, not a primary tab.

## Cards, Panels, Tables, Buttons

Cards are for independent information units. Prefer spacing, section titles, and subtle dividers over wrapping every area in a card. KPI values may use cards.

Buttons: one primary action per area; secondary actions are neutral; destructive actions are danger but not visually dominant. Do not add icons automatically.

Tables: 48-52px rows, subtle horizontal separation, clear header, subtle hover, alignment by data type, and an intentional mobile layout.

## Responsive Checks

Verify at:

```text
390px, 768px, 1280px, 1440px
```

## Prohibited Without Explicit Decision

No gradients, glassmorphism, heavy shadows, very rounded regular controls, oversized headings, more than one prominent brand color on a screen, random spacing/color values, invented logos, inactive Help/Report actions, unnecessary tabs, or pixel-copying of Microsoft Fluent or another product.
