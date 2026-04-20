# Skill Factory

> **"The first industrial revolution was marked by using machines to make machines."**
> **Skill Factory is the machine that makes skills.**

A **meta-skill** for WorkBuddy/Claw that automates the full lifecycle of skill creation — from a fuzzy idea to a polished, versioned, distributable package.

[![Version](https://img.shields.io/badge/version-2.1.0-blue.svg)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

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
- **Bilingual README standard** — skills built here are globally distributable

It's not about what Claw _can_ do — it's about turning an unbounded capability into a **reliable, high-quality pipeline**. The process is the product.

## How to Use

Just send Claw an idea:

```
新 skill：[name]，[1-2 sentences]，[source URL (optional)]
```

Or upgrade an existing skill:

```
skill升级：[name]，[what to add]，[new source URL (optional)]
```

Claw enters Phase 0 immediately. You answer 3 questions, then the factory runs.

## What's Inside

```
skill-factory/
├── SKILL.md         # Full SOP — four phases, version management, publishing spec
├── README.md        # This file
├── CHANGELOG.md     # Version history
├── LICENSE          # MIT
├── inbox/           # Drop zone for raw ideas
└── wip/             # Active work-in-progress
    └── <skill>/
        ├── BRIEF.md
        ├── raw/
        └── draft/
```

## Skills Built With This Factory

| Skill | Version | Status |
|-------|---------|--------|
| [harness](../harness) | v1.2.0 | ✅ GitHub-ready |
| [nova-reader](../nova-reader) | v1.1.0 | ✅ GitHub-ready |

---

---

## 中文说明

> **"第一次工业革命的标志，是用机器来制造机器。**
> **Skill Factory，就是那台制造技能的机器。"**

这是一个用于 WorkBuddy/Claw 的**元技能（meta-skill）**，提供从模糊想法到可发行 skill 的全链路标准化流程。

### 它解决什么问题？

每次制作 skill 时，常见的痛点：

- 需求没说清楚就开始干，做到一半发现方向不对
- 蒸馏完文章，发现漏了关键内容，还得回头重看
- 文件散落各处，想发布到 GitHub 才发现结构一团糟
- v1.0 做完了，不知道什么时候该升级，怎么管理版本

Skill Factory 用**四阶段 SOP** 系统性地解决以上全部问题。

### 核心差异化

- **Phase 0 三问锁定** — 开工前三个问题锁死需求，防止过度工程化
- **强制原文二次核对** — 蒸馏完必须回到原始来源比对，防止知识遗漏
- **语义化版本管理** — 清楚区分 MAJOR（范式重构）/ MINOR（增量添加）/ PATCH（修小问题）
- **每个 skill 独立 repo** — 从第一天起就是发行级结构
- **双语 README 标准** — 中英双语，面向全球社区分发

### 使用方式

发给 Claw 一个想法即可：

```
新 skill：[名字]，[1-2句描述]，[来源链接（可选）]
```

或升级已有 skill：

```
skill升级：[名字]，[要加什么]，[新来源链接（可选）]
```

Claw 会立刻进入 Phase 0，回答 3 个问题后，流水线自动运转。

### 版本历史

见 [CHANGELOG.md](./CHANGELOG.md)

### 开源协议

MIT — 欢迎 fork、改造和贡献。
