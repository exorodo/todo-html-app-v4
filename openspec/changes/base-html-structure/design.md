## Context

This is a greenfield single-file HTML app. There is no existing codebase, no build pipeline, and no server. The entire application — markup, styles, and scripts — lives in one `index.html` file. This ticket creates that file with only the static shell; no JavaScript behavior is introduced here.

## Goals / Non-Goals

**Goals:**
- Valid, well-structured HTML5 document with semantic landmarks
- Complete inline CSS covering reset, layout, typography, and color palette
- Empty `<script>` block in place for future feature additions
- Keyboard-accessible input area (visible focus ring, logical tab order)
- Responsive layout down to 320px viewport width

**Non-Goals:**
- Any JavaScript interactivity (handled in TODO4-20 through TODO4-25)
- Dynamic state, localStorage, filtering, or counters
- External CSS files, frameworks, or build tools

## Decisions

**Single file architecture**
All markup, styles, and scripts are inline in `index.html`. No separate `.css` or `.js` files.
- Why: Zero build tooling required; file can be opened directly in a browser with no server.
- Alternative considered: separate files — rejected because it adds complexity for no benefit at this project scale.

**CSS reset via `*, *::before, *::after { box-sizing: border-box }`** plus explicit `margin: 0; padding: 0` on body.
- Why: Prevents unexpected sizing and spacing inconsistencies across browsers without pulling in a full reset library.

**Flexbox for input row layout**
The input + button row uses `display: flex` on the `.input-area` container. Input gets `flex: 1`; button is fixed width.
- Why: Simple, no-grid, works at all viewport sizes without media queries.

**`<footer hidden>` present but invisible**
The footer element is written into the HTML but hidden via the `hidden` attribute. JS in later tickets will remove the attribute to reveal it.
- Why: Keeps future tickets simple — they only need to toggle `hidden` and populate content, not create the element.

**Color palette — neutral minimal**
Background: `#f5f5f5` (page), `#fff` (app card). Text: `#333`. Border: `#e0e0e0`. Accent: `#5c6bc0` (button).
- Why: Clean, readable, does not clash with any future status colors (green for done, red for delete).

## Risks / Trade-offs

- [Risk] Inline styles become harder to maintain as the file grows → Mitigation: keep all styles in one organized `<style>` block with clear section comments.
- [Risk] Omitting a semantic element now may require restructuring later → Mitigation: the enriched spec explicitly defines the full element tree including footer and ARIA roles.
