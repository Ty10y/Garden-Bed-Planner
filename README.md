# Garden Bed Planner

A browser-based tool for graphically designing and planning raised garden beds. Drag, size, and label plants on an interactive canvas with a real-scale 4″ grid system. Save your designs to JSON, export as PNG, or print a full layout with a plant legend.

**Live app:** https://ty10y.github.io/Garden-Bed-Planner/

---

## How to Use

1. **Open the app** — visit the live link above, or open `index.html` locally in any modern browser.
2. **Set plant size** — use the radius slider (1–18 inches) to choose a size; a live preview circle updates as you drag.
3. **Pick a color** — select from the 48-color palette.
4. **Place a plant** — click anywhere on the soil canvas to drop a plant at the current size and color. Click and drag to size the plant interactively before releasing.
5. **Label or recolor a plant** — switch to **Label/Edit** mode, then click any plant to open the edit dialog.
6. **Delete a plant** — switch to **Delete** mode and click a plant, or hold **Ctrl** while in any mode to temporarily enter delete mode.
7. **Add more beds** — click the **+** tab to create a new bed. Beds can be renamed and deleted independently.
8. **Undo/Redo** — use **Ctrl+Z** / **Ctrl+Y**, or the toolbar buttons.
9. **Zoom** — use the zoom buttons, the zoom-reset button, or scroll the mousewheel over the canvas.
10. **Save your design** — click **Save to File** to download a `garden_layout.json` file. Load it back with **Load from File**.
11. **Export or print** — click **Export PNG** to download the current bed as an image, or **Print** to get a formatted layout of all beds with a plant legend.

---

## Features

### Multi-Bed Management
- Create and manage unlimited garden beds, each on its own tab
- Rename beds inline; delete with confirmation
- Each bed has independent dimensions, plant layouts, and undo history
- Bed dimensions displayed in feet, calculated from the underlying inch grid

### Three Interaction Modes
- **Place/Move** (default) — click empty soil to place a plant; click an existing plant to move it
- **Label/Edit** — click any plant to open a dialog for renaming and recoloring it
- **Delete** — click a plant to remove it; hover shows a red X preview before you click
- Hold **Ctrl** in any mode to temporarily switch to delete mode

### Plant Customization
- Radius slider from 1–18 inches with a live preview circle
- 48-color palette covering greens, earth tones, pinks, purples, golds, and reds
- Text labels rendered directly on each plant with automatic word-wrapping
- Diameter shown in inches next to the active plant indicator

### Plant Profiles
- Save any size + color + name combination as a reusable profile
- Apply saved profiles instantly to new plants
- View, select, and delete profiles from a scrollable sidebar list
- Profiles are preserved when saving to file

### Canvas & Grid System
- 4-inch base grid; 12 inches = 1 foot with heavier foot-mark lines
- Horizontal and vertical rulers with foot markers
- Toggleable grid overlay
- Snap-to-grid centers plants and snaps radius to 2-inch increments (can be disabled)

### Zoom & Pan
- Zoom range: 0.5× to 4.0×
- Zoom in/out buttons, a reset-to-100% button, and mousewheel zoom
- Scrollbars for panning at zoomed levels
- Zoom level shown as a percentage; canvas visual center is maintained during zoom

### Undo / Redo
- Full undo/redo for all plant add, move, resize, label, and delete operations
- Per-bed history stacks with a 60-state limit
- **Ctrl+Z** to undo, **Ctrl+Y** (or **Ctrl+Shift+Z**) to redo

### Save / Load
- Save all beds, plants, and profiles to a single `garden_layout.json` file
- Load a saved file to restore the complete design
- Undo stacks are stripped before saving to minimize file size

### Export & Printing
- **PNG Export** — downloads the current bed canvas as an image (named after the bed)
- **Print** — formats all beds for printing, with a legend listing every unique plant label and color; print stylesheet hides all UI chrome

### Keyboard Shortcuts
| Shortcut | Action |
|---|---|
| Ctrl+Z | Undo |
| Ctrl+Y / Ctrl+Shift+Z | Redo |
| Ctrl (held) | Temporary delete mode |
| Enter (in edit dialog) | Save label |
| Esc (in edit dialog) | Cancel edit |

### Touch Support
- Full touchstart / touchmove / touchend support for tablet and mobile use

### UI & Design
- Earthy dark-mode color palette (sage green, wood tones, soil brown)
- Sticky toolbar; scrollable plant profiles panel
- Context-sensitive gesture hints that update based on the active mode
- Google Fonts (Playfair Display + Lato); fully functional offline once loaded
- No external dependencies — pure HTML, CSS, and vanilla JavaScript
