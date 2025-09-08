# Changelog
All notable changes to **DbD 1v1 Tracker** will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),  
and this project adheres to [Semantic Versioning](https://semver.org/).

---

## [1.2.0] - 2025-09-07
### Added
- Export modal with format selection (JSON or CSV).
- Import auto-detects file type (JSON or CSV).
- Stats:  
  - Average chase time split by Killer side and Survivor side for each killer.  
  - Best and worst map per killer by winrate (with sample size shown).

### Changed
- Toolbar layout:  
  - **Clear All** button moved to the far left.  
  - **Import** and **Export** buttons placed side-by-side.  
  - **Filter: Side** promoted to the top row near the search box.  
- Compact styling for Import/Export buttons to better fit the UI.

### Fixed
- Dropdowns in dark mode now render option text visibly.  
- Inline editing validation more consistent for time, killer, map, and opponent fields.

---

## [1.1.x] - 2025
Baseline version with:
- Dark mode UI.  
- Killer, Map, Opponent, Side, Result, Notes, and Chase Time tracking.  
- Inline editing of table rows.  
- JSON and CSV import/export.  
- Stats for overall winrate, streaks, per-killer (as Killer/Survivor), per-map, and chase time averages.  
- LocalStorage persistence.  

---

## [Unreleased]
Planned for future:
- Quick-export last used format (no modal).  
- Tiny separators between Clear / Import / Export buttons.  
- Optional "copy row" shortcut.  
- Keyboard shortcuts for Export/Search.  
- Charts for winrate and chase trends.  
