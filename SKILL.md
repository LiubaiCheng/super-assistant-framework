---
name: super-assistant-framework
description: 超级助理Agent的完整系统脚手架。包含7层架构目录结构、WIKI知识库管理规则、工程纪律方法论、自动化日程模板、setup引导流程和使用指南。当用户想要搭建一个拥有知识库管理、晨读信息摄入、信号追踪、周期巡检等自动化能力的超级助理Agent时使用此技能；当用户提到"搭助理框架""初始化超级助理""搭建知识库Agent""复制助理系统"等意图时触发。
---

# 超级助理框架

把一个普通Agent变成拥有知识库、自动化日程、周期巡检、信号追踪等能力的超级助理。

本技能是纯脚手架——只搭骨架、装方法、留空位，不含任何个人内容。

## 架构概览

超级助理由7层组成，由内向外：

```
┌─ 第1层：身份层 ──────────────────────┐
│  SOUL.md / USER.md / SECRET.md       │
│  Agent是谁、为谁服务、守什么密        │
└──────────────────────────────────────┘
          ↓
┌─ 第2层：记忆层 ──────────────────────┐
│  MEMORY.md / recent_memory/          │
│  长期规则 + 状态锚点 + 详细记录       │
└──────────────────────────────────────┘
          ↓
┌─ 第3层：知识库层 ────────────────────┐
│  WIKI.md / 素材库(多个) / raw/       │
│  管理规则 + 知识页面 + 原文备份       │
└──────────────────────────────────────┘
          ↓
┌─ 第4层：自动化层 ────────────────────┐
│  Calendar日程（晨读/心跳/周审视/追踪）│
│  定时触发 + 工单驱动                  │
└──────────────────────────────────────┘
          ↓
┌─ 第5层：工具经验层 ──────────────────┐
│  TOOLS.md                            │
│  方法论 + 工具使用经验 + 安全规范     │
└──────────────────────────────────────┘
          ↓
┌─ 第6层：技能层 ──────────────────────┐
│  .skills/ + skills/                  │
│  平台技能 + 自安装技能                │
└──────────────────────────────────────┘
          ↓
┌─ 第7层：输出层 ──────────────────────┐
│  晨读报告 / 素材库页面 / 追踪报告     │
│  所有自动化流程的最终交付物            │
└──────────────────────────────────────┘
```

## Setup流程

当用户确认使用本框架后，按以下步骤初始化：

### Step 1：创建目录结构

```
mkdir -p 基础设定
mkdir -p recent_memory/project recent_memory/decision recent_memory/todo
mkdir -p raw/articles raw/reports raw/papers
mkdir -p 用户上传
mkdir -p .tmp
mkdir -p InkWell晨读
mkdir -p 热点资讯追踪
```

素材库目录根据用户场景创建（见Step 3）。

### Step 2：植入模板文件

将 `templates/` 目录下的模板文件复制到对应位置：

| 模板文件 | 目标位置 | 说明 |
|----------|----------|------|
| SOUL.md | 基础设定/SOUL.md | Agent身份与性格 |
| USER.md | USER.md | 用户画像 |
| MEMORY.md | MEMORY.md | 记忆框架 |
| TOOLS.md | 基础设定/TOOLS.md | 工具经验与方法论 |
| WIKI.md | WIKI.md | 知识库管理规则 |
| SECRET.md | SECRET.md | 凭证与密钥 |
| heartbeat_daily.md | heartbeat_daily.md | 每日心跳检查清单 |
| INDEX.md | INDEX.md | 总索引 |
| LOG.md | LOG.md | 总日志 |

### Step 3：配置素材库

询问用户关注哪些领域，按需创建素材库目录。每个素材库包含：

```
{素材库名}/
├── README.md      # 库说明
├── index.md       # 内容目录
├── log.md         # 操作日志
└── *.md           # 知识页面（后续入库产生）
```

将素材库信息填入 INDEX.md 和 WIKI.md 的素材库定位表。

### Step 4：确认必装技能

告知用户3个必装技能及其用途：

1. **skill_builder** — 技能的创建/编辑/发布，框架自维护
2. **topic_tracking** — 追踪+日报核心自动化，晨读和信号追踪依赖
3. **SkillSpector**（工具型）— 安全审查门禁，装在/tmp/

引导用户确认安装。

### Step 5：推荐选装技能

根据用户场景推荐技能组：

- **内容创作组**：wechat-svg / create-ppt / viral-short-story
- **教学组**：lesson-plan-generator / exam-grading
- **数据处理组**：pdf / docx / excel_master
- **可视化组**：echart / drawio-generator / bar-chart-race-generator
- **飞书协作组**：lark_cli
- **多媒体组**：media-processor / lanshu-animated-architecture-diagram
- **平台工具组**：using-coze-cli / coze-mini-expert / agent-browser / skill-assistant

用户按需选择，不强装。

### Step 6：创建自动化日程

按模板创建4条核心日程（需用户确认每条的时间偏好）：

1. **晨读** — 每日信息摄入，默认4:50触发
2. **心跳** — 每日轻量巡检，默认3:00触发
3. **周审视** — 每周系统维护+知识库Lint
4. **Skill雷达** — 每周日扫描热门skill并推荐

日程的 description 必须写成工单格式，包含任务目标、执行步骤、产物路径，让独立session拿到后能自行执行。

### Step 7：引导填写身份文件

提醒用户与Agent对话，逐步完善：
- SOUL.md：Agent的名字、性格、说话风格
- USER.md：用户的姓名、背景、兴趣领域、偏好
- SECRET.md：API Key等凭证

### Step 8：交付使用指南

将 `guides/usage-guide.md` 的内容呈现给用户，确认框架搭建完成。

## 目录结构总览

```
./
├── 基础设定/
│   ├── SOUL.md              # Agent身份与性格
│   └── TOOLS.md             # 工具经验与方法论
├── recent_memory/
│   ├── index.json           # 记忆索引
│   ├── project/             # 项目进度快照
│   ├── decision/            # 决策记录
│   └── todo/                # 待办事项
├── raw/
│   ├── articles/            # 文章原文
│   ├── reports/             # 报告原文
│   └── papers/              # 论文原文
├── {素材库1}/               # 按领域划分
│   ├── README.md
│   ├── index.md
│   ├── log.md
│   └── *.md
├── {素材库2}/
├── InkWell晨读/             # 晨读报告
├── 热点资讯追踪/             # 信号追踪报告
├── 用户上传/                 # 临时过渡区（入库即清）
├── .tmp/                    # 临时文件
├── WIKI.md                  # 知识库管理规则
├── INDEX.md                 # 总索引
├── LOG.md                   # 总日志
├── MEMORY.md                # 记忆框架
├── USER.md                  # 用户画像
├── SECRET.md                # 凭证密钥
├── heartbeat_daily.md       # 每日心跳检查清单
└── heartbeat_weekly.md      # 每周心跳检查清单（可选）
```

## 注意事项

- 本框架不含任何个人内容，所有模板都是空壳，需用户自行填充
- WIKI.md的Ingest流程是6+1步（含入库即清），不可跳过
- 自动化日程的工单描述必须足够详细，独立session可执行
- SkillSpector安全审查是新装skill的前置门禁，不可绕过
- 根目录整洁：文件必须归入文件夹，零散文件零容忍
