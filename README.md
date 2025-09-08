# Chrome DevTools Demo

This is a simple demo project to help you practice and learn Chrome DevTools.  
It includes an HTML page with buttons that trigger different behaviors, so you can explore how DevTools panels work.

---

## Files
- **devtools-demo.html** → The demo page to open in Chrome.
- **README.md** → Instructions for using the demo.

---

## How to Use
1. Clone or download this repository.
2. Open `devtools-demo.html` in Google Chrome.
3. Open DevTools:
   - Press `F12`, or
   - Use `Ctrl + Shift + I` (Windows/Linux), or
   - Use `Cmd + Option + I` (Mac).
4. Interact with the page and practice using different DevTools panels.

---

## Features in the Page

### 1. Hover me / click box
- Element: `<div id="box" class="box">`
- Purpose: Practice the **Elements** panel.
- What to try:
  - Inspect the element.
  - Edit its CSS (change background, border).
  - Use the `:hov` tool to force hover styles.
  - Check attached event listeners.

### 2. Run heavy CPU task
- Button: `<button id="cpu">Run heavy CPU task</button>`
- Purpose: Practice the **Performance** panel.
- What it does: Runs a large loop that blocks the browser.
- What to try:
  - Record a Performance profile.
  - Click this button while recording.
  - Stop and inspect the flame chart for the long task.

### 3. Fetch (Network)
- Button: `<button id="fetch">Fetch (Network)</button>`
- Purpose: Practice the **Network** panel.
- What it does: Fetches sample JSON data from an API.
- What to try:
  - Click the button and watch the request in the Network tab.
  - Inspect headers, response, and timing.
  - Apply network throttling (e.g., Slow 3G) and try again.

### 4. Create memory leak
- Button: `<button id="leak">Create memory leak</button>`
- Purpose: Practice the **Memory** panel.
- What it does: Stores growing arrays in memory to simulate a leak.
- What to try:
  - Take a heap snapshot before and after clicking multiple times.
  - Compare snapshots to see retained objects.
  - Record an allocation timeline while creating leaks.

### 5. Set localStorage
- Button: `<button id="store">Set localStorage</button>`
- Purpose: Practice the **Application** panel.
- What it does: Saves a timestamped object into `localStorage`.
- What to try:
  - Open Application → Local Storage.
  - Inspect the `demo` key.
  - Clear storage and click again to see changes.

### 6. Toggle spin animation
- Button: `<button id="animate">Toggle spin animation</button>`
- Purpose: Practice the **Animations** panel.
- What it does: Toggles a spinning CSS animation on the box.
- What to try:
  - Open the Animations panel.
  - Click the button and inspect the animation timeline.
  - Adjust playback speed or scrub frames.

---

## Suggested Practice Order
1. Elements → Inspect and edit the box.
2. Console → Run small scripts like `$0.style.border = "2px solid red"`.
3. Sources → Set a breakpoint in `clickHandler` and click the box.
4. Network → Trigger the Fetch button and inspect the request.
5. Performance → Record while running the heavy CPU task.
6. Memory → Create leaks and analyze snapshots.
7. Application → Store and inspect localStorage values.
8. Animations → Toggle the spin animation and inspect it.

---

## Extra Experiments
- **Coverage**: Run a coverage report to see unused CSS/JS (the `.unused-rule` is never used).
- **Rendering**: Enable "Paint flashing" and hover the box to see repaints.
- **Recorder**: Record a flow (e.g., click Fetch) and replay it.

---
