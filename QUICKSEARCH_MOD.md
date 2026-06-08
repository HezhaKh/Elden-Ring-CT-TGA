# Quick Item Search — personal modification

This is a fork of [The Grand Archives Elden Ring Cheat Table](https://github.com/The-Grand-Archives/Elden-Ring-CT-TGA)
(v1.18.0, Elden Ring app **1.16.2**). All credit for the underlying table goes to
**The Grand Archives** and contributors — this fork only **adds one extra script** on top.

## What was added

A single Auto Assembler / Lua cheat entry — **"QUICK ITEM SEARCH"** — that gives a
fast, searchable item-spawn overlay:

- Press the **`~`** key (toggle) to open a popup window.
- **Type** to live-filter the full item list (pulled at runtime from the table's own
  `ItemDropdown` + `ItemDropdownDLC`, so no IDs are hardcoded).
- **Double-click** a result (or select + **Enter**, or the **Add** button) to put it in
  your inventory. Set a **Qty** for stacks.
- **One-click preset buttons:**
  - *Smithing stones x99* — all regular + somber stones, incl. both Ancient Dragon stones
  - *Gloveworts x99* — Grave + Ghost Glovewort [1–9]
  - *Larval Tears x20*
  - *Lord's Runes x15*

It reuses the table's global `ItemGive(id, qty, reinforceLv, upgrade, gem)` function, so
the table's master **"Open"** script must be enabled first.

## Modified file

- `ER_TGA_v1.18.0_QuickSearch.CT` — TGA v1.18.0 with the extra entry spliced in
  (entry `ID 90000001`, inserted before the root `</CheatEntries>`).

## Notes

- **Offline / single-player & Seamless Co-op only.** Like the upstream table, do not use
  this online with anti-cheat enabled.
- Requires Cheat Engine 7.4–7.6 and Elden Ring app 1.16.2.
- The game should run in **Windowed / Borderless** so the overlay can draw on top.
