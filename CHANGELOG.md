# Changelog

All notable changes to FuzzTag are listed here, newest first.

---

## [v1.1.0] — 2026-10-18

> **Big update:** SwarmUI support, custom categories, and a few new views.

### 🚀 SwarmUI Support
* **SwarmUI Tag Preservation:** Tags like `<lora:…>`, `<wildcard:…>`, `<var:…>`, `<random:…>`, `<segment:…>`, `<region:…>`, and `<object:…>` are kept exactly as typed and displayed as purple dotted blocks (never lowercased, altered, checked against Danbooru, or moved by Sort).
* **Export as `setvar`:** Added a SwarmUI variables box that wraps each ticked group in a variable (e.g., `<setvar[hair]:white hair, short hair>`).
  * Custom variable naming per group.
  * **OFF / ON toggle badge** on the box title.
  * **Stored only option:** Writes `<setvar[name,false]:…>` to save text without inserting it into the main prompt.
  * Support for wildcard blocks inside group variables.
  * Dedicated **Copy setvar block** and **Copy var calls** buttons.
* **Insert SwarmUI Tag Dropdown:** Quick-insert ready-made tags with auto-selected placeholder text (mobile-friendly).
* **Smart Tag Positioning:** Segments, regions, and objects stay in typed order and are automatically placed at the end.
* **Syntax Warnings & Quick Fixes:**
  * Detects `{a|b}` (A1111 style) and offers **Convert to `<random:…>`**.
  * Warns for unclosed SwarmUI tags, undefined `<var:…>` calls, and duplicate wildcards.

### 🎨 Custom Categories (☰ Panel)
* **Category Management:**
  * **Rename:** Type directly over category names.
  * **Recolor:** Tap the colored dot to update blocks and legend in real time.
  * **Reorder:** Drag using `⠿` handle or `▲`/`▼` buttons (affects Sort and Lines view).
  * **Add Custom Categories:** Create new categories and define tag lists separated by commas.
* **Single-Tag Rules:** Sort group applied to an individual tag always overrides list rules.
* **Reset Controls:** Individual category reset, **Reset order**, and **Reset all categories**.
* **Persistence & Layout:** Settings auto-save in browser and sync with **Copy backup / Save .json**. Responsive side-panel layout for desktop and slide-over overlay for mobile.

### 👁️ Groups & Views
* **Expression / Gaze Group:** Separated from eyes/face (`smile`, `closed mouth`, `looking at viewer`). Unticked by default in `setvar` export to keep identity clean.
* **Lines View Button:** Toggle block layout into line-by-line view matching final prompt order.
* **Resizable Preview:** Drag preview corner or tap **Expand preview** (touch screen supported).

### ✨ Small Extras
* **Link Previews & Metadata:** Added Open Graph title, description, tab favicon, and theme color.
* **Footer:** Displays version number and quick links to GitHub, Bug Reports, and Changelog.
* **Shortcuts & Quality of Life:**
  * `Ctrl + Enter` copies the final prompt.
  * Line breaks in tag input now count as commas.
  * Keeps `BREAK` (A1111 style) uppercase without converting to `break`.

---

## [v1.0.0] — 2026-10-17

* **First Public Release:** Notepad-style prompt editor built for ANIMA / Illustrious models.
* **Live Danbooru Integration:** Autocomplete, tag-type color coding, and sync status indicator.
* **Auto Cleanup:** Handles underscores, brackets, duplicate removal, weight controls, and auto-sorting into color groups.
* **Interactive Tag Blocks:** Drag-and-drop, mute, lock, group select, and character quick-fill.
* **Tag Exploration:** See also and Related tags directly from Danbooru.
* **Workflow Utilities:** History tracking, Save/Load, Copy options, and conflicting tag alerts.
* **Cross-Platform:** Full PC and mobile browser support with no installation required.