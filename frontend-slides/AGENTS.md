# AGENTS Instructions for `/frontend-slides`

Scope: These instructions apply to all files under this directory tree.

## Default behavior for presentation tasks

When a user asks for slides, decks, or presentation output in this repo:

1. Prefer this `frontend-slides` workflow first.
2. Default to **single-file HTML** output.
3. Keep **CSS inline** in a `<style>` block.
4. Keep **JavaScript inline** in a `<script>` block.
5. Avoid external dependencies unless explicitly requested.
6. Use fullscreen slides with `100vh`/`100dvh` and no page-level scrolling between sections.
7. Avoid internal scrolling inside slide content regions.
8. If content is too long, split it into continuation slides instead of allowing overflow.
9. Prioritize a distinctive visual identity (non-generic look and feel).

## Reuse flow

- Prefer `skills/frontend-slides/template.html` as a starting point.
- Follow `skills/frontend-slides/SKILL.md` workflow: outline → structure → final HTML.
- Keep decks easy to edit by centralizing content in a simple outline object.
