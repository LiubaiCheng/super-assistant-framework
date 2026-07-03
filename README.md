# 🎨 LiuBai

> **LiuBai** — Super Assistant Framework
>
> 留白——中国水墨最核心的构图智慧。
> The unpainted area matters as much as the painted.
> 空不是无，空是可能性。
> Emptiness is not absence — it is possibility.

A reusable Agent system framework — scaffold only, methods included, slots left empty. No personal settings, preferences, or knowledge base content.

---

## 🎋 The Art of LiuBai（留白之道）

LiuBai (留白) is a core principle in Chinese ink wash painting: what you leave unpainted matters as much as what you paint. This framework extends that philosophy into system design.

**计白当黑 · Designing the Void**
空白和实笔同等重要。框架每一层的留空不是遗漏，是设计。骨架是笔，空白是布。
The blank spaces in each layer aren't omissions — they're deliberate design choices. The scaffold is the brushstroke; the emptiness is the canvas.

**意在笔先 · Intent Before Action**
先定意图再行动。身份层是「意」，自动化是「笔」。意先定，笔才有方向。
Identity defines intent; automation executes it. Set your soul before your system acts.

**虚实相生 · Void and Substance in Dialogue**
Ingest是实（写入），Lint是虚（清理），Query是虚实之间。虚实交替，系统才呼吸。
Ingest writes (substance), Lint cleans (void), Query reads between both. The system breathes through this rhythm.

**疏可走马 · Spacious Enough to Ride a Horse**
框架不预设领域，就是给用户留出走马的空间。你关注什么，框架就向什么方向伸展。
The framework prescribes no domain — that spaciousness is where you gallop. Whatever you care about, the framework stretches toward it.

**生成性空白 · Generative Emptiness**
留白不是"还没填完"，而是"等着你来填"。传统模板的空=缺失，LiuBai的空=可能性。
The emptiness isn't incomplete — it's waiting. Unlike templates where blank = missing, in LiuBai blank = possibility.

---

## ✨ What It Is

LiuBai is a battle-tested Agent architecture that decomposes a super assistant into 7 layers:

```
┌─────────────────────────────────┐
│  ① Identity     SOUL / TOOLS    │  Who the Agent is, how it works
│  ② Memory       MEMORY / SECRET │  Rules, anchors, credentials
│  ③ Knowledge    WIKI            │  Ingest → Query → Lint
│  ④ Output       Directories     │  Morning briefs, tracking reports
│  ⑤ Archives     Topic KBs       │  Investment / Research / Teaching / Anything you care about
│  ⑥ Logging      INDEX / LOG     │  Entry indices, run logs
│  ⑦ Extensions   skills/scripts  │  Capabilities, scripts, tools
└─────────────────────────────────┘
```

