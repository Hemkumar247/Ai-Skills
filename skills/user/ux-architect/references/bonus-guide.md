# Structural Recommendations & Bonus Sections Guide

## Section 8 — Structural Recommendations

Always include these sub-sections:

### 8.1 Navigation Pattern Recommendation
- State the recommended pattern and WHY (based on number of sections, user type, platform)
- Call out any edge cases (e.g., "On mobile, collapse the sidebar to a bottom sheet")

### 8.2 Drop-off Risk Screens
Identify screens where users are most likely to abandon. Flag:
- Long forms (split into steps)
- Screens with too many choices (apply progressive disclosure)
- Screens that load slowly (add skeleton + optimistic UI)
- Screens where the value isn't clear yet (add onboarding tooltips)

### 8.3 Simplification Opportunities
Look for:
- Two screens that could be merged (e.g., edit + preview)
- Flows that have unnecessary confirmation steps
- Settings that could be inline instead of in a separate screen
- Modals that could be inline panels instead

### 8.4 Progressive Disclosure Opportunities
Flag screens where showing everything at once would overwhelm:
- Show basic options first, "Advanced Settings" expandable
- Onboarding: collect only essential info first, fill rest later
- Dashboard: show summary, details on tap
- Forms: show fields progressively based on previous answers

### 8.5 Accessibility Flags
For each screen or component, note WCAG 2.1 AA considerations:

| Consideration | Applies To |
|---|---|
| Minimum touch target 44×44px | All buttons, links, icons |
| Color contrast ≥ 4.5:1 (text) | All text elements |
| Don't rely on color alone for state | Error states, status indicators |
| Screen reader label for icon buttons | Navigation icons, icon-only CTAs |
| Focus indicator visible | All interactive elements |
| Form fields have visible labels | All input fields (not just placeholder) |
| Error messages linked to field | Inline validation messages |
| Keyboard navigable | Web apps especially |

---

## Bonus Section: Design Token Suggestions

When generating this section, define tokens for:

### Color Tokens
```
--color-primary:        [Main brand color — actions, CTAs]
--color-primary-dark:   [Hover/pressed state]
--color-secondary:      [Supporting accent]
--color-surface:        [Card/panel background]
--color-background:     [Page background]
--color-text-primary:   [Body text]
--color-text-secondary: [Labels, captions]
--color-text-disabled:  [Inactive elements]
--color-success:        [Confirmations, success states]
--color-warning:        [Caution, soft alerts]
--color-error:          [Errors, destructive actions]
--color-border:         [Input borders, dividers]
```

Provide hex values based on the industry:
- Fintech: trustworthy blues/greens, high contrast
- Health: calm blues, soft greens, clean white
- E-commerce: energetic accents, clean backgrounds
- SaaS: neutral grays, one strong brand color

### Spacing Scale (4px base)
```
--space-1:  4px
--space-2:  8px
--space-3:  12px
--space-4:  16px   ← default padding
--space-5:  20px
--space-6:  24px   ← section gap
--space-8:  32px
--space-10: 40px
--space-12: 48px   ← large section gap
--space-16: 64px
```

### Type Scale
```
--text-xs:   12px / line-height 1.4  ← captions, labels
--text-sm:   14px / line-height 1.5  ← secondary body
--text-base: 16px / line-height 1.6  ← body text
--text-lg:   18px / line-height 1.5  ← lead text
--text-xl:   20px / line-height 1.4  ← card titles
--text-2xl:  24px / line-height 1.3  ← section headers
--text-3xl:  30px / line-height 1.2  ← page titles
--text-4xl:  36px+ / line-height 1.1 ← hero/display
```

---

## Bonus Section: Component Inventory

List every reusable UI component the product needs. Format:

| Component | Variants | Used On Screens |
|---|---|---|
| Primary Button | Default, Loading, Disabled | All |
| Input Field | Default, Focused, Error, Disabled | All forms |
| Card | Default, Highlighted, Skeleton | Dashboard, Lists |
| Bottom Sheet | Half, Full | Detail views, filters |
| Toast | Success, Error, Info | Post-action feedback |
| Avatar | Small, Medium, Large, Initials fallback | Profile, Nav, Lists |
| Badge | Count, Dot, Status | Nav icons, list items |
| Empty State | Illustration + CTA | All list screens |
| Skeleton | Text, Card, List row | All loading screens |
| [Feature-specific] | ... | ... |

---

## Bonus Section: Cursor/AI IDE Prompt Set

Generate 5–8 ready-to-use Cursor prompts to build the screens:

```
"Read ux-spec.md and build the [Screen Name] screen as a React component.
 Use the microcopy, UI elements, and CTAs exactly as specified."

"Based on ux-spec.md Section 5 (Error States), implement all error handling
 for the [feature] flow with the exact copy provided."

"Using the component inventory in ux-spec.md, create a reusable [Component Name]
 component with all variants listed."

"Build the [Flow Name] user flow from ux-spec.md. Wire up all screens,
 handle all decision points including error paths."
```
