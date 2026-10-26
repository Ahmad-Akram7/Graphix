# Graphix test checklist

Use this checklist when reviewing a change or preparing a release. These are test cases to run, not claims that every case has already passed.

## 1. Open and explore

- [ ] Open `index.html` in a current desktop browser.
- [ ] Confirm the demo chart, summary metrics, chart controls, and table preview appear.
- [ ] Switch between Bar, Line, and Scatter; confirm the selected view changes.
- [ ] Change the category field, value field, chart title, and sort order; confirm the chart updates.
- [ ] Search the table and confirm the visible rows and count change.
- [ ] Reload the demo dataset and confirm the default view returns.

## 2. Import files

- [ ] Import a CSV with a header row.
- [ ] Test quoted commas, escaped quotes, and CRLF line endings.
- [ ] Import a JSON array of objects.
- [ ] Cancel the file picker and confirm the current dataset stays loaded.
- [ ] Test malformed JSON, an unclosed CSV quote, an unsupported extension, and an empty file.
- [ ] Test a file larger than 15 MB and a dataset larger than 100,000 rows.
- [ ] Include blank cells and mixed numeric/text values; confirm the chart handles them without crashing.

## 3. Export files

- [ ] Export the dataset as CSV, then reopen it in a spreadsheet and check headers, commas, quotes, and newlines.
- [ ] Export the chart as SVG and open it in a browser.
- [ ] Export the chart as PNG and confirm the image contains the chart.

## 4. Check accessibility and layout

- [ ] Navigate controls with the keyboard and confirm focus remains visible.
- [ ] Check that the file input, search field, and selection controls have usable labels.
- [ ] Test a narrow viewport around 320 px and browser zoom at 200%.
- [ ] Enable the operating system's reduced-motion preference and check the interface remains usable.

## 5. Keep the limits in mind

- Chart rendering is capped at 250 records; the table preview is capped at 500 rows.
- The scatter-style chart plots a selected value against record order. It does not accept separate X and Y numeric fields yet.
- These checks are manual. Do not describe the app as browser-tested or screen-reader-tested until those tests have been run and recorded.
