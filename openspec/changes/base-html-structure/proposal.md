## Why

The project has no source files yet. Before any interactive feature can be built, we need a valid, accessible HTML shell that defines the page structure, visual layout, and CSS foundation that all subsequent tickets will extend.

## What Changes

- **New file**: `index.html` at project root
- Semantic HTML skeleton with `<main>`, `<section>`, `<ul>`, and `<footer>` landmarks
- Inline `<style>` block with full CSS (reset, layout, typography, color palette)
- Empty `<script>` block reserved for future feature tickets
- No JavaScript logic introduced in this ticket

## Capabilities

### New Capabilities
- `page-shell`: The foundational HTML document structure — doctype, head metadata, viewport, title, and body layout container
- `input-area`: The text input field and Add button section for entering new todos
- `todo-list-container`: The empty `<ul>` that will hold todo items in subsequent tickets
- `app-footer`: A hidden footer element reserved for item count and filter controls (populated in later tickets)

### Modified Capabilities
<!-- none — this is the initial scaffold -->

## Impact

- Creates `index.html` (only file affected)
- No JavaScript, no dependencies, no APIs
- All future feature tickets (TODO4-20 through TODO4-25) build directly on top of this file
