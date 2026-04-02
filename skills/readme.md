# 🧠 Ai-Skills — Claude Skill Library

A curated collection of **40 Claude skills** that supercharge Claude's capabilities across business strategy, D2C brand building, software development, UX design, and document creation. Drop these into any Claude environment that supports the skills system and unlock expert-level outputs on demand.

---

## 📦 What Are Claude Skills?

Claude skills are structured `SKILL.md` files that give Claude a specialized persona, a defined output structure, and expert-level prompting instructions for a specific domain. Instead of writing long prompts every time, skills make Claude behave like a subject-matter expert the moment you trigger the right phrase.

Each skill follows this pattern:
- **You describe your situation** → Claude collects any missing context → **Claude produces a structured, expert-level output**

---

## 🗂 Repo Structure

```
skills/
├── public/          # Core utility skills (file handling, document creation)
├── user/            # Strategy, business, and dev skills
└── examples/        # Specialized creative and builder skills
```

---

## 🚀 Quick Setup

### Option 1 — Clone the repo
```bash
git clone https://github.com/Hemkumar247/Ai-Skills.git
```
Then point your Claude environment to the `skills/` folder.

### Option 2 — Download the ZIP
Download the repo as a `.zip` from GitHub and extract the `skills/` folder into your Claude workspace.

### Option 3 — Selective install
Copy only the skill folders you need into your existing `skills/` directory.

> **Note:** Skills are read by Claude at runtime — no installation scripts or dependencies needed for the skill files themselves. Some public skills (docx, pdf, pptx, xlsx) include Python/Node helper scripts that are used automatically when Claude runs document tasks.

---

## 📚 Skill Reference

### 🔧 Public Skills — Core Utilities

These handle everyday file creation and document manipulation tasks.

| Skill | Trigger Phrases | What It Does |
|-------|----------------|--------------|
| **docx** | "Word doc", ".docx", "write a report" | Create, read, edit, and manipulate `.docx` files with full formatting — TOC, headings, tracked changes, images, letterheads |
| **pdf** | "PDF", ".pdf", "merge PDFs" | Full PDF toolkit — create, merge, split, rotate, watermark, fill forms, OCR scanned PDFs, encrypt/decrypt |
| **pdf-reading** | "read this PDF", "extract from PDF" | Smart PDF content extraction — text, tables, images, form fields; chooses the right strategy for text-heavy vs scanned docs |
| **pptx** | "deck", "slides", "presentation", ".pptx" | Create, edit, parse, and extract from PowerPoint files; supports templates, layouts, speaker notes |
| **xlsx** | "spreadsheet", ".xlsx", "Excel" | Create and edit Excel files — formulas, charts, data cleaning, format conversion, tabular restructuring |
| **frontend-design** | "build a UI", "web component", "landing page" | Produces production-grade, distinctively designed frontend interfaces — React, HTML/CSS, dashboards, avoiding generic AI aesthetics |
| **file-reading** | uploaded file path at `/mnt/user-data/uploads/` | Smart file router — detects file type and picks the right reading strategy for PDF, docx, xlsx, CSV, JSON, images, archives |
| **product-self-knowledge** | "Claude pricing", "API limits", "Claude Code" | Looks up accurate, current Anthropic product facts before answering — prevents outdated info on models, plans, and features |

---

### 💼 User Skills — Business Strategy & Development

#### 📊 Market & Competitive Intelligence

| Skill | Trigger Phrases | What It Does |
|-------|----------------|--------------|
| **market-sizing-tam** | "how big is the market", "what's the TAM", "validate my market" | McKinsey-level TAM/SAM/SOM breakdown with top-down and bottom-up analysis, growth projections, investor-ready output |
| **competitive-intelligence** | "who are my competitors", "competitive analysis", "how do I differentiate" | Senior analyst-level competitive landscape — 8–10 competitor mapping, positioning maps, moat analysis, strategic gaps |
| **industry-trends** | "industry trends", "where is this industry going", "macro trends" | Goldman Sachs-style trend intelligence brief — macro/micro forces, disruption timelines, regulatory signals, investment implications |
| **swot-porters** | "SWOT analysis", "Porter's Five Forces", "assess my business" | Harvard Business School-style combined SWOT + Porter's Five Forces with cross-analysis and industry attractiveness score |
| **customer-personas** | "who is my customer", "customer persona", "ideal customer profile" | 4 deep research-grade personas with psychographics, buying behaviour, pain points, and willingness-to-pay analysis |
| **customer-journey-map** | "customer journey", "where do I lose customers", "touchpoint mapping" | McKinsey-style 7-stage lifecycle map with emotional curve, churn signals, delight opportunities, and intervention playbook |

