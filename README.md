![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/status-active-success)

# DbD 1v1 Tracker 

Single-file web app to track Dead by Daylight 1v1 results.

## Features
- Killer, Map, Opponent, Side (Killer/Survivor), Result (W/L/D)
- Chase Time input as `mm:ss` or seconds (stored as seconds; displayed `mm:ss`)
- JSON/CSV import & export (schema `dbd1v1.v3`)
- Stats: overall W/L/%, winrate as Killer by killer played, winrate vs Killer as Survivor
- LocalStorage (no server/database)

## Use
Just open `index.html` in a browser. Data stays in your browser. Use **Export JSON** to back up.

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
- This project will r

## Dev
Pure HTML/CSS/JS. No build step.

## License
MIT
