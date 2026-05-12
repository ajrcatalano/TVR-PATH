# TVR PATH — Personalized Approach to Traditional Holistics

An interactive, accessible web diagram presenting the 27 elements of the TVR PATH framework. Originally designed as a Prezi presentation, this page recreates the visual as a fully self-contained HTML file suitable for embedding in WordPress or hosting as a standalone site.

---

## What It Does

The page displays 27 elements arranged in a circle around a central animated bonfire. Each element is rendered as a wooden log. Users can:

- **Hover** over a log to preview its name and definition in the center of the circle
- **Click or tap** a log to:
  - Lock its definition in the center of the circle
  - Fade out all unrelated elements, leaving only the clicked element and its related elements visible
  - Filter the reference list below the circle to show only the clicked element and its related elements, with all definitions expanded
- **Click a related element** to pivot to its definition and relationships
- **Press ↺ Reset or Escape** to restore the full circle and list

---

## Files

| File | Description |
|---|---|
| `tvr-path.html` | The complete self-contained page (HTML, CSS, and JavaScript in one file) |
| `README.md` | This file |

No build tools, dependencies, frameworks, or external assets are required. The flame animation and all graphics are rendered with inline SVG.

---

## Accessibility

This page is built to conform with **WCAG 2.0 Level AAA** standards, including:

- All text/background combinations meet the **7:1 contrast ratio** minimum
- Full **keyboard navigation** — every log is reachable and activatable via Tab and Enter/Space
- **Screen reader support** — descriptive `aria-label` on the diagram, `aria-live` region announces definitions on selection, focus is managed correctly
- **Skip link** to bypass the diagram and jump directly to the reference list
- **Responsive layout** — the circle diagram is preserved on all screen sizes; on small phones the diagram is scrollable and a minimum size is enforced
- **Touch support** — tap targets meet the 44px minimum recommended by Apple and Google; the diagram supports pan/scroll gestures

---

## Browser Compatibility

Tested and compatible with:

- Chrome / Edge (desktop and Android)
- Safari (desktop and iOS)
- Firefox (desktop and Android)

No polyfills or special configuration required.

---

## Notes for Reviewers

- **Relationships:** Each element is linked to a specific set of related elements. Clicking a log shows only that element and its connections. These relationships are defined in the JavaScript `topicData` array near the top of the script section in `tvr-path.html`
- **Editing content:** To update a definition or element name, search for the element's `label` property in the script and edit the corresponding `def` or `related` fields
- **Flame animation:** The central bonfire uses CSS keyframe animations. If animation causes distraction or accessibility concerns, it can be disabled by removing the `<style>` block inside the flame SVG

---

*For questions or feedback, please open an issue in this repository.*
