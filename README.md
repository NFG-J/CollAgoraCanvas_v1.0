# CollAgora Canvas v1.0

CollAgora Canvas is a lightweight, local-first educational canvas tool for students, teachers and innovation teams. It is intended as a small open MVP rather than a full Miro/Mural replacement.

## What v1.0 includes

- Browser-only HTML, CSS and vanilla JavaScript.
- Built-in templates: Blank, Business Model Canvas, Lean Canvas, and Triple Bottom Line Co-creation Canvas.
- Sticky notes with editable text, colour and 1-5 vote score.
- Link/video cards with required short description.
- Image cards with required alt text.
- Drag-and-drop placement on a large canvas.
- Local save/load through `localStorage`.
- Import/export of full projects as JSON.
- Export as structured Markdown grouped by canvas section.
- Export as PNG through `html2canvas`.
- Simple template studio: add sections and export a template JSON.

## Run locally

Open `index.html` in a modern browser.

For PNG export, the page loads `html2canvas` from a CDN. If you need a fully offline version, download the library and change the script reference in `index.html`.

## Suggested Codex task

> Improve CollAgora Canvas v1.0 while keeping it browser-only and local-first. Preserve JSON project compatibility. Add tests for save/load, note creation, voting and Markdown export before adding new features.

## Repository structure

```text
CollAgoraCanvas_v1.0/
  index.html
  styles.css
  app.js
  templates/
    blank.json
    business-model-canvas.json
    lean-canvas.json
    tbl-co-creation.json
  examples/
    example-project.json
  test/
    app.test.js
  docs/
    SPEC.md
  package.json
```

## JSON model

A saved project has this shape:

```json
{
  "projectVersion": "1.0",
  "projectTitle": "Example group workshop",
  "updatedAt": "2026-06-29T00:00:00.000Z",
  "templateId": "lean-canvas",
  "canvas": { "width": 1800, "height": 1100 },
  "sections": [],
  "items": []
}
```

Item types:

- `sticky-note`
- `link-card`
- `image-card`

## Recommended next steps after v1.0

1. Resizable notes and template sections.
2. Undo/redo history.
3. Fully offline PNG export library.
4. PDF export.
5. Optional lightweight server for shared workshops.
6. AI prompt helpers based on Markdown/JSON export.

## License

MIT. Adapt as needed for your course or project context.
