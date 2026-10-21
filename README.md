# PDF Editor

A single-page PDF editor that runs entirely in your browser: add **text, symbols, images and a hand-drawn
signature** to any PDF, then download the edited file. Nothing is uploaded anywhere.

🇮🇹 **Versione italiana:** [it/README.md](it/README.md)

**Use it online:** <https://fabiofctrl.github.io/pdf-editor/>
(Italian interface: <https://fabiofctrl.github.io/pdf-editor/?lang=it>)

## Features

- **Text**: click anywhere on a page and type. Font (Arial, Helvetica, Times New Roman, Courier New, Georgia,
  Verdana, Trebuchet MS), size, bold, italic, underline, UPPER/lower case, colour.
- **Signature**: draw it with the mouse or a finger, then click where to place it.
- **Symbols**: ✓ ✗ ○ ● □ ■ ◆ △ → ★ and more, in the selected colour.
- **Images**: insert any image (PNG, JPG, …).
- Every item can be **moved**, **resized**, **rotated** and **removed** (hover over it to see the handles).
- **Download** saves a new PDF named `<original>_edited.pdf`.
- English and Italian interface: chosen from the browser language, or forced with `?lang=en` / `?lang=it`.

## Privacy

The PDF is read and written by JavaScript inside your browser tab. It is never sent to a server; GitHub Pages
only serves the page itself. The libraries are loaded from public CDNs (see below), so an internet connection is
needed to open the page.

## Run it locally

Download `index.html` and open it in a browser (Chrome, Edge, Firefox). No installation or build step.

## Libraries

| Library | Version | Used for | License |
|---|---|---|---|
| [PDF.js](https://mozilla.github.io/pdf.js/) | 3.11.174 | rendering the pages | Apache-2.0 |
| [pdf-lib](https://pdf-lib.js.org/) | 1.17.1 | writing the edited PDF | MIT |
| [Tabler Icons](https://tabler.io/icons) | 2.47.0 (webfont) | toolbar icons | MIT |

## Known limitations

- Text is written with the 14 standard PDF fonts, which only cover Western European characters
  (Windows-1252). Characters outside that set (e.g. emoji, Greek, Cyrillic, ✓ typed as text) cannot be saved as
  text: use the **Symbol** tool for marks like ✓.
- Fonts other than Times/Georgia and Courier are saved as Helvetica; underline is shown while editing but is not
  written to the PDF.
- Added items are drawn on top of the page; existing PDF text cannot be edited or removed.
- Mouse and single-finger touch only for drawing; dragging and resizing need a mouse.

## License

MIT — see [LICENSE](LICENSE).
