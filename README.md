# Falcon Way Improvements Bulletin

This is a static GitHub Pages bulletin. The layout lives in `index.html`; the editable bulletin content lives in `content.csv`.

## Brand Assets

The public page uses `assets/amrize-logo-lockup.jpg`, cropped from the official Amrize logo image in the Amrize media library. Keep `assets/amrize-logo.jpg` as the source download for future refreshes.

## Update The Bulletin

Edit `content.csv` as a table. Each visible row becomes part of the public page.

The easiest non-coder path is to use the helper editor:

1. Open `https://kylepalmer-cyber.github.io/260020.FWI-Bulliten/editor.html`.
2. Edit the rows in the form.
3. Paste the GitHub publish token.
4. Click `Publish to GitHub`.
5. Wait a minute or two for GitHub Pages to refresh.

The editor page does not save the token. It uses the token only when `Publish to GitHub` is clicked.

The token should be a GitHub fine-grained personal access token with these settings:

- Owner: `kylepalmer-cyber`
- Repository access: only `260020.FWI-Bulliten`
- Repository permissions: `Contents` set to `Read and write`
- Expiration: short, such as 30 or 90 days

If direct publishing fails, use the fallback buttons:

1. Click `Copy CSV`.
2. Click `Open GitHub editor`.
3. Select all text in GitHub's `content.csv` editor, paste the copied CSV, and commit.

Columns:

- `section`: use `hero`, `meta`, `status`, `update`, `traffic`, `overview`, `expect`, `contact`, or `note`
- `order`: display order within that section
- `label`: small label text, or `urgent` for an urgent contact card
- `date`: date shown for update rows, or timeline shown for traffic rows
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
