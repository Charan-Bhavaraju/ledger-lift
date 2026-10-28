# Ledger Lift: PDF table keyword extractor

Single-file web app for pulling keyword-matched rows (e.g. public-health spending) out of budget PDF tables.

1. Drop one or many PDFs. Tables are found per file, and the Entity (ministry or department) is detected and can be edited.
2. Filter and select tables. Check each table's detected unit (thousands, lakhs or crores).
3. Enter include and exclude keywords.
4. Review matches: untick rows you don't want, check flagged rows, and click a page number to see the row highlighted in the PDF.
5. Build the output: pick and order the columns (row details or any source value column) and rename the headers. Choose a unit to convert to.
   Copy everything, a single column, a row or a cell, or download Excel (one sheet per file plus "All rows") or CSV.

Runs fully in the browser. pdf.js, SheetJS and the fonts load from CDNs, so it needs internet. PDFs are never uploaded.

## Use locally
Double-click `index.html`.

## Deploy (GitHub Pages)
Push `index.html` to a repo → Settings → Pages → Source: `main` / root → open `https://<user>.github.io/<repo>/`.

## Known limits
- No OCR yet: scanned PDFs and regional-script text with broken font encoding are not read. Descriptions use the English text.
- One table per page; columns that appear only on later pages of a multi-page table are dropped.
