Changelog
All notable changes to FuzzTag are listed here, newest first.
v1.1.0 — 2026-10-18
Big update: SwarmUI support, custom categories, and a few new views.
Added: SwarmUI support
SwarmUI tags are kept exactly as typed. `<lora:…>`, `<wildcard:…>`, `<var:…>`, `<random:…>`, `<segment:…>`, `<region:…>` and `<object:…>` show as a purple dotted block. They are never lowercased, never changed, never checked against Danbooru, never moved by Sort, and have no weight. They no longer show as "unknown tag".
Export as setvar. A new SwarmUI variables box wraps each ticked group in a variable, for example `<setvar[hair]:white hair, short hair>`. The tags still appear in the main prompt, and segments (face, eye or hand fix) can call them back with `<var:hair>`. The text is the same everywhere, so wildcards are rolled once and the character stays consistent.
Type your own variable name for each group.
An off / ON badge on the box title shows whether setvar export is on, and you can click it to switch.
Stored only option: writes `<setvar[name,false]:…>` so the text is saved but not written in the main prompt. Add `<var:name>` where you want it.
A wildcard block can go inside a group's variable (right-click it and pick a Sort group).
Copy setvar block and Copy var calls buttons, also available in "copy as".
Insert SwarmUI tag drop-down: adds a ready-made tag with the name part selected, so you can type over it. Useful on a phone, where `<` is hard to type.
Segments, regions and objects stay in the order you typed and go last, after your sentence, because SwarmUI reads the text after them as their own prompt.
`{a|b}` warning. `{a|b}` is A1111 style and SwarmUI does not read it by default. FuzzTag warns about it and offers Convert to `<random:…>`. The insert menu uses `<random:a, b>` and `<random:a|b>`.
New warnings: a SwarmUI tag that is not closed, a `<var:…>` that nothing defines, and the same wildcard used twice.
Added: your own categories (☰ panel)
Rename a category by typing over its name.
Recolor by tapping the colored dot. Blocks and the color key change right away.
Reorder by dragging the ⠿ handle or using ▲ ▼. Sort tags and the Lines view follow this order.
Add your own category. Type a name and tap Add, then open its ⋯ panel and list the tags that belong there, separated by commas.
Sort group on a single tag always wins over the lists.
Reset buttons: one per category, plus Reset order and Reset all categories.
Everything is saved in your browser and included in Copy backup / Save .json.
Uncategorized and SwarmUI syntax always stay at the end. Your own categories get a setvar variable name automatically (you can rename it).
On a computer the panel opens beside the page, so it does not cover the blocks. On a phone it slides over the screen.
Added: groups and views
New Expression / gaze group (smile, closed mouth, looking at viewer), separate from eyes and face. It is unticked by default in setvar export, so identity variables stay clean. By default only hair, eyes and face, body and headwear are ticked.
Lines button (top right of the tag blocks): shows blocks in lines like the final prompt. Your order never changes. Remembered.
Preview size: drag the corner of the preview or press Expand preview (works on touch screens too).
Added: small extras
Link previews. Sharing the site link on Discord and other apps now shows a title and short description. The page also has a tab icon and a theme color.
Footer with the version number and links to GitHub, Report a bug, and What's new.
Ctrl + Enter copies the final prompt.
Paste a list with one tag per line. A line break in the tag box now counts as a comma.
`BREAK` (A1111 style) is kept exactly as typed and no longer turned into a lowercase `break` tag.
v1.0.0 — 2026-10-17
First public release.
Notepad-style prompt editor for ANIMA / Illustrious models.
Live Danbooru tag autocomplete and tag-type colors, with a sync status pill.
Auto cleanup (underscores, brackets, duplicates), weight control, and auto-sort into color groups.
Tag blocks you can drag, mute, lock, select in groups, and quick-fill for characters.
See also and Related tags from Danbooru for any tag.
History, Save/Load, Copy as, and warnings for conflicting tags.
Works on PC and phone, no install needed.