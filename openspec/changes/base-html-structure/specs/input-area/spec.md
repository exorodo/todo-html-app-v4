## ADDED Requirements

### Requirement: Text input field for new todos
A `<section class="input-area">` SHALL contain a text input (`<input type="text" id="new-todo">`) with placeholder "What needs to be done?" and `aria-label="New todo"`.

#### Scenario: Input is visible and labeled
- **WHEN** the page has loaded
- **THEN** a text input field is visible with placeholder "What needs to be done?"
- **AND** the input has an accessible label (aria-label or associated <label>)

#### Scenario: Input receives keyboard focus
- **WHEN** the user presses Tab from the browser address bar
- **THEN** the text input receives focus
- **AND** a visible focus ring is displayed around the input

### Requirement: Add button adjacent to input
A `<button id="add-btn" aria-label="Add todo">Add</button>` SHALL appear immediately to the right of the input within the same flex row.

#### Scenario: Button is reachable via keyboard
- **WHEN** the input has focus and the user presses Tab
- **THEN** the Add button receives focus
- **AND** a visible focus ring is displayed around the button

### Requirement: Input-button flex layout
The `.input-area` container SHALL use `display: flex` so the input stretches to fill remaining width (`flex: 1`) and the button maintains a fixed width.

#### Scenario: Layout holds at minimum width
- **WHEN** the viewport is 320px wide
- **THEN** the input and button are both visible side by side
- **AND** neither element overflows outside the container
