# NUB Cover Generator

A fast, single-page web app that generates clean, official-style cover pages for assignments and lab reports at **Northern University Bangladesh (NUB)** — fill a form, see a live A4 preview, and export a print-ready PDF or PNG in seconds.

No installs, no sign-up, no backend.

**Live demo:** [coverpage-xi.vercel.app](https://coverpage-xi.vercel.app/)

---

## Features

- **Live A4 preview** — Every field updates the cover page preview instantly, so you always see exactly what you'll download.
- **Two document modes** — Toggle between **Assignment** and **Lab Report** layouts. Lab Report mode automatically reveals lab-specific fields (lab number, date of experiment) and relabels the topic field.
- **Custom or default logo** — Drag-and-drop (or click-to-upload) your own logo, or fall back to the built-in NUB logo. One click resets to default.
- **True vector PDF export** — Uses the browser's native print engine instead of a screenshot, so the exported PDF has sharp, selectable, searchable text at any zoom level — not a blurry raster image.
- **High-res PNG export** — Renders a crisp 4x-scaled PNG via `html2canvas` for anyone who just needs an image.
- **Print-perfected layout** — Dedicated print stylesheet scales fonts and hides all UI chrome so the exported page matches a real A4 sheet edge-to-edge.
- **Responsive / mobile-friendly** — On smaller screens, the form and preview collapse into a tabbed interface instead of a cramped split view.
- **Zero dependencies to install** — Pure HTML/CSS/JS in a single file; the only external library (`html2canvas`) loads from a CDN.
- **One-click reset** — Clear the whole form back to sensible defaults without a page reload.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Structure | Semantic HTML5 |
| Styling | Vanilla CSS3 (CSS custom properties, CSS Grid/Flexbox, media queries, dedicated `@media print` rules) |
| Logic | Vanilla JavaScript (ES6, no framework) |
| PDF export | Native browser print-to-PDF (`window.print()`) for vector, selectable text |
| Image export | [html2canvas](https://html2canvas.hertzen.com/) (via CDN) |
| Fonts | Google Fonts — *Source Serif 4* (document body) & *Space Grotesk* (UI) |
| Hosting | [Vercel](https://vercel.com/) |

**Why no framework?** The entire tool is one self-contained HTML file — easy to fork, deploy anywhere, and understand top to bottom without a build step.

---

## Getting Started

Visit [coverpage-xi.vercel.app](https://coverpage-xi.vercel.app/) — the app runs entirely in the browser, no setup required.

To run it locally, download `index.html` and open it in any modern browser.

---

## Usage

1. Choose **Assignment** or **Lab Report** from the document type field.
2. Fill in course, recipient (faculty), and submitter (student) details.
3. Optionally upload a custom logo.
4. Watch the preview update live on the right.
5. Click **Download PDF** for a crisp, text-selectable PDF, or **Download PNG** for an image.

---

*Built to save NUB students the hassle of formatting cover pages by hand.*
