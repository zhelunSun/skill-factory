# Skill Factory

> **Idea go in. Versioned, publishable skill come out. 10 minutes.**

The meta-skill that turns any useful prompt, workflow, or doc into a reusable agent skill — structured, versioned, ClawHub-ready.

[![Version](https://img.shields.io/badge/version-2.5.0-blue.svg)](CHANGELOG.md)
[![Stars](https://img.shields.io/badge/dynamic/json?color=yellow&label=stars&query=stargazers_count&url=https://api.github.com/repos/zhelunSun/skill-factory)](https://github.com/zhelunSun/skill-factory)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![中文说明](https://img.shields.io/badge/README-中文版-orange.svg)](README_zh.md)

---

## Before / After

```
BEFORE (pain):
User: "my agent output too verbose. can i make it short but keep tech detail?"
Agent: <writes a giant SKILL.md, forgets version, no changelog, can't publish>
Result: A messy file. No version. No README. ClawHub? Forget it.

AFTER (10 minutes):
New skill: token-saver, cut fluff, keep technical accuracy
→ BRIEF.md (locked spec)
→ SKILL.md (282 lines, triggers, golden rules)
→ CHANGELOG.md (versioned)
→ README.md + README_zh.md (bilingual)
→ LICENSE (MIT)
→ v1.0.0 tag
→ ClawHub-ready repo
```

**From idea → published skill. Every file. Every version. 10 minutes.**

---

## Why It Works

Skill Factory is not "a better prompt." It is a **structured pipeline** that any AI agent can follow.

| Problem | Without Skill Factory | With Skill Factory |
|---------|----------------------|-------------------|
| Fuzzy ideas | Agent guesses scope, over-builds | **Phase 0 three-question lock** |
| Forgotten knowledge | Missed concepts during distillation | **Mandatory source re-read** |
| Scattered files | Can't publish | **Independent repo per skill** |
| Stagnant v1.0 | No upgrade path | **Structured 1→N workflow** |
| Version chaos | "v2 final final v3" | **Semantic versioning rules** |

The "machine that builds machines" isn't a metaphor — it's the product. Any Claw instance with this skill loaded can build production-quality skills.

---

## Factory Output

Skills built with Skill Factory, in production today:

| Skill | What It Does |
|-------|-------------|
| **[harness](https://github.com/zhelunSun/harness)** v1.2 | Agent-first engineering knowledge base |
| **[nova-reader](https://github.com/zhelunSun/nova-reader)** v1.1 | Academic paper deep-reading workflow |

---

## Quick Install

```bash
# From ClawHub (recommended)
claw skill install skillfactory

# From GitHub
git clone https://github.com/zhelunSun/skill-factory.git ~/.workbuddy/skills/skillfactory
```

Restart your session. Skill auto-loads.

---

## Quick Start

Send your AI agent:

```
New skill: [name], [1-2 sentences], [source URL (optional)]
```

Agent enters **Phase 0** immediately. 30 seconds: spec locked. 10 minutes: skill shipped.

---

## How It Works

**Four phases. Zero guesswork.**

| Phase | Name | Duration | Output |
|-------|------|----------|--------|
| 0 | Capture | 30s | `BRIEF.md` — locked spec, 3 questions |
| 1 | Collect | 1-2 min | `raw/` — auto-fetched source material |
| 2 | Distill | 5 min | `SKILL.md` + `references/` (verified) |
| 3 | Publish | 2 min | versioned repo, ClawHub-ready |

Full SOP in [SKILL.md](SKILL.md).

---

## Maintaining Skills (1→N)

Skill Factory is not only 0→1. Structured upgrade workflow:

```
Upgrade skill: [name], [change request], [new source URL (optional)]
```

1. **Inspect** — reads existing state
2. **Classify** — determines PATCH / MINOR / MAJOR
3. **Propose** — upgrade plan before changes
4. **Apply** — updates files, CHANGELOG, version
5. **Summary** — reports what changed

No more "v2 final final v3" chaos.

---

## Repo Structure

```
skill-factory/
├── SKILL.md         # Full SOP — 4 phases, versioning, publishing
├── README.md        # This file
├── README_zh.md     # 中文版
├── CHANGELOG.md
├── LICENSE          # MIT
├── inbox/           # Drop zone for raw ideas
└── wip/             # Work-in-progress
    └── <skill>/
        ├── BRIEF.md
        ├── raw/
        └── draft/
```

---

## License

MIT — fork it, adapt it, build your own factory.
