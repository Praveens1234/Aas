---
name: uiux-design
description: >
  The ultimate UI/UX design skill for creating world-class interfaces across ALL platforms —
  websites, web apps, mobile apps (iOS/Android), desktop software, portals, dashboards, admin
  systems, SaaS products, and more. Use this skill whenever the user asks to design, wireframe,
  prototype, critique, or improve any interface. Triggers on: "design a UI", "create a screen",
  "how should I lay this out", "make this look better", "UX for my app", "wireframe", "design
  system", "component design", "user flow", "dashboard layout", "mobile screen", "landing page
  design", "portal UI", "admin panel", "improve the UX", "color scheme", "typography", "spacing",
  "accessibility", "responsive design", "dark mode", "onboarding flow", or any request involving
  how software, apps, or websites should look and behave. Always use this skill — even when the
  request seems simple — because great UI/UX requires disciplined thinking, not just aesthetics.
---

# THE ULTIMATE UI/UX DESIGN SKILL
### *"You may have everything. The art is knowing what to show, where, and how."*

---

## THE CORE PHILOSOPHY: THE SPACE-INFORMATION PARADOX

This is the central challenge of all UI/UX design, and it must be internalized before a single pixel is placed:

> **You have infinite information. You have finite space. The user has zero patience.**

Every design decision is a negotiation between:
- **What exists** (all features, all data, all content)
- **What fits** (the viewport, the screen, the fold)
- **What matters** (to the user, at this moment, for this task)

The greatest designers are not those who can make things beautiful. They are those who can make **hard decisions about what to omit** — and then make what remains beautiful, clear, and effortless.

**The Three Laws of UI/UX:**
1. **The Law of One Thing** — Every screen has ONE primary purpose. One. Not three. One.
2. **The Law of Progressive Disclosure** — Show only what the user needs NOW. Reveal complexity on demand.
3. **The Law of Zero Friction** — Every tap, click, scroll, or read costs the user energy. Spend their energy budget wisely.

---

## BEFORE YOU DESIGN ANYTHING: THE DISCOVERY LAYER

Always answer these before touching design:

### 1. WHO is the user?
- Technical expert or complete novice?
- Frequent user (muscle memory matters) or occasional (discoverability matters)?
- Mobile-first or desktop-first context?
- Cultural/language context (LTR/RTL, color meanings, icon interpretation)?
- Accessibility needs (visual, motor, cognitive)?

### 2. WHAT is the job-to-be-done?
- What is the user trying to accomplish? (Not "use the app" — the actual human goal)
- What does success look like for them in 30 seconds? 5 minutes? One session?
- What are the top 3 tasks performed 80% of the time? (Design FOR these. Everything else is secondary.)

### 3. WHERE does it live?
- Platform: Web / Mobile App / Desktop App / Portal / System / Kiosk / Embedded
- Device: Phone (360–430px) / Tablet / Laptop / Large Monitor / Ultra-wide
- Environment: Office, on-the-go, one-handed, gloved hands, bright sunlight?
- Connection: Latency constraints, offline capability?

### 4. WHEN and HOW OFTEN?
- Daily driver app? → Prioritize efficiency, keyboard shortcuts, density
- Rare-use app? → Prioritize discoverability, guidance, forgiving UX
- Emergency-use app? → Prioritize speed, zero cognitive load, high contrast

---

## THE HIERARCHY OF VISUAL WEIGHT: THE MOST IMPORTANT CONCEPT IN UI

Every element on a screen competes for attention. Visual weight is how you direct that competition.

```
VISUAL WEIGHT SCALE (Highest → Lowest):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SIZE         Large > Small
COLOR        Saturated/Warm > Muted/Cool > Neutral
CONTRAST     High contrast > Low contrast
POSITION     Top-left (F-pattern) > Center > Bottom-right
ISOLATION    Element with whitespace > Crowded element  
MOTION       Moving > Static (use sparingly — animation hijacks attention)
TYPOGRAPHY   Bold/Large > Regular/Small > Light/Tiny
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**The Rule:** Every screen should have **ONE element at maximum weight** (the primary CTA or key info), **2–3 elements at medium weight** (navigation, secondary actions), and **everything else at low weight** (support, metadata, secondary info).

If everything is bold → nothing is bold. If everything screams → nothing is heard.

---

## LAYOUT FUNDAMENTALS: THE GRAMMAR OF SPACE

### The Grid System
- **Web:** 12-column grid with 24px gutters (desktop), 4-column (mobile)
- **Mobile:** 4-column or 2-column with 16px margins
- **Desktop App:** 8px base grid (all spacing multiples of 8)
- **Consistency rule:** NEVER place elements arbitrarily. Every position must be grid-justified.

### Spacing: The 8-Point Grid System
```
SPACING TOKENS:
xs   = 4px   (tight nudges, icon gaps)
sm   = 8px   (compact internal padding)
md   = 16px  (standard padding, list gaps)
lg   = 24px  (section padding)
xl   = 32px  (major section breaks)
2xl  = 48px  (hero sections, large gaps)
3xl  = 64px  (page sections)
4xl  = 96px+ (hero breathing room)
```

### The Fold Is Not Dead (But It's Complicated)
- **Above the fold:** Primary value prop, primary CTA, primary navigation
- **Critical principle:** The fold triggers **curiosity** to scroll, it doesn't end reading
- **Never hide the only CTA below fold**
- **Always signal "more below"** via content peek, scroll indicator, or visual momentum

### Reading Patterns
- **F-Pattern:** Information-dense pages (news, articles, data tables) — users scan left edges and first lines
- **Z-Pattern:** Simple landing pages — eye travels Z across the top, diagonal, across bottom
- **Gutenberg Diagram:** Top-left (primary optical area) → Top-right → Bottom-left (fallow) → Bottom-right (terminal action — perfect for CTA)
- **Layer-cake Pattern:** Headers are read, body is skipped — design headers that communicate standalone

---

## TYPOGRAPHY: THE INVISIBLE ARCHITECTURE

Typography is 95% of interface design. It is not decoration. It is structure.

### The Type Scale (Major Third — 1.250 ratio)
```
Display:    48–72px  — Hero titles, splash screens
H1:         36–48px  — Page titles
H2:         28–36px  — Section headers
H3:         22–28px  — Sub-section headers
H4:         18–22px  — Card titles, widget headers
Body-lg:    18px     — Comfortable reading body
Body:       16px     — Standard body text (NEVER go below 14px for body)
Body-sm:    14px     — Captions, labels, metadata
Tiny:       12px     — Legal, footnotes, timestamps (accessibility minimum)
```

### Font Pairing Rules
- **Rule 1:** Maximum 2 typefaces per interface (one display, one body/UI)
- **Rule 2:** Display and body fonts must have clear contrast (serif + sans, geometric + humanist)
- **Rule 3:** For data-heavy UIs (dashboards, tables): use tabular figures (monospaced numbers)
- **Rule 4:** Line height: 1.4–1.6× for body text, 1.1–1.2× for headings
- **Rule 5:** Line length: 60–80 characters per line for reading comfort (not pixels — characters)

### The Weight Discipline
- Use maximum 3 font weights per interface (e.g., Regular 400, Medium 500, Bold 700)
- Never use Light (300) for UI text under 18px — renders poorly on low-DPI screens
- Hierarchy through size FIRST, weight SECOND, color THIRD

---

## COLOR: THE EMOTIONAL ARCHITECTURE

Color communicates meaning before words are read.

### The 60-30-10 Rule
- **60% — Dominant/Neutral:** Background, surfaces, large areas (white, grey, near-black)
- **30% — Secondary:** Navigation bg, card surfaces, sidebar fills
- **10% — Accent:** CTAs, highlights, brand moments, interactive states

### Semantic Color System (Always Define These)
```
PRIMARY:    Brand action color (buttons, links, focus rings)
SUCCESS:    #22c55e range — Confirmations, completed states
WARNING:    #f59e0b range — Caution, needs attention
ERROR:      #ef4444 range — Failures, destructive actions
INFO:       #3b82f6 range — Neutral information
NEUTRAL:    Grey scale — Text, borders, backgrounds
```

### Dark Mode Is Not "Just Invert"
- Dark mode backgrounds: Use #121212 or #0f0f0f (not pure #000000 — too harsh)
- Don't invert colors — recalculate contrast ratios independently
- Reduce color saturation in dark mode (vibrant colors on dark appear to "bleed")
- Elevation in dark mode = lightness, not shadow (lighter surface = higher elevation)

### Contrast Requirements (WCAG 2.1)
```
Normal text (<18px): minimum 4.5:1 contrast ratio
Large text (≥18px bold or ≥24px): minimum 3:1
UI components, focus indicators: minimum 3:1
AAA standard: 7:1 (aim for this on critical interfaces)
```

---

## THE COMPONENT HIERARCHY: ATOMS → ORGANISMS → SCREENS

Design systems thinking is non-negotiable for any serious UI work.

```
ATOMS          — Button, Input, Icon, Badge, Avatar, Tag, Checkbox
MOLECULES      — Search Bar, Form Field + Label + Error, Card Header, Nav Item
ORGANISMS      — Navigation Bar, Data Table, Form, Card Grid, Sidebar
TEMPLATES      — Page Layout, Dashboard Layout, Auth Layout, Empty State
SCREENS/PAGES  — The complete assembled view with real content
```

**Critical rule:** Design components with all states:
- `Default` / `Hover` / `Active` / `Focus` / `Disabled` / `Loading` / `Error` / `Empty` / `Success`

A component without defined states is an unfinished component.

---

## PLATFORM-SPECIFIC MASTERY

Read the appropriate reference file based on the target platform:

| Platform | Reference File | Key Concern |
|---|---|---|
| **Website / Landing Page** | `references/web-design.md` | Conversion, trust, information architecture |
| **Web Application / SaaS** | `references/web-app-design.md` | Workflow efficiency, data density, learnability |
| **Mobile App (iOS/Android)** | `references/mobile-design.md` | Thumb zones, gesture, platform conventions |
| **Desktop Application** | `references/desktop-design.md` | Keyboard, density, multi-panel layouts |
| **Dashboard / Analytics** | `references/dashboard-design.md` | Data hierarchy, scan patterns, chart selection |
| **Admin Panel / Portal** | `references/admin-portal-design.md` | Power user density, bulk operations, navigation |
| **Design Systems** | `references/design-systems.md` | Tokens, component APIs, documentation |
| **Typography & Color Deep Dive** | `references/typography-color.md` | Detailed rules and advanced techniques |
| **Interaction & Motion Design** | `references/interaction-motion.md` | Micro-interactions, transitions, animation principles |

**When a request involves multiple platforms or complex systems — read ALL relevant reference files.**

---

## INTERACTION DESIGN PRINCIPLES

### Fitts's Law (Touch/Click Targets)
```
Mobile touch targets: MINIMUM 44×44px (Apple), 48×48dp (Google)
Desktop click targets: Minimum 24×24px, recommended 32px+
Spacing between targets: Minimum 8px (prevents mis-taps)
Primary CTA: Make it the LARGEST interactive element on screen
```

### The Action Hierarchy
Every screen has a hierarchy of actions:
1. **Primary Action** — One. The thing you WANT the user to do. Maximum visual weight.
2. **Secondary Actions** — 2–3. Supporting tasks. Medium weight.
3. **Tertiary / Destructive Actions** — Minimal weight. Never accidentally clickable.

### Feedback: The Contract With the User
Every action must produce feedback. The user must KNOW their action was received.
```
< 100ms:   Immediate feedback (visual state change) — feels instantaneous
100–300ms: Fast feedback (loading indicator not needed)
300ms–1s:  Show loading state (spinner, skeleton, progress)
1s–10s:    Show progress + cancel option
> 10s:     Break into chunks, show step progress
```

### Error Handling UX (Most Neglected Area)
- **Prevent errors first** (disable impossible actions, format hints, inline validation)
- **Error messages must be:** Human-readable, specific, and tell the user WHAT TO DO
- NEVER: "Error 404" or "Something went wrong" without guidance
- ALWAYS: "Your session expired. [Sign in again →]" — identify what, why, and how to fix

---

## INFORMATION ARCHITECTURE: WHERE EVERYTHING LIVES

### Navigation Patterns and When to Use Them
```
TOP NAV BAR:     Web apps, 5–7 primary sections, desktop-first
SIDEBAR NAV:     Admin panels, dashboards, complex apps with deep hierarchy
BOTTOM TAB BAR:  Mobile apps, 3–5 primary sections, thumb-accessible
HAMBURGER MENU:  Secondary nav, overflow items, NEVER primary nav on desktop
BREADCRUMBS:     Deep hierarchies (e-commerce, file systems, admin)
TABS:            Content switching within a page context (not global nav)
MEGA MENU:       Large content sites with many categories
```

### The 3-Click Rule (And Why It's More Complex)
Users should reach any piece of content within 3 navigation steps — but this is a guideline, not a law. More important: **every step must have clear progress and orientation** ("Where am I? Where can I go? How do I go back?")

### Content Hierarchy Per Screen
```
LEVEL 1 — WHAT IS THIS PAGE?   (Page title, clear purpose statement)
LEVEL 2 — WHAT'S MOST IMPORTANT?  (Hero content, primary data, key status)
LEVEL 3 — WHAT CAN I DO?          (Primary actions, CTAs)
LEVEL 4 — WHAT ELSE IS HERE?      (Secondary content, filters, options)
LEVEL 5 — FINE PRINT / METADATA   (Timestamps, IDs, footnotes, legal)
```

---

## THE DENSITY DIAL: CHOOSING THE RIGHT INFORMATION DENSITY

This is the most misunderstood concept. Density is not about cramming more in. It is about matching the user's cognitive mode.

```
COZY (Low Density):        Consumer apps, onboarding, marketing sites
                           → Large whitespace, large text, few elements
                           → Users are in exploratory or emotional mode

