# Falcon Way Improvements Bulletin

This is a static GitHub Pages bulletin. The layout lives in `index.html`; the editable bulletin content lives in `content.csv`.

## Update The Bulletin

Edit `content.csv` as a table. Each visible row becomes part of the public page.

Columns:

- `section`: use `hero`, `meta`, `status`, `update`, `overview`, `expect`, `contact`, or `note`
- `order`: display order within that section
- `label`: small label text, or `urgent` for an urgent contact card
- `date`: date shown for update rows
- `heading`: headline or card title
- `body`: paragraph text
- `button_label`: contact button or link label
- `button_url`: optional `mailto:`, `tel:`, `https://`, or page anchor link
- `visible`: use `yes` to show the row, or `no` to hide it

## Google Sheets Workflow

For a non-coder, the safest workflow is to keep the same columns in a Google Sheet named `Bulletin`.

1. Open Google Sheets and create a sheet with the same columns as `content.csv`.
2. Copy the current `content.csv` rows into the sheet.
3. Edit rows in Google Sheets as normal.
4. Export or publish the sheet as CSV when the public page should be updated.
5. Replace `content.csv` with the exported CSV.

For a fully live Google Sheets connection, publish the Google Sheet to the web as CSV and update `CONTENT_URL` in `index.html` one time.
