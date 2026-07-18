# AGENTS.md - AMIS Clear UI

## Scope

This repository uses the AMIS Clear UI v0.2 design standard by Aviv Matsa - Smart Information Systems.

Before changing any user interface, read:

- `docs/design/AMIS-DESIGN-STANDARD.md`
- `docs/design/amis-tokens.css`

## Design Requirements

- Treat AMIS Clear UI v0.2 as the source of truth for visual design.
- Use Fluent 2 only as conceptual inspiration. Do not copy Microsoft branding, product screens, logos, fonts, or branded assets.
- Preserve a clean, spacious, calm, professional information-system appearance.
- Prefer whitespace and hierarchy over excessive cards, borders, and shadows.
- Do not use gradients, glass effects, decorative illustrations, oversized headings, or heavy animation unless explicitly requested.
- Use the provided design tokens.
- Default theme: `azure`. Support exactly `azure`, `turquoise`, `emerald`, `violet`, `raspberry`, and `sunset`.
- Migrate saved themes: `ocean` to `azure`, `forest` to `emerald`, and `plum` to `violet`.
- Theme names must be displayed only in the current interface language.
- Theme changes must not alter semantic status colors or layout.
- Support Hebrew RTL and English LTR completely.
- Use CSS logical properties where possible.
- Use Arial as the default font unless the repository explicitly documents another licensed font.
- Do not invent or add a logo.
- Do not add Help or Report-a-problem options until working content or destinations are supplied.

## Header Requirements

The application header should include, when relevant:

- application name
- a restrained `BETA` badge while the product is beta
- current date or system date under the application name
- Hebrew/English language selection
- display settings for choosing the six AMIS themes
- an About action

Do not show contextual information such as work month, customer, case, file, or period under the application name in the header. Place contextual information in the workspace, filters, summary cards, or internal screen headings.

Do not add tabs solely to make the application appear multi-page.

## About Dialog

Every beta application must provide an About dialog containing:

- application name
- version number
- version date
- Beta status
- a warning that errors or inaccuracies may occur
- `Aviv Matsa - Smart Information Systems`
- a statement that the system was designed and developed by Aviv Matsa with the assistance of AI tools
- copyright year

## Before Completing A UI Task

1. Verify Hebrew RTL and English LTR.
2. Verify all six themes.
3. Check 390px, 768px, 1280px, and 1440px widths.
4. Confirm that no logo, Help option, or Report-a-problem option was invented.
5. Confirm that new colors and spacing use tokens.
6. Confirm About includes version number and version date.
7. Summarize deviations from the standard.