BALANCED (Medium Density): Standard SaaS, user dashboards, settings
                           → Moderate padding, clear groups, standard text
                           → Users are in task-completion mode

COMPACT (High Density):    Admin panels, data tables, professional tools,
                           trading platforms, code editors, analytics
                           → Tight padding, small text, many elements
                           → Users are in expert/power mode
```

**Rule:** NEVER apply low density to a power-user tool (they find it insulting and slow). NEVER apply high density to a consumer app (they find it overwhelming and ugly). Know your user.

---

## RESPONSIVE DESIGN: ONE DESIGN FOR ALL SCREENS

### The Breakpoint System
```
xs:  0–639px       — Mobile portrait (primary mobile target)
sm:  640–767px     — Mobile landscape / small tablet
md:  768–1023px    — Tablet portrait
lg:  1024–1279px   — Tablet landscape / small laptop
xl:  1280–1535px   — Desktop
2xl: 1536px+       — Large desktop / ultra-wide
```

### Mobile-First vs. Desktop-First Decision
- **Mobile-first:** When >50% of your users are on mobile, or when this is a consumer product
- **Desktop-first:** Admin panels, professional tools, B2B SaaS, data-heavy products
- **Adaptive (different UX per platform):** When the use case fundamentally differs between devices (don't just stack desktop columns on mobile — rethink the interaction model)

### The Responsive Transformation Checklist
When adapting from desktop → mobile:
- [ ] Navigation: Top nav → Bottom tab bar OR hamburger
- [ ] Multi-column layouts → Single column (but consider card-based alternatives)
- [ ] Hover states → Add tap states (no hover on touch)
- [ ] Data tables → Cards or horizontal scroll (never squash columns)
- [ ] Forms → Larger inputs, single-column, native input types
- [ ] Modals → Full-screen sheets on mobile
- [ ] Sidebars → Drawer/offcanvas pattern

---

## ACCESSIBILITY: DESIGN FOR EVERYONE

Accessibility is not a feature. It is a quality standard.

### The POUR Principles
- **Perceivable:** Information must be presentable to all senses (alt text, captions, contrast)
- **Operable:** All functionality available via keyboard, no time limits without override
- **Understandable:** Language is clear, errors are identified, interface is predictable
- **Robust:** Works with assistive technologies (screen readers, switch access)

### The Accessibility Checklist
```
VISUAL:
  ✓ 4.5:1 contrast for all normal text
  ✓ Never use color as the ONLY differentiator (add icons/text labels)
  ✓ Visible focus indicators on all interactive elements
  ✓ Images have descriptive alt text (decorative images: alt="")
  
MOTOR:
  ✓ All functions keyboard-accessible (Tab, Enter, Space, Arrow keys, Escape)
  ✓ Touch targets ≥ 44×44px
  ✓ No keyboard traps
  ✓ Skip navigation link for screen reader users
  
COGNITIVE:
  ✓ Consistent navigation and layout
  ✓ Error messages explain what happened AND what to do
  ✓ Input labels always visible (not just placeholder text)
  ✓ Complex processes have step indicators
  ✓ No auto-playing media without user consent
  
SCREEN READERS:
  ✓ Proper heading hierarchy (h1 → h2 → h3, never skip levels)
  ✓ ARIA labels on icon-only buttons
  ✓ Form inputs associated with labels (htmlFor / aria-labelledby)
  ✓ Live regions for dynamic content updates
