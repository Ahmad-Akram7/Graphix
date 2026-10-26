# Graphix

**Graphix — Data, made visible.** A responsive, browser-based graph and data visualization studio. The current build is a static site with no framework, backend, account, or runtime dependency.

## Features

- Load a demo dataset or import CSV / JSON files locally.
- Choose bar, line, or scatter visualizations.
- Select category and value fields, sort values, and edit the chart title.
- Search and inspect a tabular data preview.
- Export the chart as SVG or PNG and the dataset as CSV.
- Responsive layout, visible keyboard focus, accessible labels, and reduced-motion support.

## Run locally

Open `index.html` in a modern browser, or serve the project directory with any static file server. No build step or package installation is required.

## Deploy

Compatible with GitHub Pages from the repository root. In GitHub, open **Settings → Pages**, select **Deploy from a branch**, and choose the branch and `/(root)` folder you want to publish.

## Data and privacy

CSV and JSON parsing and chart rendering happen in the browser. Graphix does not upload files to a server. Imports are capped at 15 MB and 100,000 rows; chart rendering is limited to 250 plotted records and the table preview to 500 rows to keep the interface responsive.

## Current limitations

- CSV support covers common comma-separated files with quoted fields; it does not infer delimiter variants or support every spreadsheet dialect.
- Numeric values use JavaScript number conversion; locale-specific decimal formats should be normalized before import.
- The scatter view plots values against record order; it is not yet an XY chart with two numeric fields.
- No persistent workspace, multi-series configuration, or server-side processing is included.

See [manual test checklist](docs/TESTING.md) before publishing changes.
