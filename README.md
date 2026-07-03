# 🏗️ Super Assistant Framework

> 超级助理 Agent 的完整系统脚手架

一个可复用的 Agent 系统框架，只搭骨架、装方法、留空位——不含任何个人设定、偏好或知识库沉淀。

## ✨ 它是什么

Super Assistant Framework 是一套经过实战验证的 Agent 架构方法论，将超级助理系统拆解为 7 层结构：

```
┌─────────────────────────────────┐
│  ① 基础设定层  SOUL / TOOLS     │  身份、性格、工具经验
│  ② 记忆层      MEMORY / SECRET   │  行为规则、状态锚点、凭证
│  ③ 知识库层    WIKI              │  Ingest → Query → Lint 三阶段
│  ④ 产物层      各类输出目录       │  晨读、追踪、报告
│  ⑤ 素材库层    分主题知识库       │  投研 / 智序 / 教学 / 自媒体
│  ⑥ 日志层      INDEX / LOG       │  入库索引、运行日志
│  ⑦ 扩展层      skills / scripts  │  技能、脚本、外部工具
└─────────────────────────────────┘
```

**设计灵感**：源自 [Karpathy LLM Wiki 模式](https://github.com/karpathy/LLMWiki)，将知识管理从"文件堆叠"升级为"结构化流转"。

## 🚀 快速开始

### 前提条件
- 一个 [Coze](https://www.coze.cn) Agent 账号
- 基本的 Markdown 编辑能力

### 7 步 Setup

1. **安装本 Skill** — 搜索虾评「超级助理框架」或下载本 repo
2. **创建目录结构** — 按 SKILL.md 中的 7 层架构创建文件夹
3. **填充身份文件** — 用 templates/ 中的模板填写 SOUL.md、USER.md
4. **配置 WIKI 规则** — 将 WIKI.md 模板复制到工作目录，按需调整
5. **建立记忆系统** — 用 MEMORY.md 模板初始化行为规则和状态锚点
6. **设置自动化日程** — 按指南配置晨读、追踪、雷达等周期任务
7. **持续迭代** — 使用框架，沉淀经验，优化规则

📖 详细指南请阅读 [`guides/usage-guide.md`](guides/usage-guide.md)

## 📁 项目结构

```
super-assistant-framework/
├── SKILL.md                    # 主指令文件（架构图 + Setup 流程）
├── README.md                   # 本文件
├── guides/
│   └── usage-guide.md          # 完整使用指南（7 章）
└── templates/                  # 空白模板文件
    ├── SOUL.md                 # 身份与性格设定
    ├── USER.md                 # 用户画像
    ├── MEMORY.md               # 行为规则与状态锚点
    ├── TOOLS.md                # 工具使用经验
    ├── WIKI.md                 # 知识库管理规范
    ├── SECRET.md               # 敏感凭证
    ├── heartbeat_daily.md      # 每日心跳检查清单
    ├── INDEX.md                # 入库索引模板
    └── LOG.md                  # 运行日志模板
```

## 🔑 核心设计理念

- **骨架优先**：只提供结构和规则，不预设内容
- **方法沉淀**：将操作规范（Ingest/Lint/入库即清）写成规则而非一次性指令
- **分层解耦**：身份、记忆、知识、产物各层独立，互不污染
- **持续进化**：框架随使用自然生长，而非一次性配置

## 🛠️ 推荐必装 Skill

| Skill | 用途 | 必要性 |
|-------|------|--------|
| skill_builder | 自维护技能创建与迭代 | 必装 |
| topic_tracking | 话题追踪与定期简报 | 必装 |
| SkillSpector | 安全扫描与审查门禁 | 必装 |

更多选装推荐见使用指南。

## 📜 License

MIT License — 自由使用、修改和分发，请保留原作者署名。

## 🙏 致谢

- 架构灵感源自 [Andrej Karpathy 的 LLM Wiki 模式](https://github.com/karpathy/LLMWiki)
- 工程方法论借鉴了 [Superpowers](https://github.com/NexTechAI/superpowers) 和 [Headroom](https://github.com/headroomHQ/headroom) 项目
- 安全审查工具 [SkillSpector](https://github.com/skill-spector/skill-spector)

---

Made with ❤️ by 程留白 · Powered by [Coze](https://www.coze.cn)
