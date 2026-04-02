# Information Architecture & Navigation Guide

## Sitemap Format

Always use this format for the sitemap:

```
ROOT
├── Onboarding
│   ├── Splash / Landing
│   ├── Sign Up
│   │   ├── Step 1 — Basic Info
│   │   ├── Step 2 — Verification
│   │   └── Step 3 — Profile Setup
│   └── Sign In
│       ├── Email + Password
│       ├── Forgot Password
│       └── OTP Verification
├── [SECTION NAME]
│   ├── [Screen Name]
│   └── [Screen Name]
│       └── [Child Screen]
└── Settings
    ├── Profile
    ├── Notifications
    ├── Privacy & Security
    └── Help & Support
```

## Navigation Pattern Selection

### Mobile App — Decision Rules

| Condition | Recommended Pattern |
|---|---|
| 3–5 top-level sections | Bottom Tab Bar |
| 6+ top-level sections | Hamburger / Drawer |
| Hierarchical content | Stack navigation with back button |
| Wizard / onboarding | Step indicator + Next/Back |
| Content-heavy with sections | Tab bar + scroll |

**Bottom Tab Bar rules:**
- Max 5 tabs
- Always label icons (never icon-only unless icon is universally understood)
- Active state must be visually distinct
- Badge support on notification/cart tabs

### Web App — Decision Rules

| Condition | Recommended Pattern |
|---|---|
| Dashboard / tool-heavy | Left sidebar (collapsible) |
| Content site / informational | Top nav |
| Admin panel | Left sidebar + breadcrumbs |
| Multi-step forms | Step wizard (no nav) |
| Mixed content + tools | Top nav + contextual sidebar |

## Grouping Heuristics

Always group screens into logical sections. Common groups:
- **Onboarding** — everything before the user is logged in and set up
- **Core Feature** — the main thing the user came to do (name it specifically, e.g. "Booking", "Orders", "Feed")
- **Discovery / Browse** — search, explore, filter
- **Account / Profile** — user's own data
- **Settings** — preferences, notifications, privacy
- **Support / Help** — FAQ, contact, report

## IA Annotation Rules

For each screen in the sitemap, note:
- Whether it requires authentication (🔒)
- Whether it's a modal/overlay vs full screen (📋)
- Whether it has a deep-link URL (🔗)
- Whether it appears in navigation (🧭) or is only reachable by action
