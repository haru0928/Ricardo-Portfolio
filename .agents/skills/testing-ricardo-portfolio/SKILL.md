---
name: testing-ricardo-portfolio
description: Test the Ricardo Portfolio desktop, résumé, print, and responsive mobile flows end-to-end.
---

# Testing Ricardo Portfolio

## Devin Secrets Needed

None.

## Start the site

From the repository root:

```bash
python3 -m http.server 8000
```

Open `http://127.0.0.1:8000/index.html` in the existing Chrome session.

## Core desktop flow

1. Confirm the hero, live Pacific clock, uptime value, and three metrics render without placeholders.
2. Use the sticky section navigation and verify each click lands on the matching heading.
3. Open `resume.html` through the visible Résumé control.
4. Verify current education details and confirm required web fonts with `document.fonts.check` at their actual weights.
5. Open and cancel the browser print preview.
6. Use `Back to Portfolio` and confirm the live hero returns.

## Mobile flow

Test at a 390 × 844 viewport. If Playwright is unavailable, attach to Chrome's CDP endpoint at `http://127.0.0.1:29229` and call `Emulation.setDeviceMetricsOverride`.

1. Confirm desktop navigation is hidden and the hamburger control is visible.
2. Open the navigation dialog and verify every section, résumé, and contact destination is present.
3. Follow a section link and confirm the dialog closes at the correct heading.
4. Reopen and close the dialog, then scroll to verify body scrolling was restored.

## Useful checks

```bash
npx --yes html-validate@9.7.1 index.html resume.html
```

For CSS font imports inside `<style>`, use raw `&` query separators rather than HTML-escaped `&amp;`.