**Design inspiration**: [Karpathy's LLM Wiki pattern](https://github.com/karpathy/LLMWiki) — upgrading knowledge management from "file stacking" to "structured flow".

---

## 🚀 Quick Start

### Prerequisites
- A [Coze](https://www.coze.cn) Agent account
- Basic Markdown editing ability

### 7-Step Setup

1. **Install this Skill** — Search "超级助理框架" on [Xiaping](https://xiaping.coze.com) or clone this repo
2. **Create directory structure** — Follow the 7-layer architecture in SKILL.md
3. **Fill identity files** — Use templates/ to write SOUL.md, USER.md
4. **Configure WIKI rules** — Copy WIKI.md template, adjust as needed
5. **Initialize memory system** — Use MEMORY.md template for rules and anchors
6. **Set up automation schedules** — Configure morning briefs, tracking, radar
7. **Iterate continuously** — Use the framework, accumulate experience, refine rules

📖 Full guide: [`guides/usage-guide.md`](guides/usage-guide.md)

---

## 📁 Project Structure

```
liubai/
├── SKILL.md                    # Main instruction (architecture + setup flow)
├── README.md                   # This file
├── guides/
│   └── usage-guide.md          # Full usage guide (7 chapters)
└── templates/                  # Blank templates
    ├── SOUL.md                 # Identity & personality
    ├── USER.md                 # User profile
    ├── MEMORY.md               # Rules & state anchors
    ├── TOOLS.md                # Tool experience & methodology
    ├── WIKI.md                 # Knowledge base management rules
    ├── SECRET.md               # Sensitive credentials
    ├── heartbeat_daily.md      # Daily heartbeat checklist
    ├── INDEX.md                # Entry index template
    └── LOG.md                  # Run log template
```

---

## 🔑 Core Design Principles

- **Scaffold First**: Structure and rules only — no preset content
- **Method Deposition**: Operational norms (Ingest/Lint/Clean-as-you-go) as living rules, not one-shot instructions
- **Layered Decoupling**: Identity, memory, knowledge, output — independent, non-polluting
- **Continuous Evolution**: The framework grows with use, not configured once and frozen

---

## 💡 Framework Advantages

### Growth（成长性）

- **Rule Deposition**: WIKI's Ingest/Lint, TOOLS' engineering discipline, MEMORY's behavioral rules — living rules that grow with use, not static configs
- **Memory Self-Evolution**: Instant layer → Mid-term layer → Semantic retrieval — the more you use it, the better it knows you
- **Iterable Automation**: Morning sources can be added/removed, tracking topics can be toggled, Skill Radar discovers new capabilities weekly
- **Clean-as-you-go + Weekly Lint**: The system gets cleaner over time, never rotting

### Universality（普适性）

- **Scaffold First, Content Empty**: Teacher, investor, researcher, creator — fill in your own domain
- **WIKI Three-Phase Decoupling**: Ingest/Query/Lint work independently; use any subset
- **Domain-Agnostic Archives**: Investment, research, teaching, media, anything you care about — just create a directory
- **Optional Automation**: 4 automation lines are all opt-in; don't need morning briefs? Don't create them
- **Open Skill Ecosystem**: Not locked to any platform or tool

### Symbiosis（共生性）

- **Co-creation, Not Configuration**: You're not setting up a tool — you're cultivating a relationship. SOUL.md defines personality, not parameters; MEMORY records shared experiences, not a database
- **Memory as Tree Rings**: Every entry, every failed-lesson learned, every rule deposited — these are growth rings between you and your Agent. The longer you work together, the denser the rings, the deeper the understanding
- **Habits Emerge Naturally**: WIKI rules and TOOLS discipline aren't imposed — they emerge from daily collaboration. Over time, your Agent just *gets it*
- **Emptiness as Growing Room**: The framework's blanks aren't containers waiting to be filled — they're room to grow. Like spacing for a sapling to stretch into — the space itself is nourishment

### Comparison

| | LiuBai | Prompt-Only | Fixed Template |
|---|---|---|---|
| Knowledge Mgmt | Three-phase flow | Manual paste | Static stacking |
| Memory System | Three-tier + semantic retrieval | Single context | None |
| Automation | Schedule-driven work orders | Manual trigger each time | None |
| Maintainability | Weekly Lint + Clean-as-you-go | None | Manual |
| Security | SkillSpector gate | None | None |
| User Relationship | Symbiotic — deeper alignment over time | One-off conversation, no memory | None — pure tool |

---

## 🛠️ Required Skills

| Skill | Purpose | Source |
|-------|---------|--------|
| skill_builder | Skill creation & iteration | Built-in (Coze) |
| topic_tracking | Topic tracking & periodic briefings | Coze Skill Store |
| SkillSpector | Security scanning & review gate | [GitHub](https://github.com/skill-spector/skill-spector) |

More optional recommendations in the usage guide.

---

## 📜 License

MIT License — Free to use, modify, and distribute. Please retain original author attribution.

## 🙏 Acknowledgments

- Architecture inspired by [Andrej Karpathy's LLM Wiki pattern](https://github.com/karpathy/LLMWiki)
- Engineering methodology from [Superpowers](https://github.com/NexTechAI/superpowers) and [Headroom](https://github.com/headroomHQ/headroom)
- Security scanning by [SkillSpector](https://github.com/skill-spector/skill-spector)

---

Made with ❤️ by 程留白 · Powered by [Coze](https://www.coze.cn)