#### 🚀 Growth & Go-To-Market

| Skill | Trigger Phrases | What It Does |
|-------|----------------|--------------|
| **gtm-strategy** | "go to market", "how do I launch", "marketing strategy" | Complete GTM playbook — channel ranking, messaging framework, budget allocation, 14-day quick-win plan |
| **market-entry** | "market entry", "expand to new market", "should I launch in X" | Global expansion playbook — market attractiveness scoring, entry mode analysis, 12-month roadmap |
| **pricing-strategy** | "how should I price this", "pricing tiers", "value-based pricing" | Fortune 500-level pricing analysis — psychological tactics, tiered recommendations, revenue projections |
| **financial-modeling** | "unit economics", "CAC", "LTV", "burn rate", "break even" | VP Finance-grade financial model — full unit economics, 3-year projections, red flags table |
| **risk-assessment** | "what could go wrong", "risk matrix", "scenario planning" | Deloitte-style risk report — 15 scored risks, 4-scenario planning including black swan events, contingency playbook |
| **executive-strategy** | "overall strategy", "90-day plan", "what should I focus on" | McKinsey senior partner synthesis — 3 strategic paths, one clear recommendation, 90-day action plan. **Run this last after other analyses.** |

#### 🛒 D2C Brand Building (India-focused)

| Skill | Trigger Phrases | What It Does |
|-------|----------------|--------------|
| **d2c-brand-identity** | "brand name", "brand identity", "tagline", "brand voice" | 10 name options across 5 styles, brand voice guide, tagline options, complete positioning statement |
| **d2c-first-customers** | "first 100 customers", "zero budget marketing", "DM strategy" | Day-by-day Week 1 action plan, exact DM scripts, sampling strategy, 30-day tracker — zero ad spend |
| **d2c-pricing** | "D2C pricing", "pricing for quick commerce", "margin architecture" | Pricing psychology for Indian consumers, margin architecture across D2C/quick commerce/retail/Amazon |
| **d2c-packaging** | "packaging design", "unboxing experience", "packaging brief" | Complete packaging brief — materials, copy, cost breakdown, Instagrammability strategy |
| **d2c-manufacturing** | "contract manufacturer", "COGS breakdown", "FSSAI license" | Full manufacturing roadmap — sourcing map, COGS breakdown, FSSAI compliance checklist, MOQ negotiation tactics |
| **d2c-retention** | "retention strategy", "subscription model", "reduce churn" | Complete retention architecture — habit stack, subscription design, WhatsApp trigger sequences, anti-churn playbook |
| **d2c-investor-pitch** | "investor pitch", "pitch deck", "raise funding", "seed round" | Full investor pitch package — 60-second verbal pitch, slide-by-slide deck structure, cold email, objection playbook |

#### 💻 Development & Design

| Skill | Trigger Phrases | What It Does |
|-------|----------------|--------------|
| **cursor-project-starter** | "new project", "I have a project idea", "set up my Cursor project" | 7-document project starter kit — PRD, tech spec, app flow, DB schema, implementation plan, Cursor rules, README |
| **ux-architect** | "design the UX for", "create a UX spec", "map out the screens" | Developer-ready UX specification — information architecture, user flows, screen breakdowns, microcopy, error/empty/loading states, design tokens, component inventory |

---

### 🎨 Example Skills — Creative & Builder Tools

