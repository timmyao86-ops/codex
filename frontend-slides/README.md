# Frontend Slides Workflow

This folder contains an in-repo workflow for producing polished presentations as **one self-contained HTML file**.

## What this workflow is

- A reusable approach for future presentation tasks in this repository.
- A single-file slide deck pattern (inline CSS + inline JS, no external dependencies).
- A design-forward fullscreen format using `100vh`/`100dvh` slides with no internal page scrolling.
- An auto-pagination pattern that splits long content into continuation slides instead of overflowing.

## How to edit slide content

1. Open `frontend-slides/index.html`.
2. Find the `outline` JavaScript array near the top of the `<script>` block.
3. Update or add entries (`title`, `agenda`, `content`, `long-list`) to match your presentation.
4. Keep long bullet lists in `long-list` entries so the splitter can paginate them automatically.

### Content model quick guide

- `title`: big opening slide
- `agenda`: ordered list slide
- `content`: card grid or bullet content
- `long-list`: intentionally long section that auto-splits into additional slides

## How to preview the HTML

From the repository root, run one of these:

- `python3 -m http.server 8000` and open `http://localhost:8000/frontend-slides/index.html`
- or just open `frontend-slides/index.html` directly in a browser.

## How to reuse this for future decks

- Start from `frontend-slides/skills/frontend-slides/template.html` for a fresh deck.
- Draft your narrative in `frontend-slides/skills/frontend-slides/example-outline.md` style.
- Paste your outline into the template’s `outline` array.
- Verify:
  - no external JS/CSS,
  - fullscreen slide behavior,
  - long sections split into multiple slides,
  - keyboard navigation still works.
