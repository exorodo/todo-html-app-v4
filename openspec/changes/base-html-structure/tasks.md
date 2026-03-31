## 1. HTML Document Shell

- [x] 1.1 Create `index.html` with `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<body>` tags
- [x] 1.2 Add `<meta charset="UTF-8">` and `<meta name="viewport" content="width=device-width, initial-scale=1.0">` to `<head>`
- [x] 1.3 Add `<title>Todo App</title>` to `<head>`
- [x] 1.4 Add empty `<style></style>` block in `<head>` and empty `<script></script>` block at end of `<body>`

## 2. Semantic Body Structure

- [x] 2.1 Add `<main class="app">` as the single child of `<body>` (before `<script>`)
- [x] 2.2 Add `<h1>todos</h1>` as the first child of `<main>`
- [x] 2.3 Add `<section class="input-area">` after the `<h1>`
- [x] 2.4 Add `<input type="text" id="new-todo" placeholder="What needs to be done?" aria-label="New todo">` inside `.input-area`
- [x] 2.5 Add `<button id="add-btn" aria-label="Add todo">Add</button>` inside `.input-area` after the input
- [x] 2.6 Add `<section class="todo-list-area" aria-label="Todo list">` after `.input-area`
- [x] 2.7 Add `<ul id="todo-list" role="list"></ul>` inside `.todo-list-area`
- [x] 2.8 Add `<footer class="app-footer" hidden></footer>` after `.todo-list-area`, inside `<main>`

## 3. CSS Reset and Base Styles

- [x] 3.1 Add box-sizing reset: `*, *::before, *::after { box-sizing: border-box; }`
- [x] 3.2 Add body reset: `body { margin: 0; padding: 0; font-family: system-ui, sans-serif; font-size: 16px; background: #f5f5f5; color: #333; }`
- [x] 3.3 Add `.app` styles: `max-width: 480px; margin: 48px auto; background: #fff; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); overflow: hidden;`
- [x] 3.4 Add `h1` styles: `text-align: center; font-size: 2.5rem; font-weight: 300; color: #5c6bc0; padding: 24px 0 16px;`

## 4. Input Area CSS

- [x] 4.1 Add `.input-area` styles: `display: flex; gap: 8px; padding: 0 16px 16px;`
- [x] 4.2 Add `#new-todo` styles: `flex: 1; padding: 10px 12px; border: 1px solid #e0e0e0; border-radius: 4px; font-size: 1rem; outline: none;`
- [x] 4.3 Add `#new-todo:focus` styles: `border-color: #5c6bc0; box-shadow: 0 0 0 2px rgba(92,107,192,0.2);`
- [x] 4.4 Add `#add-btn` styles: `padding: 10px 18px; background: #5c6bc0; color: #fff; border: none; border-radius: 4px; font-size: 1rem; cursor: pointer;`
- [x] 4.5 Add `#add-btn:hover` styles: `background: #3f51b5;`
- [x] 4.6 Add `#add-btn:focus-visible` styles: `outline: 2px solid #5c6bc0; outline-offset: 2px;`

## 5. List and Footer CSS

- [x] 5.1 Add `#todo-list` styles: `list-style: none; margin: 0; padding: 0;`
- [x] 5.2 Add `.app-footer` styles: `padding: 10px 16px; font-size: 0.85rem; color: #888; border-top: 1px solid #e0e0e0; display: flex; justify-content: space-between; align-items: center;`

## 6. Verification

- [ ] 6.1 Open `index.html` in a browser — confirm no console errors and title reads "Todo App"
- [ ] 6.2 Verify heading "todos", input field with placeholder, and Add button are visible
- [ ] 6.3 Tab through the page — confirm input then button receive focus with visible rings
- [ ] 6.4 Resize to 320px wide — confirm no horizontal scroll and elements remain usable
- [ ] 6.5 Inspect DOM — confirm `<ul id="todo-list">` is empty and `<footer>` has `hidden` attribute
