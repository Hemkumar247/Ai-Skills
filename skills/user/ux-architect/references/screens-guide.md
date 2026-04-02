# Screen Breakdown & Microcopy Guide

## Screen Breakdown Format

Use this format for every screen:

```
──────────────────────────────────────────────────
SCREEN: [Screen Name]
Route/URL: [/path or screen identifier]
Auth required: Yes / No
──────────────────────────────────────────────────
PURPOSE
[1–2 sentences: what the user is trying to do here]

UI ELEMENTS
- [Element type]: [Description]  e.g. "Search bar: filters by name/category"
- [Element type]: [Description]
- [Element type]: [Description]

PRIMARY ACTION
[The main CTA — what moves the user forward]

SECONDARY ACTIONS
- [Action]: [Where it goes / what it does]
- [Action]: [Where it goes / what it does]

NAVIGATION
- Back: [where]
- Tab bar / sidebar item: [which one is active]
- Deep link: [yes/no, what URL]

STATES THIS SCREEN HAS
☐ Loading  ☐ Empty  ☐ Error  ☐ Partial data  ☐ Full data
──────────────────────────────────────────────────
```

## Microcopy Format

Use this table for each screen:

| Element | Copy |
|---|---|
| Screen title | [Exact text] |
| Subheading | [Exact text or "none"] |
| Primary CTA | [Button label] |
| Secondary CTA | [Button label or "none"] |
| Input: [field name] label | [Label text] |
| Input: [field name] placeholder | [Placeholder text] |
| Input: [field name] helper text | [Helper text or "none"] |
| Toast / confirmation | [Success message] |
| Empty state headline | [Text] |
| Empty state body | [Text] |
| Empty state CTA | [Button label] |

## Microcopy Rules

### Tone by Industry
| Industry | Tone | Avoid |
|---|---|---|
| Fintech / Banking | Clear, formal, trustworthy | Jargon, slang |
| Health / Medical | Calm, reassuring, precise | Alarming language |
| E-commerce | Friendly, action-oriented | Passive voice |
| SaaS / B2B | Professional, efficient | Over-casual |
| EdTech | Encouraging, clear | Condescending |
| Consumer / Social | Warm, playful | Corporate speak |

### CTA Labels — Rules
- Use verb + noun: "Save Profile", "Track Order", "Start Free Trial"
- Never: "Click Here", "Submit", "OK", "Yes"
- Destructive actions: "Delete Account" not "Confirm"
- Loading CTAs: disable the button, show spinner + "Saving…"

### Input Fields — Rules
- Labels above the field (not placeholder-as-label — it disappears on focus)
- Placeholder shows format example: "e.g. +91 98765 43210"
- Helper text for validation rules: "Must be at least 8 characters"
- Error text replaces helper text (same position, red color)

### Titles — Rules
- Screen titles: short (2–4 words), describe WHAT the user is doing
- Modals: question form preferred — "Delete this item?" not "Confirm Deletion"
- Onboarding steps: progress-oriented — "Almost there" not "Step 3 of 4"
