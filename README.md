
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/status-active-success)

# DbD 1v1 Tracker

Dark-mode, single-file web app to track **Dead by Daylight 1v1s** — log killer, map, opponent, side, result, **chase time (mm:ss or seconds)**, and notes. Includes **inline row editing**, **per-killer & per-map stats**, **winrate**, **streaks**, **average/median chase times**, and **best/worst maps per killer**. Data is stored locally in your browser (no server). Import/Export to **JSON or CSV**.

> Current version: **v1.2.0**

---

## ✨ Features

- 📝 Quick entry form with validation  
- ⏱️ Chase time input as `mm:ss` or total seconds (stored as seconds; displayed as `mm:ss`)  
- 🌙 Polished dark UI, compact controls, pill tags for results & sides  
- 🔎 Search + filters (Side, Killer, Map, Result)  
- 🧮 Stats:
  - Overall winrate, W/L/D & current streak
  - Average / median / shortest / longest chase times (combined)
  - **As Killer**: winrate & avg/median chase by killer you played
  - **As Survivor**: winrate & avg/median chase vs killer
  - Per-map winrate
  - **Per-killer overview**: avg chase (killer & survivor), **best/worst map** by winrate  
- ✏️ Inline table editing (Save/Cancel), delete rows
- 💾 LocalStorage persistence + **Import/Export** (JSON & CSV)
- 🛟 Backup reminder if you haven’t exported for a while

---

## 🚀 Getting Started

1. Download `index.html` (this repo is single-file).  
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari).  
3. Start logging matches.

> Tip: Commit the file to GitHub Pages to get a shareable URL.

---

## 📤 Import / Export

- **Export** → choose **JSON** or **CSV**.  
- **Import** → select a `.json` or `.csv` file (auto-detected).  
- JSON format supports either:
  - An array of entries `[{...}, ...]`, **or**
  - An object `{ schema: "dbd1v1.v3", exportedAt, entries: [...] }`.

**CSV columns (required):**
```
id,when,killer,map,opponent,side,result,chaseSurvivor,chaseKiller,notes
```

---

## 🗃️ Data Model (localStorage)

Storage key: `dbd1v1_entries_v3`

Each entry:
```json
{
  "id": "uuid",
  "when": "2025-09-07T00:30:00.000Z",
  "killer": "Blight",
  "map": "The Game (Gideon)",
  "opponent": "Player123",
  "side": "Killer",                 
  "result": "Win",                  
  "chaseSurvivor": 85,              
  "chaseKiller": 72,                
  "notes": "3 shack mindgames"
}
```

**Compatibility:** v1.2.0 keeps the same schema as v1.1.x.

---

## 🧭 Roadmap

### v1.2.x (polish & QoL)
- [ ] Quick-export last used format (one-click next to Export)
- [ ] Tiny separators between **Clear / Import / Export**
- [ ] Optional “copy row” to duplicate a previous match
- [ ] Keyboard shortcuts (e.g., `E` Export modal, `/` focus search)

### v1.3 — Charts & Trends
- [ ] Inline charts (no external libs): winrate over time, rolling averages
- [ ] Per-killer time series (avg chase as K + as S)
- [ ] Per-map heatmap (basic table shading)

### v1.4 — Quality & Power-user
- [ ] Multi-select filters (e.g., filter multiple killers)
- [ ] Tagging for notes (e.g., `@tiles`, `@shack`, `@mindgame`)
- [ ] Smart presets for killers & maps (editable lists in UI)

### v1.5 — Data Safety & Portability
- [ ] Auto-backup reminder with configurable interval
- [ ] Optional encrypted export (password-protected JSON)

*(Roadmap is intentionally lightweight; issues/PRs welcome!)*

---

## 🔖 Versioning

Semantic Versioning:
- **MAJOR**: data schema changes or breaking behavior  
- **MINOR**: new features, UX improvements (backward compatible)  
- **PATCH**: bug fixes, small tweaks  

**Changelog (since v1.1.x → v1.2.0):**
- Moved **Clear All** left; **Import** & **Export** side-by-side  
- Promoted **Filter: Side** to the top row  
- Export modal (JSON/CSV) with backdrop  
- Import auto-detects JSON vs CSV  
- Kept schema (`dbd1v1_entries_v3`) for compatibility  

---

## 🧾 License

MIT (see `LICENSE`).


## 🧾 License

MIT (see `LICENSE`).
