# Garden Bed Planner

A browser-based tool for graphically designing and planning raised garden beds. Place, size, and label plants on an interactive infinite canvas with a real-scale 4″ grid system. Save your designs to JSON, export as PNG, or print a full layout with a plant legend.

**Live app:** https://ty10y.github.io/Garden-Bed-Planner/

---

## How to Use

1. **Open the app** — visit the live link above, or open `index.html` locally in any modern browser.
2. **Set bed size** — use the **W** and **H** inputs in the toolbar to set your garden bed dimensions in feet (1–50 ft each direction). The canvas resizes and re-fits automatically.
3. **Set plant size** — use the radius slider (1–50 inches) to choose a size; a live preview circle updates as you drag.
4. **Pick a color** — select from the 48-color palette.
5. **Place a plant** — click anywhere on the soil canvas to drop a plant. Click and drag from empty soil to size the plant interactively before releasing.
6. **Edit a plant** — click any existing plant to open the edit dialog. From there you can rename it, recolor it, and resize it with a slider.
7. **Move a plant** — click and drag any existing plant to a new position.
8. **Delete a plant** — switch to **Delete** mode and click a plant, or hold **Ctrl** while in any mode to temporarily enter delete mode.
9. **Add more beds** — click the **+** tab to create a new bed. Beds can be renamed and deleted independently.
10. **Undo/Redo** — use **Ctrl+Z** / **Ctrl+Y**, or the toolbar buttons. Dimension changes are fully undoable alongside plant edits.
11. **Zoom** — use the zoom buttons, scroll the mousewheel over the canvas, or click the fit button to snap the bed back to fill the window.
12. **Pan** — hold **Space** and drag, or use the middle mouse button to pan without affecting plant placement.
13. **Save your design** — click **Save to File** to download a `garden_layout.json` file. Load it back with **Load from File**.
14. **Export or print** — click **Export PNG** to download the current bed as an image, or **Print** to get a formatted layout of all beds with a plant legend.

---

## Features

### Multi-Bed Management
- Create and manage unlimited garden beds, each on its own tab
- Rename beds inline; delete with confirmation
- Each bed has independent dimensions, plant layouts, and undo history
- Bed dimensions set with W/H number inputs (in feet); changes are fully undoable

### Two Interaction Modes
- **Place / Edit** (default) — all-in-one tool:
  - Click empty soil → place a plant
  - Drag from empty soil → size a plant interactively before placing
  - Click an existing plant → open the edit dialog (rename, recolor, resize)
  - Drag an existing plant → move it to a new position
- **Delete** — click a plant to remove it; hover shows a red X preview before you click
- Hold **Ctrl** in any mode to temporarily switch to delete mode

### Plant Customization
- Radius slider from 1–50 inches (2–100″ diameter) with a live preview circle
- 48-color palette covering greens, earth tones, pinks, purples, golds, and reds
- Edit dialog lets you rename, recolor, and resize any placed plant
- Text labels rendered directly on each plant with automatic word-wrapping; font size scales proportionally with plant size
- Organic scalloped / cloud-shaped plant outlines for a natural look

### Plant Profiles
- Save any size + color + name combination as a reusable profile
- Apply saved profiles instantly to new plants
- View, select, and delete profiles from a scrollable sidebar list
- Profiles are preserved when saving to file

### Canvas & Grid System
- Infinite-canvas model: the bed always fills the viewport; zoom in for detail, zoom out for overview — no page scrolling required
- 4-inch base grid; 12 inches = 1 foot with heavier foot-mark lines
- Toggleable grid overlay
- Snap-to-grid centers plants and snaps radius to 2-inch increments (can be disabled)

### Zoom & Pan
- Smooth zoom via mousewheel or zoom buttons; maintains the visual center point under the cursor
- **Fit to window** button re-centers and scales the bed to fill the viewport with a smooth animation
- Pan with **Space + drag** or **middle-mouse drag** — no scrollbars needed
- Zoom percentage displayed in the toolbar

### Animations
- **Drop-in spring** — newly placed plants animate in from zero with an ease-out-back overshoot
- **Hover pop** — hovering a plant plays a quick spring animation that overshoots and settles at a slightly larger size; cursor changes to a pointer
- **Mode button pulse** — a ripple ring confirms each mode switch
- **Fit animation** — the bed smoothly eases to fill the viewport when dimensions change or the fit button is clicked

### Undo / Redo
- Full undo/redo for all plant add, move, resize, label, recolor, and delete operations
- Bed dimension changes are also undoable — reverts both dimensions and any plants that were clamped
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
| Space + drag | Pan the canvas |
| Enter (in edit dialog) | Save changes |
| Esc (in edit dialog) | Cancel edit |

### Touch Support
- Full touchstart / touchmove / touchend support for tablet and mobile use

### UI & Design
- Earthy dark-mode color palette (sage green, wood tones, soil brown)
- Scrollable toolbar sidebar; context-sensitive gesture hints update based on the active mode
- Google Fonts (Playfair Display + Lato); fully functional offline once loaded
- No external dependencies — pure HTML, CSS, and vanilla JavaScript
