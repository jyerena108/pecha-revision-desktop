# Pecha Revision Tool — desktop

A browser tool for proofreading OCR'd Tibetan *pecha* text against the source
PDF scan. The manuscript folio and the editable OCR text sit side by side (or
stacked), so you fix OCR errors by eye-comparison. Tibetan Unicode throughout;
everything is saved per project and auto-saved.

It's the desktop counterpart to the SwiftUI iPhone app
[pecha-revision-tool-ios](https://github.com/jyerena108/pecha-revision-tool-ios),
and shares the branding of the
[Tibetan Collation Tool](https://github.com/jyerena108/tibetan-collation).

## Features

- **Projects** — create / rename / delete named projects; each remembers its
  PDF, text, split position, layout, zoom, current folio, reading crosshair and
  bookmarks. Auto-saves ~1.2 s after you stop.
- **Two panes** — pecha scan and editable text, with a draggable splitter and a
  toolbar toggle for side-by-side (PDF left, text right) or stacked (PDF above,
  text below).
- **PDF pane** — open a PDF, navigate folios, zoom / fit, and a **reading
  crosshair**: two translucent lines you place on the scan to mark where you're
  reading. Anchored to the manuscript (tracks zoom and scroll).
- **Text pane** — import / paste / export clean `.txt`; font size; Select all;
  Find & Replace (Tibetan Unicode); scroll to top / bottom.
- **Two "where am I" marks** (highlight only — nothing is inserted, so exports
  stay clean):
  - **Bookmarks** (yellow) — permanent, collect as many as you like.
  - **Here** (maroon) — a single "you are here" marker in the text.
  - A jump menu lists both by the word itself; marks track edits.

## Running it

It's a static, client-side site — no build step and no server.

- **Live:** https://jyerena108.github.io/pecha-revision-desktop/
- **Locally:** open `index.html` in a browser, or serve the folder
  (`python3 -m http.server`) and visit the printed URL.

Your projects, scans and text are stored only in your own browser
(IndexedDB) — nothing is uploaded anywhere.

## Libraries

- [PDF.js](https://mozilla.github.io/pdf.js/) renders the folios.
- [Noto Serif Tibetan](https://fonts.google.com/noto/specimen/Noto+Serif+Tibetan)
  for the Tibetan text.