| Skill | Trigger Phrases | What It Does |
|-------|----------------|--------------|
| **canvas-design** | "create a poster", "design this", "piece of art" | Generates beautiful visual art as `.png`/`.pdf` using design philosophy — posters, graphics, static visuals |
| **algorithmic-art** | "generative art", "flow fields", "particle systems" | Creates algorithmic art using p5.js with seeded randomness and interactive parameter exploration |
| **theme-factory** | "apply a theme", "style this artifact" | 10 pre-set themes (colors + fonts) for any artifact — slides, docs, HTML pages. Can also generate custom themes on the fly |
| **brand-guidelines** | "Anthropic brand colors", "company design standards" | Applies Anthropic's official brand colors and typography to any artifact |
| **frontend-design** | "build a web app", "beautiful UI" | Production-grade frontend interfaces — React, Tailwind, shadcn/ui, avoids generic AI look |
| **web-artifacts-builder** | "complex artifact", "multi-component app", "React with routing" | Elaborate multi-component Claude artifacts using React + Tailwind + shadcn/ui for state-heavy UIs |
| **doc-coauthoring** | "help me write docs", "create a proposal", "draft a spec" | Structured co-authoring workflow — context transfer, iterative refinement, reader-verification loop |
| **internal-comms** | "status report", "leadership update", "company newsletter" | Internal communication writer — status reports, 3P updates, FAQs, incident reports, newsletters |
| **mcp-builder** | "build an MCP server", "integrate external API" | Guide for creating high-quality MCP (Model Context Protocol) servers in Python (FastMCP) or TypeScript (MCP SDK) |
| **skill-creator** | "create a new skill", "improve this skill", "run evals" | Meta-skill — create, modify, benchmark, and optimize skills; includes eval runner and performance analysis |
| **slack-gif-creator** | "make a GIF for Slack", "animated GIF" | Creates animated GIFs optimized for Slack constraints — frame composer, easing, validators |

---

## 💡 How to Use a Skill

Just talk to Claude naturally. Skills activate automatically based on what you say:

```
You:    "Can you do a competitive analysis for my edtech startup in India?"
Claude: [activates competitive-intelligence skill]
        "Sure! Let me collect a few details first:
         - Product or business description?
         - Target customer?
         - Geography and price point?
         - Stage — idea, launched, or scaling?"
```

For the most powerful results with strategy skills, run them in sequence:

```
1. market-sizing-tam      → validate the opportunity
2. customer-personas      → know your buyer
3. competitive-intelligence → map the landscape
4. swot-porters           → assess your position
5. gtm-strategy           → plan the launch
6. financial-modeling     → model the numbers
7. executive-strategy     → synthesize everything into a decision
```

---

## 🗃 Full Skill List (40 total)

<details>
<summary>Click to expand full list</summary>

**Public (8)**
- docx, pdf, pdf-reading, pptx, xlsx, frontend-design, file-reading, product-self-knowledge

**User — Strategy (12)**
- competitive-intelligence, customer-journey-map, customer-personas, executive-strategy, financial-modeling, gtm-strategy, industry-trends, market-entry, market-sizing-tam, pricing-strategy, risk-assessment, swot-porters

**User — D2C (7)**
- d2c-brand-identity, d2c-first-customers, d2c-investor-pitch, d2c-manufacturing, d2c-packaging, d2c-pricing, d2c-retention

**User — Dev & Design (2)**
- cursor-project-starter, ux-architect

**Examples (11)**
- algorithmic-art, brand-guidelines, canvas-design, doc-coauthoring, internal-comms, mcp-builder, skill-creator, slack-gif-creator, theme-factory, web-artifacts-builder, frontend-design (public)

</details>

---

## 🤝 Contributing

Feel free to fork this repo and add your own skills. Follow the existing SKILL.md format — each skill needs:

1. A YAML frontmatter block with `name` and `description`
2. A clear persona definition ("You are a...")
3. A list of inputs to collect before running
4. A structured output format

PRs welcome!

---

## 📄 License

Public skills include their own `LICENSE.txt`. User and example skills are provided as-is for personal use. See individual skill folders for specific terms.

---

*Built by [Hem Kumar](https://github.com/Hemkumar247) • Chennai, India*
