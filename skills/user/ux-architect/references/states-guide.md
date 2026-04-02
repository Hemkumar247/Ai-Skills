# Error, Empty & Loading States Guide

## Error States

### Errors to Always Cover

| Category | Scenarios |
|---|---|
| Form validation | Required field empty, invalid format, value out of range, mismatch (e.g. passwords) |
| Network | No internet, request timeout, server error (500), service unavailable (503) |
| Auth | Wrong password, account locked, token expired, session timeout, unauthorized access |
| Permissions | Camera denied, location denied, notification denied, storage denied |
| Payment (if applicable) | Card declined, insufficient funds, expired card, 3DS failure, duplicate payment |
| Data conflicts | Duplicate entry, record not found, stale data, concurrent edit |
| File/upload | File too large, unsupported format, upload failed |

### Error State Format

Use this table for ALL error states:

| Field | Content |
|---|---|
| **Screen/Action** | Where this error occurs |
| **Trigger** | What causes this error |
| **Headline** | Short, plain-language title (≤ 6 words) |
| **Body copy** | What happened + what to do (1–2 sentences) |
| **Primary CTA** | Recovery action label |
| **Secondary CTA** | Fallback action (e.g. "Contact Support") or "none" |
| **Inline or full-screen?** | Inline (below field) / Toast / Banner / Full page |

### Error Copy Rules
- Headlines: state the problem, not the cause — "Couldn't save changes" not "HTTP 503 Error"
- Body: always say what to do next — "Check your connection and try again"
- Never blame the user — "Something went wrong" not "You entered an invalid value"
- Destructive errors (data loss, payment failure) need full-screen treatment, not a toast
- Inline validation: show errors on blur, not on submit (better UX)

---

## Empty States

### Screens That Need Empty States

Any screen with a list, feed, table, or grid needs an empty state. Common ones:
- Dashboard (no activity yet)
- Notifications (none yet)
- Orders / Bookings (none made yet)
- Search results (no matches)
- Filtered list (filter returns nothing)
- Saved items / Favorites
- Chat / Messages
- Cart

### Empty State Types

**1. First-time empty** — user has never done anything yet
- Illustration: welcoming, shows the feature's potential
- Headline: action-oriented — "Your orders will appear here"
- Body: brief explanation of the feature
- CTA: direct path to first action — "Place Your First Order"

**2. Zero-result search/filter**
- Illustration: light, not alarming (magnifying glass, empty box)
- Headline: "No results for '[query]'"
- Body: suggest broadening search or trying different filters
- CTA: "Clear Filters" or "Search Again"

**3. Completed/cleared empty** — user finished everything (e.g., 0 notifications)
- Positive tone: "You're all caught up!"
- No CTA needed unless there's a clear next action

### Empty State Format

| Field | Content |
|---|---|
| **Screen** | Which screen |
| **Type** | First-time / Zero-result / Cleared |
| **Illustration description** | What to show visually (describe simply) |
| **Headline** | Short, human copy |
| **Body** | 1–2 sentences max |
| **CTA** | Button label + destination |

---

## Loading & Transition States

### Loading Patterns by Context

| Context | Pattern | When to Use |
|---|---|---|
| Full page / screen load | Skeleton screen | Always preferred over spinner for content pages |
| Short action (< 1s expected) | Inline spinner on button | Form submit, toggle, quick save |
| Long operation (> 3s) | Progress bar + copy | File upload, report generation, sync |
| Background refresh | Subtle pull-to-refresh | Lists, feeds |
| Navigation transition | Page slide/fade | Between screens |

### Skeleton Screen Rules
- Match the layout of the real content exactly
- Animate with shimmer (left-to-right sweep)
- Show 3–5 placeholder rows for lists
- Never show actual data in a skeleton

### Loading Copy

| Context | Copy |
|---|---|
| Dashboard loading | "Getting your dashboard ready…" |
| Uploading file | "Uploading… [X]%" |
| Saving changes | "Saving…" (disable CTA while active) |
| Long AI/processing operation | "Analyzing your data…" |
| Login | "Signing you in…" |
| Payment processing | "Processing your payment… Don't close this page." |

### Success Transition States

After a completed action, always show feedback:

| Action | Feedback type | Copy example |
|---|---|---|
| Form saved | Toast (bottom) | "Changes saved" |
| Item deleted | Toast (bottom) + undo | "Deleted · Undo" |
| Order placed | Full confirmation screen | "Order confirmed! 🎉" |
| Payment success | Full confirmation screen | "Payment successful" |
| Profile updated | Inline banner | "Profile updated" |
| Email sent | Toast | "Email sent" |

### Transition Format

| Field | Content |
|---|---|
| **Screen / Action** | What just completed |
| **Loading pattern** | Skeleton / Spinner / Progress bar |
| **Loading copy** | Text shown during loading (or "none") |
| **Success feedback type** | Toast / Banner / Confirmation screen |
| **Success copy** | Exact message shown |
| **Duration** | How long toast stays (default: 3s) |
