# Changelog — skill-factory

All notable changes to skill-factory will be documented in this file.

Format: [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

---

## [2.0.0] - 2026-04-20

### Summary

**From SOP document to meta-skill.**

Skill Factory is now itself a publishable WorkBuddy skill. v2.0 restructures the project so it can be distributed via GitHub/ClawHub and loaded by any Claw instance, just like any other skill.

### Changed
- `SKILL.md` completely rewritten as a proper skill entry point with YAML frontmatter, trigger words, and self-contained SOP
- Added Phase 3 publishing specs: README format, ClawHub distribution checklist, version semantics
- Added skill iteration workflow (1→N upgrades)
- `README.md` rewritten as human-facing project page with selling points

### Added
- `CHANGELOG.md` (this file)
- ClawHub distribution spec in Phase 3
- Skill upgrade triggers and process
- Workspace layout reference

---

## [1.0.0] - 2026-04-18

### Summary

**Initial creation.**

Built during the harness skill development cycle as a response to 4 accumulated learnings (LRN-001 through LRN-004). Established the four-phase SOP and workspace directory structure.

### Added
- `SKILL-SOP.md` — four-phase workflow (Phase 0-3)
- `inbox/` directory — idea drop zone
- `wip/` directory — active skill workspace
- `D:/WorkBuddy/.workspace-index.md` — master skill status board
- 4 lessons from harness creation embedded into SOP
