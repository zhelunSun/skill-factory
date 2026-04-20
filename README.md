# Skill Factory

> The machine that makes machines.

A **meta-skill** for WorkBuddy/Claw that provides a standard operating procedure for building, iterating, and publishing skills — from a fuzzy idea to a polished, distributable package.

---

## The Problem It Solves

Creating a skill without a workflow leads to:
- Fuzzy specs → over-engineering before the need is clear
- Knowledge gaps → missing content from distillation without source re-verification
- Scattered files → hard to publish or share
- No iteration path → skill stagnates at v1.0

Skill Factory solves all four with a **four-phase SOP** that any Claw instance can follow.

---

## What Makes It Different

**Most skill-making is ad hoc.** Skill Factory treats skill creation as a repeatable, improvable process:

- **Phase 0 three-question lock** — prevents scope creep before work begins
- **Mandatory source re-verification** — catches missed content after distillation
- **Workspace layout standard** — every skill gets an independent repo, ready to publish
- **ClawHub distribution spec** — README format, trigger word guidelines, versioning semantics

It's not about capability — it's about organizing the workflow so skills get made faster and better each time.

---

## What's Inside

```
skill-factory/
├── SKILL.md         # Skill entry point — the full SOP
├── README.md        # This file
├── CHANGELOG.md     # Version history
├── inbox/           # Drop zone for raw ideas
└── wip/             # Active work-in-progress
    └── <skill>/
        ├── BRIEF.md
        ├── raw/
        └── draft/
```

---

## How to Use

Just send Claw an idea in any format:

```
新 skill：[name]，[1-2 sentences]，[source URL (optional)]
```

Or to iterate an existing skill:

```
skill升级：[name]，[what to add]，[new source URL (optional)]
```

Claw will enter Phase 0 immediately. You'll be asked exactly 3 questions, then work begins automatically.

---

## Skills Built With This Factory

| Skill | Version | Status |
|-------|---------|--------|
| [harness](../harness) | v1.2.0 | ✅ GitHub-ready |
| [nova-reader](../nova-reader) | v1.1.0 | ✅ GitHub-ready |

---

## Version History

See [CHANGELOG.md](./CHANGELOG.md)

---

## License

MIT — feel free to fork, adapt, and improve.
