## ADDED Requirements

### Requirement: Valid HTML5 document structure
The file `index.html` SHALL be a valid HTML5 document with `<!DOCTYPE html>`, `<html lang="en">`, `<head>` containing charset, viewport meta, and title, and a `<body>` containing a single `<main class="app">` landmark.

#### Scenario: Page loads without errors
- **WHEN** the user opens index.html in a browser
- **THEN** the page renders with no console errors
- **AND** the document title shown in the browser tab is "Todo App"

#### Scenario: Semantic landmark is present
- **WHEN** the page has loaded
- **THEN** a `<main>` element with class `app` is present in the DOM
- **AND** an `<h1>` element with text "todos" is the first visible heading

### Requirement: Responsive viewport configuration
The document SHALL include `<meta name="viewport" content="width=device-width, initial-scale=1.0">` so the layout scales correctly on all screen sizes.

#### Scenario: No horizontal scroll on narrow viewport
- **WHEN** the browser viewport is set to 320px wide
- **THEN** no horizontal scrollbar appears
- **AND** all content remains within the viewport width
