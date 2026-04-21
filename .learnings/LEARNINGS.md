# Learnings

Corrections, insights, and knowledge gaps captured during development.

**Categories**: correction | insight | knowledge_gap | best_practice

---

## [LRN-20250421-001] best_practice

**Logged**: 2026-04-21T20:55:00Z
**Priority**: medium
**Status**: pending
**Area**: docs

### Summary
ClawHub skill distribution requires clean separation between development workspace and publishable content

### Details
Original skill-factory repo contains development artifacts (inbox/, wip/, promo/) that should not be published to ClawHub. User asked for a "clean publish version" to avoid manual path management issues.

Key insight: **ClawHub minimum = SKILL.md only**, but professional distribution needs SKILL.md + README.md + LICENSE.

### Suggested Action
Establish a standard pattern:
1. Development repo (GitHub): full workspace with .gitignore exclusions
2. Publish directory: copy only core files for ClawHub upload
3. Version sync: update SKILL.md, README badges, CHANGELOG together

### Metadata
- Source: conversation
- Related Files: PUBLISH.md
- Tags: clawhub, distribution, versioning
- Pattern-Key: skill-publish-workflow
- Recurrence-Count: 1

---

## [LRN-20250421-002] insight

**Logged**: 2026-04-21T20:55:00Z
**Priority**: low
**Status**: pending
**Area**: config

### Summary
Slug vs display name: display name matters more for discoverability, but slug is permanent

### Details
User originally wanted "skill-factory" slug but it was taken. Decided on "skillfactory" (no hyphen). Display name remains "Skill Factory" for presentation.

Lesson: When slug is taken, removing hyphen is standard practice (tailwindcss vs tailwind-css).

### Metadata
- Source: conversation
- Tags: naming, slug, distribution

---
