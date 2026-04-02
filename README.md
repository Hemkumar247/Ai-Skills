# 🧠 Ai-Skills — Claude & AI Skills Collection

> **Important Notice:** This repository is a **personal collection** of AI skills gathered from multiple sources. I do not claim ownership over the majority of the skills here. Skills have been sourced from Anthropic's official skill libraries, open-source repositories, and a few have been custom-built by me. Full attribution is listed below.

---

## 📌 What Is This?

This is a curated collection of **Claude skills** — structured instruction files (SKILL.md) that give Claude specialized personas, expert-level prompting, and defined output formats for specific tasks. Think of it as a toolbox: instead of writing long prompts from scratch every time, you activate the right skill and Claude behaves like a subject-matter expert instantly.

This collection brings together skills for business strategy, D2C brand building, software development, UX design, document creation, creative work, and more — all in one place so you can work in a more organized and efficient way.

---

## ⚠️ Ownership & Attribution

This repo is a **collection**, not original work. Here's an honest breakdown of where each skill comes from:

### 🏢 Sourced from Anthropic (Proprietary)
These skills are owned by **Anthropic, PBC** and are governed by your agreement with Anthropic regarding use of their services. They are included here as they ship with Claude-enabled environments.

| Skill | License |
|-------|---------|
| `public/docx` | © 2025 Anthropic, PBC — Proprietary |
| `public/pdf` | © 2025 Anthropic, PBC — Proprietary |
| `public/pdf-reading` | © 2025 Anthropic, PBC — Proprietary |
| `public/pptx` | © 2025 Anthropic, PBC — Proprietary |
| `public/xlsx` | © 2025 Anthropic, PBC — Proprietary |
| `public/file-reading` | © 2025 Anthropic, PBC — Proprietary |

---

### 🌐 Sourced from Open-Source (Apache 2.0)
These skills are from Anthropic's public skill examples library and other open-source repositories, licensed under the **Apache License 2.0**. Original license terms are preserved in each skill's `LICENSE.txt`.

| Skill | Source |
|-------|--------|
| `public/frontend-design` | Anthropic public skills (Apache 2.0) |
| `examples/algorithmic-art` | Anthropic public skills (Apache 2.0) |
| `examples/brand-guidelines` | Anthropic public skills (Apache 2.0) |
| `examples/canvas-design` | Anthropic public skills (Apache 2.0) |
| `examples/doc-coauthoring` | Anthropic public skills (Apache 2.0) |
| `examples/internal-comms` | Anthropic public skills (Apache 2.0) |
| `examples/mcp-builder` | Anthropic public skills (Apache 2.0) |
| `examples/skill-creator` | Anthropic public skills (Apache 2.0) |
| `examples/slack-gif-creator` | Anthropic public skills (Apache 2.0) |
| `examples/theme-factory` | Anthropic public skills (Apache 2.0) |
| `examples/web-artifacts-builder` | Anthropic public skills (Apache 2.0) |

---

### 🔀 Forked from Other Repositories (MIT)
These skills were discovered and forked from third-party open-source repositories. Original authorship and licenses are fully credited here.

| Skill | Original Author | License | Source |
|-------|----------------|---------|--------|
| `user/clone-website` | [JCodesMore](https://github.com/JCodesMore) | MIT | [ai-website-cloner-template](https://github.com/JCodesMore/ai-website-cloner-template) |

---

### ✍️ Custom-Built by Me
These skills were designed and written by me from scratch, tailored for specific use cases — primarily business strategy, D2C brand building, and development workflows.

| Skill | Purpose |
|-------|---------|
| `user/competitive-intelligence` | Competitor mapping & positioning analysis |
| `user/cursor-project-starter` | 7-doc project starter kit for Cursor IDE |
| `user/customer-journey-map` | McKinsey-style 7-stage customer lifecycle map |
| `user/customer-personas` | Deep research-grade customer persona builder |
| `user/d2c-brand-identity` | Brand naming, voice, and positioning |
| `user/d2c-first-customers` | Zero-budget customer acquisition playbook |
| `user/d2c-investor-pitch` | Full investor pitch package for D2C brands |
| `user/d2c-manufacturing` | Sourcing, COGS, and FSSAI compliance roadmap |
| `user/d2c-packaging` | Packaging design brief and unboxing strategy |
| `user/d2c-pricing` | Pricing psychology and margin architecture |
| `user/d2c-retention` | Subscription and repeat purchase engine |
| `user/executive-strategy` | CEO-ready strategic synthesis and 90-day plan |
| `user/financial-modeling` | Unit economics and 3-year financial projections |
| `user/gtm-strategy` | Go-to-market playbook and launch plan |
| `user/industry-trends` | Goldman Sachs-style trend intelligence brief |
| `user/market-entry` | Market expansion and entry mode analysis |
| `user/market-sizing-tam` | TAM/SAM/SOM breakdown, investor-ready |
| `user/pricing-strategy` | Fortune 500-level pricing analysis |
| `user/risk-assessment` | Deloitte-style risk matrix and scenario planning |
| `user/swot-porters` | Combined SWOT + Porter's Five Forces |
| `user/ux-architect` | Developer-ready UX specification document |
| `public/product-self-knowledge` | Accurate Anthropic product fact-checker |

---

## 📂 Repo Structure

```
skills/
├── public/       # Core utility skills (Anthropic proprietary + open source)
├── user/         # Custom-built + forked skills
└── examples/     # Open-source example skills (Apache 2.0)
```

---

## 🚀 How to Use

1. Clone or download this repo
2. Copy the `skills/` folder into your Claude workspace (e.g. `.claude/skills/` for Claude Code, or wherever your Claude environment reads skills from)
3. Trigger any skill by describing your task naturally — Claude activates the right skill based on what you say

For a detailed breakdown of what each skill does and what phrases trigger it, see the individual `SKILL.md` files inside each folder.

---

## 📄 License Summary

| Category | License |
|----------|---------|
| Anthropic proprietary skills | Governed by your Anthropic services agreement |
| Open-source skills (Anthropic examples) | Apache License 2.0 |
| Forked third-party skills | MIT License (see individual skill folders) |
| Custom skills by me | Free to use, no warranty |

Please respect the original licenses. If you fork or redistribute this collection, preserve the original `LICENSE.txt` files inside each skill folder.

---

## 🙏 Credits

- [Anthropic](https://anthropic.com) — for building Claude and the skills system
- [JCodesMore](https://github.com/JCodesMore) — for the [ai-website-cloner-template](https://github.com/JCodesMore/ai-website-cloner-template) (MIT)
- All other open-source contributors whose work is referenced here

---

*Collected and maintained by [Hem Kumar](https://github.com/Hemkumar247) · Chennai, India*
