# Skill Factory（中文版）

> **丢个 idea 进去。10 分钟出来一个版本化、可发布的 skill。**

把任何一个有用的 prompt、工作流或文档，变成一个可复用的 agent skill——结构化、版本化、ClawHub 就绪。

[![Version](https://img.shields.io/badge/version-2.5.0-blue.svg)](CHANGELOG.md)
[![Stars](https://img.shields.io/badge/dynamic/json?color=yellow&label=stars&query=stargazers_count&url=https://api.github.com/repos/zhelunSun/skill-factory)](https://github.com/zhelunSun/skill-factory)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![English](https://img.shields.io/badge/README-English-blue.svg)](README.md)

---

## Before / After

```
BEFORE（痛点）：
用户："Agent 输出太啰嗦，能精简但不丢技术细节吗？"
Agent：写了一堆，忘了版本号，没有 CHANGELOG，不知道怎么发布。
结果：散乱文件。无版本。无 README。ClawHub？算了。

AFTER（10 分钟）：
新 skill：token-saver，压缩冗余，保留技术细节
→ BRIEF.md（锁定需求）
→ SKILL.md（282 行，触发词，黄金法则）
→ CHANGELOG.md（版本管理）
→ README.md + README_zh.md（双语）
→ LICENSE（MIT）
→ v1.0.0 tag
→ ClawHub 就绪
```

**从 idea 到发布完成的 skill。每个文件。每个版本。10 分钟。**

---

## 为什么有效

Skill Factory 不是"更好的 prompt"。它是**一套结构化的流水线**，任何 AI Agent 都可以遵循。

| 问题 | 没有 Skill Factory | 有了 Skill Factory |
|------|-------------------|-------------------|
| idea 模糊 | Agent 瞎猜范围，过度工程 | **Phase 0 三问锁定** |
| 遗漏知识 | 蒸馏过程漏掉概念 | **强制重读源材料** |
| 文件散落 | 无法发布 | **独立 repo，每个 skill 一个** |
| v1.0 停滞 | 没有升级路径 | **结构化 1→N 工作流** |
| 版本混乱 | "v2 最终版 最终修订" | **语义化版本规则** |

"用机器制造机器"不是隐喻——是产品本身。

---

## 工厂产出

用 Skill Factory 创建、正在生产环境运行的 skill：

| Skill | 做什么 |
|-------|--------|
| **[harness](https://github.com/zhelunSun/harness)** v1.2 | Agent-first 工程知识库 |
| **[nova-reader](https://github.com/zhelunSun/nova-reader)** v1.1 | 学术论文深度阅读工作流 |

---

## 快速安装

```bash
# 从 ClawHub（推荐）
claw skill install skillfactory

# 从 GitHub
git clone https://github.com/zhelunSun/skill-factory.git ~/.workbuddy/skills/skillfactory
```

重启 session。skill 自动加载。

---

## 快速开始

对你的 AI Agent 说：

```
新 skill：[名字]，[1-2句说明]，[来源 URL（可选）]
```

Agent 立刻进入 **Phase 0**。30 秒锁定需求。10 分钟 skill 发布。

---

## 怎么干的

**四阶段。零猜。**

| 阶段 | 名称 | 耗时 | 产出 |
|------|------|------|------|
| 0 | 捕获 | 30秒 | `BRIEF.md` — 锁定需求 |
| 1 | 采集 | 1-2分 | `raw/` — 自动拉取源材料 |
| 2 | 蒸馏 | 5分 | `SKILL.md` + `references/` |
| 3 | 发布 | 2分 | 版本化 repo |

完整 SOP 见 [SKILL.md](SKILL.md)。

---

## 维护已有 Skill（1→N）

不只是 0→1，还有结构化升级：

```
升级 skill：[名字]，[变更要求]，[新来源 URL（可选）]
```

1. **检查** — 读取现有状态
2. **分类** — 判断 PATCH / MINOR / MAJOR
3. **提案** — 改动前先生成计划
4. **执行** — 更新文件、CHANGELOG、版本
5. **总结** — 报告变更

---

## 仓库结构

```
skill-factory/
├── SKILL.md
├── README.md
├── README_zh.md     # 本文件
├── CHANGELOG.md
├── LICENSE          # MIT
├── inbox/           # idea 投放处
└── wip/             # 进行中的工作
```

---

## 协议

MIT — 改它、用建你的工厂。
