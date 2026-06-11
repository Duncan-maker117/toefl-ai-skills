# TOEFL AI Skills · Free v1.0

一套给 **Claude / Cursor / Windsurf / WorkBuddy** 用的托福备考 AI skills。
**免费版先上手，付费版做闭环。** 复制到本地 skills 目录，重启 IDE，就能直接开始练。

![WeChat QR](./assets/wechat-qr.jpg)

> 想直接拿 **v4.0 完整版**：微信 `19138384041`，备注 **托福 v4**。  
> 当前价格：**99 元 / 份**

---

## 这是什么

这个仓库公开的是 **v1.0 免费引流版**，包含 3 个最小可用的托福 AI skills：

| Skill | 作用 | 适合场景 |
|------|------|---------|
| `/toefl` | 托福备考总入口，负责摸底、路由、给训练建议 | 不知道先练什么 |
| `/toefl-writing` | 学术讨论写作批改、审题、练习 | 想改作文、想拆题 |
| `/toefl-reading` | 阅读精读、错题拆解、同义替换提取 | 想分析为什么错 |

这不是源码项目，也不是网站模板。**它就是能直接安装到 AI IDE 里的 prompt skill 包。**

---

## 适用平台

- Claude Code
- Cursor
- Windsurf
- WorkBuddy

只要你的工具支持本地 skill / prompt 目录，这套结构就能直接复用。

---

## 免费版能做什么

免费版主打一个 **先用上、先感受到专业度**：

- `/toefl` 先问目标等级、考试时间、今天想练什么，再把你路由到对应模块
- `/toefl-writing` 按 **Development / Organization / Language Use / Task Fulfillment** 四维批改
- `/toefl-reading` 按题型拆解错因，强制输出 **同义替换词表**
- 全部内容 **零依赖、纯文本、无安装包、无数据库**
- 中文解释逻辑，保留必要英文术语

如果你只想先试试“AI skill 到底值不值”，这个版本已经够你开箱。

---

## 安装

### 1. 克隆仓库

```bash
git clone https://github.com/Duncan-maker117/toefl-ai-skills.git
cd toefl-ai-skills
```

### 2. 复制到你的 skills 目录

```bash
# macOS / Linux
cp -r toefl toefl-writing toefl-reading ~/.claude/skills/
```

```powershell
# Windows PowerShell - Claude Code
Copy-Item -Recurse .\toefl, .\toefl-writing, .\toefl-reading $env:USERPROFILE\.claude\skills\
```

```powershell
# Windows PowerShell - WorkBuddy
Copy-Item -Recurse .\toefl, .\toefl-writing, .\toefl-reading $env:USERPROFILE\.workbuddy\skills\
```

Cursor / Windsurf 如果使用自定义 skills 目录，把这 3 个文件夹复制进去就行。

### 3. 重启你的 IDE

重启后直接输入：

```text
/toefl
```

---

## 怎么用

### 场景 1：先摸底，再分流

```text
你：/toefl
AI：先问你目标等级、考试时间、今天想练什么
AI：再自动路由到 /toefl-writing 或 /toefl-reading
```

### 场景 2：直接批改作文

```text
你：/toefl-writing
你：[粘贴题目 + 你的作文]
AI：
- 四维评分
- 逐句指出问题
- 给提分优先级
```

### 场景 3：分析阅读错题

```text
你：/toefl-reading
你：[粘贴文章 + 题目 + 你的答案 + 标准答案]
AI：
- 逐题拆错因
- 给定位句
- 提取同义替换词表
```

---

## 仓库结构

```text
toefl-ai-skills/
├── toefl/SKILL.md
├── toefl-writing/SKILL.md
├── toefl-reading/SKILL.md
├── assets/wechat-qr.jpg
├── README.md
└── LICENSE
```

每个 skill 都是一个文件夹 + 一个 `SKILL.md`。平台通过 frontmatter 里的 `name` 和 `description` 识别它。

---

## v1.0 vs v4.0

这个仓库只公开 **v1.0 免费版**。如果你想要更完整的训练闭环，升级到 **v4.0 付费版**。

| 能力 | v1.0 免费版 | v4.0 付费版 |
|------|------------|------------|
| Skills 数量 | 3 个 | 7 个 |
| 写作批改 | 学术讨论 | 学术讨论 + 句子重组 + 电邮写作 |
| 阅读训练 | 学术短文 | 学术短文 + 日常文本 + MST 适配 |
| 口语训练 | 不包含 | `/toefl-speaking` |
| 听力训练 | 不包含 | `/toefl-listening` |
| 词汇训练 | 不包含 | `/toefl-vocab` |
| Dashboard | 不包含 | `/toefl-dashboard` |
| 跨会话记忆 | 不包含 | `~/.toefl/` 数据持久化 |
| 错题追踪 | 单次分析 | 自动聚合高频错误 |
| 进度可视化 | 不包含 | 趋势图 / 雷达图 / 错题热力图 |
| 备份恢复 | 不包含 | 支持 backup / restore |

**一句话区别：**
免费版负责你先用起来。付费版负责把训练记录、错题数据、能力趋势、完整学科都串成闭环。

---

## 升级 v4.0

如果你要的是更像“托福 AI 教练系统”的版本，而不是 3 个基础 skill，直接走这里：

- **微信**：`19138384041`
- **备注**：`托福 v4`
- **价格**：`99 元 / 份`
- **交付**：完整 zip 包 + 安装说明

![WeChat QR](./assets/wechat-qr.jpg)

适合这些人：

- 想要 **口语 / 听力 / 词汇 / Dashboard** 全覆盖
- 想把练习记录、错题标签、趋势变化沉淀下来
- 不想每次都从零开始对话
- 想把 AI 从“陪聊”变成“训练系统”

---

## FAQ

### 适合 2026 新制 TOEFL 吗？

适合。免费版和付费版的文案都按 **2026 新制 TOEFL** 去设计，免费版覆盖基础写作与阅读训练，付费版再补全完整题型。

### 买完发什么？

发完整压缩包和安装说明。Windows / macOS / Linux 都能装。

### 为什么免费版只放 3 个？

因为这个仓库的目标是 **低门槛试用 + 高质量引流**。把所有核心资产全摊开，只会把你我都变成慈善家。

### 我可以自己改吗？

可以。免费版是 MIT License，拿去改、拿去学、拿去二开都行。

---

## 反馈

提 issue：<https://github.com/Duncan-maker117/toefl-ai-skills/issues>

如果你是来买完整版的，别绕路提 issue，直接扫上面的二维码就行。
