<div align="center">

# 🎯 TOEFL AI Skill — 2026 新制托福备考 AI 教练

</div>

**TOEFL AI Skill** 是一个基于 AI 的 **托福 iBT 备考教练系统**，支持 **2026 新制自动适配、四科摸底诊断、写作批改、口语训练、阅读分析、听力练习、词汇学习、Dashboard 复盘**。/**TOEFL AI Skill** is an **AI-powered TOEFL iBT prep coach** with **2026 new-format support, four-skill diagnostic, writing correction, speaking practice, reading analysis, listening training, vocabulary learning, and Dashboard review**.

> 🎁 v1.0 Lite 永久免费开源 · 🚀 v4.0 Pro 完整版加微信 `19138384041` 获取
>
> 每天 2 小时，自学托福不乱练。

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![TOEFL iBT 2026](https://img.shields.io/badge/TOEFL-iBT_2026_新制-blueviolet)](https://www.ets.org/toefl)
[![Version](https://img.shields.io/badge/version-4.0_Pro%20%7C%201.0_Lite-success)](#-版本对比)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Stars](https://img.shields.io/github/stars/Duncan-maker117/toefl-ai-skill?style=social)](../../stargazers)
[![Forks](https://img.shields.io/github/forks/Duncan-maker117/toefl-ai-skill?style=social)](../../network/members)
[![Made With](https://img.shields.io/badge/Made_with-Claude_+_WorkBuddy-ff6b6b)](#-致谢)

[English](#-english) | [简体中文](#-简体中文) | [功能模块](#-功能模块) | [快速开始](#-快速开始) | [版本对比](#-版本对比) | [微信咨询](#-联系作者)

</div>

---

## 🌟 这是什么？

**TOEFL AI Skill** 是一套跑在 AI 客户端（Claude / WorkBuddy / Cursor / Codex CLI）里的 **托福备考 AI 教练系统**。

它不是英语课、不是题库、不是机经。它是**一个严格但公正的托福老师**——

- ✅ **数据驱动**：用 CEFR 等级分（1.0-6.0）管理你的备考进度
- ✅ **智能路由**：先摸底，自动把每天 2 小时拆给最弱的一科
- ✅ **闭环训练**：训练 → 记录 → Dashboard 复盘 → 明日计划
- ✅ **2026 新制适配**：67-85 分钟新题型、MST 自适应、1.0-6.0 等级分全支持

> 🎁 **v1.0 Lite 免费开源**——你看到的就是。
> 🚀 **v4.0 Pro** 完整版覆盖 7 大模块：添加微信 `19138384041` 获取。

---

## 🎬 30 秒看懂系统闭环

```
                ┌─────────────────────┐
                │  🎯 目标分 + 考试日  │
                └──────────┬──────────┘
                           ▼
                ┌─────────────────────┐
                │   🔍 四科摸底诊断   │
                └──────────┬──────────┘
                           ▼
                ┌─────────────────────┐
                │  🚦 智能路由（最弱科）│
                └────┬────┬────┬──────┘
                     ▼    ▼    ▼    ▼
                🗣️口语 ✍️写作 📖阅读 🎧听力
                     │    │    │    │
                     └────┴────┴────┘
                           ▼
                ┌─────────────────────┐
                │  💾 训练数据落盘    │
                │  ~/.toefl/*.json    │
                └──────────┬──────────┘
                           ▼
                ┌─────────────────────┐
                │  📊 Dashboard 复盘  │
                │  趋势 + 错词 + 拼写 │
                └──────────┬──────────┘
                           ▼
                ┌─────────────────────┐
                │  📅 明日计划生成    │
                └─────────────────────┘
```

---

## ✨ 功能模块

| 模块 | v1.0 Lite（开源） | v4.0 Pro |
|------|:-----------------:|:--------:|
| 🔍 **摸底路由** | ✅ CEFR 等级换算 | ✅ + 4 科动态诊断 |
| ✍️ **写作批改** | ✅ 学术讨论写作 | ✅ + 句子重组 + 电邮 + 学术讨论 |
| 📖 **阅读分析** | ✅ 学术短文 | ✅ + Complete the Words + 日常阅读 |
| 🗣️ **口语训练** | — | ✅ 跟读句子 ×7 + 面试问答 ×4 |
| 🎧 **听力训练** | — | ✅ 听后选答 + 对话 + 公告 + 学术短讲 |
| 📚 **词汇系统** | — | ✅ 错词本 + 间隔重复 + 拼写专项 |
| 📊 **Dashboard** | — | ✅ 4 科趋势 + 弱项雷达 + 日历热力图 |
| 💾 **数据持久化** | — | ✅ `~/.toefl/` 跨会话记忆 |

---

## 🆕 2026 新制 TOEFL iBT 适配

> ETS 自 **2026 年 1 月 21 日**起对 TOEFL iBT 进行全面改制，本系统已 100% 适配。

| 维度 | 旧制 (2023-2025) | **新制 (2026 起)** |
|------|------------------|-------------------|
| 总时长 | ~116 分钟 | **~67-85 分钟** ⚡ |
| 科目顺序 | R → L → S → W | **R → L → W → S** |
| 计分制 | 0-120 | **1.0-6.0 等级分**（CEFR 直接映射）|
| 自适应 | 固定 | **阅读+听力 MST 多阶段自适应** |
| 阅读 | 长文章 ×3-4 | Complete the Words + 日常阅读 + 学术短文 |
| 听力 | 长讲座 ×3-4 | 听后选答 + 对话 + 公告 + 学术短讲 |
| 写作 | 综合写作 + 讨论 | **句子重组 ×10 + 电邮 + 学术讨论** |
| 口语 | Task 1-4 | **跟读句子 ×7 + 面试式问答 ×4** |

---

## 🚀 快速开始

### 安装 v1.0 Lite（免费开源）

#### 方式 A：Claude / WorkBuddy 用户
把 `toefl-v1/` 文件夹复制到：
- **Claude**：项目根目录的 `skills/` 下
- **WorkBuddy**：`~/.workbuddy/skills/` 下

然后在对话中输入：
```
/toefl-v1
```
或直接说「托福 lite」「托福备考」。

#### 方式 B：Cursor / Codex CLI / 其他 AI 客户端
将 `toefl/SKILL.md` 内容粘贴到项目根的 `AGENTS.md` 或 `CLAUDE.md`，作为系统提示词加载。

### 系统要求
- 支持自定义 Skill 的 AI 客户端（Claude 3.5+ / WorkBuddy / Cursor / Codex CLI）
- 无需 API Key（取决于你使用的客户端）
- 数据目录：v4.0 Pro 自动创建 `~/.toefl/`

---

## 📖 使用示例

### 1️⃣ 第一次使用
> **你**：/toefl-v1
>
> **AI**：你好，我是你的托福教练。开始之前我要先问 3 个问题：
> 1. 你的目标等级是多少？（1.0-6.0）
> 2. 考试日期？
> 3. 当前水平？（四级/六级/雅思对标）

### 2️⃣ 写作批改
> **你**：帮我批改这篇学术讨论写作
> [粘贴你的回复]
>
> **AI**：等级评分：4.0 → 改进建议 3 条 → 高分句型 2 句 → 错词加入词库

### 3️⃣ 阅读分析
> **你**：分析这篇学术短文
> [粘贴短文]
>
> **AI**：文章结构拆解 → 核心观点 → 长难句 ×3 → 学术词汇表

---

## 📁 项目结构

```
toefl-ai-skill/
├── README.md                          # 你正在看的
├── LICENSE                            # MIT
├── toefl-v1/                          # v1.0 Lite Skill（开源）
│   └── SKILL.md
├── toefl-v4/                          # v4.0 Pro Skill（付费）
│   └── SKILL.md
├── docs/
│   ├── 【展示首页】-TOEFL AI Skill 备考系统.md
│   ├── 【展示白板】-TOEFL AI Skill 本地闭环.canvas
│   └── 2026-新制改制说明.md
├── examples/
│   ├── writing-sample.md
│   ├── reading-sample.md
│   └── dashboard-preview.png
└── .github/
    ├── ISSUE_TEMPLATE/
    └── PULL_REQUEST_TEMPLATE.md
```

---

## 🤝 贡献指南

欢迎 PR！特别是：
- 📝 错词本扩充（高频托福学术词汇）
- 🐛 反馈 2026 新制题型的训练效果
- 🌐 翻译 README 到更多语言
- 📊 分享你的 Dashboard 复盘数据

提交前请先开 Issue 讨论。

---

## 📜 许可证

本项目采用 **MIT 许可证** — 详见 [LICENSE](LICENSE) 文件。

> 注意：v1.0 Lite 永久免费开源；v4.0 Pro 为付费版本（添加微信获取）。

---

## 💬 联系作者

- **微信**：`19138384041`（有偿 · 备注「TOEFL Pro」获取 v4.0 完整版）

  <p align="left">
    <img src="./assets/wechat-qr-only.jpg" alt="微信 19138384041" width="180" />
  </p>

- **GitHub Issues**：[本仓库 Issues](../../issues)
- **品牌**：启扬有道

---

## 🙏 致谢

- 灵感来源：[YANZHANLIN/ielts-claude-skills](https://github.com/YANZHANLIN/ielts-claude-skills)
- 数据驱动方法论：CEFR 欧洲语言共同参考框架
- AI 客户端：Claude / WorkBuddy / Cursor / Codex CLI

---

<div align="center">

### ⭐ 如果这个项目帮到了你，请点一个 Star — 这是开源作者最大的动力

[![Star History Chart](https://img.shields.io/github/stars/Duncan-maker117/toefl-ai-skill?style=social)](../../stargazers)

**Made with ❤️ by 启扬有道 · Duncan (Yang Lu)**

</div>

---

<a name="-english"></a>

## 🌐 English

# TOEFL AI Skill — TOEFL iBT AI Coach System

**A data-driven TOEFL iBT prep system running inside your AI client (Claude / WorkBuddy / Cursor / Codex CLI).**

### What's inside?
- 🎯 **CEFR-aligned scoring** (1.0-6.0, ETS 2026 new format)
- 🔍 **Diagnostic routing** — auto-assigns daily 2h to your weakest skill
- ✍️ **Writing** (Academic Discussion / Sentence Build-up / Email)
- 📖 **Reading** (Complete the Words / Daily Reading / Academic Passages)
- 🗣️ **Speaking** (Read Aloud ×7 + Interview Q&A ×4)
- 🎧 **Listening** (听后选答 + Dialogues + Announcements + Mini-lectures)
- 📚 **Vocabulary** + 📊 **Dashboard**

### 2026 New TOEFL iBT Format Support
ETS redesigned TOEFL iBT starting **Jan 21, 2026**:
- ⏱️ 67-85 min (down from ~116 min)
- 📐 1.0-6.0 proficiency scale (mapped to CEFR)
- 🧠 MST adaptive in Reading & Listening
- 🔄 Order: R → L → W → S

### Quick Start
1. Copy `toefl-v1/` to your AI client's `skills/` folder
2. Type `/toefl-v1` or "TOEFL prep"
3. Answer 3 onboarding questions (target score / test date / current level)

### Versions
- **v1.0 Lite (this repo)** — Free, MIT, writing + reading + routing
- **v4.0 Pro** — All 7 modules, Dashboard, persistent data · WeChat: `19138384041`

### Keywords (for search)
`toefl` `toefl-ibt` `toefl-2026` `toefl-cefr` `toefl-prep` `toefl-ai-coach`
`toefl-writing` `toefl-speaking` `toefl-listening` `toefl-reading`
`toefl-vocabulary` `ai-tutor` `english-learning` `study-abroad`
`claude-skill` `anthropic-skill` `workbuddy`

### License
MIT — see [LICENSE](LICENSE)
