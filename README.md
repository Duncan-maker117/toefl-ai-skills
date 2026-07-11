# TOEFL AI Skills

<p align="center">
  <strong>Free v1.0 for Claude / Cursor / Windsurf / WorkBuddy</strong><br/>
  托福备考 AI skills 免费版。复制到本地 skills 目录，重启 IDE，马上开练。
</p>

<p align="center">
  <img src="./assets/wechat-qr-only.jpg" alt="WeChat QR" width="180" />
</p>

<p align="center">
  想拿 <strong>v4.0 完整版</strong>：微信 <code>19138384041</code>，备注 <strong>托福 v4</strong>，当前 <strong>99 元 / 份</strong>
</p>

---

## 这是什么

这个仓库公开的是 **TOEFL AI Skills 免费版 v1.0**。核心目标很简单：让你先低门槛装上、先用起来、先判断这套训练方式适不适合自己。

免费版包含 3 个最常用的托福训练 skills：

| Skill | 作用 | 适合场景 |
|------|------|---------|
| `/toefl` | 托福备考总入口，负责摸底、路由、给训练建议 | 不知道先练什么 |
| `/toefl-writing` | 学术讨论写作批改、审题、练习 | 想改作文、想拆题 |
| `/toefl-reading` | 阅读精读、错题拆解、同义替换提取 | 想分析为什么错 |

这不是网站源码，也不是复杂项目。它就是一套能直接装进 AI IDE 的 prompt skills。

---

## 适用平台

- Claude Code
- Cursor
- Windsurf
- WorkBuddy

只要你的工具支持本地 skills / prompts 目录，这套结构就能直接使用。

---

## 免费版能做什么

免费版主打一个：**先感受到训练质量，再决定要不要升级。**

- `/toefl` 先问目标等级、考试时间、今天想练什么，再路由到合适模块
- `/toefl-writing` 按 **Development / Organization / Language Use / Task Fulfillment** 四维批改
- `/toefl-reading` 按题型拆解错因，固定输出 **同义替换词表**
- 全部内容都是 **零依赖、纯文本、可直接复制**
- 中文解释逻辑，保留必要英文术语

如果你现在只是想验证“AI skill 到底能不能真帮我备考”，这个版本已经够你上手。

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

Cursor / Windsurf 如果使用自定义 skills 目录，把这 3 个文件夹复制进去即可。

### 3. 重启 IDE

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
├── assets/wechat-qr-only.jpg
├── README.md
└── LICENSE
```

每个 skill 都是一个文件夹 + 一个 `SKILL.md`。平台通过 frontmatter 里的 `name` 和 `description` 识别它。

---

## 免费版 vs 完整版

> 🟦 **免费版**：适合先体验方法和训练逻辑。  
> 🟧 **完整版**：适合想把练习记录、错题追踪、能力趋势和完整科目训练都串起来的人。

<p align="center">
  <strong>🟦 免费版 = 先装上、先体验、先验证有效性</strong><br/>
  <strong>🟧 完整版 = 诊断 + 训练 + 记录 + 复盘 的完整闭环</strong>
</p>

| 能力 | 🟦 v1.0 免费版 | 🟧 v4.0 完整版 |
|------|---------------|---------------|
| Skills 数量 | 3 个 | 8 个 |
| 总入口路由 | ✅ `/toefl` | ✅ `/toefl` |
| 诊断规划 | ❌ 不包含 | ✅ `/toefl-diagnose` |
| 写作批改 | 学术讨论 | 学术讨论 + 句子重组 + 电邮写作 |
| 阅读训练 | 学术短文 | 学术短文 + 日常文本 + MST 适配 |
| 口语训练 | ❌ 不包含 | ✅ `/toefl-speaking` |
| 听力训练 | ❌ 不包含 | ✅ `/toefl-listening` |
| 词汇训练 | ❌ 不包含 | ✅ `/toefl-vocab` |
| 进度看板 | ❌ 不包含 | ✅ `/toefl-dashboard` |
| 跨会话记忆 | ❌ 不包含 | ✅ `~/.toefl/` 数据持久化 |
| 错题追踪 | 单次分析 | 自动聚合高频错误 |
| 进度可视化 | ❌ 不包含 | 趋势图 / 雷达图 / 错题热力图 |
| 备份恢复 | ❌ 不包含 | 支持 backup / restore |

---

## 升级 v4.0

如果你想要的不是单次问答，而是一套更完整的托福训练系统，可以直接升级到 **v4.0 完整版**。

<p align="center">
  <img src="./assets/wechat-qr-only.jpg" alt="WeChat QR" width="220" />
</p>

<p align="center">
  微信 <code>19138384041</code> ｜ 备注 <strong>托福 v4</strong> ｜ <strong>99 元 / 份</strong>
</p>

完整版更适合这些情况：

- 你想把 **口语 / 听力 / 词汇 / Dashboard** 一次补齐
- 你希望把练习记录、错题标签、趋势变化沉淀下来
- 你不想每次都从零开始对话
- 你想让 AI 更像训练系统，而不只是临时答疑工具

---

## FAQ

### 适合 2026 新制 TOEFL 吗？

适合。免费版和完整版都按 **2026 新制 TOEFL** 去设计。免费版覆盖基础写作与阅读训练，完整版进一步补全完整题型和训练闭环。

### 买完发什么？

发完整压缩包和安装说明。Windows / macOS / Linux 都能装。

### 为什么免费版先放 3 个？

因为大多数人第一次接触这类 AI skill，更需要的是 **先快速装上、先体验有效性**，而不是一上来就面对一整套复杂功能。免费版先解决“能不能用”，完整版再解决“能不能长期高效用”。

---

## 反馈

提 issue：<https://github.com/Duncan-maker117/toefl-ai-skills/issues>

如果你是想直接拿完整版，扫上面的二维码会更快。
