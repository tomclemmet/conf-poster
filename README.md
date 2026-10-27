# HTML academic poster

A plain HTML/CSS academic poster. Edit the HTML/CSS, open it in a browser, and print to PDF.

- [`index.html`](index.html) — a blank template, ready to fill in.
- [`examples/psoriasis/index.html`](examples/psoriasis/index.html) — a finished poster using the same layout, if you'd rather start from a filled-in example and strip it down. 

The template and each example are self-contained, so you can copy whichever one you want to start from.

## Editing content

- Edit text directly in `index.html` (right-click and select 'Open with', then choose a text editor to avoid opening the finished poster in your browser).

- Add images using an `<img src="images/placeholder-figure.svg" alt="Figure">` tag that refers to an image saved in `images/`. Vector image formats such as SVG or PNG work best.

# 

## Formatting and layout

* An AI tool such as Claude is recommended for editing formatting or layouts - these are competely flexible.

* Colours, fonts, and type sizes are CSS variables at the top of `css/style.css` (`--color-primary`, `--fs-body`, etc.) — change those first before touching individual rules.

* The poster is a CSS grid of boxes (banner, intro, motivation, two stacked boxes on the left, two on the right, footer). Section names in the CSS (`.intro`, `.motivation`, `.left-top`, `.right-main`, ...) describe their position/role, not any fixed content — rename headings freely.

* One box (`.left-top` in the template) has an optional QR-code box overlaid in the corner, for linking to a dataset, app, or supplementary material. Delete the `.qr-block` div and the matching `.qr-spacer` div if you don't need it.

* Poster size is set in two places and they must match: `--page-w`/`--page-h` in `style.css`, and the `@page { size: ... }` rule near the bottom of the same file. Defaults to A0 portrait (841mm × 1189mm). 

## Printing to PDF

In your browser's print dialog (Ctrl+P):

1. **Paper size** → Custom, matching the poster size (A0 default: 841 × 1189 mm)
2. **Margins** → None
3. **Scale** → 100% (not "Fit to page")
4. **Background graphics** → on
