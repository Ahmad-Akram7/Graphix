# Graphix manual test checklist

Run these checks in a current desktop browser and on a narrow mobile viewport before merging.

## Core flow
- [ ] Open `index.html`; the demo chart, three summary metrics, and data preview render.
- [ ] Switch between Bar, Line, and Scatter; the chart changes and the selected control exposes `aria-pressed="true"`.
- [ ] Change X/Y fields, title, and sort order; chart labels and values update.
- [ ] Search for a value in the dataset; the table filters and the row count updates.
- [ ] Load sample dataset; demo rows and default chart return.

## Import and error handling
- [ ] Import a CSV with headers, quoted commas, escaped quotes, and CRLF line endings.
- [ ] Import a JSON array of objects.
- [ ] Cancel file selection; current dataset remains unchanged.
- [ ] Test malformed JSON, unclosed quoted CSV, unsupported extension, empty file, and a file over the documented size cap; show an error without losing the current dataset.
- [ ] Test rows with blank cells and mixed numeric/text values; chart should skip non-numeric values rather than crash.

## Exports
- [ ] Export CSV and reopen it in a spreadsheet; headers, commas, quotes, and newlines remain correctly escaped.
- [ ] Export SVG and open it in a browser.
- [ ] Export PNG and confirm the downloaded image is not blank.

## Accessibility and responsive layout
- [ ] Navigate all controls using Tab and Enter/Space; focus is visible.
- [ ] Check labels for file input, search, and select fields.
- [ ] At 320 px wide and 200% zoom, content remains usable without controls overlapping.
- [ ] Enable reduced motion in the operating system and verify the interface does not rely on animation.

## Known boundaries
- Chart rendering intentionally plots at most 250 rows; the preview displays at most 500.
- Scatter is currently value-versus-record-order, not a two-variable scatter plot.
- This is a manual checklist, not a claim that browser automation or assistive-technology testing has passed.
