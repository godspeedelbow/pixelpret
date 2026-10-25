# Mobile layout checks

Use the browser viewport capability to test actual CSS viewport sizes, including reduced heights representing visible iPhone browser toolbars. A narrow desktop side panel alone is insufficient.

Test sizes: 320×568, 375×540, 375×600, 390×620, 430×740, 768×850.

At every size, inspect the rendered DOM bounds and confirm:

- The title and download controls fit inside the board panel.
- The keyring ends above the first bead.
- Undo, redo and reset fit inside the board panel.
- All colors and drawing tools fit inside the palette.
- The gallery fits within the viewport.
- The document has no horizontal overflow.

Also inspect a screenshot at 375×600 and test title editing, switching designs, and reload persistence. Reset the browser viewport override after testing.

The board uses a size container for the drawing area, so bead dimensions follow remaining panel space rather than a fixed viewport subtraction. Phone browser viewport resizing is handled by `100dvh`.

Viewport testing does not emulate all iOS Safari behavior. Physical iPhone checks remain useful for keyboard, touch gestures and browser-toolbar transitions.
