---
name: skill-factory
version: "2.0"
description: >
  A meta-skill for creating, iterating, and publishing WorkBuddy skills from scratch.
  Use this skill when the user wants to: build a new skill from an idea or URL, upgrade
  an existing skill with new sources, prepare a skill for GitHub publishing, or design
  a skill's repo structure. Triggers include: "新 skill", "做一个skill", "build a skill",
  "create skill", "skill制作", "把这个做成skill", "帮我把...打包成skill", "skill升级",
  "skill发行", "skill factory", "制造skill", "skill工厂", "skill from scratch",
  "我有个skill想法", "skill迭代", "skill打磨", "做一个关于...的skill".
---

# Skill Factory — The Meta-Skill for Making Skills

> "The true mark of the first industrial revolution was using machines to make machines."
> Skill Factory is the machine that makes skills.

## Purpose

Skill Factory provides a **repeatable, human-AI collaborative SOP** for going from a raw idea to a polished, publishable WorkBuddy skill. It handles:

- **0→1**: Rapid capture of fuzzy ideas → structured BRIEF → distilled skill
- **1→N**: Iterating an existing skill with new sources or structure improvements
- **N→∞**: Publishing, versioning, and ClawHub distribution

---

## How to Trigger This Skill

Just say something like:

> `新 skill：[名字或主题]，[1-2句说明]，[来源URL（可选）]`

Examples:
- `新 skill：prompt-engineering，整合 Anthropic 和 OpenAI 的提示词实践`
- `新 skill：git-workflow，规范我的 git 分支和 PR 流程，https://...`
- `skill升级：nova-reader，加入 Semantic Scholar 数据源`

Claw will immediately enter **Phase 0** — no more information needed to start.

---

## Four-Phase SOP

### Phase 0 · Capture（≤5 min）

**Goal**: Lock down the spec before any work begins.

1. Save raw idea to `inbox/<skill-name>.md` (防止遗失)
2. Ask exactly **3 questions** — no more:
   - What is the target scenario / user?
   - Are there reference sources? (If not, Claw will search)
   - Publish scope: local-only / GitHub / ClawHub distribution?
3. Generate `wip/<skill-name>/BRIEF.md`

**Key principle**: Phase 0 prevents over-engineering (LRN-003). Don't start building until the 3 questions are answered.

---

### Phase 1 · Collect（automated）

**Goal**: Gather raw material without processing.

1. `web_fetch` each source → save to `wip/<skill-name>/raw/`
2. If no sources provided, `web_search` for 2–3 high-quality references
3. Prioritize: official docs > primary blog posts > secondary analysis

**Rule**: At least 1 first-party source (official docs / original author's post). Raw content is saved as-is — no processing yet.

---

### Phase 2 · Distill（core work）

**Goal**: Extract signal, discard noise.

1. Read all `raw/` files
2. Write per skill-creator spec:
   - `SKILL.md` — triggers + workflow (≤200 lines)
   - `references/` — detailed knowledge, split by topic
   - `scripts/` — reusable code, only if needed
3. **Mandatory verification** (LRN-001): Re-fetch original source, diff against draft, check for gaps

**Quality checklist**:
- [ ] Trigger words are broad enough to cover all user phrasings
- [ ] SKILL.md has a clear "when to use" section
- [ ] Detail lives in `references/`, not bloating `SKILL.md`
- [ ] At least one mandatory re-read of primary source after distillation

---

### Phase 3 · Publish

**Goal**: Clean, versioned, standalone repo ready for GitHub/ClawHub.

#### Repo Structure (Minimal)

```
<skill-name>/
├── SKILL.md          # Entry point (triggers + workflow)
├── README.md         # Human-facing intro (see README spec below)
├── CHANGELOG.md      # Version history
├── .gitignore
└── references/       # Knowledge base
    └── *.md
```

For script-heavy skills, add:
```
└── scripts/
    └── *.py
```

#### Version Semantics

| Version | When |
|---------|------|
| `v1.0.0` | First publishable version |
| `v1.x.0` | New sources, content additions |
| `v1.x.x` | Bug fixes, trigger word tweaks |
| `v2.0.0` | Structural refactor or scope change |

#### README Spec (Selling Points)

A skill README must answer 3 questions in ≤60 seconds of reading:
1. **What problem does it solve?** (1-2 sentences, no jargon)
2. **What makes it better than asking without it?** (key differentiator)
3. **How do I use it?** (one concrete example)

Optional but recommended: badges (version, license), a "What's inside" file map.

#### ClawHub Distribution

When the user wants to publish to ClawHub:
1. Ensure `SKILL.md` frontmatter has: `name`, `version`, `description`
2. `description` must contain broad trigger phrases covering multiple phrasings
3. Create a `LICENSE` file (MIT recommended for open skills)
4. Tag the release: `git tag v1.0.0 && git push --tags`

#### Sync to Local Workspace

After publishing, sync to `~/.workbuddy/skills/<skill-name>/` so Claw can use it immediately:

```powershell
Copy-Item -Recurse -Force "D:\WorkBuddy\<skill-name>\*" "$env:USERPROFILE\.workbuddy\skills\<skill-name>\"
```

---

## Skill Iteration (1→N)

When upgrading an existing skill:

1. Create a new branch or directly update `D:/WorkBuddy/<skill-name>/`
2. Add new source to `references/` with dated filename (`source-YYYYMMDD.md`)
3. Update `SKILL.md` version field and trigger words if needed
4. Update `CHANGELOG.md`
5. Commit with semantic message: `feat: add [source name] to references`
6. Re-sync to local workspace

**Upgrade triggers**: User sends new URL, user says "skill has a gap", Claw detects missing knowledge during task.

---

## Workspace Layout

```
D:/WorkBuddy/
├── .workspace-index.md      # Master skill status board
├── skill-factory/           # This meta-skill repo
│   ├── SKILL.md             # This file
│   ├── README.md
│   ├── CHANGELOG.md
│   ├── SKILL-SOP.md         # Detailed SOP (legacy, superseded by this SKILL.md)
│   ├── inbox/               # Raw ideas drop zone
│   └── wip/                 # Active work-in-progress
│       └── <skill-name>/
│           ├── BRIEF.md
│           ├── raw/
│           └── draft/
│
├── harness/                 # ✅ v1.2.0 — ready for GitHub
├── nova-reader/             # ✅ v1.1.0 — ready for GitHub
└── <future-skills>/
```

---

## Lessons Learned (from .learnings)

| ID | Lesson | Fix in SOP |
|----|--------|-----------|
| LRN-001 | Missed content after distillation without re-reading source | Phase 2 mandatory re-fetch |
| LRN-002 | Skill evolved in workspace, hard to publish as standalone | Phase 3 independent repo |
| LRN-003 | Over-engineered before confirming real need | Phase 0 three-question lock |
| LRN-004 | Research notes mixed with skill docs | `raw/` vs `references/` separation |
