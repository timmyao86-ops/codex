---
name: frontend-slides
description: Build reusable, single-file HTML slide decks in this repository with inline CSS/JS, fullscreen sections, no overflow scrolling, and automatic continuation-slide splitting for long content.
---

# Frontend Slides Skill

Use this skill when the user asks for presentation slides, a deck, or visual narrative output in this repository.

## When to use this skill

Use for requests like:

- “Create slides for …”
- “Build a presentation deck in HTML”
- “Generate a reusable slide template”
- “Summarize this into presentation format”

## Output requirements

- Produce one self-contained HTML file.
- Inline CSS only (`<style>`).
- Inline JavaScript only (`<script>`).
- No external dependencies (no CDNs, libraries, fonts, or assets required for rendering).
- Slides must be fullscreen (`100vh` / `100dvh`).
- Prevent internal scrolling in slide bodies.
- When content exceeds available space, split into additional continuation slides.

## Slide design principles

- Distinctive visual system over generic presentation templates.
- Strong contrast, clean hierarchy, and projection-safe typography.
- Consistent compositional frame per slide (header, core content, footer).
- Minimal but intentional motion/interactions.
- Readability before decoration.

## Workflow

1. **Outline**
   - Draft message flow with sections and key points.
   - Label sections by slide intent (title, agenda, detail, long-list).

2. **Slide structure**
   - Convert outline into a structured data model (array/object).
   - Map each section to a known layout pattern.
   - Mark potentially oversized sections for split logic.

3. **Final HTML**
   - Render from structure to slide elements.
   - Apply inline CSS theme and layout primitives.
   - Add navigation and auto-splitting logic in inline JS.

## Validation checklist (before finishing)

- [ ] HTML opens directly in browser with no build step.
- [ ] No external CSS/JS or remote assets required.
- [ ] Slides fill viewport and maintain no-scroll experience.
- [ ] Long content splits into continuation slides.
- [ ] Keyboard and/or button navigation works.
- [ ] Content is easy to edit via a centralized outline structure.
