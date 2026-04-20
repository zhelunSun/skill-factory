# Skill Factory

> **"The first industrial revolution was marked by using machines to make machines."**
> **Skill Factory is the machine that makes skills.**

A **meta-skill** for WorkBuddy/Claw that automates the full lifecycle of skill creation — from a fuzzy idea to a polished, versioned, distributable package.

[![Version](https://img.shields.io/badge/version-2.1.0-blue.svg)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![中文说明](https://img.shields.io/badge/README-中文版-orange.svg)](README_zh.md)

---

## What Problem Does It Solve?

Creating a WorkBuddy skill without a workflow leads to: fuzzy specs, missed knowledge during distillation, scattered files impossible to publish, and skills that stagnate at v1.0 with no clear upgrade path.

**Skill Factory solves all of this** by treating skill creation as a repeatable, improvable process — not a one-off creative act.

## What Makes It Different?

Most skill-making is ad hoc. Skill Factory is an **end-to-end automated SOP** that any Claw instance can follow:

- **Phase 0 three-question lock** — prevents scope creep before work begins
- **Mandatory source re-verification** — catches missed content after distillation
- **Semantic versioning for skills** — know when to bump MAJOR vs MINOR vs PATCH
- **Independent repo per skill** — every skill is GitHub/ClawHub-ready from day one
- **Human-AI collaborative iteration** — not just 0→1, but 1→N ongoing improvement

It is not about what Claw *can* do — it is about turning an unbounded capability into a **reliable, high-quality pipeline**. The process is the product.

---

## Quick Start

Just send Claw an idea:

```
New skill: [name], [1-2 sentences], [source URL (optional)]
```

Or in Chinese:

```
新 skill：[名字]，[1-2句说明]，[来源链接（可选）]
```

Claw enters **Phase 0** immediately — no setup required.

---

## Example: Building the `harness` Skill

Here is how Skill Factory handled a real request end-to-end:

**Input** (30 seconds):
```
新 skill：harness，蒸馏 OpenAI 的智能体工程文章，
https://openai.com/zh-Hans-CN/index/harness-engineering/
```

**Phase 0** — Three questions answered in one message:
- Target: any Claw working on agent-first engineering
- Source: OpenAI Harness Engineering blog post
- Scope: GitHub + local workspace

**Phase 1** — `web_fetch` the source, saved to `wip/harness/raw/`

**Phase 2** — Distilled into `SKILL.md` (10 principles) + `references/` (two documents). Mandatory re-read caught 4 missed concepts including the "Ralph Wiggum loop".

**Phase 3** — Independent repo at `D:/WorkBuddy/harness/`, MIT license, bilingual README, git-tagged `v1.2.0`.

**Total time**: ~40 minutes. Without the factory, the same work took a full day of iteration and still had gaps.

---

## Four-Phase SOP Overview

| Phase | Name | Output |
|-------|------|--------|
| 0 | Capture | `BRIEF.md` — locked spec |
| 1 | Collect | `raw/` — raw source material |
| 2 | Distill | `SKILL.md` + `references/` |
| 3 | Publish | versioned repo, synced to workspace |

Full SOP details are in [SKILL.md](SKILL.md).

---

## Version Management

Skills use **Semantic Versioning** adapted for this format:

| Bump | When |
|------|------|
| `PATCH` (x.x.1) | Typo fix, trigger word tweak |
| `MINOR` (x.1.0) | New source, new section, extended triggers |
| `MAJOR` (2.0.0) | Paradigm shift, structural refactor |

**MAJOR does not mean more content** — a skill that doubles its references but keeps the same structure is still MINOR.

---

## Repo Structure

```
skill-factory/
├── SKILL.md         # Full SOP — four phases, version management, publishing spec
├── README.md        # This file (English)
├── README_zh.md     # Chinese version
├── CHANGELOG.md     # Version history
├── LICENSE          # MIT
├── inbox/           # Drop zone for raw ideas
└── wip/             # Active work-in-progress
    └── <skill>/
        ├── BRIEF.md
        ├── raw/
        └── draft/
```

---

## License

MIT — fork it, adapt it, build your own factory.
