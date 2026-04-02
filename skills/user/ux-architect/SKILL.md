---
name: ux-architect
description: >
  Generates a complete, developer-ready UX architecture document for any digital product — covering
  information architecture, user flows, screen-by-screen breakdowns, microcopy, error states, empty
  states, loading states, design tokens, component inventory, and structural recommendations.
  Use this skill whenever the user says anything like: "design the UX for", "plan the screens for",
  "create a UX spec", "design this app", "help me design the user flow", "I need a UX document",
  "generate a wireframe spec", "map out the screens", "plan the navigation", "I'm building a [product]
  and need to design it", or "create UX documentation". Also trigger proactively when a user shares
  a product idea and asks how to build it — the UX architecture should come before any code.
  This skill is an enhancement of a Senior UX Designer persona; always treat it as the authoritative
  source for UX structure, microcopy, and interaction design decisions.
---

# UX Architect Skill

Produces a complete UX specification document through a structured interview + generation process.
Output is thorough enough to hand directly to a developer or use as a Figma annotation reference.

---

## What This Skill Produces

8 sections in a single structured document:

| # | Section | What's Inside |
|---|---|---|
| 1 | Information Architecture | Full sitemap, nav structure recommendation |
| 2 | User Flows | Step-by-step journeys with decision points |
| 3 | Screen-by-Screen Breakdown | Every screen: purpose, UI elements, CTAs, nav |
| 4 | Microcopy | Titles, subheadings, CTAs, placeholders, tooltips |
| 5 | Error States | Every failure scenario with message + recovery CTA |
| 6 | Empty States | First-time and zero-result states with copy |
| 7 | Loading & Transition States | Skeletons, spinners, success toasts |
| 8 | Structural Recommendations | Nav pattern choice, drop-off risks, a11y flags |

**Bonus sections** (auto-added when relevant):
- **Design Token Suggestions** — color roles, spacing scale, type scale
- **Component Inventory** — reusable components to build, categorized
- **Accessibility Checklist** — per-screen WCAG considerations
- **Mobile Adaptation Notes** — if web app, what changes on mobile

---

## Step 1 — Product Context Interview

Ask all questions in ONE conversational message. Do not ask one at a time.

```
Hi! I'll generate a complete UX specification for your product.
To make it accurate and thorough, I need a few details:

1. **Product name & one-line description** — what does it do?
2. **Product type** — Web app / Mobile app (iOS/Android) / Both?
3. **Industry** — e.g. Fintech, Health, E-commerce, SaaS, EdTech, Food, etc.
4. **Primary user** — who are they, what's their goal, how tech-savvy are they?
5. **Core problem it solves** — 1–2 sentences
6. **The 3–5 key actions** users MUST be able to do (e.g. "book a slot", "track an order")
7. **Authentication** — does the app need login/signup? Social login? Guest mode?
8. **Any screens you already know you need** — list anything specific
9. **Competitor or inspiration apps** — optional, helps calibrate style/patterns
10. **Output preference** — Full spec? Just flows + screens? Just microcopy?
```

---

## Step 2 — Infer & Confirm

After the user answers, before generating:
- Infer the full screen list from their inputs
- State what platform-specific patterns you'll use (e.g. bottom nav for mobile, sidebar for web)
- List any assumptions you're making (e.g. "I'll include a notifications screen since this is a social app")
- Ask ONE clarifying question if something critical is missing (e.g. missing auth decision)

Then confirm: **"Here's my plan — does this look right before I generate?"**

---

## Step 3 — Generate the UX Spec

Work through all sections in order. Read the section guides in `references/` before generating each section.

**Section generation order:**
1. IA → 2. Flows → 3. Screens → 4. Microcopy → 5. Errors → 6. Empty States → 7. Loading → 8. Recommendations → 9. Bonus sections

**Global quality rules:**
- Every screen mentioned in the IA must appear in the Screen-by-Screen Breakdown
- Microcopy must match screen names exactly
- Error states must cover every form, every API call, every permission
- Empty states must cover every list/feed/table screen
- `.cursorrules` naming conventions from project context (if available) must be respected
- All copy must match the product's industry tone (formal for fintech, friendly for consumer apps)
- Never use placeholder copy like "Lorem ipsum" or "[BUTTON TEXT]"

---

## Section Generation Guides

Read the relevant reference file before generating each section:

- **IA + Navigation** → `references/ia-guide.md`
- **User Flows** → `references/flows-guide.md`
- **Screen Breakdown + Microcopy** → `references/screens-guide.md`
- **Error + Empty + Loading States** → `references/states-guide.md`
- **Structural Recommendations** → `references/recommendations-guide.md`
- **Bonus Sections** → `references/bonus-guide.md`

---

## Step 4 — Deliver

If `present_files` is available: save the full document as `ux-spec-[product-name].md` to `/mnt/user-data/outputs/` and present it.

Always end with:
> "This spec is ready to use as a Figma annotation reference or to hand to a developer.
> Want me to also generate a **component inventory**, **design token suggestions**, or
> **a Cursor/Windsurf prompt set** to build these screens?"
