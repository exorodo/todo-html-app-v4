## ADDED Requirements

### Requirement: Hidden footer element
A `<footer class="app-footer" hidden>` SHALL be present in the DOM inside `<main class="app">`, after the todo list section. It SHALL be invisible on initial load via the HTML `hidden` attribute.

#### Scenario: Footer is not visible on load
- **WHEN** the page has loaded with no todo items
- **THEN** the footer element is not visible to the user
- **AND** it does not take up space in the layout

#### Scenario: Footer exists in DOM for future use
- **WHEN** a developer inspects the DOM
- **THEN** a `<footer class="app-footer">` element is present
- **AND** it has the `hidden` attribute set
