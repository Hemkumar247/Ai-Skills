# 📁 Project Documentation Index
## {{PROJECT_NAME}}

---

## What Is This Folder?

This folder contains all the **structured documentation** you need to feed into Cursor (or any
AI-powered IDE) to build {{PROJECT_NAME}} from scratch.

Instead of explaining your project to the AI every time, place these files in your project root
and the AI reads them automatically to understand what to build, how to build it, and what rules
to follow.

---

## Documents in This Folder

| File | What It Is | Use It For |
|---|---|---|
| `PRD.md` | Product Requirements Document | Features list, goals, success metrics |
| `technical-spec.md` | Technical Specification | Architecture, functions, API details |
| `app-flow.md` | App Flow & User Journey | How users move through the system, edge cases |
| `schema.md` | Database Schema | All tables/collections, field names, data types |
| `implementation-plan.md` | Build Checklist | Phase-by-phase tasks with checkboxes |
| `.cursorrules` | AI IDE Rules File | Tells Cursor how to write code for this project |

---

## How to Use These in Cursor

1. Create a new project folder (e.g., `{{PROJECT_FOLDER_NAME}}/`)
2. Copy ALL files from this folder into it
3. Open the folder in Cursor (`File → Open Folder`)
4. Cursor auto-detects `.cursorrules` and applies the rules
5. Start prompting using the examples below

---

## Ready-to-Use Cursor Prompts

```
"Read PRD.md and technical-spec.md, then write the {{MAIN_FUNCTION_1}} function"

"Based on schema.md, write a function to {{COMMON_DB_OPERATION}}"

"Write the {{MAIN_FUNCTION_2}} function as described in technical-spec.md"

"Based on implementation-plan.md Phase {{PHASE_NUM}}, write all the functions needed for {{PHASE_NAME}}"

"Review app-flow.md Journey {{N}} and implement the error handling for {{EDGE_CASE}}"
```

---

## Build Order (Follow This Sequence)

```
1. {{BUILD_STEP_1}} (implementation-plan.md Phase 1)
2. {{BUILD_STEP_2}} (implementation-plan.md Phase 2)
3. {{BUILD_STEP_3}} (implementation-plan.md Phase 3)
4. {{BUILD_STEP_4}} (implementation-plan.md Phase 4)
5. {{BUILD_STEP_5}} (implementation-plan.md Phase 5)
6. {{BUILD_STEP_6}} (implementation-plan.md Phase 6)
```

---

## Quick Reference: Key Decisions

| Decision | Choice | Reason |
|---|---|---|
| {{DECISION_1}} | {{CHOICE_1}} | {{REASON_1}} |
| {{DECISION_2}} | {{CHOICE_2}} | {{REASON_2}} |
| {{DECISION_3}} | {{CHOICE_3}} | {{REASON_3}} |

---

*Generated for: {{PROJECT_NAME}} MVP*
*Ready to use in: Cursor, Windsurf, or any AI-powered IDE*
