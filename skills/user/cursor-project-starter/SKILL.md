---
name: cursor-project-starter
description: >
  Generates a complete Cursor AI IDE project starter kit — 7 documents — from a brainstorming
  conversation with the user. Use this skill whenever the user wants to start a new project,
  says "let's start a new project", "I have a project idea", "help me plan a new app/system/tool",
  "set up my Cursor project", or wants to brainstorm and immediately get working project files.
  Also trigger when the user says things like "I want to build X from scratch" or "help me plan
  out X before I start coding". Always use this skill proactively when a new project is being
  initiated — don't wait for the user to ask for documentation explicitly.
---

# Cursor Project Starter Kit

Generates 7 structured project documents through a brainstorming interview, ready to drop
into Cursor (or any AI IDE) so the AI understands the full project from the start.

---

## The 7 Documents This Skill Produces

| File | Purpose |
|---|---|
| `PRD.md` | Product Requirements — features, goals, metrics, risks |
| `technical-spec.md` | Architecture, tech stack, functions, API details |
| `app-flow.md` | User journeys, system states, edge cases |
| `schema.md` | Database/data structure — all tables/collections + columns |
| `implementation-plan.md` | Phased build checklist with tasks and checkboxes |
| `README.md` | Project index — explains every file, how to use in Cursor |
| `.cursorrules` | Cursor AI rules — code style, naming, patterns, anti-patterns |

---

## Step 1 — Brainstorm Interview

Before writing any documents, conduct a structured interview. Ask ALL of these questions in a
single conversational message (not one at a time). Group them naturally.

### Core Questions

**What is the project?**
- What does it do in one sentence?
- Who are the users (primary + secondary)?
- What problem does it solve?

**Tech Stack:**
- What language/runtime? (e.g., Python, Node.js, Google Apps Script, React)
- What database or storage? (e.g., PostgreSQL, Firestore, Google Sheets, MongoDB)
- What external APIs or services? (e.g., OpenAI, Stripe, WhatsApp, Google Maps)
- Any hosting/deployment target? (e.g., Vercel, GCP, AWS, serverless)

**Features:**
- What are the 3–5 core features for MVP?
- What is explicitly OUT OF SCOPE for now?
- Any "nice to have" features?

**Data:**
- What are the main data entities? (e.g., users, orders, products, sessions)
- What fields does each entity need?

**Flows:**
- Walk through the main user journey step by step
- Are there admin/owner flows separate from customer flows?
- What are 2–3 key edge cases or failure scenarios?

**Constraints:**
- Timeline or deadline?
- Cost constraints (free tier only? budget ok?)
- Any security or compliance requirements?

---

## Step 2 — Fill Gaps & Confirm

After the user answers:
- Infer anything not explicitly stated (e.g., if they say "React app", infer Vite/Next.js as likely choice)
- Ask for clarification ONLY on blockers (missing DB choice, unclear primary user)
- Summarize your understanding in 3–5 bullet points
- Ask: "Does this match your vision? Ready to generate the files?"

---

## Step 3 — Generate All 7 Documents

Generate all files in sequence. Write each one completely before moving to the next.
Use the templates in `templates/` as structural guides — replace all placeholder content
with the user's actual project details.

**Generation order:**
1. `PRD.md` — establish requirements first (everything else references this)
2. `technical-spec.md` — architecture derived from PRD
3. `schema.md` — data model derived from tech spec
4. `app-flow.md` — user journeys referencing the features in PRD
5. `implementation-plan.md` — phased tasks referencing all above
6. `.cursorrules` — rules derived from tech stack and patterns established above
7. `README.md` — index file written last (references all others)

**Quality checks per document:**
- No placeholder text like `[FILL IN]` or `YOUR_VALUE` left in final output
- Tech stack must be consistent across ALL documents
- Function names in `.cursorrules` must match function names in `technical-spec.md`
- Schema column names in `schema.md` must match references in `technical-spec.md`
- All phase tasks in `implementation-plan.md` should reference the correct companion doc

---

## Step 4 — Package & Deliver

Save all 7 files to `/mnt/user-data/outputs/` in a flat structure (no subfolder needed).
Present them to the user with `present_files`.

Tell the user:
> "Drop all these files into your Cursor project root folder. Cursor will auto-detect
> `.cursorrules`. Then start prompting with references like:
> `'Read PRD.md and technical-spec.md, then write the [function name] function'`"

---

## Document Templates

See `templates/` folder for the structural template of each document.
Read the relevant template before generating that document.

- `templates/PRD-template.md`
- `templates/technical-spec-template.md`
- `templates/app-flow-template.md`
- `templates/schema-template.md`
- `templates/implementation-plan-template.md`
- `templates/cursorrules-template.md`
- `templates/README-template.md`

---

## Key Principles

- **Project-specific, not generic** — every document must feel written FOR this project, not copy-pasted
- **Cross-referenced** — documents must refer to each other (e.g., implementation-plan references PRD phases)
- **Cursor-optimized** — README must include ready-to-use Cursor prompt examples specific to the project
- **No server assumption** — if user didn't mention a server, default to serverless/managed options
- **Indian context awareness** — if project targets India, default to INR, Indian phone format (+91), UPI/Razorpay, Aadhaar-aware considerations where relevant
