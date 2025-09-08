<<<<<<< HEAD
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/status-active-success)

# DbD 1v1 Tracker 
=======
# DbD 1v1 Tracker
>>>>>>> 3619ff3 (chore:prepare v1.2.0 release (README + CHANGELOG))

Dark-mode, single-file web app to track **Dead by Daylight 1v1s** — log killer, map, opponent, side, result, **chase time (mm:ss or seconds)**, and notes. Includes **inline row editing**, **per-killer & per-map stats**, **winrate**, **streaks**, **average/median chase times**, and **best/worst maps per killer**. Data is stored locally in your browser (no server). Import/Export to **JSON or CSV**.

> Current version: **v1.2.0**

---

<<<<<<< HEAD
# DbD 1v1 Tracker — Roadmap

This roadmap outlines planned features and improvements for the Dead by Daylight 1v1 Tracker.  
Items are grouped by priority and release stage. Contributions and feedback are welcome!

---

## ✅ Current Features (v1.0)
- Dark mode UI
- Track: Killer, Map, Opponent, Side (Killer/Survivor), Result (W/L/D), Chase Time (mm:ss or sec), Notes
- LocalStorage persistence (no backend required)
- Import/Export: JSON & CSV
- Stats dashboard:
  - Overall winrate
  - Winrate **as Killer** (by killer played)
  - Winrate **vs Killer** (when playing Survivor)
  - Average chase times
- Single-file app (just open `index.html` in a browser)

---

## 🛠️ Near-Term Goals (v1.1 – v1.2)
- **Per-map winrate** (analyze strengths/weaknesses on different maps)
- **Current streak tracking** (e.g., W3, L2, etc.)
- **Expanded stats panel**:
  - Median chase time
  - Longest/shortest chases
- **Improved UX**:
  - Inline editing instead of prompts
  - Clearer mobile layout

---

## 🚀 Medium-Term Goals (v2.x)
- **Data visualizations**:
  - Charts for winrate trends
  - Line charts for chase times over time
  - Bar charts for killers/maps
- **Multiple profiles**:
  - Track results for multiple players/teams
- **Tagging system**:
  - Add tags to matches (e.g., “scrim”, “tournament”, “practice”)
- **Export to Excel (.xlsx)** with formatting

---

## 🌐 Long-Term Vision (v3.x+)
- **Cloud sync** (optional login to back up and sync across devices)
- **Team dashboard**:
  - Aggregate stats for all team members
  - Shareable reports
- **Discord bot integration**:
  - Record matches via commands (`!1v1 add ...`)
- **Mobile PWA**:
  - Installable on phone
  - Offline-first support

---

## 📌 Notes
- This project will remain **open-source** and under the MIT License.
- Roadmap is flexible: priorities may shift based on feedback or contributions.

## Dev
Pure HTML/CSS/JS. No build step.
=======
## ✨ Features
>>>>>>> 3619ff3 (chore:prepare v1.2.0 release (README + CHANGELOG))

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
