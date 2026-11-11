# Sheetala Pet Industries — website (v2 design)

A single-page, responsive site: `index.html` (no build step, no framework).

## Add the Pixabay photos & videos

The page has 17 media slots (hero video, product, technology, industry and
contact visuals). Until media is downloaded, each slot shows a designed
teal placeholder, so the site is presentable either way.

1. Get a free API key: log in at https://pixabay.com/api/docs/ — your key is shown on that page.
2. From this folder run (Node 18+):

   ```bash
   PIXABAY_KEY=your_key_here node fetch-pixabay.mjs
   ```

This downloads everything into `assets/img` and `assets/video` and writes
`assets/media.js`, which the page picks up automatically. A small "Photos &
videos: Pixabay" credit appears in the footer.

Want a different picture? Edit that slot's search words (`q`) or result
number (`pick`) in `SLOTS` at the top of `fetch-pixabay.mjs`, and run it again.

## Deploy

Upload the whole folder (including `assets/`) to Vercel, Netlify or any static host.

## Editing content

Products, technology tabs, process steps, industries, reasons, clients and the
ticker are short arrays at the top of the `<script>` near the end of `index.html`.
The quote form opens the visitor's email app with the details filled in, addressed to
sheetalapetindustries@gmail.com.