```

---

## EMPTY STATES, LOADING STATES & EDGE CASES

### Empty States (The Most Neglected Design Opportunity)
An empty state is NOT just "No data found." It is a teaching moment and an opportunity for conversion.

**Anatomy of a great empty state:**
1. **Illustration or Icon** — Sets tone, confirms this is intentional
2. **What's Empty** — Be specific ("No projects yet" not "Nothing here")
3. **Why It Matters / What This Area Does** — Contextual education
4. **Primary CTA** — Direct path to resolution ("Create your first project →")

### Skeleton Screens vs. Spinners
- **Skeleton screens:** Preferred for content-heavy layouts (social feeds, article lists, card grids) — shows structure before content, feels faster
- **Spinners:** Use for short operations (<2s), targeted areas, action confirmations
- **Progress bars:** Use when duration is predictable, or for multi-step processes
- **NEVER:** Show a full-page spinner on a page that could load progressively

### Error States Hierarchy
```
INLINE VALIDATION:  Real-time as user types (email format, password strength)
FIELD-LEVEL ERROR:  On blur/submit — red border + error message below field
FORM-LEVEL ERROR:   Summary at top of form for multi-field submission errors
PAGE-LEVEL ERROR:   Full page 404/500 with clear navigation back
TOAST/SNACKBAR:     Non-blocking, transient confirmations and minor errors
MODAL DIALOG:       Critical confirmations only (destructive actions)
```

---

## THE DESIGN CRITIQUE FRAMEWORK

When evaluating or improving an existing design, use this structured assessment:

### The VICES Framework
```
V — Visual Hierarchy:    Can I identify the primary element in 3 seconds?
I — Information Load:    Is there anything that can be removed without loss?
C — Consistency:         Are patterns repeated reliably? Is the system coherent?
E — Effort/Friction:     How many steps/clicks to complete the core task?
S — Space:               Is whitespace used as a design tool, or just filler?
```

### The 5-Second Test
Show the design to someone for exactly 5 seconds. Ask:
1. What is this page for?
2. What's the most important thing on this page?
3. What can you do on this page?

If they can't answer all three correctly → the design has failed its primary job.

---

## OUTPUT FORMAT GUIDE: HOW TO DELIVER DESIGN WORK

Depending on the request, deliver in the most appropriate format:

| Request Type | Deliverable |
|---|---|
| Layout structure, wireframe | ASCII wireframe + annotated explanation |
| Visual design, UI | HTML/CSS artifact (full rendered UI) OR React component |
| Design critique | VICES framework analysis + specific recommendations |
| Color palette | Named palette with hex codes + usage rules + contrast ratios |
| Typography system | Type scale table + pairing rationale + usage examples |
| Component spec | State-by-state breakdown with dimensions, colors, behaviors |
| User flow | Mermaid flowchart + decision point annotations |
| Design system | Token tables + component catalog + usage guidelines |
| Mobile screen | Device-framed HTML/React artifact with touch target annotations |
| Full design spec | Markdown document with all specs, annotated wireframes, component breakdown |

### When Building HTML/React UI Artifacts:
- Always apply this skill's principles: visual hierarchy, spacing system, typography
- Include ALL interactive states in CSS (hover, focus, active, disabled)
- Make it responsive unless explicitly told not to
- Use semantic HTML (nav, main, section, article, aside, footer)
- Never use placeholder gray boxes — use realistic representative content

---

## THE ANTI-PATTERNS: WHAT GREAT DESIGNERS NEVER DO

```
✗ NEVER: Multiple competing primary CTAs (two "primary" buttons destroy hierarchy)
✗ NEVER: Placeholder text as the only label (disappears when user types — accessibility failure)
✗ NEVER: Hamburger menus for primary navigation on desktop
✗ NEVER: Disable the submit button without telling the user why it's disabled
✗ NEVER: Auto-advance carousels (users are reading; you're interrupting)
✗ NEVER: Horizontal scrolling on mobile (except intentional carousel/map contexts)
✗ NEVER: Using color alone to convey meaning (color blindness affects 8% of males)
✗ NEVER: Modal-on-modal stacking (you've lost the user)
✗ NEVER: Infinite scroll + footer content (users can never reach the footer)
✗ NEVER: Light grey text on white background (#999 on #fff fails WCAG)
✗ NEVER: Centering body text on large screens (horrible readability past 60ch)
✗ NEVER: Tooltips on mobile (no hover state — content is permanently hidden)
✗ NEVER: Generic "Submit" button labels (use the action: "Create Account", "Save Changes")
✗ NEVER: Icons without labels for non-universal icons (hamburger/close are known; others aren't)
✗ NEVER: Asking for information you don't need in forms (every extra field drops conversion ~10%)
```

---

## QUICK DECISION TREES

### "Should this be a modal or a new page?"
- **Modal if:** Small amount of content, quick action, user needs current page context to complete the action
- **New page if:** Complex form, multi-step process, shareable URL needed, substantial content

### "Should this be a card or a list row?"
- **Card if:** Visual content matters, items are roughly equal in importance, grid browse mode
- **List row if:** Scanning by one attribute (name, date), dense data, sequential reading, table comparison

### "Where should the primary CTA go?"
- **Always visible** — not buried below fold
- **After the value proposition** — never before the user understands what they're agreeing to
- **Isolated** — significant whitespace around it, no competing elements

### "Should I use tabs or a sidebar for navigation?"
- **Tabs:** Parallel content on same level, fewer than 7 items, content comparison likely
- **Sidebar:** Deep hierarchy, many items, frequent switching expected, power-user context

---

---


---

## ═══════════════════════════════════════════════════════
## PLATFORM DEEP-DIVE: MOBILE APP UI/UX
## iOS · Android · React Native · Flutter
## ═══════════════════════════════════════════════════════

---

## THE MOBILE CONTEXT: DESIGN FOR THE REAL WORLD

Mobile is not "desktop with smaller screens." It is a fundamentally different context:
- Used one-handed, on-the-go, often distracted
- Network is unreliable — design for offline/slow states
- Battery is precious — avoid heavy animations, background processes
- Screen is an extension of the body — feedback must feel physical

---

## THE THUMB ZONE: THE MOST IMPORTANT MOBILE CONCEPT

For a standard phone (~390px wide), held one-handed:
```
┌─────────────────┐
│  ╔═══════════╗  │  ← HARD REACH (danger zone for primary actions)
│  ║           ║  │
│  ║  Natural  ║  │  ← COMFORTABLE REACH (sweet spot)
│  ║   Reach   ║  │
│  ║           ║  │
│  ╚═══════════╝  │  ← EASY REACH
│  [TAB BAR HERE] │  ← PERFECT for primary nav
└─────────────────┘
```

**Rules:**
- Primary CTAs and tab navigation → BOTTOM of screen
- Destructive actions → TOP (hard to reach = harder to accidentally tap)
- Search → TOP (acceptable — one hand can reach if needed, or use two hands)
- Never put "Delete" or "Confirm" near "Cancel" — separate by distance

---

## iOS vs ANDROID: PLATFORM CONVENTIONS

You MUST respect platform conventions. Users have muscle memory. Breaking it breaks trust.

### iOS Human Interface Guidelines
```
Navigation:   Large Title (scrolling collapses to inline title)
Back gesture: Swipe from left edge (NEVER remove this)
Tab bar:      Bottom, 3–5 items, icon + label, always visible
Modal:        Slides up from bottom (sheet pattern)
Destructive:  Red text in action sheets, confirmation required
Controls:     SF Symbols for icons (system-native recognition)
Typography:   San Francisco (system font) — use SF Pro
Haptics:      Selection feedback, success, warning, error impacts
Status bar:   Design around Dynamic Island / notch
Safe areas:   Always respect top (status/notch) and bottom (home indicator)
```

### Android Material Design 3
```
Navigation:   Navigation bar (bottom, 3–5 items) OR Navigation drawer
Back gesture: System gesture from left/right edge (don't override)
FAB:          Floating Action Button for primary action — bottom right
Sheets:       Bottom sheets for additional options/content
Typography:   Roboto or Google Sans (or your brand font + Material scale)
Colors:       Material You dynamic color system — support user theming
Motion:       Shared element transitions, container transforms
Safe areas:   EdgeToEdge — draw behind status bar and navigation bar
Ripple:       Touch feedback must use ripple on all tappable elements
```

---

## MOBILE NAVIGATION PATTERNS

### Bottom Tab Bar (Most Common, Best UX)
```
- 3 items minimum, 5 maximum
- All tabs always visible — no tab should disappear
- Active state: filled icon + label + brand color
- Badge: Number badge for notifications (max "99+")
- Mid tab "special action": common for camera, compose, etc. (slightly larger)
```

### Top Navigation + Back
```
- Use for drill-down navigation (list → detail → sub-detail)
- Back button: Always present when navigated away from root
- Title: Current screen name (not app name after root)
- Right side: Max 2 icon actions (more → "..." overflow)
```

### Hamburger/Drawer (Use Sparingly)
```
- Only for secondary navigation, not primary app destinations
- Content inside: User profile/avatar at top, nav items, secondary links
- Never put your most important destinations inside a drawer
```

---

## MOBILE TYPOGRAPHY

```
iOS Base:     17pt body, 15pt secondary, 13pt caption (all scalable with Dynamic Type)
Android Base: 16sp body, 14sp secondary, 12sp caption (sp = scale-independent pixels)

MINIMUM readable size:    12px/sp/pt (absolute minimum — prefer 14px+)
Touch target with label:  The label can be smaller but the WHOLE row must be ≥44pt/48dp

Dynamic Type (iOS): MUST support — test at largest accessibility size (310% scale)
Font scaling (Android): MUST support sp units — never px for text
```

---

## MOBILE FORMS: THE MOST PAINFUL PART OF MOBILE UX

Forms are where mobile apps lose users. Every extra field is a conversion killer.

```
RULE 1: Ask for the minimum. Every removed field improves conversion.
RULE 2: Use the right keyboard:
  - Email address: inputmode="email" or type="email"
  - Phone: type="tel"
  - Numbers: inputmode="numeric" or type="number"
  - URL: type="url"
  - Search: type="search" (shows search/go key)
  
RULE 3: Auto-fill support:
  - Enable autocomplete attributes (email, name, tel, address, cc-number, etc.)
  - Support Face ID / Touch ID / Passkeys for auth

RULE 4: Input focus behavior:
  - When keyboard appears → scroll the focused input INTO VIEW (never behind keyboard)
  - Next button on keyboard → moves to next field
  - Last field → Done/Submit

RULE 5: Validation:
  - Validate on blur (when user leaves field), not on keystroke
  - Exception: Password strength → real-time is acceptable and helpful

RULE 6: Date/time pickers:
  - Use native pickers (best familiarity, accessibility)
  - Or custom only if native is genuinely worse for your use case
```

---

## MOBILE GESTURES

```
TAP:           Primary action (activate, select, navigate)
DOUBLE TAP:    Like/zoom (Instagram convention — only use where expected)
LONG PRESS:    Context menu, alternative actions, selection mode
SWIPE LEFT/RIGHT: Delete item (left→), archive, swipe actions
SWIPE DOWN:    Dismiss modal sheets, pull-to-refresh
SWIPE UP:      Show/expand bottom sheets
PINCH:         Zoom in/out (maps, images, documents)
DRAG:          Reorder items, seek in media, drag handles
ROTATE:        Rotate objects (drawing apps, maps)
```

**Rule:** Never use a gesture as the ONLY way to discover a feature. Gestures must be supplemented by visible affordances. (Example: Swipe to delete → also show delete button on long press)

---

## MOBILE PERFORMANCE UX

```
App launch:        < 1 second to first meaningful paint (perceived startup)
Screen transitions: 300ms standard, 200ms for small transitions
List scrolling:    Must be 60fps (no jank — this destroys trust immediately)
Image loading:     Progressive loading + blur-up OR skeleton placeholder
Pull to refresh:   Indicate loading state immediately (spinner appears at pull threshold)
Offline state:     Show cached content with "last updated X ago" banner
                   Never show a blank screen — show what you have, explain what's missing
```

---

## MOBILE-SPECIFIC DESIGN PATTERNS

### The Card
The dominant mobile content unit. Cards must have:
- Clear visual hierarchy within the card
- Clear tap affordance (entire card is tappable OR explicit button)
- Consistent height OR clearly defined variable height pattern
- Image aspect ratio locked (don't let images reflow card heights erratically)

### Pull-to-Refresh
- Show spinner at threshold position
- Spinner drops back to top on release
- Content updates with subtle animation (not a full page reload flash)

### Swipe Actions
- Left swipe: Destructive action (Delete) — use red
- Right swipe: Positive action (Archive, Favorite) — use brand color or green
- Always show a visual "drag handle" hint or instruction on first use

### Bottom Sheet
- Drag handle indicator at top (12px wide pill, 4px tall, 40% opacity)
- Snap points: Half-height, full-height (optional: closed)
- Content scrolls INSIDE the sheet when full-height
- Background dimmed, tap-to-dismiss

### Toast / Snackbar (Mobile)
- Position: Bottom of screen (above tab bar)
- Duration: 3s (info), 5s (with action), persistent (error requiring action)
- Max 1 line + optional 1 action button
- NEVER stack multiple toasts — queue them

---

## MOBILE ACCESSIBILITY

```
VoiceOver (iOS) / TalkBack (Android):
  - All images: contentDescription / accessibilityLabel
  - Interactive elements: Role, label, state (checked, selected, disabled, expanded)
  - Custom gestures: Must have single-tap alternative for screen reader users
  - Reading order: Must match visual order

Dynamic Type / Font Scaling:
  - ALL text must scale with system font size preference
  - Layout must reflow gracefully at large sizes (text wraps, containers expand)
  - Test at maximum accessibility size — many apps completely break

Reduce Motion:
  - Respect prefers-reduced-motion / UIAccessibility.isReduceMotionEnabled
  - Replace sliding transitions with fade when reduce motion is on
  - Never remove ALL animation — remove disorienting parallax and slides

Color & Contrast:
  - Check contrast in both light AND dark mode
  - Test with Grayscale mode enabled (common accessibility setting)
```
---

## ═══════════════════════════════════════════════════════
## PLATFORM DEEP-DIVE: WEBSITES, WEB APPS & DESKTOP SOFTWARE
## SaaS Products · Landing Pages · Portals · Desktop Apps
## ═══════════════════════════════════════════════════════

---

## SECTION A: WEBSITES & LANDING PAGES

### The Landing Page's One Job
A landing page has exactly one goal: convert visitor to the next step (sign up, purchase, contact, download). Every element either supports this goal or is noise.

### Above-the-Fold Formula
```
┌────────────────────────────────────────────────────────┐
│  [LOGO]                    [Nav items]  [CTA Button]   │
├────────────────────────────────────────────────────────┤
│                                                        │
│   HEADLINE: One clear, specific, outcome-focused       │
│   statement. What does the user GET? (Not what          │
│   your product IS — what they ACHIEVE)                 │
│                                                        │
│   Subheadline: Supporting context, a bit longer,       │
│   addresses who it's for or how it works.              │
│                                                        │
│   [PRIMARY CTA]    [Secondary action]                  │
│                                                        │
│   Social proof: "Trusted by 10,000+ teams" / logos    │
│                                          [VISUAL/HERO] │
└────────────────────────────────────────────────────────┘
```

**Headline Rules:**
- Outcome-focused: "Close 3x More Deals" not "The Best CRM Platform"
- Specific beats vague: "Save 5 hours/week on reporting" not "Save time"
- One idea: If you need a comma, it's two headlines. Split them.

### The Trust Hierarchy
Place trust signals in this order (as user scrolls):
1. **Social proof counts** (above fold) — "10,000+ customers"
2. **Logo wall** (well-known customer logos, just below fold)
3. **Feature proof** (HOW it works, screenshots/video)
4. **Testimonials** (real quotes, with real name/photo/company)
5. **Case studies** (detailed ROI stories)
6. **Security/compliance badges** (near purchase/sign-up)
7. **Guarantees / Risk reversal** (next to final CTA — "Cancel anytime")

### Navigation Design for Websites
```
Desktop nav:
  - Max 6–7 primary nav items
  - Right side: 1 ghost button (secondary action) + 1 solid button (primary CTA)
  - Sticky on scroll: YES for most marketing sites
  - Background: Transparent-to-white on scroll is elegant
  - Mega menus: Only for genuinely complex product taxonomies

Mobile nav:
  - Hamburger menu is ACCEPTABLE here (not primary app navigation)
  - Full-screen overlay preferred over drawer for simpler sites
  - Duplicate the primary CTA in mobile menu
  - Close button: Top right AND clicking overlay dismisses
```

---

## SECTION B: WEB APPLICATION (SaaS) DESIGN

### The SaaS Information Architecture Hierarchy
```
APP SHELL:         Always visible — logo, global nav, user avatar, notifications
PAGE LAYOUT:       Main content area + sidebar (optional) + page header
PAGE HEADER:       Page title + primary action + breadcrumb (if nested)
CONTENT AREA:      The actual work area — tables, forms, editors, dashboards
CONTEXTUAL PANELS: Side panels that appear based on selection/action
MODALS:            Confirmations, quick create, critical decisions only
```

### Onboarding: The Most Important UX in SaaS

A user who fails to reach the "Aha! Moment" in the first session is likely gone forever.

```
ONBOARDING FLOW DESIGN:
┌─────────────────────────────────────────────────────────┐
│ Step 1: EMPTY STATE WELCOME                             │
│   - Friendly illustration                               │
│   - Clear "what this is" in 1 sentence                 │
│   - Single CTA: "Get started" / "Create your first X"  │
├─────────────────────────────────────────────────────────┤
│ Step 2: FIRST ACTION (Quick Win)                        │
│   - The simplest possible version of core value         │
│   - Fill-in-the-blank, not open-ended form             │
│   - "Create project" not 20-field setup wizard         │
├─────────────────────────────────────────────────────────┤
│ Step 3: AHA MOMENT                                      │
│   - The moment the user sees value                      │
│   - Celebrate: Confetti, success message, "You did it"  │
│   - Immediately show next step (don't leave them idle) │
├─────────────────────────────────────────────────────────┤
│ Step 4: PROGRESSIVE SETUP                               │
│   - Profile, team invite, integrations — LATER          │
│   - Progress bar showing optional vs. required          │
│   - Dismissible — never trap the user in setup         │
└─────────────────────────────────────────────────────────┘

PROGRESS INDICATOR: "Step 2 of 5" OR percentage bar
SKIP OPTION: Always available (they can set up later)
EMAIL SEQUENCE: Supplement in-app onboarding with email prompts
```

### Settings Architecture
```
SETTINGS ORGANIZATION (universal pattern):
  Account / Profile      → Personal details, avatar, password
  Workspace / General   → Org-level name, timezone, language
  Notifications         → Email, in-app, push notification preferences
  Members & Permissions → Team management, roles, invitations
  Integrations          → Third-party connections
  Billing & Plans       → Subscription, invoices, upgrade
  Security              → 2FA, API keys, sessions
  Danger Zone           → Delete account, data export (at bottom, visually separated)

NEVER put settings in a modal — give them a dedicated page or panel
ALWAYS provide back navigation from settings
SHOW current values as defaults in all settings inputs
```

### Notification Design
```
IN-APP NOTIFICATION BELL:
  - Red dot or number badge when unread
  - Dropdown panel: Max 10 recent, "View all" link
  - Each notification: Avatar/icon + description + timestamp + link
  - Mark all as read option
  - Group similar notifications ("John and 3 others commented")

TOAST NOTIFICATIONS:
  - Position: Top-right (desktop), bottom-center (mobile)
  - Duration: 3s (success), 5s (info/warning), persistent with X (error)
  - Stack max 3 toasts — queue the rest
  - Never dismiss an error toast automatically
  
INLINE BANNERS:
  - Use for page-level alerts (trial expiring, feature announcement)
  - Always dismissible
  - Max 1 banner at a time
  - Position: Below main header, above page content
```

---

## SECTION C: DESKTOP APPLICATION DESIGN

Desktop apps serve power users. The rules are different.

### Desktop ≠ Website
```
Desktop apps have:
  - Keyboard shortcuts (users EXPECT and DEMAND them)
  - Menu bar / ribbon (File, Edit, View, Tools, Help)
  - Right-click context menus (always expected on selectable elements)
  - Drag-and-drop (files, items, panels)
  - Window resizing (design must be fluid from minimum to maximum sizes)
  - Multiple windows / panels (sidebar + main + inspector is classic)
  - Offline-first (file-based apps — data persists without network)
```

### Desktop Layout Archetypes

**Three-Panel (The Classic — VSCode, Figma, Finder):**
```
┌──────┬──────────────────────────────┬──────────┐
│      │                              │          │
│ NAV  │   MAIN WORKSPACE             │ INSPECTOR│
│ TREE │   (editor, canvas, content)  │ / PROPS  │
│      │                              │          │
│      │                              │          │
└──────┴──────────────────────────────┴──────────┘
```
- Left panel: Navigation tree / file explorer / layer panel
- Center: Primary work area — given the most space
- Right panel: Properties, inspector, settings for selected item

**Document + Toolbar (Word, Photoshop):**
```
┌────────────────────────────────────────────────────┐
│ MENU BAR: File  Edit  View  Insert  Format  Help   │
├────────────────────────────────────────────────────┤
│ TOOLBAR: [Bold][Italic][Underline]... [Quick tools]│
├──────────────────────────────────┬─────────────────┤
│                                  │                 │
│        DOCUMENT / CANVAS         │   PROPERTIES    │
│                                  │   PANEL         │
│                                  │   (collapsible) │
└──────────────────────────────────┴─────────────────┘
│ STATUS BAR: Zoom 100% | Page 3/12 | Word count    │
└────────────────────────────────────────────────────┘
```

**Dashboard Hub (Slack, Discord):**
```
┌───┬────────────────────┬──────────────────────────┐
│   │                    │                          │
│ACT│   CHANNEL LIST /   │   MESSAGE / CONTENT      │
│ION│   CONVERSATION     │   AREA                   │
│BAR│   SIDEBAR          │                          │
│   │                    │                          │
└───┴────────────────────┴──────────────────────────┘
```

### Keyboard-First Design Rules
```
Every primary action MUST have a keyboard shortcut.
Standard patterns to ALWAYS respect:
  Ctrl/Cmd + N:     New (file, item, document)
  Ctrl/Cmd + O:     Open
  Ctrl/Cmd + S:     Save
  Ctrl/Cmd + Z:     Undo
  Ctrl/Cmd + Y / Shift+Z: Redo
  Ctrl/Cmd + C/X/V: Copy/Cut/Paste
  Ctrl/Cmd + A:     Select all
  Ctrl/Cmd + F:     Find/Search
  Ctrl/Cmd + W:     Close tab/window
  Ctrl/Cmd + Q:     Quit application
  Escape:           Cancel / Close / Dismiss
  Enter:            Confirm / Submit
  Tab:              Next field
  Arrow keys:       Navigate lists, move selected items
  Delete/Backspace: Delete selected item (with confirmation for destructive)
  F2 or Enter:      Edit selected item (rename)

DISPLAY shortcuts: In tooltips, in menu bar, in command palette
COMMAND PALETTE: Ctrl/Cmd + K — the most powerful power-user feature
```

### Desktop Context Menus
```
Every right-clickable element needs a context menu with:
  - Primary actions for that item (Open, Edit, Rename, Duplicate)
  - Copy/Paste actions
  - --- separator ---
  - Destructive action at bottom (Move to Trash / Delete)

Context menu rules:
  - Max 10 items before needing submenu
  - Submenu arrow: Right-pointing chevron
  - Disabled items: Visible but greyed (shows what's possible, not just what's active)
  - Never put the only way to do something in a context menu (also have a button)
```

### Desktop Window Management
```
Minimum window size: Define and enforce (nothing should break below minimum)
Flexible panels: Resizable with drag handles (show resize cursor on hover)
Collapsed panels: Icon-only sidebar saves space, click to expand
Panel memory: Remember panel widths/positions between sessions
Multi-window: Each window is independent — state not shared but data synced
Tabs within window: For document-based apps (multiple open files)
```

---

## SECTION D: DESIGN SYSTEMS & COMPONENT LIBRARIES

### Design Token Architecture
```
TIER 1 — PRIMITIVE TOKENS (raw values):
  color-blue-500: #3b82f6
  font-size-16: 16px
  space-4: 4px

TIER 2 — SEMANTIC TOKENS (purpose-assigned):
  color-action-primary: {color-blue-500}
  color-text-body: {color-gray-900}
  space-component-padding: {space-4}

TIER 3 — COMPONENT TOKENS (component-specific):
  button-primary-background: {color-action-primary}
  button-primary-padding-x: {space-component-padding}
```

Why three tiers? When your brand color changes from blue to purple, you change ONE primitive token and the entire system updates. This is the power of semantic tokens.

### Component API Design (for design systems)
Each component must document:
```
PROPS/VARIANTS:
  - size: sm | md | lg | xl
  - variant: primary | secondary | ghost | destructive
  - state: default | loading | disabled | error | success

SLOTS/COMPOSITION:
  - What can be composed inside this component?
  - What does it accept as children?

ACCESSIBILITY:
  - ARIA role
  - Keyboard behavior
  - Screen reader announcements

USAGE GUIDELINES:
  - When to use this vs. similar components
  - Anti-patterns (what NOT to do with this component)
  - Examples (code + visual)
```

### The Component Decision Matrix
```
NEED                               → COMPONENT
Single important action            → Button (Primary)
Secondary or competing action      → Button (Secondary) / Ghost button
Dangerous / irreversible action    → Button (Destructive, usually red)
Text-based navigation              → Link (not a button)
Single selection from short list   → Radio Group (if ≤6 options visible)
                                   → Select/Dropdown (if >6 options)
Multiple selection from list       → Checkboxes (if ≤6) or Multi-select
Binary on/off preference           → Toggle Switch
Short text input                   → Input (text)
Long text input                    → Textarea
Structured data with rows          → Table (sortable, filterable)
Visual browsing                    → Card Grid
Status / category label            → Badge / Tag / Chip
Key metric emphasis                → Stat Card / KPI Card
Temporary feedback                 → Toast / Snackbar
Critical confirmation              → Modal Dialog
Secondary information              → Tooltip (hover) or Popover (click)
Page organization                  → Tabs (sibling content)
Navigation hierarchy               → Breadcrumb
Loading unknown-duration content   → Skeleton / Shimmer
Loading known-duration             → Progress Bar / Stepper
```
---

## ═══════════════════════════════════════════════════════
## PLATFORM DEEP-DIVE: DASHBOARDS & DATA VISUALIZATION
## Analytics · Admin Panels · BI · Trading UIs · Monitoring
## ═══════════════════════════════════════════════════════

---

## THE DASHBOARD DESIGN PHILOSOPHY

A dashboard is not a collection of charts. It is an **answer to a specific question** someone has to ask every time they show up to work.

Before designing a single widget:
1. **What question does this dashboard answer?** (One primary question. Maybe 2–3 supporting questions.)
2. **Who is asking this question?** (Executive? Operator? Analyst? On-call engineer?)
3. **What decision does this data enable?** (If no decision follows from seeing the data — the widget doesn't belong on the dashboard)
4. **How often is this dashboard viewed?** (Daily → optimize for change detection. Rarely → optimize for orientation and comprehension)

**The three types of dashboards:**
```
STRATEGIC:    High-level KPIs for executives. Very few metrics. 
              "Are we on track?" Daily or weekly view.
              
OPERATIONAL:  Real-time or near-real-time. Operational staff.
              "Is anything wrong? What do I do?" Used constantly.
              
ANALYTICAL:   Deep-dive, filters, drill-down. Analysts.
              "Why is X happening?" Used in investigation sessions.
```

Design differently for each type. They are not the same product.

---

## INFORMATION HIERARCHY ON DASHBOARDS

```
ZONE 1 — STATUS OVERVIEW (Top, Full Width):
  KPI scorecards, trend indicators, alert banners
  → Answers: "Is everything OK? What's the headline number?"
  → User time: 3–5 seconds

ZONE 2 — PRIMARY CHARTS (Large, Center):
  The 1–3 most important charts for the dashboard's core question
  → Answers: "What does the trend look like? What's changing?"
  → User time: 20–60 seconds

ZONE 3 — SUPPORTING DETAIL (Secondary, Below/Right):
  Breakdowns, comparisons, tables, secondary metrics
  → Answers: "Why? What's driving it? What are the components?"
  → User time: 2–10 minutes (only if Zone 1+2 raised questions)

ZONE 4 — FILTERS & CONTROLS (Top bar or sidebar):
  Date range, segment selectors, view toggles
  → Persistent, always accessible, not visually dominant
```

---

## CHART SELECTION: THE MOST IMPORTANT DASHBOARD DECISION

Choosing the wrong chart type is worse than showing no chart at all.

### The Chart Decision Matrix

```
WHAT ARE YOU SHOWING?          USE THIS:
──────────────────────────────────────────────────────
Change over time               → Line chart (continuous data)
                               → Bar chart (discrete periods, few data points)
                               → Area chart (volume/cumulative, stacked comparisons)

Comparison (few categories)    → Bar chart (horizontal for long labels)
                               → Grouped bar (side-by-side comparison)
                               → Bullet chart (vs. target)

Comparison (many categories)   → Horizontal bar chart (sorted)
                               → Table with inline spark/bar

Part-to-whole (few parts)     → Donut chart (max 5 segments)
                               → Stacked bar (showing both total and parts)
                               → Waffle chart (for percentages)

Part-to-whole (many parts)    → Treemap
                               → Stacked bar with "other" bucket

Correlation / Relationship    → Scatter plot
                               → Bubble chart (3 variables)
                               → Heatmap (matrix correlation)

Distribution                  → Histogram
                               → Box plot (comparing distributions)
                               → Violin plot

Geospatial                    → Choropleth map (rates/densities)
                               → Point map (locations/events)
                               → Proportional symbol map (quantities by location)

Single KPI / Progress          → Scorecard (big number)
                               → Gauge / Radial (limited use — hard to read)
                               → Progress bar (linear, very readable)
                               → Spark line (trend in compact form)
──────────────────────────────────────────────────────
NEVER USE for data dashboards: 3D charts, pie charts with >5 segments,
dual-axis line charts (they mislead), decorative visualizations.
```

---

## CHART DESIGN RULES

### The Data-Ink Ratio (Edward Tufte's Principle)
Every pixel of ink must serve the data. Remove:
- Gridlines that aren't needed (use subtle guides, not grid lines)
- Axis labels that are obvious from context
- Chartjunk: decorative elements, 3D effects, shadows on charts, gradient fills
- Unnecessary chart borders
- Legend if color mapping is self-evident from direct labels

### Color in Charts
```
CATEGORICAL:     Each category gets a distinct color (max 8–10 colors)
                 Use color-blind-safe palettes (avoid red+green alone)
                 
SEQUENTIAL:      Light-to-dark single hue for ordered data (low→high)
                 Example: Light blue → Dark blue for population density

DIVERGING:       Two hues with neutral midpoint (positive/negative)
                 Example: Red → White → Green for performance vs. target

HIGHLIGHT:       One color stands out, everything else is neutral grey
                 Use this for "calling attention" to one data series

THRESHOLD COLOR: Green/amber/red for status (traffic light pattern)
                 Only use when there are clear performance thresholds
```

### Typography in Charts
```
Chart title:    16–20px, bold, states the insight (not just "Sales Over Time" → "Q4 Sales Up 23%")
Axis labels:    12–13px, 60% opacity, don't rotate text unless unavoidable
Data labels:    11–14px, on chart only when < 10 data points
Tooltips:       14px, clean formatting, all relevant values, clear labels
Legend:         12px, placed at top or right, ordered by visual prominence
```

---

## KPI SCORECARDS / STAT CARDS

The most important element on most dashboards. Design them carefully.

```
ANATOMY OF A SCORECARD:
┌─────────────────────┐
│ METRIC LABEL        │  ← 12–14px, muted color, uppercase or medium weight
│                     │
│ 1,284,320           │  ← 28–48px, bold, primary color
│                     │
│ ↑ 12.4% vs last mo  │  ← 12–14px, green/red semantic color + icon
└─────────────────────┘

Rules:
- Show the number first, label second (the number is why you're here)
- Always show comparison: vs. prior period, vs. target, vs. benchmark
- Delta indicator: Use arrows + color + percentage (all three, not just one)
- For large numbers: Format intelligently (1.2M, not 1,284,320 — unless precision matters)
- Spark line in card: Shows trend at a glance — highly valuable addition
```

---

## THE DENSITY CHALLENGE IN DASHBOARDS

Dashboards are inherently high-density. But density must be earned:

```
TOO SPARSE:    10 widgets on a large monitor → feels empty, unprofessional,
               user has to scroll to find what should be immediately visible

OPTIMAL:       14–20 meaningful widgets on a 1440px dashboard
               → Complete picture above the fold or with minimal scroll
               → Every widget earns its space

TOO DENSE:     30+ widgets → cognitive overload, nothing stands out,
               user can't find what matters, the dashboard has no purpose
```

**Density tools:**
- **Tabs:** Separate operational vs. analytical views without removing features
- **Drill-down:** Show summary, allow click-to-detail — don't show all details by default
- **Filters:** Don't show separate charts for each segment — show one filterable chart
- **Progressive disclosure:** Hover for more detail, click for full breakdown

---

## REAL-TIME / LIVE DASHBOARDS

For monitoring systems, trading platforms, infrastructure dashboards:

```
UPDATE INDICATORS:
  - Timestamp: "Last updated: 3 seconds ago" (always visible, always updating)
  - Live badge: Pulsing green dot for live data
  - Stale indicator: Amber/red when data hasn't updated in threshold time

CHANGING VALUES:
  - Flash animation on change (50ms yellow flash → return to normal)
  - Color coding: Green flash for increase, red flash for decrease
  - NEVER animate numbers counting up — just snap to new value
  - For trading: Show change direction, magnitude, velocity together

ALERTS & ANOMALIES:
  - Alert banner at top (dismissible after acknowledgment)
  - Anomalous data point highlighted on chart (different color, tooltip explaining)
  - Alert sound (opt-in only — never play sounds by default)

PERFORMANCE:
  - WebSocket for true real-time (not polling)
  - Virtualize long lists/tables — never render 10,000 rows to the DOM
  - Throttle re-renders — no more than 60fps visual updates
  - Show connection status prominently (Connected / Reconnecting / Offline)
```

---

## DATA TABLES: OFTEN THE BEST VISUALIZATION

Never underestimate a well-designed table. For many dashboards, it IS the right answer.

```
TABLE DESIGN RULES:

HEADERS:
  - Short, clear column names (abbreviate with tooltip if needed)
  - Sticky header on scroll (critical for long tables)
  - Sort indicator on active column (arrow up/down)
  - All numeric columns: right-aligned (so decimal points line up)
  - All text columns: left-aligned
  - Fixed column widths OR well-reasoned flex widths

ROWS:
  - Row height: 40–48px (compact), 48–56px (comfortable)
  - Alternating row colors: Very subtle (2–3% lightness difference) OR just row hover
  - Row hover: Always visible, even on touch (for accessibility and visual feedback)
  - Zebra striping: Optional, helps tracking across wide tables

NUMBERS IN TABLES:
  - Use monospace/tabular figures (all digits same width for column alignment)
  - Thousands separators (1,284 not 1284)
  - Consistent decimal places per column
  - Units in column header, not repeated in every cell
  - Conditional formatting: Color coding for thresholds (use subtle backgrounds, not text color)

PAGINATION vs. INFINITE SCROLL:
  - Pagination: Better for data work (you know where you are, can bookmark)
  - Infinite scroll: Better for browsing (social, content discovery)
  - NEVER: Infinite scroll + needing to find items you've scrolled past

SEARCH & FILTER:
  - Column-level filter (click header → filter popover)
  - Global search above table
  - Active filters shown as dismissible chips
  - "X results" count updates in real time

BULK OPERATIONS:
  - Checkbox column (first column, fixed width)
  - Select-all checkbox in header
  - Floating action bar appears when rows selected
  - Count of selected items in action bar
  - Action bar disappears on deselect (not a permanent toolbar)
```

---

## ADMIN PANEL / PORTAL SPECIFIC RULES

### Navigation
```
Sidebar navigation:
  - Fixed width: 240–280px
  - Collapsible to icon-only: 56–64px (save screen space)
  - Section grouping with headers
  - Current page highlighted (left border accent, background fill)
  - Sub-navigation: Expanding accordion or separate panel
  - User profile at BOTTOM of sidebar (not competing with nav)
```

### Form-Heavy Admin Interfaces
```
- Two-column form layout (label left, input right) for dense forms — ONLY on desktop
- Full-width single column for complex or long forms
- Group related fields with visual sections (dividers, background groups)
- Inline editing: Double-click to edit table cells → saves clicks for bulk edits
- Auto-save vs. explicit save: Auto-save with visible "Saving..." indicator preferred
  for long forms where losing work is painful
```

### Permission & Role States
```
- Disabled elements: 50% opacity + cursor:not-allowed + tooltip explaining WHY
- Role-restricted sections: Clearly labeled (lock icon + "Admin only")
- Upgrade gates: Clear upgrade CTA, not just a locked icon
- Read-only mode: Visual distinction (input becomes styled text, not grey input)
```
---

## ═══════════════════════════════════════════════════════
## INTERACTION DESIGN, MOTION & MICRO-INTERACTIONS
## Animation Principles · Transitions · States · Haptics
## ═══════════════════════════════════════════════════════

---

## THE PURPOSE OF MOTION IN UI

Animation is not decoration. Every animation must serve at least one of these functions:

```
1. ORIENTATION:     Help users understand WHERE they are and WHERE they came from
                    (page transitions, shared element transitions)
                    
2. CAUSALITY:       Show the relationship between action and result
                    (button press → form appears, delete → item removes)
                    
3. FEEDBACK:        Confirm that an action was received
                    (button press state, form submission, toggle switch)
                    
4. ATTENTION:       Direct focus to what matters right now
                    (notification pulse, error shake, highlight flash)
                    
5. CONTINUITY:      Maintain context during content change
                    (skeleton loading, progressive reveal, lazy loading)
```

**If an animation doesn't serve any of these — remove it.**

---

## ANIMATION TIMING: THE PHYSICS OF DIGITAL MOTION

Motion that feels natural follows the physics of the physical world. Objects don't start and stop at constant speed.

### Easing Curves

```
LINEAR:           Feels robotic, unnatural — AVOID for most UI transitions
                  → Use ONLY: loading bars, progress indicators, countdowns

EASE-IN:          Starts slow, ends fast — feels like acceleration
                  → Use: Elements LEAVING the screen (they "fly away")
                  → CSS: cubic-bezier(0.4, 0.0, 1, 1)

EASE-OUT:         Starts fast, ends slow — feels like deceleration
                  → Use: Elements ENTERING the screen (they "land")
                  → CSS: cubic-bezier(0.0, 0.0, 0.2, 1)

EASE-IN-OUT:      Slow start, fast middle, slow end — feels organic
                  → Use: Elements moving WITHIN the screen
                  → CSS: cubic-bezier(0.4, 0.0, 0.2, 1)

SPRING:           Overshoots then settles — feels bouncy and alive
                  → Use sparingly: Mobile dialogs, mobile sheets, playful apps
                  → Too much spring = toy app (inappropriate for professional tools)
```

### Duration Guidelines

```
MICRO:     50–150ms   — State changes (hover, focus, toggle, checkbox tick)
SHORT:     150–300ms  — Small element appearances (dropdown, tooltip, popover)
MEDIUM:    300–500ms  — Page elements entering/exiting, modals, side panels
LONG:      500–800ms  — Page transitions, large content area changes
EXTRA:     800ms+     — Intro animations, onboarding — USE VERY SPARINGLY

RULE: When in doubt, make it FASTER than you think. UIs feel sluggish at
      durations that feel "right" to designers but feel slow to users.
      A 400ms transition that felt smooth in prototyping will feel laggy
      after a user has used your app for 100 hours.
```

---

## MICRO-INTERACTIONS: THE SOUL OF AN INTERFACE

Micro-interactions are the tiny moments of delight and confirmation that make an interface feel alive and trustworthy.

### The Anatomy of a Micro-interaction
```
TRIGGER → RULES → FEEDBACK → LOOPS + MODES

Example — Liking a post:
  TRIGGER:   User taps heart icon
  RULES:     If not liked → like. If liked → unlike.
  FEEDBACK:  Heart fills with red, scales 1.0→1.3→1.0, particle burst
  LOOPS:     Liked count increments. State persists on refresh.
```

### Essential Micro-interactions Catalog

**Button States:**
```
DEFAULT:   Base style
HOVER:     Slight scale (1.01–1.02), background darken/lighten, shadow increase
ACTIVE:    Scale down (0.97–0.98) — physical press sensation
FOCUS:     2–3px ring in primary color, 2px offset from button
LOADING:   Spinner replaces label OR spinner added + label greys out
SUCCESS:   Checkmark replaces/supplements label (green), brief
ERROR:     Shake animation (3–4px left-right, 200ms, ease-out)
DISABLED:  40–50% opacity, cursor:not-allowed, no hover effects
```

**Form Input States:**
```
DEFAULT:   Grey border (#d1d5db)
HOVER:     Slightly darker border
FOCUS:     Brand color border + shadow ring
VALID:     Green border + checkmark icon (on blur)
INVALID:   Red border + error icon + error message below
LOADING:   Spinner inside input (e.g., username availability check)
DISABLED:  Light grey background, no border highlight, cursor:not-allowed
```

**Toggle Switch Animation:**
```
Duration:   200ms
Easing:     ease-in-out
Track:      Background color transitions (grey → brand color)
Thumb:      Slides from left to right (transform: translateX)
Scale:      Thumb briefly scales up 1.1× during transition (optional, feels great)
```

**Checkbox:**
```
Duration:   150ms
Checked:    Background fills, checkmark draws in with path animation
Indeterminate: Dash appears (for partial selection states)
```

**Like / Favorite / Reaction:**
```
Heart/Star:  Scale 1.0 → 1.5 → 1.0, color fills (ease-out then ease-in)
             Optional: Particle burst (hearts/stars fly out radially)
Duration:    400–600ms for the full sequence
```

---

## PAGE & SCREEN TRANSITIONS

### Web App Page Transitions
```
SAME-LEVEL NAVIGATION:    Fade in/out (200–300ms) — safest, always correct
                          OR Crossfade + slight scale (new page scales from 0.98 → 1.0)

DRILL-DOWN (list→detail): Slide left to enter, slide right to go back
                          Shared element: Item card expands to fill new page

GO BACK:                  Reverse the entrance animation

TAB SWITCHING:            Fade between tab content, no directional movement

MODAL OPEN:               Scale from trigger element (origin: source)
                          OR Scale from center (0.9→1.0 + fade, 200ms ease-out)

MODAL CLOSE:              Reverse (scale down + fade, 150ms ease-in)

SHEET (mobile):           Slide up from bottom (300ms ease-out spring)
SHEET DISMISS:            Slide down (200ms ease-in)
```

### Loading Transitions
```
SKELETON SCREENS:
  - Use when: List items, cards, profile pages, content-heavy layouts
  - Shimmer direction: Left to right (matches reading direction)
  - Colors: Light grey (#e5e7eb → #f3f4f6) light mode
             Dark grey (#374151 → #4b5563) dark mode
  - Duration of shimmer loop: 1.2–1.5s
  - Match skeleton to actual content shape EXACTLY

SKELETON → CONTENT TRANSITION:
  - Fade in content at 0% → 100% opacity, 150ms
  - NEVER have skeleton and content visible simultaneously (jarring)
  
PROGRESSIVE LOADING:
  - Load and show items as they arrive (don't wait for all items)
  - Each new item fades in from 0→100% opacity, 100ms
  - Stagger: 30–50ms delay between each item
```

---

## STAGGER ANIMATIONS: LISTS & GRIDS

When multiple items appear, stagger their entrance for a polished effect.

```
STAGGER TIMING:
  Fast list (8+ items):    20–30ms between items
  Medium list (4–7 items): 40–60ms between items
  Slow/featured (2–3):     80–100ms between items

ENTRANCE ANIMATION:
  - Translate: From 0,16px → 0,0 (items slide up slightly)
  - Opacity: 0 → 1
  - Duration per item: 200–300ms, ease-out
  
EXAMPLE STAGGER CSS:
  .item:nth-child(1) { animation-delay: 0ms; }
  .item:nth-child(2) { animation-delay: 30ms; }
  .item:nth-child(3) { animation-delay: 60ms; }
  ...

RULE: Cap total stagger duration at 500ms.
      If you have 20 items at 50ms stagger = 1000ms wait for last item = bad.
      Reduce delay or only stagger the first 8 items.
```

---

## SCROLL ANIMATIONS (USE WITH RESTRAINT)

Scroll-triggered animations are powerful but dangerous:

```
GOOD USES:
  - Landing page section reveals (opacity + slight translateY)
  - Parallax background only (not content — content parallax causes nausea)
  - Progress bars that fill on scroll into view
  - Number counters that start when visible

BAD USES (avoid these):
  - Entire page content hidden until scrolled to (punishes fast scrollers)
  - Heavy parallax on all elements (causes motion sickness)
  - Animations triggered by specific scroll positions that are easy to miss
  - Any animation that BLOCKS or DELAYS information (user is waiting to scroll past)

PERFORMANCE RULE:
  - Only animate: opacity, transform (translate, scale, rotate)
  - NEVER animate: width, height, top, left, margin, padding in scroll handlers
  - Use IntersectionObserver (not scroll event listeners)
  - Use will-change: transform sparingly for complex animations
```

---

## HAPTIC FEEDBACK (MOBILE)

On mobile, motion has a physical counterpart: haptics. They must match.

```
iOS Haptic Types:
  selection:  Light tap — selection change, toggle switch
  light:      Soft impact — confirming non-critical actions
  medium:     Standard impact — confirming important actions
  heavy:      Strong impact — critical confirmations, errors
  success:    Two-tap pattern — task completed successfully
  warning:    Nudge pattern — caution state
  error:      Three-tap descending — failure, blocked action

Rules:
  NEVER: Haptics without visual feedback (they must pair)
  NEVER: Excessive haptics (users will disable them app-wide)
  ALWAYS: Respect system "Reduce Haptics" accessibility setting
```

---

## ANIMATION ACCESSIBILITY

Motion can cause real physical discomfort for users with vestibular disorders.

```
MEDIA QUERY: prefers-reduced-motion

@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

WHAT TO DISABLE:
  ✓ Parallax scrolling effects
  ✓ Auto-playing videos and carousels
  ✓ Large-scale animations (page transitions, full-screen animations)
  ✓ Zoom/scale effects that move large areas
  ✓ Bounce and spring effects

WHAT CAN STAY (even with reduced motion):
  ✓ Opacity fades (no spatial movement)
  ✓ Color transitions
  ✓ Very small movements (<10px displacement)
  ✓ Loading indicators (essential for feedback)
```

---

## DRAG AND DROP UX

```
AFFORDANCES (How user knows it's draggable):
  - Drag handle icon (6-dot grip) → explicit, best for lists
  - cursor: grab on hover → implicit, works for large areas
  - Visual hint on first use ("Drag to reorder") → helpful for discoverability

DURING DRAG:
  - Dragged item: Lift shadow (box-shadow increases), slight scale up (1.03–1.05)
  - Dragged item: 80–90% opacity (translucent — shows it's "in flight")
  - Drop zone: Highlight with dashed border or colored background
  - Other items: Animate out of the way smoothly (spring physics)
  - Ghost image: Dragged element at cursor (browser native or custom)

ON DROP:
  - Item settles into position with spring animation
  - Shadow returns to normal
  - Opacity returns to 100%
  - Auto-save the new order

CANCEL / ESCAPE:
  - Pressing Escape returns item to original position (animated)
  - Dropping outside valid zone: Return animation to original position
```
---

## ═══════════════════════════════════════════════════════
## ADVANCED TYPOGRAPHY & COLOR THEORY
## Type Systems · Color Science · Dark Mode · Iconography
## ═══════════════════════════════════════════════════════

---

## TYPOGRAPHY: THE INVISIBLE ARCHITECTURE (DEEP DIVE)

### Why Typography Is 95% of UI Design

Text is how interfaces communicate. Before any color, image, or animation loads — text conveys meaning. Typography is not about choosing a "nice font." It is the entire system of how information is structured, weighted, and presented.

### Type Classification for UI

```
HUMANIST SANS (Recommended for most UI body text):
  Examples: Inter, IBM Plex Sans, Söhne, Neue Haas Grotesk
  Character: Warm, readable, functional. The workhorse of digital UI.
  Use when: Body text, system interfaces, general-purpose applications

GEOMETRIC SANS (Strong personality, excellent for display):
  Examples: Circular, Futura, DM Sans, Nunito (rounded)
  Character: Modern, clean, approachable. Often used in brand/consumer contexts.
  Use when: Marketing, consumer apps, tech brands

GROTESQUE / NEO-GROTESQUE (Classic, trustworthy):
  Examples: Helvetica Neue, Arial, Aktiv Grotesk, Acumin
  Character: Neutral, functional, authoritative. Corporate gravitas.
  Use when: Finance, enterprise, professional tools

SERIF (Trust, editorial authority):
  Examples: Tiempos, Georgia, Freight Text, Playfair Display
  Character: Traditional, authoritative, luxurious.
  Use when: Editorial, luxury products, legal/finance documents, reading-heavy content

MONOSPACE (Code, data, technical):
  Examples: JetBrains Mono, Fira Code, IBM Plex Mono
  Character: Technical, precise, equal-width columns.
  Use when: Code editors, terminals, data tables, API docs, technical values

SLAB SERIF (Bold presence, accessible):
  Examples: Zilla Slab, Rockwell, Clarendon
  Character: Friendly yet authoritative. Highly legible at all sizes.
  Use when: Educational products, strong brand identities, children's products
```

### The Perfect Pair Formula
```
DISPLAY FONT (headlines, hero text) + BODY FONT (reading, UI text)

Principles:
  - Contrast in classification: Serif display + sans body = excellent
  - Contrast in style: Geometric display + humanist body = excellent
  - Same classification: OK if clearly different weights/sizes
  - Never: Two fonts that are "almost the same" — looks like a mistake

Top reliable pairings:
  Fraunces + Inter                (editorial warmth + functional clarity)
  Playfair Display + Source Sans  (classical elegance + modern readability)
  Cabinet Grotesk + Instrument Serif (contemporary + humanist warmth)
  DM Serif Display + DM Sans     (same family, designed to pair)
  Clash Display + Satoshi         (modern geometric boldness)
```

### Variable Fonts: The Power Move
Variable fonts contain multiple stylistic variations in a single file:
```
font-weight:    100–900 (any value, not just 400/700)
font-width:     Condensed to expanded
font-slant:     Custom italic angle
Custom axes:    Some fonts have brand-specific axes (grade, optical size)

Benefits: Fewer HTTP requests, fine-grained control, smooth animated transitions
          (weight can animate — great for hover effects on bold display text)

Usage: font-variation-settings: 'wght' 450, 'wdth' 95;
```

### Optical Sizing
At large sizes (40px+), reduce letter-spacing (or use negative values).
At small sizes (12–14px), increase letter-spacing slightly for readability.
```
Hero (60px+):     letter-spacing: -0.03em to -0.05em
H1 (40–48px):     letter-spacing: -0.02em
H2 (28–36px):     letter-spacing: -0.01em
H3 (20–24px):     letter-spacing: 0em (neutral)
Body (16–18px):   letter-spacing: 0em to 0.01em
Caption (12px):   letter-spacing: 0.02em to 0.03em (slightly wider for legibility)
ALL CAPS text:    Always add letter-spacing: 0.08–0.12em (CAPS need air)
```

### Typographic Rhythm: Line Height Deep Dive
```
Tight (headlines):        line-height: 1.0–1.2  → Use for 1–2 line display text only
Standard (subheadings):   line-height: 1.3–1.4  → Good for short blocks
Comfortable (body text):  line-height: 1.5–1.7  → Ideal for reading
Loose (long-form):        line-height: 1.7–1.9  → Very long-form, educational
Code blocks:              line-height: 1.5–1.6  → Consistent, helps scan vertically
```

### Measure (Line Length) Rules
The optimum line length for reading body text is **60–80 characters**.

```
At 16px body text:   max-width: 65ch  → approximately 600–680px
At 18px body text:   max-width: 65ch  → approximately 650–720px

NEVER: Full-width text blocks on large monitors (1000px+ wide body text)
       — users' eyes have to travel too far back to the next line

ALWAYS: Apply max-width to article content, prose, forms, email content
EXCEPTION: Dashboards, tables, code blocks can be wider — not reading content
```

---

## COLOR SCIENCE FOR UI DESIGNERS

### The HSL Model: Think Like a Designer

RGB is for machines. HSL (Hue, Saturation, Lightness) is for designers.

```
Hue:        0–360 degrees on the color wheel
              0/360 = Red, 60 = Yellow, 120 = Green, 180 = Cyan,
              240 = Blue, 300 = Magenta
Saturation: 0% = Grey (no color), 100% = Full color
Lightness:  0% = Black, 50% = Pure color, 100% = White

Power of HSL for design systems:
  Same hue, vary lightness → tints and shades (your gray scale)
  Same hue + lightness, vary saturation → muted vs vibrant variants
  Shift hue by 30° → analogous colors (naturally harmonious)
  Shift hue by 180° → complementary color (maximum contrast)
```

### Building a Complete Color Scale
For every brand color, you need a full 10-step scale:

```
EXAMPLE: Brand Blue (hsl(221, 91%, 60%))

50:   hsl(221, 100%, 97%)  ← near white, backgrounds
100:  hsl(221, 95%, 93%)  ← tinted white, hover backgrounds
200:  hsl(221, 93%, 85%)  ← light tint
300:  hsl(221, 92%, 75%)  ← medium light
400:  hsl(221, 91%, 65%)  ← light-medium (accessible on dark)
500:  hsl(221, 91%, 60%)  ← BRAND COLOR (your core)
600:  hsl(221, 82%, 50%)  ← medium dark (text on light bg - test contrast)
700:  hsl(221, 75%, 42%)  ← dark (body text - good contrast)
800:  hsl(221, 70%, 32%)  ← very dark
900:  hsl(221, 65%, 20%)  ← near black, dark backgrounds

Use: 50–200 for backgrounds and fills
     500–600 for interactive elements
     700–900 for text on light backgrounds
     300–500 for text on dark backgrounds
```

### The Psychology of Color in UI

```
BLUE:     Trust, calm, professionalism, technology
          → Finance, B2B SaaS, healthcare, social networks
          → Danger: Overused — be specific with your shade

GREEN:    Growth, success, nature, health, money
          → Success states universally
          → Danger: Can feel ecological/environmental without intent

RED:      Urgency, error, danger, passion, energy
          → Error states universally, sale/discount pricing, alerts
          → Danger: Don't use red for anything neutral — it triggers alarm

ORANGE:   Energy, enthusiasm, call-to-action, value
          → CTAs for e-commerce (high conversion color)
          → Danger: Can feel cheap if misused, watch saturation

PURPLE:   Premium, creativity, spirituality, royalty
          → Premium products, creative tools, AI/tech products
          → Danger: AI washing — every AI product used purple in 2023

YELLOW:   Warning, attention, optimism, clarity
          → Warning states, highlights, optimistic brands
          → Danger: Very difficult to achieve sufficient contrast

BLACK:    Luxury, sophistication, power, elegance
          → Premium fashion, luxury brands, high-contrast design
          → Danger: Can feel heavy and cold without warm undertones

WHITE:    Cleanliness, space, simplicity, purity
          → Space and breathing room (use as a design tool)
          → Danger: Pure white (#fff) can be harsh — use off-white for backgrounds

GREY:     Neutral, professional, balanced, modern
          → The backbone of every UI color system
          → Use warm greys (slightly yellow) or cool greys (slightly blue)
            — never mix warm and cool greys in the same UI
```

### Contrast: The Accessibility Non-Negotiable

WCAG 2.1 contrast ratios — check with tools (Colour Contrast Analyser, browser devtools):

```
TEXT CONTRAST:
  Normal text (<18px regular, <14px bold):  Minimum 4.5:1  (AA)
  Large text (≥18px regular, ≥14px bold):  Minimum 3:1    (AA)
  Enhanced (AAA):                           7:1 for normal, 4.5:1 for large

UI COMPONENT CONTRAST:
  Button borders, input borders, icons:     Minimum 3:1

COMMON FAILS (check these first):
  ✗ #767676 on #FFFFFF = 4.48:1 (barely fails AA for normal text)
  ✗ #9CA3AF on #FFFFFF = 2.85:1 (major fail — common grey)
  ✗ White text on yellow/light green buttons (very common mistake)
  ✗ Light grey placeholder text on white inputs
  ✗ Dark blue on black (dark mode mistakes)
  
SAFE COMBINATIONS:
  ✓ #374151 on #FFFFFF = 10.7:1 (excellent)
  ✓ #FFFFFF on #2563EB = 4.53:1 (passes AA for normal)
  ✓ #111827 on #F9FAFB = 17.7:1 (excellent — dark on off-white)
```

### Dark Mode Color System
```
DARK MODE IS NOT INVERSION. It is a separate color system.

SURFACES (NOT pure black):
  Background:      #09090b or #0f0f0f or #111113
  Surface 1:       #18181b (cards, panels — slightly lighter)
  Surface 2:       #1c1c1f (elevated components — slightly lighter)
  Surface 3:       #27272a (even more elevated)
  Border:          #3f3f46 (subtle dividers)
  
TEXT (NOT pure white):
  Primary:         #fafafa (near white — softer than pure white)
  Secondary:       #a1a1aa (muted, 60–70% opacity equivalent)
  Tertiary:        #71717a (disabled, timestamps)
  
COLORS (ADJUSTED):
  Reduce saturation 10–15% for all brand colors in dark mode
  Increase lightness for colors used as text (must maintain contrast)
  Never use the same brand color on both light and dark (recalibrate)
  
SHADOWS IN DARK MODE:
  Box shadows don't work on dark backgrounds (shadow is darker than background)
  Use elevation via SURFACE LIGHTNESS instead:
  Lowest elevation:  darkest surface color
  Highest elevation: lightest surface color
  OR use subtle borders instead of shadows
```

### Color-Blind Design
8% of males, 0.5% of females have some form of color vision deficiency.

```
MOST COMMON: Red-Green (Deuteranopia/Protanopia)
  → Never use ONLY red vs. green to differentiate (common in charts, status)
  → Add: Pattern fills on charts, icons, text labels, shape differences

TESTING: 
  → Figma: Plugins "Color Blind" or "A11y - Color Contrast Checker"
  → Mac: Accessibility Display settings → Color Filters → Protanopia/Deuteranopia
  → Chrome DevTools: Rendering → Emulate vision deficiencies

SAFE COMBINATIONS:
  Blue + Orange (most accessible pair — neither affects deuteranopia significantly)
  Blue + Yellow
  Purple + Yellow
  Black + Yellow

ALWAYS PAIR COLOR WITH:
  → Shape (triangle=warning, circle=info, octagon=stop)
  → Icon (✓ for success, ✗ for error, ! for warning)
  → Text label (never rely on color alone for meaning)
  → Pattern (for charts: different fill patterns per category)
```

---

## ICONOGRAPHY SYSTEM

### Icon Grid and Design Rules
```
STANDARD SIZES:    16px, 20px, 24px, 32px, 48px (always multiples of 4)
DESIGN ON:         24px grid with 2px padding = 20px active area
STROKE WIDTH:      1.5px or 2px (consistent throughout entire set)
CORNER RADIUS:     Match your UI border-radius language (sharp vs. rounded)
STYLE:             Outline (most versatile) OR Filled (higher weight, active states)
MIXING RULE:       NEVER mix outline and filled styles in the same context

ICON LIBRARIES:
  Lucide:          Clean, consistent, MIT license (recommended)
  Heroicons:       Tailwind-aligned, two weights (24px outline/solid)
  Phosphor:        6 weights, very comprehensive
  Material Symbols: Google's variable font icon system
  SF Symbols:      iOS/macOS native only (Apple ecosystem)

ICON + LABEL RULE:
  Most icons need a text label. Only universally recognized icons can stand alone:
  ✓ Standalone OK: Search (magnifying glass), Close (×), Menu (hamburger),
                   Home, Back arrow, Share, Delete (trash), Add (+), Edit (pencil)
  ✗ Needs Label:   Industry-specific icons, abstract concepts, anything ambiguous
```

### Icon States
```
DEFAULT:   Base color (inherit text color or explicit icon-color)
HOVER:     Slightly darker/lighter (10–15% lightness shift)
ACTIVE:    Filled version OR brand color
DISABLED:  40% opacity
LOADING:   Spinner replaces icon OR spins alongside
```
---

## ═══════════════════════════════════════════════════════
## DESIGN SYSTEMS, UX RESEARCH & PROCESS
## Tokens · Component APIs · User Research · Heuristics
## ═══════════════════════════════════════════════════════

---

## DESIGN SYSTEMS: THE OPERATING SYSTEM OF A PRODUCT

A design system is not a component library. It is:
- A **shared language** between design and engineering
- A **set of decisions made once** so they don't have to be made again and again
- A **living product** that evolves alongside the product it serves

### The Three Layers of a Design System

```
LAYER 1 — FOUNDATION (Design Tokens + Primitives)
  Colors, Typography, Spacing, Shadows, Borders, Radii, Z-index
  → These are the atoms — no UI meaning, just raw values
  → Defined once, referenced everywhere
  → Change a foundation token → everything updates

LAYER 2 — COMPONENTS
  Buttons, Inputs, Cards, Navigation, Tables, Modals, Alerts
  → Assembled from Layer 1 tokens
  → Documented with all states and variants
  → Accessible and tested

LAYER 3 — PATTERNS & TEMPLATES
  How components combine to solve recurring UX problems
  Form layouts, Empty states, Onboarding flows, Settings pages
  → Documented as reusable patterns, not rigid templates
```

### Design Token Naming Convention
```
FORMAT: {category}-{property}-{variant}-{state}

EXAMPLES:
  color-background-primary
  color-background-primary-hover
  color-text-secondary
  color-text-secondary-disabled
  space-component-padding-sm
  border-radius-interactive
  shadow-elevation-2
  font-size-body
  font-weight-heading
  
RULES:
  - Semantic names (NOT "blue-500" in semantic tokens — use "color-action-primary")
  - Consistent structure (always same order: category-property-variant-state)
  - Hierarchical (category always first)
  - No abbreviations (use "background" not "bg" — reduces ambiguity)
```

### Spacing System Design
```
BASE UNIT: 4px

Full scale:
  0:    0px
  0.5:  2px   (hairline gaps, micro-nudges)
  1:    4px   (icon internal padding, tight inline gaps)
  2:    8px   (small component padding, close related items)
  3:    12px  (medium-tight)
  4:    16px  (standard component padding, list item gaps)
  5:    20px  (slightly generous padding)
  6:    24px  (section internal spacing, card padding)
  8:    32px  (generous padding, major internal sections)
  10:   40px  (large section spacing)
  12:   48px  (major section breaks)
  16:   64px  (large section separators)
  20:   80px  (hero padding, large feature spacing)
  24:   96px  (page margins on large screens)

COMPONENT SPACING TOKENS (semantic):
  component-padding-xs: {space-2}  → 8px
  component-padding-sm: {space-3}  → 12px
  component-padding-md: {space-4}  → 16px
  component-padding-lg: {space-6}  → 24px
  component-gap-sm:     {space-2}  → 8px
  component-gap-md:     {space-4}  → 16px
  section-gap:          {space-12} → 48px
  page-margin:          {space-6}  → 24px (mobile), {space-12} → 48px (desktop)
```

### Border Radius System
```
Choose ONE personality: Sharp (0px), Subtle (4px), Rounded (8px), Soft (16px), Pill (9999px)
Mix WITHIN a system using size relationships — smaller elements have proportionally smaller radius:

SHARP UI:         sm=0, md=0, lg=0, full=0 (enterprise, professional tools)
BALANCED UI:      sm=2px, md=4px, lg=6px, full=9999px
MODERN UI:        sm=4px, md=8px, lg=12px, full=9999px (most SaaS today)
FRIENDLY/SOFT:    sm=6px, md=12px, lg=16px, xl=24px, full=9999px
PLAYFUL:          sm=8px, md=16px, lg=24px, full=9999px (consumer, B2C)

Rule: Badges/Tags/Chips can always use pill (9999px) regardless of system
      Interactive buttons: Usually 1–2 steps above card radius
```

---

## UX RESEARCH: DESIGN IS A HYPOTHESIS, RESEARCH IS THE TEST

### The Research Hierarchy for Design
```
GENERATIVE RESEARCH (Understand the problem):
  User Interviews:     30–60 min, 5–8 participants, open-ended questions
  Ethnographic study:  Observe users in their natural environment
  Diary studies:       Users log behavior over days/weeks
  → OUTPUT: Jobs-to-be-done, pain points, mental models

EVALUATIVE RESEARCH (Test the solution):
  Usability Testing:   5 users find 85% of usability problems (Nielsen's Law)
  A/B Testing:         Statistical validation of design decisions
  5-Second Test:       First impression comprehension check
  Card Sorting:        IA validation (how users categorize content)
  Tree Testing:        Navigation structure validation
  → OUTPUT: Usability issues, conversion data, preference data

ANALYTICS (Measure behavior at scale):
  Heatmaps:           Where users click, move, and scroll (Hotjar, FullStory)
  Session recordings: Watch real user sessions
  Funnel analysis:    Where users drop off in flows
  → OUTPUT: Quantitative validation, discovery of unknown problems
```

### How to Conduct a Usability Test (5 Users, 60 minutes)
```
PREPARATION:
  1. Define: 3–5 specific tasks to test (not "explore the app" — specific tasks)
  2. Recruit: 5 users matching your target persona
  3. Prepare: Prototype or staging environment, screen recording, consent

FACILITATION RULES:
  ✓ Think-aloud protocol: "Please say everything you're thinking as you do this"
  ✓ Never help: If they're stuck, ask "What would you try next?" (not how to do it)
  ✓ Open questions: "What do you expect will happen?" not "Do you understand this?"
  ✓ Observe silence: Confusion often reveals itself in pauses and facial expressions
  ✗ Never: Explain what something is before they interact with it
  ✗ Never: Lead the witness ("Is this button clear?")
  ✗ Never: Apologize for the prototype ("It doesn't work yet but...")

TASKS (Example format):
  "You want to add a new team member to your workspace.
   Please do this as you normally would."
  → Specific goal, realistic scenario, no hints on HOW to do it

METRICS:
  - Completion rate (did they finish the task?)
  - Time-on-task (how long did it take?)
  - Error rate (how many wrong paths taken?)
  - Satisfaction rating (post-task: "How difficult was this?" 1–7)
```

### The Problem Statement Framework
Before designing solutions, articulate the problem precisely:

```
FORMAT:
  [User] needs [to accomplish goal] 
  because [underlying motivation/need], 
  but [current barrier/problem].

EXAMPLE:
  "Marketing managers need to generate weekly performance reports
  because they present them to stakeholders every Monday,
  but the current process requires exporting from 3 tools and
  manually assembling in Excel, taking 3–4 hours each week."

AVOID:
  "Users need a better dashboard" — too solution-focused
  "We need to improve the UX" — not a user problem statement
```

---

## THE UX DESIGN PROCESS

### The Double Diamond Model
```
DISCOVER        DEFINE           DEVELOP          DELIVER
(Diverge)       (Converge)       (Diverge)        (Converge)
    ◆               ◆               ◆               ◆
Research →  Problem framing → Ideation →    Solution delivery
Interviews  → Pain points   → Wireframes → Prototypes → Testing
Observation → Personas      → Concepts  → High-fi designs
Analytics   → Opportunity   → Iteration → Dev handoff
              statement
```

### Design Handoff: The Bridge to Engineering
```
WHAT ENGINEERING NEEDS FROM DESIGN:
  Component specs:      Dimensions (px, % or auto), padding, margin, gap
  Color values:         Hex, HSL, or design token name (preferred)
  Typography:           Font name, weight, size, line-height, letter-spacing
  States:               All interactive states documented (not just default)
  Behavior:             Animation specs (duration, easing, what triggers what)
  Edge cases:           Long text, empty state, loading, error, max items
  Asset export:         Icons (SVG), images (format, retina 2×/3× specs)
  Responsive:           Breakpoint behavior documented for each component

WHAT NOT TO DO IN HANDOFF:
  ✗ Handing off only the happy path (no states, no edge cases)
  ✗ Pixel-perfect requirements for responsive elements (use flex/constraints)
  ✗ Leaving animation undefined ("make it nice" = nightmare for engineers)
  ✗ Font sizes in pt instead of px/rem (causes size mismatches)
  ✗ Undocumented component logic ("the designer will explain it")

TOOLS:
  Figma DevMode: Industry standard — inspect values, export assets, view tokens
  Zeplin: Alternative to Figma DevMode
  Storybook: Living component documentation in code
  Zero-height: Design system documentation sites
```

---

## THE 10 HEURISTICS FOR UI EVALUATION (Nielsen)

Every design should be evaluated against these. These are your universal quality checklist.

```
1. VISIBILITY OF SYSTEM STATUS
   → Does the user always know what's happening?
   → Loading states, progress indicators, confirmation messages

2. MATCH BETWEEN SYSTEM AND REAL WORLD
   → Does it speak the user's language, not internal jargon?
   → "Save" not "Persist to storage"; "Delete" not "Remove entity"

3. USER CONTROL AND FREEDOM
   → Can users undo mistakes? Is there always an "escape hatch"?
   → Undo, cancel, back button, "are you sure?" for destructive actions

4. CONSISTENCY AND STANDARDS
   → Do similar things look and behave similarly?
   → Does it follow platform conventions (iOS/Android/Web)?

5. ERROR PREVENTION
   → Are errors prevented before they happen?
   → Confirmation dialogs, disabling impossible actions, format hints

6. RECOGNITION RATHER THAN RECALL
   → Does the UI show options rather than requiring users to remember?
   → Visible menus, smart defaults, recent items, autocomplete

7. FLEXIBILITY AND EFFICIENCY OF USE
   → Are there shortcuts for power users?
   → Keyboard shortcuts, bulk actions, command palette

8. AESTHETIC AND MINIMALIST DESIGN
   → Is every element necessary?
   → Every extra element competes with the important elements

9. HELP USERS RECOGNIZE, DIAGNOSE, AND RECOVER FROM ERRORS
   → Are error messages clear, specific, and actionable?
   → "Password must be 8+ characters, include a number" not "Invalid input"

10. HELP AND DOCUMENTATION
    → Is help available when needed (not instead of good design)?
    → Inline hints, tooltips, contextual help, empty state guidance
```

---

## SPECIALIZED UI CONTEXTS

### Forms: The Most Conversion-Critical UI
```
FIELD ORDERING PSYCHOLOGY:
  Easy → Hard (build momentum)
  Personal → Transactional (build trust first)
  Name + Email before Credit Card — always
  
REQUIRED vs. OPTIONAL:
  If 90%+ of fields are required: mark OPTIONAL fields only
  If many optional fields: mark REQUIRED fields only
  Never mark both — choose the minority

INPUT MASKING:
  Phone: (555) 555-5555 (format as typed)
  Credit card: 4242 4242 4242 4242 (spaces every 4 digits)
  Date: MM/DD/YYYY (format hint in placeholder)
  
SMART DEFAULTS:
  Country: Auto-detect from IP (allow override)
  State/Province: Cascade from country selection
  Currency: Based on country
  Timezone: Auto-detect from browser
  
VALIDATION TIMING:
  ON BLUR (leaving field): Validate completeness and format
  ON CHANGE (typing): Password strength, real-time availability check
  ON SUBMIT: Full validation, show all errors at once
  NEVER: Validate format while user is still typing (premature error)
```

### Search UX
```
SEARCH INPUT:
  - Placeholder: "Search..." (not instructions — users ignore placeholder)
  - Clear button: × appears as soon as user types
  - Search icon: Left side (indicates purpose), or triggers search if right side
  - Keyboard: Cmd/Ctrl+K to focus (expected convention)
  - Mobile: Full-width, auto-focused on tap

RESULTS:
  - Instant results: Debounce 300ms after keystroke (not on every keystroke)
  - Zero results: Show "No results for X" + suggestions/alternatives
  - Loading: Skeleton of expected results, not spinner
  - Highlighting: Bold/highlight the matching term in results
  
FILTERS:
  - Active filters: Displayed as dismissible chips above results
  - Filter count: "X results" updates in real time
  - Filter persistence: Remember filters in URL params (shareable)
  - Clear all: One-click to remove all active filters
```
