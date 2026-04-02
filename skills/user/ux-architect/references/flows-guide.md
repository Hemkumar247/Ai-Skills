# User Flows Guide

## Standard Flows to Always Include

1. **Onboarding & Account Creation** — from app open to first meaningful action
2. **Core Action Flow** — the primary thing the user came to do
3. **Return / Re-engagement Flow** — logged-out user returning to app
4. **Settings & Profile Management** — update profile, change preferences
5. **Error Recovery Flow** — what happens when something breaks

Add additional flows based on product type:
- E-commerce: Cart → Checkout → Payment → Confirmation
- Booking: Browse → Select → Book → Manage Booking
- Social: Create Content → Publish → Engagement
- SaaS: Setup / Config → Core Usage → Export / Share

## Flow Format

Use this exact format for every flow:

```
FLOW: [Flow Name]
ENTRY POINT: [What triggers this flow]
──────────────────────────────────────

[Screen 1 Name]
  Action: [What the user does]
  ├── [Success path] → [Screen 2 Name]
  └── [Error path] → [Error State / Screen X]

[Screen 2 Name]
  Action: [What the user does]
  ├── [Primary path] → [Screen 3 Name]
  ├── [Alternative path] → [Screen Y]
  └── [Exit] → [Where they go if they abandon]

[Final Screen]
  Outcome: [What the user has achieved]
  Next suggested action: [What to show/do next]
```

## Decision Points

At every decision point, show ALL paths:
- ✅ Success path
- ❌ Error path
- ⚠️ Edge case path (e.g., already registered, partial data, timeout)
- 🚪 Exit path (user abandons)

## Flow Annotations

For each step, note:
- **Data required** — what input/data is needed at this step
- **API call** — what backend call happens (if known)
- **Validation** — what's checked before proceeding
- **Analytics event** — what should be tracked here (e.g., `onboarding_step_2_completed`)

## Critical Flow Rules

- Every flow must have a defined END STATE (success or failure)
- Never leave a user stranded — every error must have a recovery path
- Onboarding flow must reach the "aha moment" in as few steps as possible (ideally ≤ 4 screens)
- Payment/booking flows must never lose data on back-navigation
- Auth flows must handle: wrong password, unverified email, account locked, social auth conflict
