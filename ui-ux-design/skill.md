---
name: uiux-design
version: 2.0
description: >
  The definitive UI/UX design skill for creating world-class interfaces across ALL platforms —
  websites, web apps, mobile apps (iOS/Android), desktop software, portals, dashboards, admin
  systems, SaaS products, AI/chat interfaces, e-commerce, and more. Use this skill whenever
  the user asks to design, wireframe, prototype, critique, audit, or improve any interface.

  Triggers on: "design a UI", "create a screen", "wireframe", "design system", "component
  design", "user flow", "dashboard layout", "mobile screen", "landing page design", "portal UI",
  "admin panel", "improve the UX", "color scheme", "typography", "spacing", "accessibility",
  "responsive design", "dark mode", "onboarding flow", "chat interface", "AI UI", "form design",
  "data table", "empty state", "loading state", "error state", "button design", "navigation",
  "information architecture", "user research", "usability", "conversion rate", "A/B test for
  design", "design critique", "design handoff", "design tokens", "microcopy", "UX writing",
  "animation", "micro-interactions", "icon system", "color palette", or any request about
  how software, apps, or websites should look, feel, or behave.

  ALWAYS use this skill — even for "simple" requests — because world-class UI/UX requires
  disciplined thinking, not just aesthetics. The principles here prevent the thousands of
  small errors that separate amateur from professional interfaces.
---

# THE DEFINITIVE UI/UX DESIGN SKILL  ·  v2.0
### *"You may have everything. The art is knowing what to show, where, when — and what to leave out."*

---

## ▸ HOW TO USE THIS SKILL

This skill is a complete reference system. Navigate it by need:

- **Starting from scratch?** → Begin at §1 (Philosophy), then jump to the relevant Platform Deep-Dive (§10)
- **Critiquing existing design?** → §17 (Evaluation), §1.6 (Visual Weight), §7 (Interaction)
- **Specific component/pattern?** → §6 (Components), §11 (Specialized Patterns)
- **Color/Typography questions?** → §3 (Typography), §4 (UX Writing), §5 (Color)
- **Accessibility review?** → §8 (full WCAG 2.2)
- **Performance/technical UX?** → §12
- **Building a design system?** → §6.4 (Tokens), §15

**Output principle:** Always deliver the most actionable format for the request (see §18 Output Guide).

---

# SECTION 1: PHILOSOPHY & FOUNDATIONS

---

## 1.1 THE CORE PHILOSOPHY: THE SPACE-INFORMATION PARADOX

This is the central challenge of all UI/UX design. Internalize it before placing a single element:

> **You have infinite information. You have finite space. The user has zero patience.**

Every design decision is a negotiation between:
- **What exists** (all features, all data, all content)
- **What fits** (the viewport, the screen, the fold)
- **What matters** (to the user, at this moment, for this task)

The greatest designers are not those who make things beautiful. They are those who make **hard decisions about what to omit** — and then make what remains beautiful, clear, and effortless.

---

## 1.2 THE FOUR LAWS OF UI/UX

```
LAW 1 — THE LAW OF ONE THING
  Every screen has ONE primary purpose. One. Not three. One.
  If you can't state it in 6 words, the screen doesn't know what it is.

LAW 2 — THE LAW OF PROGRESSIVE DISCLOSURE
  Show only what the user needs NOW.
  Reveal complexity on demand. Complexity is available, not present.

LAW 3 — THE LAW OF ZERO FRICTION
  Every tap, click, scroll, or read costs the user energy.
  Spend their energy budget wisely. Never make them work harder than necessary.

LAW 4 — THE LAW OF REVERSIBILITY
  Every destructive action must be reversible or confirmed.
  The terror of permanence breaks trust immediately and permanently.
```

---

## 1.3 GESTALT PRINCIPLES: THE GRAMMAR OF VISUAL PERCEPTION

Before users consciously read anything, their visual system applies these rules automatically. Design with them, not against them.

```
PROXIMITY
  Elements close together are perceived as related.
  → Use tight spacing within groups, generous spacing between groups.
  → Don't rely on lines/borders to group what spacing can achieve.

SIMILARITY
  Elements that look alike are perceived as belonging together.
  → Use consistent style (color, shape, size) for elements of the same type.
  → Break similarity intentionally to create hierarchy.

CONTINUITY
  The eye follows the path of least resistance — lines and curves.
  → Use alignment to create visual flow that guides users through content.
  → Lists, grids, and aligned layouts exploit continuity naturally.

CLOSURE
  The mind completes incomplete shapes.
  → Partial content (truncated text, peeking cards) signals "more below."
  → Rounded corners and bordered containers don't always need solid fills.

FIGURE/GROUND
  The eye distinguishes subjects (figure) from context (ground).
  → Backgrounds must always recede; content must always advance.
  → Modals, tooltips, dropdowns establish figure by separating from ground.

COMMON FATE
  Elements moving in the same direction are perceived as a group.
  → Animate related items together; animate unrelated items independently.
  → Grouped hover states signal logical grouping.

FOCAL POINT
  An element that stands out attracts the eye first.
  → Every screen needs exactly one focal point: the primary CTA or key information.
  → Everything else should support the focal point, not compete with it.

SYMMETRY & ORDER
  Symmetrical layouts feel stable and organized.
  → Use symmetry for formal, trustworthy contexts (banking, legal, healthcare).
  → Use asymmetry intentionally for dynamic, modern contexts.
```

---

## 1.4 COGNITIVE LAWS & MENTAL MODELS

These laws are empirically validated and should inform every design decision:

```
HICK'S LAW
  Decision time increases logarithmically with the number of choices.
  → More options = slower decisions. Ruthlessly reduce choices.
  → Prefer progressive disclosure over showing all options at once.
  → Application: Reduce navigation items. Eliminate redundant CTAs.

MILLER'S LAW  
  Working memory holds 7±2 items simultaneously.
  → Chunk related items into groups of 5–7 maximum.
  → Application: Navigation with 5–7 items, form sections grouped by topic.

JAKOB'S LAW
  Users spend most of their time on OTHER websites.
  → They expect YOUR site to work the same way as the sites they know.
  → Platform conventions aren't optional — they are the contract.
  → Innovation should be in function, not in interaction patterns that already work.

FITTS'S LAW
  Time to hit a target = f(distance ÷ target size).
  → Primary actions: Largest, nearest to the user's cursor/thumb.
  → Destructive actions: Smaller, farther away, requiring deliberate movement.
  → Application: Big CTA buttons. Tiny delete buttons. Positioned accordingly.

DOHERTY THRESHOLD
  Productivity soars when computer and human react in < 400ms.
  → Sub-400ms interactions feel instant. Above 1s feels "slow."
  → Provide immediate visual feedback for all interactions.

PEAK-END RULE
  Users judge an experience by its peak moment and its end.
  → The worst moment (error, frustration) and final moment determine perception.
  → Design the error state as carefully as the success state.
  → End flows on a high note (success animation, clear next step).

ZEIGARNIK EFFECT
  People remember incomplete tasks better than completed ones.
  → Use progress indicators and completion percentages strategically.
  → "Your profile is 60% complete" is more powerful than "Edit profile."

THE AESTHETIC-USABILITY EFFECT
  Users perceive aesthetically pleasing designs as more usable.
  → Beautiful interfaces get more patience during problems.
  → But beauty never substitutes for usability — it supplements it.
```

---

## 1.5 DISCOVERY LAYER: BEFORE YOU DESIGN ANYTHING

Always answer these questions before touching any design work:

### WHO is the user?
- Technical expert or complete novice? (determines vocabulary, defaults, help text density)
- Frequent user (muscle memory matters) or occasional (discoverability matters)?
- Mobile-primary or desktop-primary context?
- Cultural/language context (LTR/RTL, color meanings, icon interpretation, date formats)?
- Accessibility needs: visual (contrast, screen reader), motor (touch target size, keyboard), cognitive (clear language, reduced complexity)?

### WHAT is the job-to-be-done?
- What is the user trying to accomplish? (Not "use the app" — the actual human goal)
- What does success look like in 30 seconds? 5 minutes? One session?
- What are the top 3 tasks performed 80% of the time? (Design FOR these. Everything else is secondary.)
- What are users trying to avoid? (Errors, data loss, embarrassment, wasted time?)

### WHERE does it live?
- Platform: Web / Mobile App / Desktop App / Portal / Kiosk / Embedded / TV / Watch
- Device: Phone (360–430px) / Tablet / Laptop / Large Monitor / Ultra-wide
- Environment: Office, on-the-go, one-handed, gloved hands, bright sunlight, noisy?
- Connection: Always-on, unreliable cellular, offline-first requirement?

### WHEN and HOW OFTEN?
```
Daily driver app       → Prioritize efficiency, keyboard shortcuts, density
Rare-use app           → Prioritize discoverability, guidance, forgiving UX
Emergency-use app      → Prioritize speed, zero cognitive load, extreme clarity
Occasional task app    → Guided flows, smart defaults, undo at every step
High-stakes decisions  → Confirmation patterns, preview states, clear consequences
```

---

## 1.6 VISUAL WEIGHT HIERARCHY: THE MOST IMPORTANT CONCEPT IN UI

Every element on a screen competes for attention. Visual weight is how you control that competition.

```
VISUAL WEIGHT SCALE (Highest → Lowest Attention)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SIZE         Large > Small
COLOR        Saturated/Warm > Muted/Cool > Neutral
CONTRAST     High contrast > Low contrast
POSITION     Top-left (F-pattern start) > Center > Bottom-right
ISOLATION    Element with whitespace > Crowded element
MOTION       Moving > Static  (use sparingly — animation HIJACKS attention)
TYPOGRAPHY   Bold/Large > Regular/Small > Light/Tiny
SHAPE        Irregular/Unique > Rectangular/Common
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**The Distribution Rule:**
Every screen should have:
- **ONE element at maximum weight** (primary CTA or key data point)
- **2–3 elements at medium weight** (navigation, secondary actions, section headers)
- **Everything else at low weight** (support content, metadata, labels, secondary info)

If everything is bold → nothing is bold.
If everything screams → nothing is heard.

---

## 1.7 THE DENSITY DIAL

Density is not about cramming more in. It is about matching the user's cognitive mode.

```
COZY (Low Density)
  For: Consumer apps, onboarding screens, marketing sites, checkout flows
  Characteristics: Large whitespace, large text, few elements, generous padding
  Users are in: Exploratory, emotional, or evaluative mode
  Padding: 24–32px internal, 48–64px between sections
  Text: 16–18px body, generous line height

BALANCED (Medium Density)
  For: Standard SaaS, user dashboards, settings pages, productivity apps
  Characteristics: Moderate padding, clear groups, standard text sizes
  Users are in: Task-completion mode
  Padding: 16–24px internal, 32–48px between sections
  Text: 15–16px body

COMPACT (High Density)
  For: Admin panels, data tables, professional tools, trading platforms, IDEs
  Characteristics: Tight padding, smaller text, many elements per screen
  Users are in: Expert/power mode — they WANT more on screen
  Padding: 8–12px internal, 16–24px between sections
  Text: 13–14px body

CRITICAL RULE:
  NEVER apply low density to a power-user tool (they find it insulting and slow).
  NEVER apply high density to a consumer app (they find it overwhelming).
  KNOW YOUR USER.
```

---

# SECTION 2: LAYOUT & SPATIAL DESIGN

---

## 2.1 THE GRID SYSTEM

```
WEB (12-Column):
  Desktop (1280px+):   12 columns, 24px gutters, 80–120px margins
  Laptop (1024px):     12 columns, 24px gutters, 48–80px margins
  Tablet (768px):      8 columns, 16px gutters, 24–32px margins
  Mobile (360–639px):  4 columns, 16px gutters, 16–20px margins

MOBILE APP:
  Standard:   4-column with 16px margins
  Compact:    2-column with 12px margins

DESKTOP APP:
  8px base grid — ALL spacing and sizing are multiples of 8

CONSISTENCY RULE:
  Never place elements arbitrarily. Every position must be grid-justified.
  The moment one element breaks the grid without intention, the grid breaks.
```

---

## 2.2 THE 8-POINT SPACING SYSTEM

All spacing derives from multiples of 4px (base unit) or 8px (standard unit):

```
SPACING TOKEN SCALE:
  0.5:   2px    (hairline gaps, micro-nudges between tight elements)
  1:     4px    (icon internal gap, badge padding, tight inline)
  2:     8px    (compact internal padding, close related items)
  3:     12px   (medium-tight padding)
  4:     16px   (standard component padding, list item gaps)  ← Most-used
  5:     20px   (slightly generous padding)
  6:     24px   (section internal spacing, card padding)
  8:     32px   (generous section padding)
  10:    40px   (large section spacing)
  12:    48px   (major section breaks, hero sub-sections)
  16:    64px   (large section separators, between page sections)
  20:    80px   (hero padding, major feature spacing)
  24:    96px   (maximum margin / page-level breathing room)

SEMANTIC SPACING TOKENS:
  component-gap-xs:    8px   (tight internal spacing within one component)
  component-gap-sm:    12px  (comfortable internal spacing)
  component-gap-md:    16px  (standard component padding)
  component-gap-lg:    24px  (generous card padding)
  section-gap:         48px  (between major page sections)
  page-margin-mobile:  16px  (left/right margin on mobile)
  page-margin-desktop: 48px  (left/right margin on desktop)
```

---

## 2.3 READING PATTERNS & EYE TRACKING

Design WITH natural eye movement, not against it:

```
F-PATTERN
  Where: Information-dense pages, articles, data-heavy lists, email
  How: Eye reads first horizontal line fully, second line partially, 
       then scans vertically down the left edge
  Design for it: Most critical info in first line of each section
                 Key words at the LEFT edge of each paragraph
                 Left-aligned text always for body content

Z-PATTERN
  Where: Simple landing pages, sparse layouts with few elements
  How: Eye travels: top-left → top-right → diagonal → bottom-left → bottom-right
  Design for it: Logo top-left, navigation top-right, headline diagonal,
                 CTA bottom-right (the "terminal action zone")

GUTENBERG DIAGRAM
  Zones: Primary Optical Area (top-left) → Fallow Areas → Terminal Action (bottom-right)
  Design for it: Most important content top-left, CTA bottom-right
                 Avoid placing important content in top-right or bottom-left

LAYER-CAKE PATTERN
  Where: Any structured content with headers
  How: Users read headers, skip body text, stopping when a header matches their need
  Design for it: Headers must communicate meaning STANDALONE (not just labels)
                 "Your account is expiring" > "Account Status"
```

---

## 2.4 THE FOLD: WHAT IT IS AND ISN'T

```
ABOVE THE FOLD:
  Must contain: Primary value proposition, primary CTA, primary navigation
  
CRITICAL PRINCIPLE:
  The fold is not a wall. It is a curiosity trigger.
  A good fold makes users WANT to scroll — it doesn't end reading.
  
RULES:
  ✓ ALWAYS signal "more below" via content peek, subtle scroll indicator,
    or visual momentum (element partially cut off)
  ✓ NEVER put the only CTA below fold
  ✓ NEVER end a section perfectly at the fold (triggers false bottom)
  ✗ NEVER make users guess whether scrolling is possible
  ✗ NEVER trap all value above fold with nothing below (users trust what they discover)
```

---

## 2.5 RESPONSIVE DESIGN & BREAKPOINTS

### The Breakpoint System
```
xs:   0–639px     Mobile portrait (primary mobile target)
sm:   640–767px   Mobile landscape / small tablet
md:   768–1023px  Tablet portrait
lg:   1024–1279px Tablet landscape / small laptop
xl:   1280–1535px Standard desktop
2xl:  1536px+     Large desktop / ultra-wide
```

### Mobile-First vs. Desktop-First
```
Mobile-first:   When >50% of users are on mobile; consumer products; content sites
Desktop-first:  Admin panels, professional tools, B2B SaaS, data-heavy products

ADAPTIVE (different UX per platform): When the use case fundamentally differs.
  Don't just stack desktop columns on mobile. Rethink the interaction model.
  A data table that works on desktop may need to become cards on mobile.
```

### The Responsive Transformation Checklist
When adapting from desktop → mobile:
```
Navigation:    Top nav → Bottom tab bar OR hamburger
Layouts:       Multi-column → Single column (consider card alternatives)
Hover states:  → Add visible tap states (NO hover on touch devices)
Data tables:   → Cards with key fields, OR horizontal scroll container
Forms:         → Larger inputs (min 44px), single-column, native input types
Modals:        → Full-screen sheets on mobile
Sidebars:      → Drawer/offcanvas pattern
Tooltips:      → Remove entirely (no hover) OR convert to long-press info panels
Density:       → Increase touch targets, reduce density on mobile
```

---

## 2.6 CSS CONTAINER QUERIES (MODERN RESPONSIVE)

Container queries enable components to respond to their parent container's size — not the viewport. This is a paradigm shift for component-based design.

```
USE CASE: A card in a 3-column grid should behave differently than
          the same card in a 1-column list.

TRADITIONAL (Viewport Query):
  @media (max-width: 768px) { /* card layout */ }
  → Problem: Card doesn't know it's in a narrow container at desktop width

MODERN (Container Query):
  .card-container { container-type: inline-size; }
  @container (max-width: 400px) { /* narrow card variant */ }
  → Correct: Card responds to its container, not the viewport

DESIGN IMPLICATIONS:
  Design components for a range of container widths, not just viewport widths.
  A single component needs: compact variant (< 300px), standard (300–600px), 
  expanded (> 600px). Design all three when building component specs.
```

---

## 2.7 CONTENT HIERARCHY PER SCREEN

Every screen must establish a clear content hierarchy:

```
LEVEL 1 — WHAT IS THIS PAGE?
  Page title, clear purpose statement
  → 1 H1 per page, always. This is not optional.

LEVEL 2 — WHAT'S MOST IMPORTANT?
  Hero content, primary data, key status, primary KPI
  → User sees this in the first 3 seconds

LEVEL 3 — WHAT CAN I DO?
  Primary action, main CTA, key form, primary task
  → The most visually prominent interactive element

LEVEL 4 — WHAT ELSE IS HERE?
  Secondary content, supporting data, filters, options
  → Available but not competing for attention

LEVEL 5 — FINE PRINT / METADATA
  Timestamps, IDs, footnotes, legal text, secondary navigation
  → Present but visually receded (smaller, lower contrast)
```

---

# SECTION 3: TYPOGRAPHY

---

## 3.1 THE TYPE SCALE

Typography is 95% of interface design. It is not decoration. It is structure.

### Major Third Scale (1.250 ratio — most versatile for UI)
```
Display:   48–72px   — Hero titles, splash screens, marketing moments
H1:        36–48px   — Page titles (1 per page)
H2:        28–36px   — Section headers
H3:        22–28px   — Subsection headers, card titles
H4:        18–22px   — Widget headers, sidebar titles
Body-lg:   18px      — Comfortable long-form reading
Body:      16px      — Standard body text (NEVER below 14px for body)
Body-sm:   14px      — Captions, labels, metadata, secondary content
Tiny:      12px      — Legal, footnotes, timestamps (WCAG accessibility minimum)
```

### Font Weight Discipline
```
Maximum 3 weights per interface:
  Regular (400)  — Body text, labels
  Medium (500)   — Slight emphasis, navigation
  Bold (700)     — Headings, strong emphasis, CTAs

NEVER use Light (300) for UI text under 18px — renders poorly on low-DPI screens.
Hierarchy: size FIRST, weight SECOND, color THIRD.
```

---

## 3.2 TYPE CLASSIFICATION FOR UI

```
HUMANIST SANS (Best for most UI body text)
  Examples: Inter, IBM Plex Sans, Söhne, Neue Haas Grotesk
  Character: Warm, readable, functional. The workhorse of digital UI.
  Use when: Body text, system interfaces, general-purpose applications

GEOMETRIC SANS (Strong personality, excellent for display)
  Examples: Circular, Futura, DM Sans, Nunito (rounded variant)
  Character: Modern, clean, approachable. Consumer tech personality.
  Use when: Marketing, consumer apps, tech startups

GROTESQUE / NEO-GROTESQUE (Neutral authority)
  Examples: Helvetica Neue, Arial, Aktiv Grotesk, Acumin Pro
  Character: Neutral, functional, authoritative. Corporate gravitas.
  Use when: Finance, enterprise, professional tools

SERIF (Trust, editorial authority)
  Examples: Tiempos, Georgia, Freight Text, Playfair Display
  Character: Traditional, authoritative, premium.
  Use when: Editorial content, luxury products, legal/finance, reading-heavy content

MONOSPACE (Technical precision)
  Examples: JetBrains Mono, Fira Code, IBM Plex Mono, Geist Mono
  Character: Technical, precise, equal-width columns.
  Use when: Code editors, terminals, data tables, technical values, API documentation

SLAB SERIF (Bold, accessible presence)
  Examples: Zilla Slab, Rockwell, Clarendon
  Character: Friendly yet authoritative. Highly legible at all sizes.
  Use when: Educational products, strong brand identities, accessibility-critical contexts
```

---

## 3.3 FONT PAIRING

```
PRINCIPLE: One display font + one body font. Maximum 2 typefaces.
RULE: Contrast in classification or weight = harmonious pair.
      Two similar fonts = looks like a mistake, not a choice.

PROVEN PAIRINGS:
  Fraunces + Inter                 Editorial warmth + functional clarity
  Playfair Display + Source Sans   Classical elegance + modern readability
  Cabinet Grotesk + Instrument Serif  Contemporary boldness + humanist warmth
  DM Serif Display + DM Sans       Same family, designed to pair (foolproof)
  Clash Display + Satoshi          Modern geometric display

FOR DATA-HEAVY UIs (dashboards, tables):
  Use tabular figures (monospaced numbers) — every digit same width
  Test font at all sizes — some "display" fonts are unreadable at 12px
```

---

## 3.4 OPTICAL SIZING: LETTER-SPACING BY SIZE

At large sizes, reduce letter-spacing. At small sizes, increase it slightly.

```
Hero (60px+):       letter-spacing: -0.04em  to  -0.05em
H1  (40–48px):      letter-spacing: -0.02em
H2  (28–36px):      letter-spacing: -0.01em
H3  (20–24px):      letter-spacing:  0em     (neutral)
Body (16–18px):     letter-spacing:  0em  to  0.01em
Caption (12px):     letter-spacing:  0.02em  to  0.03em
ALL-CAPS text:      letter-spacing:  0.08em  to  0.12em  (CAPS always need air)
Code/Mono:          letter-spacing:  0em     (monospace already has built-in tracking)
```

---

## 3.5 TYPOGRAPHIC RHYTHM

```
HEADLINES:      line-height: 1.0–1.2   (tight — display text only)
SUBHEADINGS:    line-height: 1.3–1.4   (short blocks)
BODY TEXT:      line-height: 1.5–1.7   (comfortable reading — this is the sweet spot)
LONG-FORM:      line-height: 1.7–1.9   (educational, documentation, articles)
CODE BLOCKS:    line-height: 1.5–1.6   (vertical scanning needs consistency)

LINE LENGTH (MEASURE):
  Optimal reading measure: 60–80 characters (not pixels — characters)
  At 16px: max-width: 65ch  ≈  600–680px
  At 18px: max-width: 65ch  ≈  650–720px
  NEVER: Full-width text on large monitors. Eyes travel too far back.
  ALWAYS: Apply max-width to article, prose, form content, email
  EXCEPTION: Dashboards, tables, code blocks — not reading content
```

---

## 3.6 VARIABLE FONTS

Variable fonts contain multiple stylistic variations in a single file:

```
AXES:
  font-weight:    100–900 (any value, not just multiples of 100)
  font-width:     Condensed to expanded
  font-optical-size: Optimized for different display sizes
  font-slant:     Custom italic angle

BENEFITS:
  Fewer HTTP requests (one file vs. multiple weights)
  Fine-grained control
  Smooth weight animations possible (hover effects on display text)

CSS USAGE:
  font-variation-settings: 'wght' 450, 'wdth' 95;

TOP VARIABLE FONTS:
  Inter Variable, Recursive, Fraunces, Dela Gothic One, Outfit
```

---

# SECTION 4: UX WRITING & MICROCOPY

---

## 4.1 WHY MICROCOPY IS 50% OF UX QUALITY

Microcopy is every word in the interface that isn't "content" — labels, button text, error messages, placeholders, tooltips, confirmation dialogs, onboarding copy.

**Bad microcopy makes a beautiful UI feel frustrating.**
**Great microcopy makes a simple UI feel effortless.**

The rule: Write the way a smart, helpful human would speak. Not like a machine. Not like legal counsel. Not like marketing.

---

## 4.2 BUTTON LABELS

The most read text in any interface. Every button should answer: "What will happen when I click this?"

```
RULES:
  ✓ Use the ACTION VERB that describes what happens (not just "OK" or "Submit")
  ✓ Be specific: "Create Account" > "Submit" > "OK"
  ✓ Match the heading/context: confirmation modal says "Delete Project?" → button says "Delete Project"
  ✓ Front-load the verb: "Save Changes" > "Changes Saved?"
  ✗ NEVER: "OK", "Submit", "Yes" as primary CTA labels (ambiguous)
  ✗ NEVER: "Click Here" or "Learn More" without context
  ✗ NEVER: Disable a button without indicating why (tooltip or inline message)

VERB PATTERNS:
  Creating something:    "Create [Thing]", "Add [Thing]", "New [Thing]"
  Saving:                "Save Changes", "Save [Thing]", "Update [Thing]"
  Sending:               "Send Message", "Send Invite", "Send Request"
  Navigating:            "Continue", "Next", "Get Started", "View [Thing]"
  Destructive:           "Delete [Thing]", "Remove [Thing]", "Cancel [Thing]"
  Confirming purchase:   "Pay $29", "Complete Order", "Subscribe"

SECONDARY BUTTON (cancel/escape):
  Pair with primary: "Delete Project" / "Keep Project"
  Not just: "Delete" / "Cancel" — be specific what you're canceling
```

---

## 4.3 ERROR MESSAGES

Error messages are the highest-stakes microcopy. Bad errors destroy trust.

```
THE ANATOMY OF A GREAT ERROR MESSAGE:
  1. WHAT happened (clear, specific)
  2. WHY it happened (if helpful and non-technical)
  3. HOW to fix it (specific, actionable)

PRINCIPLES:
  ✓ Human language — not machine codes or technical jargon
  ✓ Specific — not generic ("something went wrong")
  ✓ Actionable — tell the user what to do NEXT
  ✓ Blame the system, not the user — "We couldn't process that" > "You made an error"
  ✓ First person for system errors: "We couldn't load your dashboard"
  ✓ Second person for user input: "Your password needs at least 8 characters"
  ✗ NEVER: "Error 403" or "ENOENT" without human translation
  ✗ NEVER: "Something went wrong. Please try again." (what? why? try again how?)
  ✗ NEVER: Apologize excessively (once is fine; repetition feels hollow)

EXAMPLES:
  ✗ "Invalid input"
  ✓ "Enter a valid email address (example: name@company.com)"

  ✗ "Password is incorrect"
  ✓ "Wrong password. Try again, or reset your password."

  ✗ "Error 500. Internal server error."
  ✓ "We're having trouble loading this page. Try refreshing — if it keeps happening, we're on it."

  ✗ "Payment failed"
  ✓ "Your card was declined. Check your card details or try a different card."

  ✗ "File upload failed"
  ✓ "That file is too large. Files must be under 10 MB. Try compressing it first."
```

---

## 4.4 FORM LABELS & PLACEHOLDER TEXT

```
LABELS (always visible text above the field):
  ✓ Always show labels — NEVER rely on placeholder alone
  ✓ Short and specific: "Email" not "Please enter your email address"
  ✓ Sentence case (not Title Case or ALL CAPS): "Company name" not "COMPANY NAME"
  ✓ Indicate required vs. optional: mark the minority (see §11B)
  ✓ For complex fields: add helper text below (not inside placeholder)

PLACEHOLDER TEXT:
  PURPOSE: Hint at format/example, NOT repeat the label
  ✓ Good: Email field, placeholder "jane@company.com" (shows format)
  ✓ Good: Search field, placeholder "Search projects..." (shows scope)
  ✗ Bad: Placeholder = Label ("Enter your email address") — disappears on focus
  ✗ Bad: Instructions in placeholder ("Must be 8-20 characters") — lost when typing

HELPER TEXT (below field, always visible):
  ✓ Format hints: "Include country code (e.g. +1 555-555-5555)"
  ✓ Character limits: "0/280 characters"
  ✓ Constraints: "Must be 8+ characters with a number and symbol"
  ✓ Context: "This will appear on your public profile"
```

---

## 4.5 CONFIRMATION DIALOGS

```
ANATOMY:
  Title:   States exactly what is about to happen (not a generic "Are you sure?")
  Body:    Explains consequences (what will be lost, what will change)
  Actions: Specific verb buttons (NOT "OK/Cancel")

TEMPLATE:
  Title:   "Delete [item name]?"
  Body:    "This will permanently delete [item] and all [associated data].
            This can't be undone."
  Primary: "Delete [item]"  (red/destructive color)
  Cancel:  "Keep [item]"    (neutral color, clear escape)

WHEN TO REQUIRE CONFIRMATION (not just a dialog):
  For highly destructive actions (delete account, delete workspace, bulk delete 100+ items):
  → Require user to TYPE the name of the thing being deleted
  Example: "Type DELETE to confirm" or "Type your project name to confirm deletion"
  This is intentionally friction. It prevents accidents on irreversible actions.

NEVER CONFIRM:
  Actions that are easily reversible don't need confirmation dialogs.
  "Are you sure you want to log out?" → No. Just log out.
  "Are you sure you want to remove this tag?" → No. Just allow undo.
```

---

## 4.6 EMPTY STATE COPY

An empty state is a teaching moment and an onboarding opportunity — not just "Nothing here."

```
ANATOMY OF A GREAT EMPTY STATE:
  1. Illustration or Icon  → Sets tone, confirms this is intentional
  2. What's Empty         → Specific: "No projects yet" not "Nothing here"
  3. Why It Matters       → Brief: "Projects help you organize your work"
  4. Primary CTA          → Specific action: "Create your first project →"
  5. (Optional) Secondary → "Or import from [other tool]"

COPY PRINCIPLES:
  ✓ Encouraging, not clinical ("Start fresh" > "No data found")
  ✓ Context-aware ("Invite your team to get started" on empty team page)
  ✓ Action-oriented (always give a next step)
  ✗ Never: "No results", "Nothing here", "Empty" as final message

TYPES:
  First-run empty:      User just signed up. Welcoming + motivating.
  Search/filter empty:  "No results for '[query]'" + "Try [suggestion]"
  Cleared/deleted:      Celebrate or acknowledge ("All caught up! ✓")
  Permission empty:     "You don't have access to view this" + who to contact
  Error empty:          "We couldn't load this" + retry option
```

---

## 4.7 ONBOARDING & INSTRUCTIONAL COPY

```
PRINCIPLES:
  ✓ Tell users what they'll accomplish, not what they'll do with the feature
      "Connect your calendar to schedule meetings automatically"
      NOT "Our Calendar Integration™ synchronizes your events bidirectionally"
  ✓ One concept per step. Never explain two things at once.
  ✓ Progress language: "Step 2 of 5" or "You're almost there"
  ✓ Celebrate small wins: "Nice work! You've connected your first integration."
  ✓ Skip always available: "Set this up later" — never trap users in setup
  ✗ Never jargon during onboarding. Users don't yet know your vocabulary.
  ✗ Never exclamation points for features: "You can create unlimited projects!"
    feels like a pitch. Exclamation marks for genuine celebration only.

TOOLTIP COPY:
  ✓ One sentence. Answers "what does this do?" or "when should I use this?"
  ✓ Present tense: "Shows total revenue for the selected period"
  ✗ Not a mini-article: 4 lines of tooltip = UI design failure
```

---

## 4.8 NUMBERS, DATES & UNITS IN UI

```
NUMBERS:
  Large numbers:  Format for scannability (1.2M, not 1,234,567 — unless precision matters)
  Negative:       Always use − (minus sign) not - (hyphen), and color red
  Percentages:    + prefix for increases: "+12.4%", "–3.1%"
  Currency:       Include symbol and match locale format: "$1,234.56" or "€1.234,56"
  Zero-state:     Show "0" with context, not blank: "0 active projects"
  Loading/unknown: Use "—" (em dash), not "null" or "undefined"

DATES & TIME:
  Relative (< 24 hours ago): "Just now", "5 minutes ago", "2 hours ago"
  Relative (< 7 days):       "Yesterday", "3 days ago"
  Absolute (older):          "Jun 8, 2025" or localized format
  Ambiguous:                 Never write "06/08/25" (is it June 8 or August 6?)
  Time zones:                Show timezone when users operate across zones
  Duration:                  "1h 24m" not "84 minutes" for times over an hour

UNITS:
  File sizes: KB, MB, GB (not bytes for human display)
  Distances: Match user locale (miles/km)
  Never: Mix units in the same column of a table
```

---

# SECTION 5: COLOR

---

## 5.1 THE 60-30-10 RULE

```
60% — DOMINANT/NEUTRAL
  Backgrounds, surfaces, large areas
  Values: White, off-white (#F8FAFC), very light grey, near-black in dark mode

30% — SECONDARY
  Navigation backgrounds, card surfaces, sidebar fills, content containers
  Values: Light grey (#F1F5F9), medium grey (#E2E8F0), or subtle brand tint

10% — ACCENT
  CTAs, highlights, brand moments, active states, links
  Values: Your brand primary color, used sparingly so it MEANS something
```

---

## 5.2 SEMANTIC COLOR SYSTEM

Always define ALL of these before designing any component:

```
PRIMARY:      Brand action color
              → Buttons, links, focus rings, active states, interactive highlights

SUCCESS:      #22c55e range (green)
              → Confirmations, completed states, positive deltas, valid inputs

WARNING:      #f59e0b range (amber)
              → Caution states, expiring items, needs-attention alerts

ERROR:        #ef4444 range (red)
              → Failures, destructive actions, invalid inputs, critical alerts

INFO:         #3b82f6 range (blue)
              → Neutral information, tips, announcements, non-critical notices

NEUTRAL:      Full grey scale (#F9FAFB → #111827)
              → Text, borders, backgrounds, disabled states, placeholders

NEVER mix semantic colors:
  Don't use SUCCESS green for brand color (confuses action with confirmation)
  Don't use WARNING amber for brand color (confuses identity with caution)
  Reserve semantic colors for their meaning only.
```

---

## 5.3 BUILDING A COMPLETE COLOR SCALE

For every brand color, build a full 10-step scale (Tailwind-style convention):

```
EXAMPLE: Brand Blue  hsl(221, 91%, 60%)

50:   hsl(221, 100%, 97%)   Near-white backgrounds, very subtle tints
100:  hsl(221, 95%,  93%)   Tinted backgrounds, hover on white
200:  hsl(221, 93%,  85%)   Light tint, focus ring background
300:  hsl(221, 92%,  75%)   Medium-light (accessible on dark backgrounds)
400:  hsl(221, 91%,  65%)   Lighter interactive (hover on primary)
500:  hsl(221, 91%,  60%)   ← BRAND COLOR (core)
600:  hsl(221, 82%,  50%)   Hover/pressed state for primary
700:  hsl(221, 75%,  42%)   Text on light backgrounds (test contrast)
800:  hsl(221, 70%,  32%)   Dark text, dark mode borders
900:  hsl(221, 65%,  20%)   Near-black, dark mode surfaces

USAGE GUIDE:
  50–200:  Backgrounds, hover states, subtle fills
  500–600: Interactive elements (buttons, links, active states)
  700–900: Text on light backgrounds (always check contrast)
  300–500: Text on dark backgrounds (always check contrast)
```

---

## 5.4 DARK MODE: A SEPARATE COLOR SYSTEM

Dark mode is NOT inversion. It is a completely separate system with its own contrast calculations.

```
SURFACE SCALE (avoid pure black — too harsh, no elevation distinction):
  Page Background:    #09090b  or  #0f0f0f  or  #111113
  Surface Level 1:    #18181b  (cards, panels — slightly lighter)
  Surface Level 2:    #1c1c1f  (elevated components, selected items)
  Surface Level 3:    #27272a  (highest elevation, dropdowns)
  Border:             #3f3f46  (subtle dividers, input borders)
  Strong Border:      #52525b  (more visible dividers)

TEXT SCALE (avoid pure white — harsh and tiring):
  Primary Text:       #fafafa  (near-white — 95% lightness)
  Secondary Text:     #a1a1aa  (muted — use for labels, timestamps)
  Tertiary Text:      #71717a  (disabled states, very low-priority info)
  Placeholder:        #52525b  (even more muted)

BRAND COLORS IN DARK MODE:
  Reduce saturation 10–15% (vibrant colors "bleed" on dark backgrounds)
  Increase lightness for text usage (maintain contrast ratio)
  Example: Blue #3b82f6 (light mode) → #60a5fa (dark mode, more accessible)
  NEVER use identical brand color on both modes without testing contrast

ELEVATION IN DARK MODE:
  Shadows don't work on dark (shadow would be darker than background)
  Use surface lightness for elevation instead:
    Lowest elevation = darkest surface (#09090b)
    Highest elevation = lightest surface (#27272a)
  Alternative: Subtle borders instead of shadows

AUTO-DETECTION:
  Always implement: @media (prefers-color-scheme: dark) { }
  Provide manual override toggle (user preference stored in localStorage)
  Respect system preference as default, allow override
```

---

## 5.5 CONTRAST REQUIREMENTS (WCAG 2.2)

```
TEXT CONTRAST (AA Standard):
  Normal text (<18px regular, <14px bold):   Minimum 4.5:1
  Large text (≥18px regular, ≥14px bold):   Minimum 3:1
  
TEXT CONTRAST (AAA Standard — aim for critical interfaces):
  Normal text:   7:1
  Large text:    4.5:1

NON-TEXT UI CONTRAST (buttons, inputs, icons):
  Minimum 3:1 for focus indicators, input borders, icon fills

NEW IN WCAG 2.2:
  Focus Visible (2.4.11): Focus indicator must be at least 3:1 contrast
                          AND at least 2px thick around the element
  Target Size (2.5.8):    Interactive targets must be ≥24×24 CSS pixels
                          (unless adequate spacing compensates)

COMMON FAILS (check these first):
  ✗ #767676 on #FFFFFF = 4.48:1  (barely fails — common body text color)
  ✗ #9CA3AF on #FFFFFF = 2.85:1  (major fail — very common grey)
  ✗ White text on yellow buttons  (almost always fails)
  ✗ Light grey placeholder on white input (fails in almost every implementation)
  ✗ Dark blue text on black dark-mode backgrounds
  ✗ Brand green (#22c55e) on white = 1.6:1 (major fail — never use as text)

SAFE COMBINATIONS:
  ✓ #374151 on #FFFFFF = 10.7:1   (excellent dark grey on white)
  ✓ #FFFFFF on #2563EB = 4.53:1   (white on brand blue — passes AA normal)
  ✓ #111827 on #F9FAFB = 17.7:1   (near-black on off-white — excellent)
  ✓ #FFFFFF on #16A34A = 4.6:1    (white on accessible green)
  
TOOLS: 
  Figma: A11y Color Contrast Checker plugin
  Web: webaim.org/resources/contrastchecker
  Browser DevTools: Accessibility inspector shows contrast ratios live
```

---

## 5.6 COLOR-BLIND ACCESSIBLE DESIGN

8% of males, 0.5% of females have some form of color vision deficiency. Never use color as the ONLY differentiator.

```
MOST COMMON: Red-Green (Deuteranopia/Protanopia)
  Most users cannot distinguish red from green at similar lightness levels.
  
RULE: Color + Shape + Icon + Text label (use multiple channels)
  
NEVER RELY ON COLOR ALONE:
  ✗ Red dot = error, green dot = success (add icons: ✕ and ✓)
  ✗ Red bar vs green bar in charts (add labels or patterns)
  ✗ "The items in red need attention" in instructional copy

SAFE COLOR PAIRS (for charts and status indicators):
  Blue + Orange      (safest pair — both visible in all deficiencies)
  Blue + Yellow
  Purple + Yellow  
  Black + Yellow
  Blue + Red         (works for deuteranopia — not for protanopia)

TESTING:
  Figma: "Color Blind" plugin, or "Stark" plugin
  macOS: System Preferences → Accessibility → Display → Color Filters
  Chrome DevTools: Rendering → Emulate vision deficiency

ICON PAIRING (always include alongside status colors):
  Success:  ✓ checkmark icon + green color
  Warning:  ⚠ triangle icon + amber color
  Error:    ✕ X icon + red color
  Info:     ⓘ circle-i icon + blue color
  Pattern fills: For charts — use different patterns per category, not just colors
```

---

# SECTION 6: COMPONENT SYSTEM

---

## 6.1 ATOMIC DESIGN: ATOMS → ORGANISMS → SCREENS

Design systems thinking is non-negotiable for serious UI work. Every component exists within a hierarchy:

```
ATOMS (single-purpose, indivisible)
  Button, Input, Icon, Badge, Avatar, Tag, Checkbox, Radio,
  Toggle Switch, Spinner, Skeleton, Divider, Tooltip, Label

MOLECULES (2–3 atoms working together)
  Search Bar (Input + Icon + Button)
  Form Field (Label + Input + Error Message + Helper Text)
  Card Header (Avatar + Title + Timestamp + Menu)
  Nav Item (Icon + Label + Badge)
  Stat Card (Label + Number + Delta Indicator + Trend)

ORGANISMS (complex, self-contained sections)
  Navigation Bar, Sidebar, Data Table, Form, Card Grid,
  Modal Dialog, Filter Panel, Toast Stack, Data Chart

TEMPLATES (page-level structural patterns)
  Dashboard Layout, Auth Layout (centered), App Shell (nav + content),
  Settings Layout, Empty State Template, Onboarding Wizard

SCREENS / PAGES (real content applied to templates)
  The final assembled view with actual content, not lorem ipsum
```

**Critical rule:** Every component must be designed with all states:
`Default | Hover | Active | Focus | Disabled | Loading | Error | Empty | Success`
A component without all states documented is an unfinished component.

---

## 6.2 COMPONENT DECISION MATRIX

```
NEED                                → COMPONENT
───────────────────────────────────────────────────────────────────────
Single important action             → Button (Primary)
Secondary or supporting action      → Button (Secondary) / Ghost Button
Dangerous / irreversible action     → Button (Destructive, red-tinted)
Navigation within app               → Link (not a button)
Single selection from ≤5 options    → Radio Group (all visible)
Single selection from >5 options    → Select / Dropdown
Multiple selection from ≤6 options  → Checkboxes
Multiple selection from >6 options  → Multi-select / Combobox
Binary on/off preference            → Toggle Switch
Short text input                    → Input (text)
Long-form text                      → Textarea (resizable)
Number with constraints             → Number Input with min/max
Structured data in rows             → Table (sortable, filterable)
Visual content browsing             → Card Grid
Status / category indicator         → Badge / Chip / Tag
Key metric with context             → Stat Card / KPI Card
Transient feedback (non-blocking)   → Toast / Snackbar
Critical confirmation               → Modal Dialog (confirm/cancel)
Supporting detail on demand         → Tooltip (hover) / Popover (click)
Content on same level               → Tabs
Navigation hierarchy                → Breadcrumb
Unknown-duration loading            → Skeleton / Shimmer
Known-duration progress             → Progress Bar
Multi-step workflow                 → Stepper
Nested/hierarchical navigation      → Accordion / Tree / Nested nav
Date selection                      → Date Picker (native preferred on mobile)
Range selection                     → Range Slider
Rich-text input                     → WYSIWYG Editor (see §11C)
File selection                      → File Upload (see §11C)
───────────────────────────────────────────────────────────────────────
```

---

## 6.3 DESIGN TOKEN ARCHITECTURE (THREE TIERS)

The foundation of any scalable design system. Three tiers ensure single-point-of-change for global updates.

```
TIER 1 — PRIMITIVE TOKENS (raw values, no UI semantics):
  color-blue-500:        #3b82f6
  color-gray-900:        #111827
  font-size-16:          16px
  space-4:               4px
  border-radius-8:       8px
  shadow-md:             0 4px 6px -1px rgb(0 0 0 / 0.1)

TIER 2 — SEMANTIC TOKENS (purpose-assigned, reference primitives):
  color-action-primary:          {color-blue-500}
  color-action-primary-hover:    {color-blue-600}
  color-text-body:               {color-gray-900}
  color-text-secondary:          {color-gray-500}
  color-background-page:         {color-white}
  color-background-surface:      {color-gray-50}
  space-component-padding:       {space-4}
  border-radius-interactive:     {border-radius-8}

TIER 3 — COMPONENT TOKENS (component-specific, reference semantic):
  button-primary-background:     {color-action-primary}
  button-primary-background-hover: {color-action-primary-hover}
  button-primary-padding-x:      {space-component-padding}
  button-primary-border-radius:  {border-radius-interactive}
  input-border-color:            {color-border-default}
  input-border-color-focus:      {color-action-primary}

POWER OF THREE TIERS:
  Brand color changes from blue → purple?
  → Change ONE primitive token: color-blue-500: #8b5cf6
  → ALL buttons, links, focus states, active states update automatically
  → No manual search-and-replace across hundreds of components
```

---

## 6.4 SHADOW SYSTEM

Shadows communicate elevation — how "lifted" above the surface an element is:

```
SHADOW SCALE:
  shadow-xs:    0 1px 2px 0 rgb(0 0 0 / 0.05)         (subtle — inputs, badges)
  shadow-sm:    0 1px 3px 0 rgb(0 0 0 / 0.1),
                0 1px 2px -1px rgb(0 0 0 / 0.1)        (cards at rest)
  shadow-md:    0 4px 6px -1px rgb(0 0 0 / 0.1),
                0 2px 4px -2px rgb(0 0 0 / 0.1)        (dropdowns, popovers)
  shadow-lg:    0 10px 15px -3px rgb(0 0 0 / 0.1),
                0 4px 6px -4px rgb(0 0 0 / 0.1)        (modals, floating elements)
  shadow-xl:    0 20px 25px -5px rgb(0 0 0 / 0.1),
                0 8px 10px -6px rgb(0 0 0 / 0.1)       (large modals, drawers)
  shadow-2xl:   0 25px 50px -12px rgb(0 0 0 / 0.25)   (full-screen overlays)

ELEVATION RULES:
  Static content:    No shadow (it lives on the surface)
  Interactive cards: shadow-sm (lifted but grounded)
  Hover state:       shadow-md (more lift on hover)
  Dropdown/popover:  shadow-md (floating over content)
  Modal/dialog:      shadow-lg (significantly elevated)
  Full overlay:      shadow-2xl (maximum separation)

DARK MODE: Replace shadows with surface lightness (see §5.4)
  Shadows don't read on dark backgrounds.
  Use border or slightly lighter background for elevation instead.
```

---

## 6.5 BORDER RADIUS SYSTEM

Choose ONE personality and be consistent. Never mix systems.

```
SHARP SYSTEM:          sm=0px,  md=0px,  lg=0px,  pill=0px
  → Enterprise software, security tools, some finance products

SUBTLE SYSTEM:         sm=2px,  md=4px,  lg=6px,  pill=9999px
  → Professional tools, B2B SaaS with formal tone

MODERN SYSTEM:         sm=4px,  md=8px,  lg=12px, pill=9999px
  → Most SaaS products today — versatile, contemporary

FRIENDLY SYSTEM:       sm=6px,  md=12px, lg=16px, xl=24px, pill=9999px
  → Consumer apps, educational tools, collaboration software

PLAYFUL SYSTEM:        sm=8px,  md=16px, lg=24px, pill=9999px
  → B2C, games, youth-oriented products

RULES:
  Smaller elements → proportionally smaller radius within your system
  Badges/Chips → always pill (9999px) regardless of system
  Buttons → usually 1 step above card radius within your system
  Input fields → match button radius for visual consistency
  Never mix sharp and rounded in the same component context
```


# SECTION 7: INTERACTION DESIGN & MOTION

---

## 7.1 FITTS'S LAW & TOUCH TARGETS

```
Mobile touch targets:     MINIMUM 44×44px (Apple HIG), 48×48dp (Google Material)
Desktop click targets:    Minimum 24×24px, recommended 32–40px+
Spacing between targets:  Minimum 8px (prevents mis-taps and mis-clicks)
Primary CTA:              Make it the LARGEST interactive element on screen
Destructive actions:      SMALLER + MORE DISTANT from primary actions

WCAG 2.2 — Target Size (2.5.8):
  Minimum 24×24 CSS pixels for all interactive targets.
  If smaller, sufficient spacing must compensate.
  AAA standard (2.5.5): 44×44 CSS pixels minimum.
```

---

## 7.2 THE ACTION HIERARCHY

Every screen needs a clear hierarchy of actions — not a flat list:

```
1. PRIMARY ACTION (one per screen)
   What you WANT the user to do. Maximum visual weight.
   → Filled button in brand color, largest button on screen

2. SECONDARY ACTIONS (2–3 per screen)
   Supporting tasks the user may legitimately want.
   → Outlined or ghost button, noticeably smaller visual weight

3. TERTIARY / DESTRUCTIVE ACTIONS (treat with extreme caution)
   Rarely needed, potentially harmful.
   → Text-only link style OR separated in space from primary
   → Red for destructive: never accidentally clickable near primary

SPACING RULE:
  Primary and destructive actions must never be adjacent.
  Design physical distance as a safeguard.
```

---

## 7.3 FEEDBACK TIMING: THE USER'S CONTRACT

Every action must produce feedback. The user must KNOW their action was received:

```
< 100ms:    Immediate (visual state change only)
            → Feels instantaneous. Button hover, toggle, checkbox.
            → MUST be this fast for all visual state changes.

100–300ms:  Fast response (no loading indicator needed)
            → Dropdown opening, popover appearing, tooltip showing.

300ms–1s:   Needs loading indicator
            → Spinner on button, progress ring, skeleton overlay.
            → Cancel option not needed at this speed.

1s–10s:     Show progress + cancel option
            → Progress bar with percentage if deterministic
            → Spinner + "Cancel" if indeterminate

> 10s:      Break into steps or move to background
            → "We're processing your request. We'll notify you when it's done."
            → Show queue position or ETA if possible
            → Email/push notification on completion

DOHERTY THRESHOLD: Keep everything interactive under 400ms.
Above 400ms, productivity and trust erode measurably.
```

---

## 7.4 ERROR HANDLING UX

```
PRIORITY ORDER:
  1. PREVENT errors (disable impossible actions, format hints, constraints)
  2. DETECT errors early (inline validation as users complete each field)
  3. RECOVER gracefully (clear message, specific fix, no data loss)

ERROR STATE HIERARCHY:
  Inline validation:    Real-time as user types (email format, password strength only)
  Field-level error:    On blur — red border + error text below field
  Form-level error:     Summary at top for submit with multiple errors
  Toast/snackbar:       Non-blocking, transient notifications
  Modal dialog:         Critical confirmations requiring user decision
  Page-level error:     Full 404/500 page with clear navigation back

ERROR MESSAGE RULES (see §4.3 for copy):
  → Human language, not machine codes
  → Specific: what happened, why, what to do
  → Never blame the user
  → Always offer a path forward
```

---

## 7.5 ANIMATION: EASING & DURATION

### Easing Curves
```
LINEAR:         Feels robotic and mechanical — AVOID for UI
                → Only use for: progress bars, countdowns, loading loops

EASE-IN:        Slow start, fast finish — feels like "leaving"
                → Elements EXITING screen (fly away, dismiss, fade out)
                → CSS: cubic-bezier(0.4, 0.0, 1, 1)

EASE-OUT:       Fast start, slow finish — feels like "arriving"
                → Elements ENTERING screen (appear, drop in, open)
                → CSS: cubic-bezier(0.0, 0.0, 0.2, 1)

EASE-IN-OUT:    Slow → fast → slow — feels organic and natural
                → Elements MOVING within screen (reorder, slide, shift)
                → CSS: cubic-bezier(0.4, 0.0, 0.2, 1)

SPRING:         Overshoots target, then settles — feels alive and physical
                → Mobile sheets, playful modals, bouncy confirmations
                → Use sparingly — inappropriate for professional tools
                → CSS: Use spring physics library (Framer Motion, react-spring)
```

### Duration Reference
```
MICRO (50–150ms):    State changes — hover, focus ring, toggle, checkbox
SHORT (150–300ms):   Small appearances — dropdown, tooltip, popover
MEDIUM (300–500ms):  Element enter/exit — modals, side panels, cards
LONG (500–800ms):    Screen transitions, large content changes
EXTRA (800ms+):      Intro animations, onboarding — VERY SPARINGLY

GOLDEN RULE: When in doubt, make it FASTER than you think.
  Animations that feel "right" in prototype feel "slow" after 100 hours of use.
  A 400ms transition becomes a 400ms annoyance every single time.
```

---

## 7.6 MICRO-INTERACTIONS CATALOG

### Button States
```
DEFAULT:    Base style (brand color fill, white text)
HOVER:      Background darkens 8–10%, scale 1.01–1.02, shadow increases
ACTIVE:     Scale DOWN 0.97–0.98 (physical press sensation) + darker background
FOCUS:      2–3px ring in primary color, 2px offset from button edge (WCAG 2.2 compliant)
LOADING:    Spinner replaces label OR spinner + greyed-out label + cursor:wait
SUCCESS:    Checkmark (✓) + brief green flash → returns to default (200ms)
ERROR:      Shake animation (3–4px left-right, 200ms, ease-out)
DISABLED:   40–50% opacity, cursor:not-allowed, NO hover effects, tooltip explaining why
```

### Form Input States
```
DEFAULT:    Border #d1d5db, white background
HOVER:      Border slightly darker (#9ca3af)
FOCUS:      Brand color border (#3b82f6 example) + soft shadow ring (0 0 0 3px color/20%)
VALID:      Green border + checkmark icon on right (on blur only)
INVALID:    Red border (#ef4444) + error icon + error message text below
LOADING:    Spinner inside input right side (availability check, address lookup)
DISABLED:   Light grey background (#f9fafb), no border highlight, cursor:not-allowed
READ-ONLY:  No border (or very subtle), styled as text, not input
```

### Toggle Switch
```
Duration:   200ms ease-in-out
Track:      Background transitions grey → brand color
Thumb:      Translates from left to right (transform: translateX)
Optional:   Thumb scales 1.1× mid-transition (feels great on quality apps)
Checked:    Brand color track, thumb at right position
Disabled:   40% opacity, no transition on click
```

### Like / Favorite / Reaction
```
Heart/Star fill:  Scale 1.0 → 1.5 → 1.0, color fills (ease-out → ease-in)
Particle burst:   Optional — hearts/stars fly out radially (adds delight)
Duration:         400–600ms for full sequence
Counter:          Increments with brief scale animation
```

---

## 7.7 PAGE & SCREEN TRANSITIONS

```
SAME-LEVEL NAVIGATION:
  → Fade 0→100% opacity (200–300ms) — safest, always contextually correct
  → OR: Crossfade + slight scale (new page 0.98→1.0)

DRILL-DOWN (list → detail):
  → Slide left entering, slide right going back (matches mental model of depth)
  → BEST: Shared element transition (clicked card expands to fill page)

TAB SWITCHING:
  → Fade only — no directional movement (tabs are parallel, not hierarchical)

MODAL OPEN:
  → Scale from trigger point (transform-origin: source button) + fade 0→1
  → OR: Scale from center (0.9→1.0 + fade, 200ms ease-out)

MODAL CLOSE:
  → Reverse entrance (scale 1.0→0.9 + fade 1→0, 150ms ease-in, faster than open)

BOTTOM SHEET (mobile):
  → Slide up from below viewport (translateY: 100% → 0, 300ms ease-out spring)
  → Dismiss: Slide down (200ms ease-in, faster than open)

VIEW TRANSITIONS API (modern web, 2024+):
  → @view-transition { navigation: auto; }
  → document.startViewTransition(() => { /* DOM change */ })
  → Enables smooth shared-element transitions natively in browser
  → Progressive enhancement: falls back gracefully if unsupported
```

---

## 7.8 SKELETON LOADING

```
USE SKELETON WHEN:
  → Content layout is predictable (you know what's loading)
  → Loading takes 300ms–3s
  → Content-heavy layouts: feeds, card grids, profile pages, article lists

USE SPINNER WHEN:
  → Short operations < 1.5s
  → Loading area is too small for skeleton
  → Action-initiated loading (button press → result)

USE PROGRESS BAR WHEN:
  → Duration is predictable or measurable
  → Multi-step processes with known total

SKELETON DESIGN RULES:
  Shape: Match actual content shape EXACTLY (not generic rectangles)
  Color: Light: #e5e7eb shimmer to #f3f4f6 | Dark: #374151 shimmer to #4b5563
  Shimmer: Left-to-right direction (matches reading direction)
  Duration: 1.2–1.5s loop per shimmer pass
  Transition: Content fades in at 0→100% opacity (150ms) — never simultaneous with skeleton
  
NEVER: Full-page spinner on a page that could load progressively
ALWAYS: Load what you have, show skeleton for what's loading
```

---

## 7.9 STAGGER ANIMATIONS

When multiple items appear, stagger their entrance:

```
Fast list (8+ items):     20–30ms between items
Medium list (4–7 items):  40–60ms between items
Featured (2–3 items):     80–100ms between items

ENTRANCE ANIMATION (per item):
  translate: from (0, 16px) → (0, 0)
  opacity: 0 → 1
  duration per item: 200–300ms, ease-out

HARD RULE: Cap total stagger at 500ms.
  20 items × 50ms = 1000ms wait for last item = frustrating, not delightful.
  If >10 items: reduce delay to 20ms, or only stagger the first 8.
```

---

## 7.10 DRAG & DROP UX

```
AFFORDANCES (how user knows it's draggable):
  Explicit: Drag handle icon (6-dot grip ⠿) — best for lists, most discoverable
  Implicit: cursor:grab on hover — best for large draggable areas
  Hint on first use: "Drag to reorder" tooltip or instruction

DURING DRAG:
  Dragged item:   box-shadow increases, scale 1.03–1.05, opacity 0.8–0.9
  Drop zone:      Highlighted (dashed border, colored background)
  Other items:    Animate smoothly out of the way (spring physics)
  Ghost:          Dragged element at cursor position

ON DROP:
  Item settles with spring animation
  Shadow and opacity return to normal
  Auto-save new order immediately (optimistic update)

CANCEL / ESCAPE:
  Escape key → item returns to original position (animated)
  Drop outside valid zone → return animation to source
  
KEYBOARD EQUIVALENT:
  Always provide a keyboard method (select + arrow keys, or context menu "Move up/down")
  Drag is a progressive enhancement, not the only path
```

---

## 7.11 HAPTIC FEEDBACK (MOBILE)

On mobile, haptics pair with visual feedback to create physical sensation:

```
iOS HAPTIC PATTERNS:
  selection:   Light tap — for selection changes, picker scroll, toggle
  light:       Soft impact — confirming non-critical actions
  medium:      Standard impact — confirming important actions, success
  heavy:       Strong impact — critical errors, blocked actions
  success:     Two-tap pattern — task successfully completed
  warning:     Nudge — caution, needs attention
  error:       Three-tap descending — failure, blocked, destructive prevented

RULES:
  NEVER: Haptics without paired visual feedback
  NEVER: Haptics on scroll or hover (excessive, disruptive)
  NEVER: More than one haptic per user action
  ALWAYS: Respect UIAccessibility.isReduceHapticFeedbackEnabled
  ALWAYS: Use success haptic on task completion — small moments of satisfaction
```

---

## 7.12 ANIMATION ACCESSIBILITY

Motion can cause real physical discomfort for users with vestibular disorders.

```
CSS MEDIA QUERY (ALWAYS implement):
  @media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
      animation-duration:        0.01ms !important;
      animation-iteration-count: 1      !important;
      transition-duration:       0.01ms !important;
      scroll-behavior:           auto   !important;
    }
  }

WHAT TO DISABLE with reduced motion:
  ✓ Parallax scrolling (causes motion sickness)
  ✓ Auto-playing videos and carousels
  ✓ Large-scale animations (full-screen, page-level)
  ✓ Zoom/scale effects covering large areas
  ✓ Bounce and spring physics effects
  ✓ Continuous looping animations

WHAT CAN REMAIN (safe, no spatial movement):
  ✓ Opacity fades (no position change)
  ✓ Color transitions
  ✓ Very small movements (<10px displacement)
  ✓ Loading indicators (essential feedback — keep them)
  ✓ Focus indicators
```

---

## 7.13 SCROLL ANIMATIONS (USE WITH RESTRAINT)

```
GOOD USES (subtle, purposeful):
  Landing page section reveals (opacity + translateY of 20–30px)
  Progress bars filling on scroll into view
  Number counters starting when element enters viewport
  Subtle parallax background (not content — content parallax causes nausea)

BAD USES (avoid entirely):
  Content hidden until scrolled to → punishes fast scroll users
  Heavy parallax on text/content → universal nausea risk
  Animations that BLOCK the user from reading/interacting
  Animations triggered at exact scroll positions easy to miss

PERFORMANCE RULE:
  Only animate: opacity, transform (translate, scale, rotate)
  NEVER animate: width, height, top, left, margin, padding, border-width
  Use IntersectionObserver (not scroll event listeners — much more efficient)
  Use will-change: transform sparingly for complex animations only
```

---

# SECTION 8: ACCESSIBILITY (WCAG 2.2 COMPLETE)

---

## 8.1 THE POUR PRINCIPLES

Accessibility is not a feature. It is a quality standard.

```
PERCEIVABLE:    Information is presentable to all senses
                Alt text, captions, sufficient contrast, no color-only meaning

OPERABLE:       All functions work via keyboard, no inaccessible traps
                Keyboard navigation, focus management, no time limits without override

UNDERSTANDABLE: Language is clear, errors identified, UI is predictable
                Plain language, labeled forms, consistent navigation, clear errors

ROBUST:         Works with current AND future assistive technology
                Semantic HTML, valid code, ARIA only where needed
```

---

## 8.2 COMPLETE WCAG 2.2 CHECKLIST

### VISUAL
```
✓ Normal text: 4.5:1 contrast minimum (≥7:1 for AAA)
✓ Large text (18px+ regular, 14px+ bold): 3:1 minimum
✓ UI components (borders, icons, focus indicators): 3:1 minimum
✓ Focus indicators: 3:1 contrast + minimum 2px thick (NEW in 2.2)
✓ Color is NEVER the only way to convey information (always add label/icon)
✓ Images have descriptive alt text (decorative: alt="")
✓ Logos and brand icons: alt text is brand name
✓ Complex images (charts): described in adjacent text or long description
✓ Text over images: sufficient contrast in ALL quadrants of overlap
```

### MOTOR / KEYBOARD
```
✓ ALL functions operable via keyboard (Tab, Shift+Tab, Enter, Space, Arrow, Escape)
✓ Visible focus indicator on ALL interactive elements (no outline:none without replacement)
✓ Focus order is logical (matches visual reading order)
✓ No keyboard traps (always a way out)
✓ Skip navigation link to main content (first focusable element)
✓ Touch targets ≥ 44×44px (iOS), 48×48dp (Android), 24×24px minimum for web (WCAG 2.2)
✓ Minimum spacing between touch targets to prevent mis-taps
✓ No drag-only interactions — always a keyboard or click alternative (NEW in 2.2)
✓ Pointer gestures (swipe, pinch) all have simple single-pointer alternatives
✓ No pointer-cancellation unless necessary (allow mouseup/touchend cancellation)
```

### COGNITIVE
```
✓ Consistent navigation across all pages (same order, same location)
✓ Consistent component behavior (button behaves as button everywhere)
✓ Error messages describe what went wrong AND how to fix it
✓ Input labels always visible (not just placeholder text)
✓ Complex processes have step indicators / progress markers
✓ No auto-playing media without user consent
✓ No flashing content (>3 flashes/second can trigger seizures)
✓ Plain language (explain acronyms on first use)
✓ Don't remove or hide help UI — consistent help available (NEW in 2.2)
✓ Accessible authentication: don't require cognitive tasks that exclude users (NEW in 2.2)
✓ Complex tasks can be abandoned and resumed with data retained (NEW in 2.2)
```

### SCREEN READERS
```
✓ Proper heading hierarchy: h1 → h2 → h3 (NEVER skip levels)
✓ ARIA labels on icon-only buttons: aria-label="Close dialog"
✓ Form inputs associated with labels: htmlFor / aria-labelledby
✓ Required fields: aria-required="true"
✓ Error messages linked to inputs: aria-describedby="error-id"
✓ Live regions for dynamic updates: aria-live="polite" (non-urgent) / "assertive" (urgent)
✓ Modal dialogs trap focus and have aria-modal="true"
✓ Tables: proper <thead>, <th scope="col/row">, caption if needed
✓ Images with text: text in alt attribute (don't rely on CSS background)
✓ SVG icons: role="img" aria-label="..." OR aria-hidden="true" if decorative
✓ Loading states: aria-busy="true" on the container being updated
✓ Expandable sections: aria-expanded="true/false"
✓ Selected items: aria-selected="true"
✓ Alert messages: role="alert" for immediate announcements
```

---

## 8.3 ARIA PATTERNS (COMMON IMPLEMENTATIONS)

```
DIALOG / MODAL:
  <div role="dialog" aria-modal="true" aria-labelledby="dialog-title">
    <h2 id="dialog-title">Confirm Deletion</h2>
    ...
  </div>
  → On open: Move focus to first interactive element or dialog heading
  → Trap focus within modal while open
  → On close: Return focus to trigger element

COMBOBOX / AUTOCOMPLETE:
  <input role="combobox" aria-expanded="true" aria-controls="listbox-id"
         aria-autocomplete="list" aria-activedescendant="option-3">
  <ul role="listbox" id="listbox-id">
    <li role="option" id="option-1">Option One</li>
  </ul>

TABS:
  <div role="tablist">
    <button role="tab" aria-selected="true" aria-controls="panel-1">Tab 1</button>
    <button role="tab" aria-selected="false" aria-controls="panel-2">Tab 2</button>
  </div>
  <div role="tabpanel" id="panel-1">...</div>
  → Arrow keys navigate between tabs (not Tab key)

LIVE REGIONS:
  aria-live="polite"    → Announces after current speech finishes (form saves, search results)
  aria-live="assertive" → Interrupts immediately (errors, urgent alerts)
  aria-atomic="true"    → Announces entire region, not just changed parts

STATUS MESSAGES:
  <div role="status">Saved successfully</div>    → polite announcement
  <div role="alert">Payment failed</div>         → assertive announcement

PROGRESS:
  <div role="progressbar" aria-valuenow="65" aria-valuemin="0" aria-valuemax="100"
       aria-label="Upload progress">65%</div>
```

---

## 8.4 KEYBOARD NAVIGATION DESIGN

```
STANDARD KEY BEHAVIORS (ALWAYS respect these conventions):
  Tab:           Move forward through interactive elements
  Shift+Tab:     Move backward through interactive elements
  Enter:         Activate button, follow link, submit form
  Space:         Toggle checkbox, activate button, scroll page
  Arrow keys:    Navigate within a component (tabs, lists, sliders, menus)
  Escape:        Close modal/dialog/dropdown, cancel action
  Home/End:      First/last item in a list

FOCUS ORDER:
  Must match visual reading order (top-to-bottom, left-to-right for LTR)
  Logical for the task flow (form fields in the order you'd fill them)
  Never random or confusing

FOCUS MANAGEMENT:
  Opening modal → move focus INTO modal (first element or heading)
  Closing modal → return focus TO the element that opened it
  Dynamic content appearing → move focus to new content if it's a task result
  Page navigation (SPA) → move focus to new page heading (h1)
  Inline errors appearing → announce via aria-live, consider moving focus

VISIBLE FOCUS INDICATOR REQUIREMENTS (WCAG 2.2):
  Must be: At least 3:1 contrast against adjacent colors
  Must be: At least 2px thick (outline or equivalent)
  Must be: Visible around the entire focused element
  
SKIP LINKS:
  First focusable element on page
  Hidden by default, visible on focus
  Text: "Skip to main content"
  Target: <main id="main-content">
```

---

## 8.5 INCLUSIVE DESIGN (NEURODIVERGENT USERS)

Designing for neurodivergent users (ADHD, dyslexia, autism spectrum) benefits everyone:

```
FOR ADHD:
  ✓ Clear visual hierarchy — obvious where to look and what to do next
  ✓ Progress indicators — show how much is left, what's completed
  ✓ Autosave everywhere — prevents catastrophic loss from distraction
  ✓ Reduce visual noise — declutter, remove non-essential information
  ✓ Clear feedback for every action — nothing "invisible"
  ✓ Minimize distracting animations — they pull focus involuntarily

FOR DYSLEXIA:
  ✓ Sans-serif fonts (easier to decode letter forms)
  ✓ Generous line height (1.5–1.7× for body text)
  ✓ Left-aligned text (NEVER justified — creates variable river gaps)
  ✓ Adequate spacing between paragraphs (paragraph-gap ≥ 1.5× line height)
  ✓ Short line length (60–70ch maximum)
  ✓ Icons alongside text labels (dual-coding reduces decoding load)
  ✓ Option for increased spacing (support text-spacing user override)

FOR AUTISM SPECTRUM:
  ✓ Predictable layouts — same elements in same positions
  ✓ Literal language — no idioms, metaphors, or ambiguous CTAs
  ✓ Explicit instructions — never assume user will infer
  ✓ Consistent behavior — never surprise the user
  ✓ Clear state transitions — always show what changed and why
  ✓ Reduce sensory overload — avoid aggressive animations, sounds, notifications

UNIVERSAL BENEFITS:
  These practices improve ALL users' experiences under stress, distraction,
  or cognitive load — which describes most mobile usage contexts.
```

---

# SECTION 9: INFORMATION ARCHITECTURE

---

## 9.1 NAVIGATION PATTERNS: DECISION GUIDE

```
TOP NAVIGATION BAR:
  Use when: Web apps, 4–7 primary sections, desktop-first, flat hierarchy
  Pros: Always visible, familiar, efficient for frequent switching
  Cons: Limited space, doesn't scale to deep hierarchies
  Best for: Marketing sites, simple SaaS, content sites

SIDEBAR NAVIGATION:
  Use when: Admin panels, dashboards, complex apps, deep hierarchy needed
  Pros: More room for items, sub-navigation visible, collapsible
  Cons: Takes screen width, less familiar on consumer apps
  Width: 240–280px expanded, 56–64px icon-only collapsed

BOTTOM TAB BAR (mobile):
  Use when: Mobile apps, 3–5 primary sections
  Pros: Thumb-accessible, always visible, platform convention
  Cons: Limited to 5 items, takes vertical space
  Rule: 3 items minimum, 5 maximum. All tabs always visible.

HAMBURGER MENU:
  Use when: Secondary/overflow navigation, NEVER primary on desktop
  Mobile: Acceptable for marketing sites, NOT for primary app nav
  Inside: User profile at top, nav items, secondary links at bottom

BREADCRUMBS:
  Use when: Deep hierarchies (3+ levels), e-commerce, file systems, admin
  Format: Home > Category > Subcategory > Current Page
  Always make every breadcrumb link clickable except current page

MEGA MENU:
  Use when: Large content sites with many categories (e-commerce, media)
  Trigger on hover (desktop) + click option (accessible)
  Show on hover with 200ms delay (prevents accidental triggers)

TABS (within page):
  Use when: Parallel content at same hierarchy level, ≤7 items
  NOT for: Global navigation between different sections
  Keyboard: Arrow keys navigate between tabs (not Tab key)

COMMAND PALETTE:
  Use when: Power-user apps, frequent context switching, many possible actions
  Trigger: Cmd/Ctrl+K (universal convention — do not deviate)
  Contains: Recent items, all navigable screens, all actions
  Fuzzy search: Always included
```

---

## 9.2 THE 3-CLICK RULE (CONTEXTUAL)

Users should reach any key content in ≤3 navigation steps — but this is a guideline, not a law.

More important than click count: **every step must have clear progress and orientation**:
- Where am I right now?
- Where can I go from here?
- How do I go back?

If every step is fast and obvious, 4 clicks beats 3 confusing clicks.

---

# SECTION 10: PLATFORM DEEP-DIVES

---

## ══════════════════════════════════════════
## 10A: MOBILE APP UI/UX (iOS · Android)
## ══════════════════════════════════════════

### 10A.1 THE MOBILE CONTEXT

Mobile is not "desktop with smaller screens." It is a fundamentally different context:
- Used one-handed, on-the-go, frequently interrupted and distracted
- Network is unreliable — always design for slow or missing connection
- Battery is limited — avoid heavy animations, background processing, excessive polling
- Screen is an extension of the body — feedback must feel physical (touch, haptics, sound)
- Sessions are short — users complete fragments, then return

---

### 10A.2 THE THUMB ZONE (ONE-HANDED USE)

For a standard phone (~390px wide), held one-handed in right hand:

```
┌─────────────────┐
│  ╔═══════════╗  │  ← HARD REACH  (danger zone for primary actions)
│  ║           ║  │     Top of screen — awkward reach
│  ╠═══════════╣  │
│  ║  NATURAL  ║  │  ← COMFORTABLE REACH (sweet spot)
│  ║   REACH   ║  │     Center to bottom-center — primary action zone
│  ╠═══════════╣  │
│  ║           ║  │  ← EASY REACH
│  ║           ║  │     Bottom third — effortless access
│  [TAB BAR]  ││  │  ← PERFECT for primary navigation
└─────────────────┘
```

**Rules:**
- Primary CTAs, tab navigation, confirmation buttons → BOTTOM of screen
- Destructive actions → TOP (hard to reach = harder to accidentally tap)
- Search → TOP (acceptable — users typically use two hands for search, or one can reach if needed)
- Never place "Delete" adjacent to "Confirm" — physically separate them

---

### 10A.3 iOS vs ANDROID PLATFORM CONVENTIONS

You MUST respect platform conventions. Breaking them breaks trust instantly.

#### iOS Human Interface Guidelines
```
Navigation:    Large Title at top (scrolling collapses to small inline title)
Back gesture:  Swipe from left edge — NEVER disable this gesture
Tab bar:       Bottom, 3–5 items, filled icon + label for active state
Modals:        Slide up from bottom (sheet pattern, not centered dialogs)
Destructive:   Red text in action sheets, always requires confirmation
Icons:         SF Symbols (system-native recognition, adapt to Dynamic Type)
Typography:    San Francisco (SF Pro Text + SF Pro Display)
Haptics:       Selection, success, warning, error patterns
Status bar:    Design around Dynamic Island / notch (respect safe areas)
Safe areas:    Always respect: top (status bar/notch), bottom (home indicator)
               CSS: padding-top: env(safe-area-inset-top)
               CSS: padding-bottom: env(safe-area-inset-bottom)
```

#### Android Material Design 3
```
Navigation:    Navigation bar (bottom, 3–5 items) OR Navigation drawer
Back gesture:  System gesture from left/right edge — never override
FAB:           Floating Action Button for primary action — bottom right
Sheets:        Bottom sheets for contextual options and content
Typography:    Roboto or Google Sans (or brand font + Material type scale)
Colors:        Material You dynamic color system — respect user theming
Motion:        Shared element transitions, container transforms
Edge-to-edge:  Draw behind status bar and navigation bar (EdgeToEdge)
Ripple:        ALL tappable elements MUST show ripple touch feedback
Snackbar:      Bottom of screen, brief, with optional single action
```

---

### 10A.4 MOBILE NAVIGATION PATTERNS

#### Bottom Tab Bar (Most Common, Best UX)
```
Items: 3 minimum, 5 maximum (all always visible — never hide/show tabs)
Active: Filled icon + label + brand color
Inactive: Outlined icon + label + muted color
Badge: Number for unread count ("99+" for large numbers)
Mid-tab special action: Slightly larger icon for compose/create (common pattern)
Height: 49pt (iOS), 56dp (Android) + safe area bottom inset
```

#### Drill-Down Navigation (List → Detail)
```
Back button: Always present when navigated from root
Title: Current screen name (NOT app name after root level)
Right side: Maximum 2 icon actions + "..." overflow for more
Swipe back: Always active (don't override — it's a platform expectation)
```

#### Hamburger/Drawer (Use Sparingly)
```
Only for: Secondary navigation, not primary app destinations
Content: User profile/avatar at top, nav items, settings at bottom
NEVER: Put your most important destinations only inside a drawer
```

---

### 10A.5 MOBILE TYPOGRAPHY

```
iOS Base (Dynamic Type compatible):
  Body:       17pt  (system default)
  Secondary:  15pt
  Caption:    13pt
  All text MUST support Dynamic Type (up to 310% scale — test this!)

Android (sp units only):
  Body:       16sp  (sp = scale-independent pixels)
  Secondary:  14sp
  Caption:    12sp
  All text MUST use sp units — NEVER px for text on Android

MINIMUM readable:    12pt/sp (prefer 14pt+ for anything important)
Touch target rows:   Label can be small, but entire ROW must be ≥44pt/48dp
```

---

### 10A.6 MOBILE FORMS: THE MOST PAINFUL MOBILE UX

Forms are where mobile apps lose users. Minimize ruthlessly.

```
RULE 1: Ask for minimum. Every removed field improves completion rate.
RULE 2: Use correct keyboard type for each field:
  Email:    inputmode="email" or type="email"
  Phone:    type="tel"
  Numbers:  inputmode="numeric" (or type="number" for quantity inputs)
  URL:      type="url"
  Search:   type="search" (shows search/go key)
  Currency: inputmode="decimal"

RULE 3: Enable autofill:
  autocomplete="email", "name", "tel", "address-line1", "postal-code",
  "cc-number", "cc-expiry", "cc-csc", "current-password", "new-password"
  Support Face ID / Touch ID / Passkeys for auth flows

RULE 4: Keyboard behavior:
  When keyboard appears → focused input must scroll INTO VIEW (never behind keyboard)
  returnKeyType="next" for all fields except last
  returnKeyType="done"/"go" for last field
  
RULE 5: Validation:
  ON BLUR — validate completeness and format (when user leaves field)
  ON CHANGE — password strength only (real-time is helpful here)
  ON SUBMIT — full validation, show all errors simultaneously
  NEVER — validate email format while user is still typing (premature error)

RULE 6: Date/Time pickers:
  Use NATIVE pickers by default (best familiarity and accessibility)
  Custom ONLY if the native picker genuinely fails the use case
```

---

### 10A.7 MOBILE GESTURES

```
TAP:           Primary action — activate, select, navigate
DOUBLE TAP:    Like/zoom (only where this is an established convention)
LONG PRESS:    Context menu, alternative actions, selection mode
SWIPE LEFT:    Destructive action (delete) — use red background
SWIPE RIGHT:   Positive action (archive, favorite) — use brand color or green
SWIPE DOWN:    Dismiss modal sheets, pull-to-refresh
SWIPE UP:      Expand/show bottom sheets
PINCH:         Zoom in/out (maps, images, documents)
DRAG:          Reorder items, seek in media
TWO-FINGER TAP: Undo (iOS convention for text input)

CRITICAL RULE:
  Never use a gesture as the ONLY way to access a feature.
  Gestures must be supplemented by visible affordances.
  Swipe-to-delete → also accessible via long-press context menu.
```

---

### 10A.8 MOBILE PATTERNS

#### The Card (Dominant Mobile Content Unit)
```
Tap affordance:    Entire card tappable OR explicit visible button — never ambiguous
Aspect ratio:      Image aspect ratio locked (16:9, 4:3) — no reflow
Hierarchy:         Clear primary info (title), secondary info (subtitle, metadata)
Loading:           Skeleton placeholder for image area
Min height:        Auto — don't force fixed height unless content is uniform
```

#### Pull-to-Refresh
```
Threshold: Rubber-band physics below threshold, spinner appears AT threshold
Release:   Spinner retracts to top bar, content updates with fade-in
Never:     Full-page reload flash (jarring and breaks orientation)
```

#### Bottom Sheet
```
Drag handle: 32–40px wide pill, 4px tall, 40% opacity, centered at top
Snap points: Closed, half-height, full-height (3 optional snap positions)
Scroll: Content scrolls WITHIN the sheet when at full-height
Dismiss: Tap background, swipe down, or Escape key
Background: Dimmed with backdrop 40% black opacity
```

#### Swipe Actions on List Items
```
Left swipe: Destructive (red background, trash icon + "Delete")
Right swipe: Positive (brand/green, archive icon + "Archive")
Reveal hint: First-time use animation showing the action exists
Full swipe: Optional — full swipe = immediate action (with haptic, not just reveal)
```

#### Toast / Snackbar (Mobile)
```
Position:   Bottom of screen, ABOVE tab bar (16px gap)
Duration:   3s for info, 5s for action, persistent for errors
Content:    Max 1 line + optional 1 action button ("Undo", "View")
Stack rule: NEVER stack — queue multiple toasts, show sequentially
```

---

### 10A.9 MOBILE PERFORMANCE UX

```
App launch:            < 1 second to first meaningful paint
Screen transitions:    300ms standard, 200ms for small transitions
List scrolling:        Must maintain 60fps (jank destroys trust immediately)
Image loading:         Progressive loading + blur-up OR skeleton placeholder
Offline state:         NEVER blank screen — show cached content + "Last updated X ago"
Pull to refresh:       Spinner appears at pull threshold immediately
Large lists:           Virtualize (only render visible rows + buffer)
```

---

## ══════════════════════════════════════════
## 10B: WEBSITES & LANDING PAGES
## ══════════════════════════════════════════

### 10B.1 THE LANDING PAGE FORMULA

A landing page has exactly ONE job: convert visitor to next step (sign up, purchase, contact).
Every element either supports this goal or is noise.

**Above-the-Fold Structure:**
```
┌──────────────────────────────────────────────────────────┐
│  [LOGO]                      [Nav items]  [CTA Button]   │
├──────────────────────────────────────────────────────────┤
│                                                          │
│   HEADLINE: One clear outcome-focused statement.         │
│   What does the user ACHIEVE? (Not what your product IS) │
│   "Close 3× More Deals in Half the Time"                │
│                                                          │
│   SUBHEADLINE: Supporting context, brief. Who it's for   │
│   or how it works in one sentence.                       │
│                                                          │
│   [PRIMARY CTA — "Start Free Trial"]                    │
│   [Secondary — "Watch Demo (2 min)"]                    │
│                                                          │
│   Social proof: "Trusted by 12,000+ sales teams"        │
│   [Customer logo wall — recognizable brands]             │
│                                            [HERO IMAGE] │
└──────────────────────────────────────────────────────────┘
```

**Headline Rules:**
- Outcome-focused: "Close 3× More Deals" NOT "The Best CRM Platform"
- Specific beats vague: "Save 5 hours/week on reporting" NOT "Save time"
- One idea: If you need a comma, split into two separate statements

---

### 10B.2 THE TRUST HIERARCHY (Scroll Order)

Place trust signals in this order as user scrolls — each layer earns the next:

```
1. SOCIAL PROOF COUNT (above fold)    "12,000+ teams trust [product]"
2. LOGO WALL (just below fold)        Recognizable customer logos
3. FEATURE PROOF (how it works)       Screenshots, video, interactive demo
4. TESTIMONIALS (real quotes)         Name + photo + company + role = credibility
5. CASE STUDIES (ROI stories)         Specific results, named customers
6. SECURITY/COMPLIANCE BADGES         Near the purchase decision point
7. RISK REVERSAL (near final CTA)     "Cancel anytime" "30-day money back"
```

---

### 10B.3 NAVIGATION DESIGN

```
DESKTOP:
  Primary items:     Max 5–7 (more = Hick's Law penalty)
  Right side:        1 ghost button (secondary) + 1 filled button (primary CTA)
  Sticky behavior:   Yes for most marketing sites (CTA always accessible)
  Transparency:      Transparent with blur → solid background on scroll
  Active state:      Underline or bold for current page/section

MOBILE:
  Hamburger:         Acceptable here for marketing sites (not primary app nav)
  Menu style:        Full-screen overlay preferred over slide-in drawer
  Include:           Duplicate the primary CTA in the mobile menu
  Dismiss:           × button top-right AND tapping overlay background
```

---

### 10B.4 CONVERSION OPTIMIZATION (CRO) PRINCIPLES

```
REDUCE COGNITIVE LOAD:
  One primary CTA per section — never two competing actions of equal weight
  Remove form fields ruthlessly — each field drops conversion ~10%
  Show pricing clearly — hiding price builds anxiety and loses trust

SOCIAL PROOF POSITIONING:
  Place testimonials NEAR the action they're meant to support
  Place logos NEAR the product section they validate
  Case study results near the relevant feature explanation

RISK REDUCTION:
  "No credit card required" immediately below free trial CTA
  "Cancel anytime" next to subscription CTA
  "SOC 2 certified" near enterprise plan CTA
  "100% money back guarantee" next to purchase button

FRICTION AUDIT:
  Every step between intent and conversion is friction
  Remove required fields → form completion increases
  Remove sign-up before demo → demo engagement increases
  Add progress indicator → multi-step form completion increases 20%+

A/B TEST PRIORITY (highest impact first):
  1. Headline text
  2. Primary CTA button copy
  3. CTA button position (above/below fold)
  4. Social proof type (count vs logos vs testimonials)
  5. Form field count
  6. CTA button color
  7. Page length
```

---

## ══════════════════════════════════════════
## 10C: WEB APPLICATION (SaaS) DESIGN
## ══════════════════════════════════════════

### 10C.1 SAAS INFORMATION ARCHITECTURE

```
APP SHELL (always visible):    Logo, global nav, notifications bell, user avatar
PAGE HEADER:                   Page title + primary action + breadcrumb (if nested)
CONTENT AREA:                  Main work area — tables, forms, editors, dashboards
CONTEXTUAL PANELS:             Side panels appearing on selection or action
MODALS:                        Critical confirmations and quick-create only
```

---

### 10C.2 ONBOARDING: THE MOST IMPORTANT UX IN SaaS

A user who fails to reach their "Aha! Moment" in the first session is likely gone forever.
The goal: Get from "sign up" to "value experienced" as fast as possible.

```
ONBOARDING FLOW STRUCTURE:

STEP 1 — EMPTY STATE WELCOME
  Friendly illustration (not stock photo, not scary blank screen)
  "What this is" in 1 sentence
  Single CTA: "Create your first project" (specific, not "Get started")

STEP 2 — FIRST ACTION (Quick Win)
  The simplest possible version of core value delivery
  Fill-in-the-blank or guided, not open-ended
  AVOID: 20-field setup wizard before any value is seen

STEP 3 — AHA MOMENT
  The moment they see VALUE from their input
  Celebrate: Confetti, success state, "You just [achieved X]"
  Immediately show NEXT step (don't leave them idle after celebration)

STEP 4 — PROGRESSIVE SETUP
  Profile photo, team invites, integrations → DEFER these to later
  Progress bar showing completion (optional vs. required clearly marked)
  Always dismissible — never trap users in setup flows

RULES:
  ✓ Skip option always available on every step
  ✓ Progress indicator "Step 2 of 5" sets expectations
  ✓ Email sequence supplements in-app onboarding (not replaces it)
  ✓ Tooltip-based product tours: trigger on first use, not login
  ✗ Never front-load setup before showing value
  ✗ Never make inviting teammates required before using the product
```

---

### 10C.3 SETTINGS ARCHITECTURE

```
UNIVERSAL SETTINGS ORGANIZATION:
  Account / Profile        Personal details, avatar, display name, password
  Workspace / General      Organization name, timezone, language, date format
  Notifications            Email, in-app, push preferences per notification type
  Members & Permissions    Team management, roles, invitation management
  Integrations             Third-party connections, webhooks, API
  Billing & Plans          Subscription, invoices, usage, upgrade/downgrade
  Security                 2FA, session management, API keys, audit log
  Danger Zone              Delete account, export data (bottom, visually separated)

RULES:
  NEVER put settings in a modal — give them a dedicated page or full-panel
  ALWAYS provide back navigation from settings
  ALWAYS show current value as pre-filled default in all settings inputs
  ALWAYS confirm destructive settings changes (email change, password change)
  Danger Zone: Red border, separate section, explicit confirmation required
```

---

### 10C.4 NOTIFICATION DESIGN

```
IN-APP NOTIFICATION BELL:
  Badge: Red dot for unread, number badge when count > 0 ("99+" for large counts)
  Panel: Max 10 recent, "View all notifications" link at bottom
  Each item: Icon/avatar + description + relative timestamp + link
  Mark as read: Individual + "Mark all read" option
  Group similar: "John and 3 others commented on Project X"

TOAST NOTIFICATIONS:
  Position:   Top-right (desktop), bottom-center (mobile)
  Durations:  3s (success/info), 5s (with action), persistent until dismissed (error)
  Stack:      Max 3 visible; queue the rest
  Error toast: NEVER auto-dismiss — let user read and dismiss manually

INLINE BANNERS (page-level alerts):
  Position:   Below main header, above page content
  Types:      Trial expiring, feature announcement, required action
  Max:        1 banner at a time (stack causes visual chaos)
  Always:     Dismissible (unless it's a required action)
```

---

## ══════════════════════════════════════════
## 10D: DESKTOP APPLICATION DESIGN
## ══════════════════════════════════════════

### 10D.1 DESKTOP CONTEXT

Desktop apps serve power users who demand efficiency. The rules are fundamentally different:
- Keyboard shortcuts are EXPECTED and DEMANDED (not optional)
- Menu bar, right-click context menus are platform conventions
- Drag-and-drop for files and interface elements
- Window resizing must be graceful from minimum to maximum
- Multiple panels visible simultaneously (sidebar + main + inspector)

---

### 10D.2 DESKTOP LAYOUT ARCHETYPES

**Three-Panel (VSCode, Figma, Xcode, most creative tools):**
```
┌──────┬────────────────────────────────┬──────────┐
│      │                                │          │
│ NAV  │   MAIN WORKSPACE               │ INSPECTOR│
│ TREE │   (editor, canvas, content)    │ / PROPS  │
│      │   ← Receives most screen space │          │
└──────┴────────────────────────────────┴──────────┘
```

**Document + Toolbar (Office apps, Photoshop, Keynote):**
```
┌──────────────────────────────────────────────────┐
│ MENU BAR: File  Edit  View  Insert  Format  Help  │
├──────────────────────────────────────────────────┤
│ TOOLBAR:  [B][I][U]...[alignment]...[quick tools] │
├───────────────────────────────────┬──────────────┤
│                                   │              │
│         DOCUMENT / CANVAS         │  PROPERTIES  │
│                                   │  PANEL       │
└───────────────────────────────────┴──────────────┘
│ STATUS BAR: Zoom 100% | Page 3/12 | Word count   │
└──────────────────────────────────────────────────┘
```

**Dashboard Hub (Slack, Discord, Teams):**
```
┌───┬────────────────────┬────────────────────────┐
│   │                    │                        │
│ACT│  CHANNEL / ITEM    │  MESSAGE / CONTENT     │
│ION│  LIST SIDEBAR      │  MAIN AREA             │
│BAR│                    │                        │
└───┴────────────────────┴────────────────────────┘
```

---

### 10D.3 KEYBOARD-FIRST DESIGN

```
UNIVERSAL SHORTCUTS (NEVER override, always document):
  Cmd/Ctrl + N:          New (file, item, document, record)
  Cmd/Ctrl + O:          Open
  Cmd/Ctrl + S:          Save
  Cmd/Ctrl + Shift + S:  Save As
  Cmd/Ctrl + Z:          Undo
  Cmd/Ctrl + Y / Shift+Z: Redo
  Cmd/Ctrl + C/X/V:      Copy / Cut / Paste
  Cmd/Ctrl + A:          Select All
  Cmd/Ctrl + F:          Find / Search
  Cmd/Ctrl + K:          Command Palette (newer convention, widely expected)
  Cmd/Ctrl + W:          Close tab/window
  Cmd/Ctrl + Q:          Quit application
  Escape:                Cancel / Close / Dismiss (universal)
  Enter:                 Confirm / Submit
  F2 or Enter on item:   Rename / edit selected item
  Delete/Backspace:      Delete selected item (with confirmation for destructive)
  Arrow keys:            Navigate lists, move selected elements
  Space:                 Toggle/activate selected item, preview file

DISPLAY shortcuts:
  → In tooltips (hover over button → shows keyboard shortcut)
  → In menu bar (always show shortcut next to menu item)
  → In command palette (fuzzy search with shortcut visible)

COMMAND PALETTE (power-user essential):
  Trigger: Cmd/Ctrl + K (do not change this)
  Contents: All navigable screens, all executable actions, recent items
  Search: Fuzzy matching (typo-tolerant)
  Show: Last 5 recently used items by default
```

---

### 10D.4 CONTEXT MENUS

```
EVERY right-clickable / long-pressable element needs a context menu:
  Primary actions for that item (Open, Edit, Rename, Duplicate)
  Copy / Paste actions where applicable
  ─── separator ───
  Destructive action at BOTTOM (Move to Trash / Delete)

CONTEXT MENU RULES:
  Max 10 items before submenus needed
  Submenu: right-pointing chevron →
  Disabled items: visible but greyed (shows possibility, not just current ability)
  Never: Only way to do something is via context menu (also provide button)
  Keyboard: Right-click menu accessible via Shift+F10 or context menu key
```

---

### 10D.5 WINDOW MANAGEMENT

```
Minimum window size:  Define and enforce (nothing breaks below this size)
Flexible panels:      Resizable via drag handles (resize cursor on hover)
Collapsed panels:     Icon-only sidebar (56–64px) saves space, expands on click
Panel memory:         Save panel widths/positions between sessions (user preference)
Multi-window:         Independent windows — state not shared, but data synced
Tabs within window:   For document apps (multiple open files, like a browser)
Split view:           Two panels side-by-side (implement for power-user contexts)
```

---

## ══════════════════════════════════════════
## 10E: DASHBOARDS & DATA VISUALIZATION
## ══════════════════════════════════════════

### 10E.1 THE DASHBOARD PHILOSOPHY

A dashboard is not a collection of charts. It is an **answer to a specific question** someone has to ask every time they come to work.

**Before designing a single widget, answer:**
1. What ONE question does this dashboard answer?
2. Who is asking? (Executive, operator, analyst, engineer on-call?)
3. What DECISION does seeing this data enable? (If no decision follows — the widget doesn't belong)
4. How often is it viewed? (Daily → optimize for change detection | Rarely → optimize for orientation)

**The Three Dashboard Types:**
```
STRATEGIC:     Executive KPIs. Very few metrics. "Are we on track?"
               Daily/weekly view. No drill-down needed.

OPERATIONAL:   Real-time. Operational staff. "Is anything broken? What do I do?"
               Used constantly. Alerts, anomalies, status indicators.

ANALYTICAL:    Deep-dive. Analysts. "Why is this happening?"
               Used in investigation sessions. Heavy filtering, drill-down, exploration.

DESIGN DIFFERENTLY FOR EACH TYPE. They are not the same product.
```

---

### 10E.2 DASHBOARD INFORMATION HIERARCHY

```
ZONE 1 — STATUS OVERVIEW (Top row, full width):
  KPI scorecards, trend indicators, critical alerts
  → "Is everything OK? What's the headline number?"
  → User time: 3–5 seconds

ZONE 2 — PRIMARY CHARTS (Large, center):
  1–3 most important charts for the dashboard's core question
  → "What does the trend look like? What's changing?"
  → User time: 20–60 seconds

ZONE 3 — SUPPORTING DETAIL (Secondary, below/right):
  Breakdowns, comparisons, data tables, secondary metrics
  → "Why? What's driving it?"
  → User time: 2–10 minutes (only if Zones 1+2 raised questions)

ZONE 4 — FILTERS & CONTROLS (Top bar or sidebar):
  Date range, segment selectors, view toggles
  → Persistent, accessible, NOT visually dominant
```

---

### 10E.3 CHART DECISION MATRIX

Choosing the wrong chart type is worse than showing no chart.

```
WHAT TO SHOW               →  USE THIS CHART
──────────────────────────────────────────────────────────
Change over time            →  Line chart (continuous data)
(continuous data)           →  Area chart (volume/cumulative, stacked)
Change over time            →  Bar chart (discrete periods, few points)
(discrete periods)

Comparison (few categories) →  Bar chart (horizontal for long labels)
                            →  Grouped bar (side-by-side)
                            →  Bullet chart (actual vs. target)

Comparison (many cats.)     →  Horizontal bar, sorted descending
                            →  Table with inline sparkbar

Part-to-whole (≤5 parts)    →  Donut chart (center shows total)
                            →  Stacked bar (shows both total and parts)

Part-to-whole (>5 parts)    →  Treemap
                            →  Stacked bar with "other" bucket

Correlation / relationship  →  Scatter plot
                            →  Bubble chart (3 variables)
                            →  Heatmap (matrix correlation)

Distribution                →  Histogram
                            →  Box plot (comparing distributions)

Geospatial                  →  Choropleth (rates/densities by region)
                            →  Point map (event locations)
                            →  Proportional symbol (quantities by location)

Single KPI                  →  Big number scorecard
Progress toward goal        →  Progress bar (linear, readable)
                            →  Gauge (use sparingly — harder to read)
Trend context               →  Sparkline (in-row, compact trend)

──────────────────────────────────────────────────────────
NEVER USE in data dashboards:
  ✗ 3D charts (distorts data proportions)
  ✗ Pie charts with >5 segments (impossible to compare slices)
  ✗ Dual-axis line charts (they mislead — slopes not comparable)
  ✗ Decorative visualizations (art ≠ data communication)
  ✗ Waterfall charts for simple comparisons (overkill)
```

---

### 10E.4 CHART DESIGN RULES

**The Data-Ink Ratio (Tufte's Principle):**
Every pixel must serve the data. Remove anything that doesn't:
- Gridlines that aren't needed (use light guide lines only when they aid reading)
- Axis labels obvious from context
- Chartjunk: decorative elements, 3D effects, shadows on charts, gradient fills
- Legends when direct labels are clearer (label data series directly on chart)

**Chart Typography:**
```
Title:        16–20px bold — states the INSIGHT ("Q4 Revenue Up 23%", not "Revenue")
Axis labels:  12–13px, 60% opacity, don't rotate text unless absolutely unavoidable
Data labels:  11–14px, on chart only when ≤10 data points (not every bar in a 30-bar chart)
Tooltips:     14px, all relevant values, clearly labeled, formatters for numbers
Legend:       12px, ordered by visual prominence, placed at top or right
```

**Color in Charts:**
```
CATEGORICAL:  Each category = distinct color. Max 8–10 categorical colors.
              Always use color-blind-safe palette (blue+orange safe; red+green NOT safe)

SEQUENTIAL:   Light-to-dark single hue for ordered/quantitative data
              Example: light blue → dark blue for low → high population density

DIVERGING:    Two hues with neutral midpoint for +/- data
              Example: Red → White → Green for below/at/above target

HIGHLIGHT:    One color stands out, everything else neutral grey
              Use to call attention to ONE series or data point

THRESHOLD:    Green/amber/red for status (traffic light pattern)
              Only when there are clear performance thresholds defined
```

---

### 10E.5 KPI SCORECARDS

```
ANATOMY:
┌─────────────────────┐
│ METRIC LABEL        │  12–14px, muted color, uppercase or medium weight
│                     │
│ 1,284,320           │  28–48px, bold, primary color
│                     │
│ ↑ 12.4% vs last mo  │  12–14px, green/red semantic + icon + percentage
│                     │
│ [sparkline         ]│  Optional — 4-week trend at a glance
└─────────────────────┘

RULES:
  Show number first, label second (the number is the reason you're here)
  ALWAYS show comparison: vs. prior period OR vs. target OR vs. benchmark
  Delta indicator: arrows + color + percentage (use all three, not just one)
  Large numbers: "1.2M" not "1,284,320" — unless precision is the point
  Negatives: Red + downward arrow for bad, Red + upward arrow for good-but-unexpected
  Sparkline in card: High value addition — shows trajectory without click
```

---

### 10E.6 DATA TABLES (OFTEN THE BEST VISUALIZATION)

```
HEADERS:
  Short clear names (abbreviate with tooltip for long labels)
  Sticky header on scroll (critical for tables taller than viewport)
  Sort indicator on active column (↑ or ↓, grey arrow on hoverable columns)
  All numbers: right-aligned (decimal points line up)
  All text:    left-aligned

ROWS:
  Height: 40–48px compact / 48–56px comfortable
  Hover: Always visible highlight (even on touch for accessibility)
  Alternating row colors: Optional — very subtle (2–3% lightness diff)

NUMBERS IN TABLES:
  Use tabular figures (all digits same width for column alignment)
  Thousands separators: "1,284" not "1284"
  Consistent decimal places per column
  Units in HEADER, not repeated in each cell
  Conditional formatting: Subtle background colors, not just text color

PAGINATION vs INFINITE SCROLL:
  Pagination:     Data work, known total, need to find specific item
  Infinite scroll: Browsing, discovery, social content
  Virtual scroll: Large lists (10,000+ rows) — only render visible rows

SEARCH & FILTER:
  Global search above table
  Column-level filter via header click → filter popover
  Active filters shown as dismissible chips above table
  Result count "Showing 47 of 1,284 results" updates in real time

BULK OPERATIONS:
  Checkbox column (first, fixed width)
  Select-all in header
  Floating action bar appears when rows selected (shows count + actions)
  Bar disappears on deselect — not a permanent toolbar
  Actions in bar: specific to selected item types
```

---

### 10E.7 REAL-TIME & LIVE DASHBOARDS

For monitoring, trading platforms, infrastructure dashboards:

```
UPDATE INDICATORS:
  Timestamp:      "Last updated: 3 seconds ago" — always visible, continuously updating
  Live badge:     Pulsing green dot for live data stream
  Stale state:    Amber/red when data hasn't updated within threshold time

CHANGING VALUES:
  Flash on change: 50ms yellow highlight → return to normal (not distracting, confirms change)
  Color flash: green = increase, red = decrease (with reduce-motion fallback)
  NEVER: Count-up number animation — just snap to new value
  For financial: Show change direction + magnitude + velocity simultaneously

ALERTS & ANOMALIES:
  Alert banner at top (dismissible after user acknowledgment)
  Anomalous point highlighted on chart (different color, tooltip explaining)
  Alert sound: opt-in ONLY — NEVER play sounds by default

PERFORMANCE:
  WebSocket for true real-time (not polling — polling wastes bandwidth, adds latency)
  Virtualize long lists — never render 10,000 rows to DOM
  Throttle re-renders — cap at 60fps visual updates
  Show connection status prominently (●Connected / ●Reconnecting / ●Offline)
```

---

## ══════════════════════════════════════════
## 10F: ADMIN PANELS & PORTALS
## ══════════════════════════════════════════

### 10F.1 ADMIN SIDEBAR NAVIGATION

```
Width:          240–280px expanded, 56–64px icon-only collapsed
Current page:   Left border accent (3–4px) + background fill (brand color tint)
Groups:         Section headers with uppercase labels or dividers
Sub-navigation: Expanding accordion OR fly-out panel on hover
User profile:   BOTTOM of sidebar (not competing with nav hierarchy)
Collapse:       Toggle button (saves space — power users use keyboard shortcuts)
```

### 10F.2 FORM-HEAVY ADMIN INTERFACES

```
Dense forms:     Two-column (label-left, input-right) on desktop ONLY
Long forms:      Full-width single column for complex/multi-field forms
Field grouping:  Visual sections with dividers or background groups
Inline editing:  Double-click table cells to edit in-place (power-user efficiency)
Auto-save:       Preferred for long forms — "Saving..." indicator, "Saved ✓" on complete
Explicit save:   "Save Changes" button required for critical config changes

FORM VALIDATION IN ADMIN:
  Admins are power users — less hand-holding needed
  But still: real-time validation for format constraints
  And: clear diff indicators ("This will affect 847 records")
```

### 10F.3 PERMISSION & ROLE STATES

```
Disabled (no permission):  50% opacity + cursor:not-allowed + tooltip explaining WHY
Role-restricted sections:  Lock icon + "Admin only" label + explain what role can access
Upgrade gates:             Clear upgrade CTA, not just a grey-out
Read-only mode:            Input becomes styled text (not disabled grey input)
                           Visual distinction: no border, different background
Dangerous permissions:     Two-step confirmation + explain impact
```

### 10F.4 BULK OPERATIONS (Admin-Critical)

```
Selection:    Checkbox per row, select-all in header, shift-click for range selection
Feedback:     "47 items selected" in floating bar
Actions:      Delete, Export, Assign, Change Status, Archive (context-appropriate)
Confirmation: For destructive bulk actions — show count and consequences
Progress:     Progress bar for bulk operations that take time
Error handling: "42 succeeded, 5 failed" with details on failures
```


## ══════════════════════════════════════════
## 10G: E-COMMERCE UI PATTERNS
## ══════════════════════════════════════════

### 10G.1 PRODUCT CARDS & LISTINGS

```
PRODUCT CARD ANATOMY:
  Image:        Locked aspect ratio (1:1 or 4:3). Hover: secondary image or zoom.
  Brand/vendor: Small, muted — above product name
  Product name: 2 lines max, truncate with ellipsis
  Price:        Bold, prominent. Sale price: original struck-through, new price red/prominent.
  Rating:       Star icons + count "★★★★☆ (284)"
  Key attribute: Color swatches OR size indicators inline
  CTA:          "Add to Cart" visible on hover (desktop), always visible on mobile

LISTING PAGE CONTROLS:
  Sort:         "Relevance | Price ↑↓ | Rating | New Arrivals"
  Filter:       Left sidebar (desktop) OR filter sheet (mobile)
  Active filters: Chips above results, individually dismissible + "Clear all"
  Count:        "Showing 24 of 184 products" updates in real time
  View toggle:  Grid (2–4 col) vs List view for scanning different attributes

PAGINATION vs INFINITE SCROLL:
  E-commerce: Prefer pagination (users return to a specific page number)
  "Load more" button: Middle ground — good for browsing contexts
  Infinite scroll: Only for social-style discovery feeds
```

### 10G.2 PRODUCT DETAIL PAGE

```
ABOVE THE FOLD:
  Images:      Gallery (min 3 images, zoom on hover, swipe on mobile)
               Video: Optional product video as first or second media
  Title:       H1, clear, descriptive
  Price:       Large, prominent, directly below title
  Rating:      Linked to reviews section below
  Variants:    Color/size/option selector (clearly shows out-of-stock)
  CTA area:    Quantity selector + "Add to Cart" (primary) + "Wishlist" (secondary)
  Trust:       "Free shipping over $50" / "In stock, ships today" / "Easy returns"

BELOW THE FOLD:
  Description:   Tabbed or accordion (Description, Specifications, Reviews)
  Reviews:       Star distribution chart + recent reviews + filter by rating
  Related items: "Customers also bought" or "Similar products"
  Recently viewed: Persistent personalized carousel

VARIANT SELECTION RULES:
  Out-of-stock variants: Visible but strikethrough or greyed (show existence, not availability)
  Selected state: Clear visual selection (filled, border, checkmark)
  Image update: Main image changes when color/variant selected
  Price update: Price updates immediately on variant change
```

### 10G.3 SHOPPING CART

```
MINI CART (dropdown/slide-out):
  Show: After "Add to Cart" action
  Duration: Stays open briefly (3s) or until dismissed
  Contents: Item count, thumbnail, name, price, quantity control, remove
  Footer: Subtotal + "View Cart" + "Checkout" CTAs

FULL CART PAGE:
  Editable: Quantity +/- inline, remove item, save for later
  Item line: Thumbnail + name + attributes (size/color) + unit price + quantity + line total
  Order summary: Subtotal, shipping estimate, tax (if calculable), order total
  Promo code: Expandable inline (not separate page)
  CTA: "Continue to Checkout" — high contrast, above and below on long carts
  Trust signals: Lock icon, payment logos, easy return policy near CTA

EMPTY CART:
  Friendly message + CTA to continue shopping + "Recently viewed" items below
```

### 10G.4 CHECKOUT FLOW

```
CHECKOUT PRINCIPLES:
  Step count: Maximum 3 pages (Contact → Shipping → Payment → Review)
  Guest checkout: ALWAYS available above-the-fold (not buried)
  Progress indicator: Steps with labels visible throughout
  Editable: Each section editable from review step without losing other data
  Security: "Secure checkout" with SSL badge visible throughout
  Error recovery: Never clear already-entered data on validation error

STEP 1 — CONTACT INFORMATION:
  Email first (enables abandoned cart recovery)
  "Sign in" option available but not required
  Password optional at this stage

STEP 2 — SHIPPING:
  Address autocomplete (Google Places or equivalent)
  Shipping method selection with price + delivery estimate
  Saved addresses for returning customers

STEP 3 — PAYMENT:
  Card number with real-time format masking (XXXX XXXX XXXX XXXX)
  Card type auto-detected (show Visa/Mastercard/Amex icon)
  Expiry: MM/YY format, auto-advance after month entry
  CVV: Tooltip showing where to find it (card front/back varies)
  Express checkout: Apple Pay / Google Pay / PayPal at top if available
  Billing address: "Same as shipping" checked by default

REVIEW & CONFIRMATION:
  Show all: Items, shipping address, payment method (last 4 digits), totals
  Final CTA: "Place Order — $XX.XX" (price on button removes surprises)
  Post-purchase: Order number, confirmation email sent, tracking info
```

---

## ══════════════════════════════════════════
## 10H: AUTH & ACCOUNT DESIGN
## ══════════════════════════════════════════

### 10H.1 LOGIN & REGISTRATION DESIGN

```
LOGIN PAGE BEST PRACTICES:
  Layout:   Centered card on light/brand background (or split-screen with marketing)
  Fields:   Email + Password only (no username — email IS the identifier)
  CTA:      "Sign In" (not "Login" or "Submit")
  Links:    "Forgot password?" below password field, right-aligned
  Alternative: Social auth buttons above OR below form (pick ONE layout, be consistent)
  Error:    "Incorrect email or password" (vague intentionally — security)
            Never tell which field is wrong (prevents email enumeration attacks)

REGISTRATION PAGE:
  Fields:   Email + Password + (optional) Name for first step
            DEFER: Phone, company, role, payment — later onboarding steps
  Password: Show/hide toggle (eye icon) — ALWAYS include this
            Strength indicator: real-time visual bar + specific requirements
  Terms:    Checkbox or "By continuing, you agree to..." — must be present
  CTA:      "Create Account" or "Get Started" (not "Register" or "Submit")
  Already have account: "Sign in" link — prominently visible

UNIFIED FLOW (RECOMMENDED):
  One email field with "Continue" button
  System detects: existing account → show password field
                  new account → show registration fields
  Benefits: Removes cognitive load of "which page am I on?"
```

### 10H.2 PASSWORD DESIGN

```
PASSWORD FIELD REQUIREMENTS:
  Always: Show/hide toggle (eye icon) — no exceptions
  Strength meter: Visual bar (4 levels: weak/fair/good/strong) + color coding
  Requirements list: Real-time checkmarks as user satisfies each requirement
    ✓ At least 8 characters
    ✓ One uppercase letter
    ✓ One number
    ✓ One special character
  Copy-paste: NEVER disable paste on password fields (breaks password managers)
  Autocomplete: "new-password" on create, "current-password" on sign in

PASSWORD RESET:
  Step 1: Email field + "Send Reset Link"
  Step 2: "Check your email" confirmation (don't confirm email existence)
  Step 3: New password page (link in email, 1-hour expiry)
  Success: Auto sign-in after reset + redirect to intended destination
  Link expiry: Clear message + resend option — not a generic error

PASSWORDLESS / PASSKEYS (2024+ standard):
  Magic link: Email with one-click sign-in (no password needed)
  Passkey: Device biometric (Face ID, Touch ID) — support where available
  TOTP codes: 6-digit time-based code as 2FA
  Push prompt: Notification to approved device for 2FA
```

### 10H.3 SOCIAL & SSO AUTH

```
BUTTON DESIGN:
  Official brand colors and logos only (Google: white bg, specific colors)
  "Continue with Google" / "Continue with Apple" / "Sign in with SSO"
  Button: full-width, icon + text, clearly distinct from each other
  Ordering: Most-used first (Google typically most common for B2B)
  Separator: "or" divider between social buttons and email form

APPLE SIGN-IN REQUIREMENTS (for iOS apps):
  MUST offer Apple Sign In if offering any other social sign-in
  Apple button: Black background (#000000), white text, Apple logo
  Hide email option: Support users who choose to hide email from your app
```

### 10H.4 MULTI-FACTOR AUTHENTICATION

```
TOTP (Authenticator App):
  Setup: QR code + manual code alternative (some users can't scan QR)
  Input: 6 digits, auto-advance when complete, auto-submit
  Error: "That code has expired. Wait for the next code." (not generic error)
  Recovery codes: Show ONCE after setup, force download/copy acknowledgment

SMS 2FA:
  Show partially masked number: "We sent a code to +1 •••• ••• 4218"
  Resend option: After 30-second cooldown (show countdown timer)
  Auto-read SMS: Implement WebOTP API (browsers auto-fill the code)

TRUSTED DEVICES:
  Offer "Don't ask again on this device for 30 days" after successful 2FA
  Show list of trusted devices in security settings with revoke option
```

---

# SECTION 11: SPECIALIZED UI PATTERNS

---

## ══════════════════════════════════════════
## 11A: AI & CONVERSATIONAL INTERFACES
## ══════════════════════════════════════════

This is the most rapidly evolving UI category. These patterns reflect current best practices as of 2025.

### 11A.1 CHAT UI DESIGN

```
MESSAGE ANATOMY:
  User message:     Right-aligned OR left-aligned with avatar
  AI message:       Left-aligned, AI avatar/icon + content
  Timestamps:       Relative, shown on hover (desktop) or between message groups
  Message grouping: Cluster consecutive messages from same sender (< 5 min apart)
  Avatar:           User: photo or initials. AI: product icon/avatar.

INPUT AREA:
  Position:       Fixed at bottom, always visible
  Textarea:       Auto-expanding (min 1 line, max 6–8 lines before scroll)
  Send trigger:   Enter key (with Shift+Enter for new line) OR Send button
  Attachments:    Paperclip icon, file preview inline before sending
  Stop button:    CRITICAL — appears during AI generation, replaces send button
  Character count: Show when approaching limit (e.g., at 80% of max)

THREAD / CONVERSATION:
  Scroll:        Auto-scroll to bottom on new message
  Override:      If user scrolls up, stop auto-scroll. Show "↓ New message" banner.
  Load more:     "Load earlier messages" at top (don't pre-load all history)
  Empty state:   Welcome screen with suggested prompts (3–6 clickable examples)
```

### 11A.2 STREAMING RESPONSE PATTERNS

Streaming is the dominant delivery mode for AI responses. Design for the in-progress state.

```
WHILE STREAMING:
  Cursor: Blinking cursor at end of streaming text (shows it's actively writing)
  Stop button: Prominent "■ Stop generating" — this is critical UX
  Copy button: Hidden while streaming, appears when complete
  Scroll: Continue auto-scroll as new content streams in

STREAMING TEXT RENDERING:
  Never: Show raw markdown syntax while streaming (***word*** or **word**)
  Always: Render markdown in real time as tokens arrive
  Code blocks: Show language indicator + copy button immediately when block opens
  Tables: Difficult to stream — consider showing as loading then rendering complete

MULTI-MODAL STREAMING:
  Images: Placeholder with loading state while generating
  Progressive: Show low-res then high-res if supported
  Error: "Image generation failed" with retry option inline

LATENCY HANDLING:
  < 500ms to first token: No loading state needed
  500ms–2s to first token: Typing indicator (...) while waiting
  > 2s to first token: "Thinking..." with animated indicator
  No response: "Something went wrong. Try again." with retry CTA
```

### 11A.3 PROMPT INTERFACE DESIGN

```
INPUT ENHANCEMENTS:
  Slash commands:   "/" triggers command menu (change mode, select tool, etc.)
  @mentions:        "@" triggers user/document/context selector
  File upload:      Drag-and-drop into chat window (shows preview before send)
  Voice input:      Microphone button (mobile-critical, optional on desktop)
  Prompt templates: Preset prompts for common tasks (discoverable, not hidden)

CONVERSATION MANAGEMENT:
  History panel:    Left sidebar with conversation list
  Search:           Search within history by keyword
  Rename:           Editable conversation title (auto-generated, user-overridable)
  Delete:           With confirmation ("Delete this conversation? This can't be undone.")
  New chat:         Always accessible (top of sidebar, keyboard shortcut Cmd+Shift+N)
  Export:           Download conversation as markdown or PDF

MULTI-TURN CONTEXT:
  Thread indicator: Show when AI refers to earlier context ("As you mentioned earlier...")
  Context window:   Consider showing "Context: 12,000 / 100,000 tokens" for developer tools
  Branch/fork:      Advanced — allow editing an earlier message and creating a new branch
```

### 11A.4 TRUST, TRANSPARENCY & AI LOADING STATES

Trust is the central challenge of AI interfaces. Every design decision should build or maintain it.

```
TRANSPARENCY PATTERNS:
  Source citations:   Link to sources when knowledge comes from retrievable documents
  Confidence signals: "I'm not certain, but..." or "This may be outdated — verify with..."
  Tool use display:   Show when AI is using tools ("Searching the web...", "Running code...")
  Reasoning display:  Optional "Show reasoning" expandable section for complex answers

TRUST-BUILDING:
  Accuracy caveats:   Include for medical, legal, financial advice — always recommend professionals
  Uncertainty flags:  "This was accurate as of [date]" for time-sensitive information
  Feedback mechanism: Thumbs up/down on each response — show that feedback matters
  Correction flow:    Easy way to tell AI it made a mistake and regenerate

AI GENERATION STATES:
  Pending (0–500ms):   No indicator (first-token latency)
  Thinking (>500ms):   Animated "..." OR "Analyzing..." / "Thinking..." with subtle animation
  Streaming:           Cursor, stop button, live rendering
  Complete:            Copy, share, regenerate options appear
  Error:               Specific error message + retry + alternative suggestion
  Rate limited:        "You've reached the limit. Try again in X minutes." or upgrade CTA

CONTENT WARNINGS:
  Sensitive topics:   Clear disclaimer before AI-generated advice
  Medical:            "I'm an AI. This is not medical advice. Please consult a doctor."
  Legal:              "This is not legal advice. Consult a qualified attorney."
  Financial:          "This is not financial advice. Consider a licensed advisor."
```

### 11A.5 AI FEEDBACK MECHANISMS

```
PER-RESPONSE:
  Thumbs up/down:      Minimum viable feedback (every AI product needs this)
  Reaction picker:     Optional — emoji reactions for tone/usefulness
  Copy button:         Prominent after response complete
  Regenerate:          "Regenerate response" with optional prompt modification
  
DETAILED FEEDBACK:
  "What went wrong?" dropdown: Too long, Too short, Inaccurate, Harmful, Off-topic, Other
  Open text: Optional "Tell us more" — low friction but valuable
  Flag button: For harmful or inappropriate responses (important safety mechanism)

RATING DISPLAY:
  Never show aggregate ratings to users (gaming risk, creates bias)
  Instead: Show "Your feedback helps improve [product name]" — thank them
```

---

## ══════════════════════════════════════════
## 11B: FORMS (DEEP DIVE)
## ══════════════════════════════════════════

### 11B.1 FIELD PSYCHOLOGY

```
ORDERING RULES:
  Easy → Hard:          Build momentum (name before tax ID)
  Personal → Transactional: Build trust before sensitive data (name before payment)
  Related fields together: Addresses together, payment details together
  Time-sensitive last:  Email/name first (enables abandoned form recovery)

REQUIRED vs. OPTIONAL:
  If 90%+ fields required: Mark OPTIONAL fields only
  If many optional:        Mark REQUIRED fields only  
  Never mark both:         Choose the minority to mark — not both
  Asterisk legend:         "* Required" near top of form — always explain the symbol

FORM LENGTH RULE:
  Every field removed improves completion rate.
  Every field not removed should pass the test: "What do we DO with this data?"
  If you can't answer that — remove the field.
```

### 11B.2 INPUT TYPES & KEYBOARDS

```
ALWAYS use correct input type for each field:
  type="email"         Email — email keyboard on mobile, @ key prominent
  type="tel"           Phone — numeric dial pad on mobile
  type="number"        Numeric quantity — numeric keyboard
  inputmode="numeric"  Numeric code (PIN, credit card) — numeric keyboard, no minus sign
  inputmode="decimal"  Currency, measurements — numeric keyboard with decimal
  type="url"           URL — URL keyboard with .com / / buttons
  type="search"        Search — search/go key on mobile keyboard
  type="password"      Password — masked, show/hide toggle required
  type="date"          Date — native date picker (acceptable on desktop, preferred on mobile)
  type="datetime-local" Date + time selection
  type="file"          File upload (see §11C.3)
  type="color"         Color picker (native)
  type="range"         Range slider

AUTOCOMPLETE ATTRIBUTES:
  "name"               Full name
  "given-name"         First name
  "family-name"        Last name
  "email"              Email address
  "tel"                Phone number
  "street-address"     Street address
  "postal-code"        ZIP/postal code
  "country"            Country
  "cc-number"          Credit card number
  "cc-exp"             Credit card expiry
  "cc-csc"             Credit card CVV
  "current-password"   Sign-in password
  "new-password"       New/changed password
```

### 11B.3 INPUT MASKING & SMART FORMATTING

```
PHONE:      Format as typed: (555) 555-5555 or +1 555 555 5555
CREDIT CARD: Groups of 4: 4242 4242 4242 4242 (spaces as user types)
             Auto-detect card type from first digits (show Visa/MC icon)
DATE:       MM/DD/YYYY with auto-advance between segments
TIME:       HH:MM with AM/PM toggle
SSN/TIN:    XXX-XX-XXXX (mask after entry — show only last 4)

SMART DEFAULTS (auto-populate when possible):
  Country:    Detect from IP/browser locale (allow override)
  State:      Cascade from country selection
  Timezone:   Auto-detect from browser Intl API
  Currency:   Based on country
  Date format: Match user locale (MM/DD or DD/MM)
```

### 11B.4 VALIDATION TIMING

```
ON CHANGE (while typing):
  ✓ Password strength meter (real-time is helpful and expected)
  ✓ Character count approaching limit
  ✓ Real-time availability check (username, slug) — with debounce 300ms
  ✗ NOT: Email format (user hasn't finished typing)
  ✗ NOT: Any other format validation (premature errors frustrate users)

ON BLUR (when user leaves field):
  ✓ Email format validation
  ✓ Phone format validation
  ✓ Required field (was anything entered?)
  ✓ Length constraints
  → Show error message BELOW the field with × icon

ON SUBMIT:
  ✓ Full form validation
  ✓ Show ALL field errors simultaneously (not one at a time)
  ✓ Scroll to first error automatically
  ✓ Announce errors to screen readers via aria-live

NEVER:
  ✗ Validate email format while user is still typing
  ✗ Show "field required" errors before user has touched the form at all
  ✗ Remove error on blur (user may have fixed another field — re-validate)
```

### 11B.5 MULTI-STEP FORMS / WIZARDS

```
PROGRESS INDICATOR:
  Show: "Step 2 of 5" AND visual step indicators (circles with numbers)
  Labels: Name each step ("Contact Info", "Shipping", "Payment")
  Completed: Filled/checkmark. Current: Active color. Upcoming: Muted.
  Progress bar: Optional — shows percentage instead of steps

STEP RULES:
  Group related fields: Address fields together, never split across steps
  One concept per step: Don't mix unrelated concerns
  Back always available: Previous step button at every step
  Data preservation: Going back NEVER clears data from later steps
  Save progress: Auto-save draft so user can return if session interrupted

VALIDATION STRATEGY:
  Validate EACH STEP on "Next" click before advancing
  User can go BACK without re-validating completed steps
  Final review: Show summary of all steps before final submission
  Edit: Allow editing any step from review without losing other steps
```

### 11B.6 COMPLEX FORM PATTERNS

**Conditional Logic (show/hide fields based on answers):**
```
  Reveal fields smoothly with animation (not jarring instant appearance)
  ARIA: Use aria-hidden="false" when fields become visible
  Never: Remove required fields while hidden (causes confusing validation errors)
  Instead: Set required dynamically or use separate validation logic
```

**Repeating Field Groups (add team members, add items):**
```
  "Add another" button below the group
  Remove button on each item (trash icon, right side, right-aligned)
  Drag to reorder: Optional for prioritized lists
  Limit indicator: "You can add up to 5 team members" if there's a limit
  Minimum: If 1 required, show 1 and don't allow removal below 1
```

---

## ══════════════════════════════════════════
## 11C: COMPLEX UI COMPONENTS
## ══════════════════════════════════════════

### 11C.1 RICH TEXT EDITORS / WYSIWYG

```
TOOLBAR:
  Essential controls: Bold, Italic, Underline, Strikethrough
  Structure: H1, H2, H3, Paragraph, Blockquote
  Lists: Ordered, Unordered, Checklist
  Insert: Link, Image, Code block, Horizontal rule, Table
  Alignment: Left, Center, Right (only if truly needed — usually just left)
  History: Undo, Redo

FORMAT BAR (INLINE):
  Show contextual formatting bar when text selected (bubble above selection)
  Contains: Bold, Italic, Link, Clear formatting
  Keyboard shortcuts: Cmd+B, Cmd+I, Cmd+K for link — always work

SLASH COMMANDS:
  Type "/" to trigger block type selector (Notion-style)
  Searchable: Type "/" + letter to filter (e.g., "/head" shows heading options)
  Most common at top, searchable beyond that

CODE BLOCKS:
  Language selector dropdown: auto-detect language from content
  Copy button: Top-right of code block
  Line numbers: Optional toggle
  Syntax highlighting: Always

PERFORMANCE:
  Large documents (>10k words): Virtual rendering critical
  Image upload: Progressive upload with placeholder while uploading
  Auto-save: Every 3–5 seconds to draft/local storage
  Collaborative: Real-time cursors with user color + name tooltip (Operational Transform or CRDT)
```

### 11C.2 DATE & TIME PICKERS

```
DATE PICKER:
  Input display: MM/DD/YYYY formatted text input (keyboard-enterable)
  Calendar popup: Triggered on focus OR calendar icon click
  Calendar header: Left/right arrows for month navigation, click month/year to select faster
  Today: Highlighted as current date
  Selected: Clearly filled (not just outlined)
  Disabled dates: Visible but unclickable with muted appearance
  Range selection: First click = start, second = end; selection shows highlighted range
  Keyboard: Arrow keys navigate days, Enter selects, Escape closes

TIME PICKER:
  Input: HH:MM text field (24h or 12h + AM/PM based on locale)
  Selector: Scrollable list OR dropdown for hours and minutes
  Steps: 15-minute increments common (not every minute for most use cases)
  Native: Prefer native time picker on mobile

RELATIVE DATE SHORTCUTS:
  "Today", "Yesterday", "This week", "Last 7 days", "Last 30 days", "Custom range"
  Display after selection: Show selected date/range in human-readable format
```

### 11C.3 FILE UPLOAD DESIGN

```
SINGLE FILE:
  Trigger: Button "Choose file" OR full drop zone with dashed border
  Drop zone: Dashed border + cloud upload icon + "Drag & drop or browse"
  Hover: Background color changes to show it's an active drop target
  Active drop: Border becomes solid + color intensifies

MULTIPLE FILES:
  Drop zone same design, shows "multiple files accepted"
  File list: Each file shows: icon/thumbnail + filename + filesize + remove ×
  Upload progress: Per-file progress bar (not one global bar)
  Order: Most recently added at top

VALIDATION:
  File type: Instant error if wrong type on selection ("Only PDF, JPG, PNG accepted")
  File size: Instant error if too large ("File is 24MB. Maximum is 10MB.")
  Count limit: "You can upload up to 5 files" visible before AND after limit reached

DURING UPLOAD:
  Progress: Percentage bar per file
  Speed: Optional "2.4 MB/s" for large files
  Cancel: × to cancel mid-upload
  Retry: For failed uploads — show error + retry button per file

COMPLETION:
  Preview: Image thumbnails for images, file icon for other types
  Success: Checkmark on each completed file
  Persistent: After upload completes, files remain visible with remove option
```

### 11C.4 COMMAND PALETTE

```
TRIGGER: Cmd/Ctrl+K — do not use any other shortcut (this is now universal)
APPEARANCE: Full-width modal at top 25% of viewport

INPUT:
  Auto-focus on open
  Placeholder: "Search actions, pages, and settings..."
  Fuzzy search: Typo-tolerant matching
  Keyboard: Arrow up/down to navigate results, Enter to execute, Escape to close

RESULTS:
  Sections: "Recent", "Navigation", "Actions", "Settings" (clearly labeled)
  Result item: Icon + label + keyboard shortcut (right-aligned if available)
  Selected: Highlighted with background fill
  Loading: Show results as they filter (instant, no spinner needed)

DEFAULTS (before typing):
  Last 5 recently used items
  5 most frequently used global actions
  Current context-relevant actions

COMMAND TYPES:
  Navigation: "Go to Settings → Notifications"
  Actions:    "Create new project", "Invite team member"
  Search:     "Find in documents: [query]"
  Settings:   "Toggle dark mode", "Change language"
```

### 11C.5 SEARCH UX (ADVANCED)

```
SEARCH INPUT:
  Placeholder:  "Search..." with scope context ("Search projects...")
  Clear button:  × appears as soon as user types
  Search icon:   Left = decorative (always show). Right = trigger button.
  Keyboard:      Cmd/Ctrl+K or Cmd/Ctrl+F to focus — respect context
  Mobile:        Full-width, auto-focus on tap, "cancel" button to dismiss

RESULTS:
  Instant results: Debounce 300ms after keystroke (never on every keystroke)
  Highlight:      Bold/highlight the matching term within results
  Result anatomy: Title (with highlight) + type/category + snippet + icon
  Zero results:   "No results for '[query]'" + "Try: [similar terms]" + broader suggestions
  Loading:        Skeleton of expected result shape (not full-page spinner)

FILTERS:
  Active filters: Chips above results, individually dismissible + "Clear all"
  Count:          "47 results" updates in real time with filter changes
  Persistence:    Filters persist in URL params (shareable, refreshable)
  Facets:         "Category (3) ▼" shows count of matching items per filter option

EMPTY RESULTS PAGE:
  Acknowledge the query: "No results for 'prject'" (show the typo'd query)
  Suggest correction: "Did you mean 'project'?"
  Alternative actions: "Try searching all [categories]" or "Browse [section]"
  Recent searches: Show as quick-access
```

---

## ══════════════════════════════════════════
## 11D: NOTIFICATION SYSTEMS
## ══════════════════════════════════════════

### 11D.1 NOTIFICATION HIERARCHY

```
INTERRUPT LEVEL 1 — Critical alerts:
  Full-screen takeover OR modal dialog
  For: Payment failure, account suspended, critical security issue
  User must acknowledge before continuing

INTERRUPT LEVEL 2 — In-app banner:
  Top of page, dismissible
  For: Trial expiring, maintenance window, important announcement
  Duration: Until dismissed or condition resolved

INTERRUPT LEVEL 3 — Toast / snackbar:
  Bottom-center (mobile) or top-right (desktop), auto-dismiss
  For: Action confirmations, async completions, non-critical warnings
  Duration: 3s (info/success), 5s (with action button), persistent (errors)

INTERRUPT LEVEL 4 — Notification bell:
  Passive, user-initiated to read
  For: All other notifications that don't require immediate attention
  Badge: Unread count
```

### 11D.2 NOTIFICATION BELL (IN-APP)

```
BELL ICON:
  Unread badge: Red dot (any unread) or number badge (count)
  Animation: Subtle wiggle on new notification (once, not continuous)
  
NOTIFICATION PANEL:
  Position: Fixed dropdown below bell icon
  Width: 360–400px (desktop), full width (mobile)
  Max visible: 10 most recent, "View all" link to full notification page
  
NOTIFICATION ITEM:
  Icon: Avatar (for user actions) or product icon (for system events)
  Content: "[Actor] [action] [object]" e.g. "Sarah commented on Q4 Report"
  Timestamp: Relative ("2m ago", "Yesterday") on right side
  Unread indicator: Blue dot left side OR bold text
  Link: Entire item tappable, navigates to relevant context
  
GROUPING:
  Cluster same-type notifications: "Sarah and 3 others commented on Q4 Report"
  Group by category: Comments, Mentions, System
  
CONTROLS:
  Mark all as read: Text button at top
  Per-item dismiss: On hover, × button appears
  Settings link: "Notification preferences" at bottom
```

### 11D.3 PUSH NOTIFICATIONS

```
PERMISSION REQUEST:
  NEVER ask on first load — user has no context for why they'd want notifications
  Ask AFTER a contextual trigger: after completing first task, after clear value shown
  Explain value before prompting: "Get notified when someone comments on your work"
  Custom pre-prompt modal: Show your own dialog before OS prompt (you only get one chance)

NOTIFICATION CONTENT:
  Title: Brief, specific (not app name alone — they already know what app it is)
  Body: The actual message or event (not marketing copy)
  Icon: App icon (consistent, recognizable)
  Action: Relevant deep-link on tap (not just home screen)
  Action buttons: Optional (iOS max 4, Android flexible)

NOTIFICATION TYPES:
  Transactional: Order shipped, password changed, payment received → send immediately
  Social: Someone commented, tagged, followed → slight batching (5-min buffer)
  Marketing: New feature, sale → segment by preference, send at optimal time
  Never: Spam, irrelevant, or too-frequent notifications (users disable or uninstall)

PREFERENCE MANAGEMENT:
  Categories: Let users control per-type (comments, mentions, system, marketing)
  Timing: "Quiet hours" or "Do not disturb" schedule
  Channel: Email + push preference independently
  Easy to find: Settings → Notifications (never buried)
```

### 11D.4 ACTIVITY FEEDS

```
FEED ITEM ANATOMY:
  Avatar:     Actor performing action
  Action:     Verb + object "[Sarah] [commented on] [Q4 Report]"
  Timestamp:  Relative time, right-aligned
  Preview:    Brief content preview if applicable (first 100 chars of comment)
  Link:       Navigate to context
  Reaction:   Optional like/react button inline

FEED DESIGN:
  Sorting: Newest first (default), grouped by day ("Today", "Yesterday", "Jun 8")
  Loading: Skeleton on initial load, progressive loading on scroll
  Real-time: New items appear at top with "New activity" banner (not auto-prepended)
  Empty: "No recent activity. Your team's actions will appear here."
  
FILTERING:
  "All activity" vs "Your mentions" vs by action type
  Per-member filtering for large teams
```

---

## ══════════════════════════════════════════
## 11E: REAL-TIME & COLLABORATIVE UI
## ══════════════════════════════════════════

### 11E.1 PRESENCE INDICATORS

```
ONLINE STATUS:
  Green dot (online), Yellow dot (away/idle), No dot (offline)
  Position: Bottom-right of avatar (overlapping)
  Size: 8–10px dot, 2px white border (separates from avatar background)

TYPING INDICATORS:
  Chat/messaging: "Sarah is typing..." or animated three-dot (...) with avatar
  Documents: Show cursor with user name and color
  Multiple users: "Sarah and 2 others are typing..."

VIEWING INDICATORS:
  "Sarah is viewing this page" → subtle avatar row above content
  Document editing: Show cursors with user name tags
  "Last edited by Sarah, 3 min ago" on collaborative items

USER COLORS:
  Auto-assign distinct colors per user (ensure no two users have same color in view)
  Colors must meet 3:1 contrast on the surface they appear on
  Colors should be distinguishable even for color-blind users (vary shape too)
```

### 11E.2 LIVE UPDATE PATTERNS

```
OPTIMISTIC UPDATES:
  Show the change immediately before server confirmation
  On success: Confirm quietly (state is already correct)
  On failure: Revert + show error "Change couldn't be saved. Try again."
  
LIVE DATA UPDATES:
  New items in list: Slide in from top with brief highlight (green flash)
  Changed values: Flash animation on changed cell/value (50ms yellow → normal)
  Removed items: Fade out + slide/collapse to remove
  Prevent scroll jump: When new items added at top of scrolled list, maintain scroll position
    "12 new items" banner at top instead of jumping

CONFLICT RESOLUTION:
  Two users edit same field:
    → Last write wins (simplest — show "Last saved by [user]" timestamp)
    → OR merge: Show diff, let user choose which version
    → OR lock: "Sarah is currently editing this field"
  
  Stale content warning:
    "This page has been updated by Sarah. Refresh to see changes?"
    → Show "Refresh" button, don't force reload
```

### 11E.3 MULTIPLAYER PATTERNS

```
COLLABORATIVE CURSORS:
  Each user: Custom cursor color + name label
  Label shows on hover or always (depends on density)
  Smooth movement: Interpolate position updates (don't teleport)
  Away threshold: Cursor fades after 30s of inactivity

SELECTION & HIGHLIGHTING:
  Another user's selection: Transparent colored highlight with user indicator
  Multiple selections: Each user's color layered (max 20% opacity per user)

DOCUMENT LOCKING (for linear workflows):
  Section-level locks (not full document)
  "Sarah is editing this section" + estimated time if available
  Auto-release: After 2 minutes of inactivity
  Override: "Take over editing" with warning

SIMULTANEOUS USERS INDICATOR:
  Facepile of current viewers at top of document
  Max 5 avatars shown + "+3 more" overflow
  Tooltip on hover: Names of all current viewers
  Recent: Show faded for users active in last 10 minutes
```

---

## ══════════════════════════════════════════
## 11F: ERROR PAGES & EDGE STATES
## ══════════════════════════════════════════

### 11F.1 ERROR PAGES (404, 500, MAINTENANCE)

**404 Page:**
```
REQUIRED ELEMENTS:
  Clear title: "Page not found" (not a raw "404 error")
  Brief explanation: "This page may have been moved, deleted, or never existed."
  Navigation: Return to homepage + most common destinations
  Search: Optional — let them search from the error page
  
DESIGN TONE: Helpful, not panicked. Optionally playful (brand-appropriate).
  
WHAT TO AVOID:
  ✗ Technical jargon or error codes prominently
  ✗ Dead ends with no navigation options
  ✗ "Error 404" as the headline
```

**500 / Server Error Page:**
```
REQUIRED ELEMENTS:
  Clear title: "Something went wrong" (not "500 Internal Server Error")
  Explanation: "We're having trouble processing your request right now."
  Action: "Try again" button + "Go to homepage" button
  Status: Link to status page if you have one
  Report: Option to report the issue (optional but appreciated)
  
TONE: Apologetic but reassuring ("We're working on it")
NEVER: Show stack traces or technical error details to end users
```

**Maintenance Page:**
```
REQUIRED ELEMENTS:
  Title: "We're down for maintenance" or "[Product] will be back soon"
  Duration: "We'll be back by [time] [timezone]" (give a time, even if estimate)
  What's happening: "We're making some improvements" (no need for detail)
  Alternative: "Check our status page: [URL]" or "Follow @[handle] for updates"
  Contact: Support contact for urgent matters
```

### 11F.2 PAYWALL & UPGRADE PATTERNS

```
FEATURE GATING (soft wall):
  Teaser: Show the feature exists, show value, then gate
  Modal or inline: "This is a Pro feature. Upgrade to access analytics."
  Preview: Blur/lock overlay over feature screenshot (show what they'd get)
  CTA: "[Upgrade to Pro → $29/mo]" with cancel/close option
  
HARD LIMIT (quota reached):
  Banner: "You've used 5/5 projects. Upgrade for unlimited projects."
  Disable new creation button: With tooltip "Upgrade to create more"
  Show: How much would unlock by upgrading (not just generic "upgrade")

TRIAL EXPIRY:
  7-day warning: Subtle banner ("Your trial ends in 7 days. Upgrade to keep access.")
  3-day warning: More prominent, show what they'll lose
  1-day warning: Modal on login (not dismissible without action or explicit skip)
  Expired: Graceful read-only access or export data before losing it
  NEVER: Immediate loss of all data — always give export window

PRICING PAGE DESIGN:
  Most popular: Visually highlighted (colored border, "Most popular" badge)
  Feature comparison: All plans side-by-side table (not hidden)
  Price display: Monthly + annual toggle, annual savings prominent ("Save 33%")
  CTAs: Different per plan ("Start Free", "Start Trial", "Contact Sales")
  FAQ: Common objections answered below pricing
```


# SECTION 12: PERFORMANCE & TECHNICAL UX

---

## 12.1 CORE WEB VITALS (CWV)

Core Web Vitals are Google's UX-focused performance metrics. Poor scores directly degrade user experience and search rankings.

```
LCP — LARGEST CONTENTFUL PAINT (Loading Experience)
  Measures:  Time for largest visible element to render (hero image, headline)
  Target:    < 2.5 seconds (Good) | 2.5–4s (Needs Improvement) | > 4s (Poor)

  UX Impact: Users perceive page as loaded when main content appears
  Design actions:
    → Prioritize above-fold images: add loading="eager" + fetchpriority="high"
    → Avoid hero sections that depend on slow JS bundles
    → Size hero images correctly for each breakpoint
    → Use <link rel="preload"> for critical hero images

INP — INTERACTION TO NEXT PAINT (Responsiveness — replaced FID in 2024)
  Measures:  Delay between user interaction and next visual update
  Target:    < 200ms (Good) | 200–500ms (Needs Improvement) | > 500ms (Poor)

  UX Impact: Directly measures "does the UI feel responsive?"
  Design actions:
    → Instant visual feedback on click/tap (<100ms state change)
    → Never block the main thread for >50ms with synchronous work
    → Optimistic UI updates before server confirmation
    → Avoid heavy recalculations triggered by user input

CLS — CUMULATIVE LAYOUT SHIFT (Visual Stability)
  Measures:  Total amount of unexpected layout movement during page load
  Target:    < 0.1 (Good) | 0.1–0.25 (Needs Improvement) | > 0.25 (Poor)

  UX Impact: Content jumps as page loads — users lose their place or misclick
  Design actions:
    → Always set width/height on images (prevents shift when they load)
    → Reserve space for async content (skeleton screens)
    → Avoid inserting content above existing content dynamically
    → Be careful with web fonts — use font-display: swap with size adjustments
    → Fixed-height containers for ad slots and dynamic content
```

---

## 12.2 LOADING STRATEGIES & THEIR UX IMPLICATIONS

```
SSR (SERVER-SIDE RENDERING):
  UX:     Fast first paint, content available immediately, good SEO
  Best:   Marketing pages, e-commerce, blogs, content-heavy sites
  Watch:  Time-to-interactive may lag behind visual render (buttons inactive briefly)

SPA (SINGLE-PAGE APPLICATION):
  UX:     Initial load slower, subsequent navigation instant (no full reloads)
  Best:   Web apps, dashboards, tools with heavy interactivity
  Watch:  Must implement loading states for every route transition
          Must handle deep-linking and browser back button correctly

STATIC SITE GENERATION:
  UX:     Fastest possible delivery, fully pre-rendered
  Best:   Marketing, documentation, content that changes infrequently
  Watch:  Dynamic content requires client-side fetching after initial load

PARTIAL HYDRATION / ISLANDS:
  UX:     Fast initial render with interactive components loading progressively
  Best:   Mixed content/interactive pages (Next.js, Astro, Qwik)
  Design: Design for progressive loading — page is usable before fully interactive
```

---

## 12.3 PERFORMANCE BUDGETS

Define performance expectations as design constraints, not afterthoughts:

```
PAGE WEIGHT BUDGETS:
  Marketing page:    < 500KB total, < 200KB JavaScript
  Web application:   < 1MB initial, < 500KB JavaScript
  Mobile web:        Treat every KB as if users pay per byte

IMAGE OPTIMIZATION:
  Format:    WebP/AVIF first, JPEG/PNG fallback
  Responsive: Use <picture> + srcset for multiple breakpoints
  Lazy load:  loading="lazy" for below-fold images
  Placeholder: Blur-up (base64 tiny version) or colored box while loading

FONT LOADING:
  Maximum 2 font families, 2–3 weights each
  Subset fonts to used characters (especially for non-Latin scripts)
  Self-host if possible (one less DNS lookup)
  font-display: swap (prevents invisible text during font load)

CRITICAL CSS:
  Inline critical above-fold CSS in <head>
  Defer non-critical CSS loading
  Never block rendering with large stylesheets
```

---

## 12.4 OFFLINE-FIRST & PWA UX

```
OFFLINE STATE DESIGN (RULES):
  NEVER: Show blank screen when offline
  ALWAYS: Show cached content + "You're offline" banner
  Label: "Last updated [relative time]" on stale cached content
  Queue: Actions taken offline queued for sync when connected
  Sync indicator: "Syncing..." then "Synced ✓" when connection restored

OFFLINE BANNER:
  Position: Top of screen (below nav), not blocking content
  Color: Amber/yellow with icon (network-disconnected icon)
  Content: "You're offline. Showing cached data from [X ago]."
  Auto-dismiss: When connection restored (with brief "Back online ✓" confirmation)

SERVICE WORKER UX:
  Update available: "A new version is available. Refresh to update." (non-blocking)
  Don't force-refresh: Let user finish current task, then reload
  Background sync: Queue writes, sync automatically when online
```

---

## 12.5 VIRTUAL SCROLLING (LARGE LISTS)

For lists with thousands of items, render only what's visible:

```
WHEN TO VIRTUALIZE: Lists > 500 items (DOM performance degrades significantly)
IMPLEMENTATION: react-virtual, react-window, @tanstack/virtual

UX REQUIREMENTS:
  Native scroll feel:  No scroll jumpiness or blank white flashes
  Consistent item height: Fixed-height rows render much more smoothly
  Variable height:    Requires estimation + measurement after render (complex)
  Search:             Full search across all items (not just visible)
  Selection:          Maintain selection state for non-visible items
  Scroll position:    Restore exact scroll position on back navigation

DESIGN IMPLICATIONS:
  Cannot use CSS :nth-child animations on variable window items
  Cannot use sticky positioning on virtualized items without workarounds
  Accessibility: aria-rowcount total, aria-rowindex per visible row
```

---

# SECTION 13: INTERNATIONALIZATION & LOCALIZATION

---

## 13.1 RTL (RIGHT-TO-LEFT) DESIGN

Arabic, Hebrew, Farsi, Urdu require mirrored layouts. Plan for RTL from day one — retrofitting is painful.

```
LAYOUT MIRRORING:
  Text:          Right-aligned, flows right-to-left
  Icons:         Directional icons must flip (arrows, back/forward, progress)
  Navigation:    Sidebar moves to right side, breadcrumbs reverse
  Reading order: Top-right primary optical area (not top-left)
  Page layout:   Everything mirrors across vertical axis

CSS APPROACH:
  Use logical properties (not physical):
    margin-inline-start: instead of margin-left
    padding-inline-end: instead of padding-right
    text-align: start instead of text-align: left
    border-inline-start: instead of border-left
  
  Apply RTL globally:
    <html dir="rtl" lang="ar">
    OR :dir() CSS pseudo-class for component-level

WHAT DOES NOT MIRROR:
  Numbers: Still read left-to-right in RTL context
  Time: 9:30 AM still reads left-to-right
  Mathematical expressions: Left-to-right always
  Media controls: Play/pause, progress bar — leave as-is
  Flags and logos: Never mirror
  Checkmarks, stars: Never mirror

ICON CHECKLIST FOR RTL:
  ✓ Mirror: back arrow, forward arrow, chevrons, pagination arrows, 
            text alignment icons, list-with-arrow-right icons
  ✗ Don't mirror: Upload/download arrows, clock, calendar, play/pause,
                  settings gear, trash icon, checkmark, ×/close
```

---

## 13.2 TEXT EXPANSION & CONTRACTION

When translating from English, text length changes dramatically:

```
EXPANSION (English → other language):
  German:    +30% average
  Finnish:   +30% average  
  Russian:   +30% average
  French:    +25% average
  Spanish:   +20% average

CONTRACTION:
  Chinese:   -40% (character-dense)
  Japanese:  -30%
  Korean:    -15%

DESIGN RULES:
  Never: Fixed-width containers for translated text (they'll overflow)
  Always: Flexible widths with min/max constraints
  Test:   All UI elements with 1.3× longer text before shipping
  Buttons: Must expand horizontally (not truncate)
  Navigation labels: Must wrap or truncate gracefully at double length
  Error messages: Often 2× longer when translated — design for this
```

---

## 13.3 DATE, TIME, NUMBER & CURRENCY FORMATTING

```
DATES:
  US:           MM/DD/YYYY  (6/10/2025)
  Europe/most:  DD/MM/YYYY  (10/6/2025) or DD.MM.YYYY
  ISO 8601:     YYYY-MM-DD  (2025-06-10) — safe for technical/API contexts
  Danger: "06/10/2025" — is this June 10 or October 6? NEVER use without locale

  Always use Intl.DateTimeFormat() for display:
  new Intl.DateTimeFormat('fr-FR').format(date) → "10/06/2025"
  new Intl.DateTimeFormat('en-US', {dateStyle:'long'}).format(date) → "June 10, 2025"

NUMBERS:
  US/UK:        1,234,567.89  (comma thousands, period decimal)
  Europe:       1.234.567,89  (period thousands, comma decimal)
  Switzerland:  1 234 567.89  (space thousands)
  
  Always use Intl.NumberFormat():
  new Intl.NumberFormat('de-DE').format(1234567.89) → "1.234.567,89"

CURRENCY:
  Symbol position varies: $1,234 (US) vs 1.234 € (Germany) vs £1,234 (UK)
  Always use Intl.NumberFormat with style: 'currency'
  Show ISO code for international audiences: "USD 1,234.56" removes ambiguity

TIME:
  12-hour (AM/PM): US, Canada, Australia, some Latin America
  24-hour:         Most of Europe, Asia, Africa, military
  Detect from locale, allow user override
```

---

## 13.4 CULTURAL COLOR CONSIDERATIONS

```
Context matters. These are generalizations — always research your specific market.

WHITE:   Purity/cleanliness (Western) | Mourning/death (parts of East Asia)
RED:     Danger/error (global) | Luck/prosperity (China) | Mourning (parts of Africa)
GREEN:   Success/nature (global) | Forbidden (Indonesia) | Religious significance (Islam)
BLUE:    Trust/professional (global — most universal "safe" color)
YELLOW:  Caution (global) | Royalty (some SE Asia) | Mourning (parts of Middle East)
PURPLE:  Royalty/luxury (Western) | Death/mourning (parts of Latin America, Thailand)

PRACTICAL RULE:
  Use semantic/functional colors (success green, error red) globally
  For brand colors in new markets: research before assuming Western associations transfer
```

---

# SECTION 14: PRIVACY & COMPLIANCE DESIGN

---

## 14.1 PRIVACY-BY-DESIGN PRINCIPLES

```
1. PROACTIVE:    Build privacy in from the start, not as an afterthought
2. DEFAULT:      Maximum privacy protection by default (opt-out, not opt-in for privacy)
3. EMBEDDED:     Privacy is part of the design, not a separate feature
4. POSITIVE-SUM: Privacy AND security, not privacy VS security
5. TRANSPARENT:  What data, why, for how long — clearly communicated
```

---

## 14.2 COOKIE CONSENT PATTERNS

Legal requirement in EU (GDPR), UK, California (CCPA), and many other jurisdictions.

```
BANNER DESIGN:
  Position:   Bottom of screen (not blocking content) OR bottom-left corner
  Size:       Compact — one or two lines of text + buttons (not full-page takeover)
  Contrast:   Must meet WCAG contrast requirements (often missed)
  Persistence: Show until user makes a choice (not just dismissed by scrolling)

REQUIRED ACTIONS:
  Accept all:     One clear button ("Accept all cookies")
  Reject all:     EQUALLY prominent button — GDPR requires this
  Customize:      "Manage preferences" for granular control
  
  ILLEGAL PATTERNS (dark patterns — enforce in EU):
  ✗ Reject button smaller, lighter, or harder to find than Accept
  ✗ Pre-checked optional categories
  ✗ Using "X" close to mean "Accept" (closing = rejected/essential only)
  ✗ Hiding reject option behind multiple clicks when accept is one click

PREFERENCE CENTER:
  Categories:  Essential (always on, locked) | Analytics | Marketing | Personalization
  Per-category: Explanation of what this category does and why
  Toggle:       Clear on/off for each non-essential category
  Save button:  "Save preferences" (not auto-save on toggle)

RESPECT CHOICES:
  No re-asking within 12 months of a choice made
  Store consent record server-side (not just cookie — user clears cookies)
  Withdraw consent: Easy way to change preferences (usually in footer)
```

---

## 14.3 DATA PRIVACY UI PATTERNS

```
ACCOUNT DATA EXPORT:
  GDPR Art. 20 requires data portability
  Export button in Settings → Account (not buried)
  Format: JSON or CSV (machine-readable)
  Timeline: Process within 30 days maximum (show expected timeline to user)
  Notify: Email confirmation when export is ready

ACCOUNT DELETION:
  "Delete Account" in Settings → Danger Zone (clearly separated, red)
  Confirmation: Type "DELETE" or account email to confirm
  Grace period: Offer 30-day recovery window (warn about this clearly)
  What's deleted: List everything that will be permanently removed
  What's retained: Legal compliance (invoices, transactions kept per law)
  Timeline: Immediate access removal + 30-day data purge (communicate this)

DATA USAGE TRANSPARENCY:
  "Why do we collect this?": Inline tooltip next to each data field in forms
  Privacy policy: Plain-language summary at top (before legal boilerplate)
  Data retention: Clearly state "We keep this for X months/years"
  Third-party sharing: Explicit disclosure of any data sharing
```

---

## 14.4 SECURITY UX DESIGN

```
SESSION MANAGEMENT:
  Timeout warning: "Your session expires in 5 minutes" banner (not just sudden logout)
  Extend option: "Keep me signed in" button on timeout warning
  Logout all: "Sign out of all devices" option in Security settings
  Active sessions: List of devices/sessions with location, last active, revoke option

PASSWORD CHANGE:
  Require current password before setting new one
  Invalidate all other sessions after password change (with notification)
  Email confirmation: "Your password was changed. This wasn't you? [Secure account →]"

2FA SETUP:
  Clear step-by-step setup wizard
  Recovery codes: Shown ONCE, must be acknowledged (checkbox: "I've saved these codes")
  Backup methods: Offer SMS as backup to authenticator app
  Disable: Requires 2FA verification to disable (prevents attacker disabling it)
```

---

# SECTION 15: DESIGN SYSTEMS (DEEP DIVE)

---

## 15.1 THE THREE LAYERS

A design system is not a component library. It is:
- A **shared language** between design and engineering
- A **set of decisions made once** that don't need to be remade
- A **living product** that evolves with the product it serves

```
LAYER 1 — FOUNDATION (Design Tokens + Primitives)
  Colors, Typography, Spacing, Shadows, Borders, Radii, Z-index scale
  → Raw values, no UI meaning
  → Change here → everything updates

LAYER 2 — COMPONENTS
  Buttons, Inputs, Cards, Navigation, Tables, Modals, Alerts
  → Assembled from Layer 1 tokens
  → All states documented, accessible, tested
  
LAYER 3 — PATTERNS & TEMPLATES  
  How components combine to solve recurring UX problems
  Form layouts, Empty states, Settings pages, Onboarding flows
  → Patterns, not rigid templates — adaptable to context
```

---

## 15.2 TOKEN NAMING CONVENTION

```
FORMAT: {category}-{property}-{variant}-{state}

CATEGORY:    color | space | font | border | shadow | radius | z-index
PROPERTY:    background | text | border | padding | size | weight | height
VARIANT:     primary | secondary | success | warning | error | neutral | brand
STATE:       default | hover | active | focus | disabled | loading | selected

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
  Semantic names ONLY in Tier 2+ (not "blue-500" — use "color-action-primary")
  Consistent structure (always same order: category → property → variant → state)
  No abbreviations in semantic tier ("background" not "bg" — less ambiguity)
  Document: What is this token for? When is it used? What not to use it for?
```

---

## 15.3 COMPONENT API DESIGN

Every component in a design system must document:

```
PROPS / VARIANTS:
  size:       xs | sm | md | lg | xl
  variant:    primary | secondary | ghost | destructive | link
  state:      default | loading | disabled | error | success
  
COMPOSITION SLOTS:
  What can be placed inside the component?
  What does it accept as children?
  What slots are available? (leading-icon, trailing-icon, label, description)

ACCESSIBILITY CONTRACT:
  ARIA role: What role does this component expose?
  Keyboard behavior: How does keyboard navigation work?
  Screen reader announcement: What gets announced on interaction?
  Focus management: Where does focus go on open/close/activate?
  Required ARIA props: What must consuming developers provide?

USAGE GUIDELINES:
  When to use this vs. similar components
  Anti-patterns: "Never use this inside a table cell"
  Max usage: "One primary button per section"
  Code examples: Working code snippets (not pseudo-code)
  Visual examples: All variants + all states shown

CHANGE LOG:
  Version introduced
  Version modified + what changed + migration guide
  Deprecated: When removed and what replaces it
```

---

## 15.4 DESIGN SYSTEM GOVERNANCE

```
CONTRIBUTION PROCESS:
  Proposal: GitHub issue or RFC doc (describe need, proposed solution)
  Review: Design + Engineering leads review (minimum 2 reviewers)
  Build: Component built with full state coverage + accessibility
  Test: Automated tests + accessibility audit + cross-browser
  Document: All states, usage guidelines, code examples
  Release: Versioned release with changelog + migration notes
  Announce: Team notification + example implementations

VERSIONING:
  Follow semantic versioning: MAJOR.MINOR.PATCH
  MAJOR: Breaking changes (component rename, prop removal)
  MINOR: New components, new non-breaking variants
  PATCH: Bug fixes, style adjustments

TOKEN DEPRECATION:
  Deprecate old token → new token exists for 2 releases minimum
  Show warning in Figma + console on use of deprecated token
  Remove only after migration grace period
```

---

# SECTION 16: UX RESEARCH & PROCESS

---

## 16.1 THE RESEARCH HIERARCHY

```
GENERATIVE RESEARCH (Understand the problem — diverge):
  User Interviews:     1:1, 30–60 min, open-ended questions
                       Goal: Understand mental models, jobs-to-be-done, pain points
  Diary Studies:       Users log experiences over 1–4 weeks
                       Goal: Real behavioral data over time (not recall)
  Contextual Inquiry:  Observe users in their natural environment
                       Goal: Discover undisclosed behaviors and workarounds
  Surveys:             Quantitative, 100+ responses, validate hypotheses
  → OUTPUT: Jobs-to-be-done, pain points, mental models, opportunity areas

EVALUATIVE RESEARCH (Test the solution — converge):
  Usability Testing:   5 users find 85% of usability issues (Nielsen's Law)
  A/B Testing:         Statistical validation of design decisions (need traffic)
  5-Second Test:       First-impression comprehension check
  Card Sorting:        IA validation (how users categorize content)
  Tree Testing:        Navigation structure validation (findability)
  Prototype Testing:   Figma/InVision clickthrough before any code written
  → OUTPUT: Usability problems, task completion data, preference validation

ANALYTICS (Measure at scale):
  Heatmaps:           Where users click, move, scroll (Hotjar, Microsoft Clarity)
  Session recordings: Watch real user flows — discover unexpected paths
  Funnel analysis:    Where users drop off in critical flows
  Search logs:        What users search for reveals what they can't find
  Error logs:         What errors users encounter most frequently
  → OUTPUT: Quantitative validation, pattern discovery, regression detection
```

---

## 16.2 USER INTERVIEW GUIDE

```
PREPARATION:
  Write your questions first, then pilot-test them on a colleague
  Prepare: Recording consent, screener criteria, 5–8 participants

OPENING (5 min):
  "Tell me a bit about yourself and your role"
  "How do you currently handle [area of interest]?"
  Build rapport before product-specific questions

EXPLORATION (30–40 min):
  "Walk me through the last time you [did the task]"
  "What was the hardest part of that?"
  "What tools or workarounds do you use?"
  "Show me how you do that [watch them actually do it]"

CLOSING (5 min):
  "Is there anything important I didn't ask about?"
  "What would make this much better for you?"

FACILITATION RULES:
  ✓ Think-aloud: "Talk me through what you're thinking"
  ✓ Open questions: "Tell me about..." not "Do you think..."
  ✓ Follow silence: Count to 5 in your head before speaking — silence often reveals
  ✓ Follow threads: If they mention something unexpected, explore it
  ✗ Never lead: "Would you say this is confusing?" → "How was that for you?"
  ✗ Never defend: Resist explaining design decisions (you're there to learn)
  ✗ Never fix: Don't tell them how to do something if they're struggling
```

---

## 16.3 USABILITY TESTING (5 USERS, 60 MIN)

```
TASK FORMAT:
  Scenario-based: "You just got hired as the project manager for a 5-person team.
                   Please add your first team member."
  → Specific goal, realistic scenario, NO hints on HOW to do it
  → 3–5 tasks per session (quality > quantity)

METRICS:
  Task completion rate:  Did they finish? (Binary or self-rated success)
  Time-on-task:         How long did it take? (Benchmark against baseline)
  Error rate:           How many wrong paths / backtracking actions?
  Satisfaction rating:  Post-task "How difficult was this?" (1–7 Likert scale)
  Think-aloud data:     Qualitative insight into mental model vs. design model

ANALYSIS:
  Rainbow spreadsheet:  Issues in rows, participants in columns
  Severity rating:      1 (cosmetic) to 4 (prevents task completion)
  Fix prioritization:   High-severity × High-frequency = highest priority
  Pattern threshold:    3+ participants hitting the same issue = confirmed problem

REMOTE TESTING:
  Tools: UserTesting.com, Maze, Lookback, Lyssna (formerly UsabilityHub)
  Benefits: Faster recruitment, broader geography, async possible
  Challenges: Less control, tech issues, harder to follow up
```

---

## 16.4 THE DOUBLE DIAMOND PROCESS

```
DISCOVER        DEFINE           DEVELOP          DELIVER
(Diverge)       (Converge)       (Diverge)        (Converge)
    ◆               ◆               ◆               ◆
Research   → Problem frame → Ideation    → Solution
Interviews → Pain points  → Wireframes  → Prototypes
Observation→ Personas     → Concepts    → Testing
Analytics  → Opportunity  → Iteration   → Handoff
             statement
```

---

## 16.5 DESIGN HANDOFF: THE BRIDGE TO ENGINEERING

```
WHAT ENGINEERING NEEDS FROM DESIGN:

Component specs:
  → Dimensions (px, % or auto — specify which), padding, margin, gap
  → All states: Default, hover, active, focus, disabled, loading, error, empty, success
  → Breakpoint behavior: How each component adapts across all breakpoints
  
Visual values:
  → Colors: Design token names preferred over raw hex values
  → Typography: Font name, weight, size (px or rem), line-height, letter-spacing
  → Shadows: Exact box-shadow values OR token name
  → Border: Width, style, color, radius
  
Behavior:
  → Animation: Duration, easing function, what triggers what, what returns to default
  → Interaction: Exactly what happens on click, hover, focus, keyboard activation
  → State transitions: Which state leads to which state under what conditions
  
Edge cases (CRITICAL — usually missing):
  → Empty state: What shows when there's no data?
  → Loading state: What shows while data loads?
  → Error state: What shows when it fails?
  → Long text: What happens with 200 characters in a field designed for 20?
  → Truncation: Where does text truncate? Is there a tooltip showing full text?
  → Max items: What happens when a list has 500 items vs. 5?
  
Assets:
  → Icons: SVG (not PNG), with semantic names
  → Illustrations: SVG or optimized PNG/WebP
  → Images: Aspect ratios + focal point for responsive cropping

WHAT NOT TO DO IN HANDOFF:
  ✗ Handoff only the happy path (no states, no edge cases, no errors)
  ✗ Use pt instead of px/rem for font sizes (causes mismatches)
  ✗ Leave animation described as "make it smooth" (nightmare for engineers)
  ✗ Mark pixel-perfect requirements on responsive elements (use flex/constraints)
  ✗ Leave component logic undocumented ("the designer will explain it later")

RECOMMENDED TOOLS:
  Figma Dev Mode:   Industry standard — inspect values, export assets, view tokens
  Storybook:        Living component documentation in code (component library)
  Zeroheight:       Design system documentation sites
  Supernova:        Token sync between Figma and code
```

---

## 16.6 DESIGN QA

Design QA is the review of implemented designs against specifications before ship.

```
QA CHECKLIST:
  Visual accuracy:    
    □ Colors match design tokens (not hardcoded hex)
    □ Spacing matches design (8pt grid — check with browser ruler)
    □ Typography: font, weight, size, line-height all correct
    □ Border radius consistent with design system
    □ Shadows match elevation spec

  States:
    □ Hover states implemented (not just default)
    □ Focus indicators visible and WCAG-compliant
    □ Disabled state visually distinct
    □ Loading state shown during async operations
    □ Error state implemented and styled

  Responsiveness:
    □ Test at all defined breakpoints
    □ No horizontal scroll at any breakpoint (except intentional)
    □ Touch targets ≥ 44px on mobile
    □ No text overflow or truncation issues

  Accessibility:
    □ Keyboard navigation works completely
    □ Screen reader test (VoiceOver/NVDA) — all content readable
    □ Contrast ratios pass (use browser DevTools check)
    □ No missing alt text

  Edge cases:
    □ Empty state shown
    □ Long text doesn't break layout
    □ Error state shown
    □ Loading state shown

QA PROCESS:
  Designer reviews implementation (not developer self-review)
  Use browser zoom 200% to expose layout issues
  Test with: Chrome, Firefox, Safari, Mobile Safari, Chrome Mobile
  File issues: Screenshot + spec reference + expected vs. actual
```

---

# SECTION 17: EVALUATION & MEASUREMENT

---

## 17.1 NIELSEN'S 10 HEURISTICS (COMPLETE REFERENCE)

```
1. VISIBILITY OF SYSTEM STATUS
   Principle: Always keep users informed about what's happening.
   Questions: Does the user always know what's happening?
              Are there loading states, progress indicators, confirmations?
   Failures:  Silent form submission, no confirmation after save, 
              no indicator that something is processing

2. MATCH BETWEEN SYSTEM AND REAL WORLD
   Principle: Use the user's language, not system jargon.
   Questions: Does it speak in the user's vocabulary?
              Are metaphors and concepts familiar?
   Failures:  "Persist to storage" instead of "Save"
              "Authentication credentials" instead of "Email and password"

3. USER CONTROL AND FREEDOM
   Principle: Support undo and redo. Always provide an escape hatch.
   Questions: Can users undo mistakes? Is there always a way back?
   Failures:  No undo for destructive actions
              No way to cancel a running process
              No back button or escape from a flow

4. CONSISTENCY AND STANDARDS
   Principle: Follow platform conventions. Same things look and work the same.
   Questions: Do similar things look and behave similarly?
              Does it follow platform conventions (iOS/Android/Web)?
   Failures:  Primary button sometimes blue, sometimes green
              "Save" button on left in one modal, right in another
              Custom swipe gesture contradicts iOS standard

5. ERROR PREVENTION
   Principle: Prevent errors before they occur.
   Questions: Are errors prevented proactively?
              Are irreversible actions confirmed?
   Failures:  No confirmation before deleting
              No format hints before validation error
              Allowing impossible combinations without feedback

6. RECOGNITION RATHER THAN RECALL
   Principle: Show options — don't make users remember.
   Questions: Does the UI show options rather than requiring memory?
              Are recent items, defaults, and suggestions visible?
   Failures:  Command-line only interface without autocomplete
              No recently used items for frequent operations
              User must remember exact syntax

7. FLEXIBILITY AND EFFICIENCY OF USE
   Principle: Shortcuts for experts; guided paths for novices.
   Questions: Can power users work faster?
              Are there keyboard shortcuts, bulk actions, macros?
   Failures:  No keyboard shortcuts in a tool used daily
              No bulk actions on lists used by admins
              No command palette in complex applications

8. AESTHETIC AND MINIMALIST DESIGN
   Principle: Every extra element competes with important elements.
   Questions: Is every element necessary?
              Does anything non-essential distract from the primary task?
   Failures:  3 CTAs on one page with equal visual weight
              Sidebar full of rarely-used options
              Decorative elements pulling attention from key data

9. HELP USERS RECOGNIZE, DIAGNOSE, AND RECOVER FROM ERRORS
   Principle: Error messages must be human-readable, specific, and actionable.
   Questions: Are errors explained in plain language?
              Do they tell the user what to do?
   Failures:  "Error 403" without explanation
              "Something went wrong" with no guidance
              "Invalid input" without specifying which field or what's invalid

10. HELP AND DOCUMENTATION
    Principle: Even good design sometimes needs documentation.
    Questions: Is help available when needed?
               Is contextual help available without leaving the task?
    Failures:  Help only accessible via separate documentation site
               No tooltips, no inline hints, no contextual guidance
               Empty onboarding with no guidance on first use
```

---

## 17.2 DESIGN CRITIQUE: THE VICES FRAMEWORK

Use this structured framework for evaluating any design:

```
V — VISUAL HIERARCHY
  Can the primary element be identified in 3 seconds or less?
  Is there exactly ONE maximum-weight element?
  Does visual weight match information importance?
  Test: Cover everything except each element — does it "deserve" its weight?

I — INFORMATION LOAD
  Is there anything that can be removed without loss of value?
  Is the cognitive load appropriate for the user's expertise level?
  Does every element on screen earn its place?
  Test: Remove each element — does anything important disappear?

C — CONSISTENCY
  Are patterns repeated reliably across the interface?
  Do similar components behave the same way everywhere?
  Does the system feel coherent or patched together?
  Test: Would a user expect X to work the same way in a different context?

E — EFFORT / FRICTION
  How many steps to complete the primary task?
  Are there any unnecessary steps?
  What is the cognitive cost of the most common workflow?
  Test: Time yourself completing the primary task. Every second of confusion costs.

S — SPACE
  Is whitespace used as a design tool or just leftover area?
  Does spacing create appropriate grouping?
  Are breathing room and density appropriate for the user type?
  Test: Reduce all whitespace by 50% — does meaning change?
```

---

## 17.3 THE 5-SECOND TEST

Show the design to someone for exactly 5 seconds. Then ask:
1. What is this page for?
2. What is the most important thing on this page?
3. What can you do here?

If they cannot answer all three correctly → the design has failed its primary job.

Run this test BEFORE investing in full visual design. It's free, fast, and reveals fundamental hierarchy failures.

---

## 17.4 UX METRICS

```
TASK-BASED METRICS:
  Task completion rate:   % of users who successfully complete the primary task
                          Target: > 90% for critical flows
  Time-on-task:           How long to complete the task?
                          Benchmark against prior version or competitor
  Error rate:             Number of mistakes per task
                          Target: < 1 unintentional error per session on primary flow
  Learnability:           Does completion rate improve with repeated use?

SATISFACTION METRICS:
  NPS (Net Promoter Score):
    "How likely are you to recommend [product] to a colleague?" (0–10)
    Score: % Promoters (9–10) minus % Detractors (0–6)
    Benchmark: >50 = excellent, 30–50 = good, 0–30 = needs work

  CSAT (Customer Satisfaction Score):
    "How satisfied are you with [feature/experience]?" (1–5 stars or 1–7 scale)
    Best for: Post-task satisfaction, after-support survey
    Benchmark: > 4.0/5 = excellent

  CES (Customer Effort Score):
    "How easy was it to [accomplish the task]?" (1–7, 7 = very easy)
    BEST predictor of churn — effort predicts loyalty better than satisfaction
    Benchmark: > 5.5/7 = good

BEHAVIORAL METRICS (from analytics):
  Activation rate:    % of signups who reach "Aha! Moment" in first session
  Feature adoption:   % of users who use a key feature at least once
  Retention rate:     % of users returning after day 1, 7, 30
  Drop-off rate:      % abandoning at each step of a critical funnel
  Search rate:        % using site search (high = navigation is failing)
  Error encounter:    % of sessions with validation or system errors
```

---

## 17.5 A/B TESTING FOR UI DESIGN

```
WHEN TO A/B TEST:
  ✓ High-traffic pages with clear conversion goals
  ✓ Validating between two genuinely different approaches
  ✓ Confirming quantitative impact of a UX improvement
  ✗ Not: Testing color preferences (low signal, high noise)
  ✗ Not: When sample size is too small (< 1000 visitors/variation for significance)

WHAT TO TEST (highest ROI order):
  1. Headline copy
  2. CTA button text
  3. CTA placement (above vs. below fold)
  4. Social proof type and position
  5. Form field count
  6. Number of steps in checkout
  7. Page length / content depth

STATISTICAL RIGOR:
  Minimum significance: 95% confidence before declaring winner
  Minimum runtime: 2 business cycle periods (often 2 weeks minimum)
  Single variable: Only change ONE thing between variants
  Define success metric BEFORE starting (not after seeing results)
  Segment: Check if result holds across mobile/desktop, new/returning users

PITFALLS:
  Peeking early: Don't stop test at first significant result — wait for full runtime
  Multiple testing: Every additional variant increases false-positive risk
  Novelty effect: New design may win short-term but fade — run until stable
  Sample pollution: Ensure variants are truly independent (no crossover)
```

---

# SECTION 18: OUTPUT FORMAT GUIDE

---

## 18.1 CHOOSING THE RIGHT DELIVERABLE

Match deliverable format to the nature of the request:

```
REQUEST TYPE                     →  DELIVERABLE FORMAT
─────────────────────────────────────────────────────────────────────
Layout structure / wireframe     →  ASCII wireframe + annotated explanation
Full UI design                   →  React JSX or HTML/CSS artifact
Component design                 →  React component with all states
Design critique                  →  VICES framework analysis + recommendations
Color palette                    →  Named palette with hex, usage rules, contrast ratios
Typography system                →  Scale table + pairing rationale + usage examples
Component spec                   →  State-by-state breakdown with values and behaviors
User flow                        →  Mermaid flowchart + decision point annotations
Design system                    →  Token tables + component catalog + guidelines
Mobile screen                    →  Device-framed React/HTML artifact
Information architecture         →  Structured hierarchy diagram + navigation logic
Onboarding flow                  →  Step-by-step wireframes + copy + logic
Dashboard design                 →  React artifact with sample data + chart selection
Animation spec                   →  CSS/JS code + timing rationale
Full design spec document        →  Markdown: specs + wireframes + component breakdown
─────────────────────────────────────────────────────────────────────
```

---

## 18.2 WHEN BUILDING HTML/CSS OR REACT ARTIFACTS

Always apply these principles to every artifact produced:

```
VISUAL HIERARCHY:
  → ONE maximum-weight element per section
  → Correct use of spacing tokens (multiples of 4/8)
  → Appropriate density for user type
  → Color used semantically (not decoratively)

INTERACTIVE STATES:
  → EVERY interactive element has hover, focus, active, disabled states in CSS
  → Focus indicators ALWAYS visible (never outline:none without replacement)
  → Loading states implemented for async actions

RESPONSIVE:
  → Default: Mobile-first CSS, responsive unless explicitly scoped to one platform
  → Breakpoints: xs/sm/md/lg/xl following the system in §2.5

SEMANTIC HTML:
  → <nav>, <main>, <section>, <article>, <aside>, <footer>, <header>
  → Heading hierarchy: h1 → h2 → h3 (never skip levels)
  → Buttons for actions, links for navigation (not interchangeable)
  → Form labels associated with inputs (htmlFor or aria-labelledby)

CONTENT:
  → NEVER placeholder gray boxes — use realistic representative content
  → Representative variety: short and long text variants, edge cases shown
  → Real human names, realistic data, appropriate amounts of content

ACCESSIBILITY:
  → ARIA labels on icon-only buttons
  → Alt text on all images
  → Color contrast always passing WCAG AA minimum
```

---

## 18.3 ASCII WIREFRAME FORMAT

Use this format for quick structural communication:

```
DESKTOP (1280px):
┌──────────────────────────────────────────────────────────┐
│ [LOGO]          Nav Item  Nav Item  Nav Item  [CTA]      │  ← Header/Nav
├──────────────────────────────────────────────────────────┤
│                                                          │
│  [H1 Headline — outcome-focused statement]              │  ← Hero
│  Subheadline context sentence (1 line)                  │
│  [Primary CTA]  [Secondary CTA]                         │
│                                  [Hero Image/Visual]    │
├──────────────────────────────────────────────────────────┤
│  [Feature 1]    [Feature 2]    [Feature 3]              │  ← Feature section
│  Icon + title   Icon + title   Icon + title             │
│  Description    Description    Description              │
└──────────────────────────────────────────────────────────┘

MOBILE (390px) — same section:
┌─────────────────┐
│ [LOGO]    [≡]   │  ← Mobile nav with hamburger
├─────────────────┤
│ [Hero Image]    │  ← Image first on mobile
│                 │
│ H1 Headline     │  ← Content below
│ Subheadline     │
│ [Primary CTA]   │  ← Full-width CTA on mobile
│ [Secondary CTA] │
├─────────────────┤
│ [Feature 1]     │  ← Single column on mobile
│ [Feature 2]     │
│ [Feature 3]     │
└─────────────────┘

ANNOTATIONS:
  ← Always explain design decisions adjacent to structure
  → Not just WHAT it is, but WHY this layout serves the user
```

---

# SECTION 19: ANTI-PATTERNS

Never do these. They are tested, confirmed UX failures.

```
HIERARCHY & LAYOUT:
  ✗ Multiple competing primary CTAs (two "primary" buttons destroy hierarchy)
  ✗ Hamburger menu for primary navigation on desktop (buries critical paths)
  ✗ Centering body text on large screens (horrible readability past 60ch)
  ✗ Auto-advancing carousels (users are reading; you're interrupting)
  ✗ Infinite scroll when users need to return to a specific item (no anchor)
  ✗ Infinite scroll + footer (footer is permanently unreachable)
  ✗ Modal-on-modal stacking (user is now cognitively lost)
  ✗ Horizontal scrolling on mobile without explicit affordance (swipe context)

FORMS:
  ✗ Placeholder text as the ONLY label (disappears on focus — accessibility failure)
  ✗ "Submit" as button label (what will happen? be specific)
  ✗ Generic "OK" for confirmation dialog (specify the action: "Delete Project")
  ✗ Disabling submit button without visible reason (why is it disabled?)
  ✗ Validating email format while user is still typing (premature frustration)
  ✗ Clearing form data on validation error (catastrophic for long forms)
  ✗ Asking for unnecessary information (every extra field drops completion ~10%)
  ✗ Disabling paste on password fields (breaks password managers)

VISUAL DESIGN:
  ✗ Using color as the ONLY differentiator (color blindness affects 8% of males)
  ✗ Light grey text on white background (#999/#aaa on #fff fails WCAG)
  ✗ Pure black (#000) on pure white (#fff) for body text (too harsh — use #111 on #fafafa)
  ✗ Pure white backgrounds in dark mode (#000000 — too harsh)
  ✗ Tooltips on mobile (no hover = permanently hidden content)
  ✗ Every word bold (nothing is emphasized when everything is emphasized)
  ✗ 3D charts for data visualization (always distorts perception)
  ✗ Pie charts with >5 segments (impossible to compare slice sizes)

INTERACTION:
  ✗ Removing iOS back-swipe gesture (violates platform contract, loses trust)
  ✗ Sound effects by default (plays in public, immediately disabled, user uninstalls)
  ✗ Auto-playing video with sound (same outcome as above)
  ✗ Requiring login before showing any value (show value first, gate later)
  ✗ Requiring email verification before any product use (high drop-off point)
  ✗ Showing loading spinner for < 100ms operations (spinner is jarring, not helpful)
  ✗ 3-second+ page load with no progress indicator (user thinks it crashed)
  ✗ Confirm dialogs for easily-reversible actions ("Are you sure you want to log out?")

DARK PATTERNS (unethical — never implement):
  ✗ Roach motel: Easy to sign up, impossible to cancel
  ✗ Disguised ads: Sponsored content styled to look like organic results
  ✗ Confirmshaming: "No thanks, I don't want to save money"
  ✗ Misdirection: Focus attention away from the right choice
  ✗ Hidden costs: Revealing fees at the final checkout step
  ✗ Cookie banner reject buried 3 layers deep while Accept is one click
  ✗ Pre-checked boxes for marketing consent
  ✗ Trick questions: Double negatives in privacy settings
```

---

# SECTION 20: QUICK DECISION TREES

---

## COMPONENT DECISIONS

**"Should this be a modal or a new page?"**
- **Modal:** Small content, quick action, user needs current context
- **New page:** Complex form, multi-step, shareable URL needed, substantial content, settings

**"Should this be a card or a list row?"**
- **Card:** Visual content matters, items are comparable, grid browse mode
- **List row:** Scanning by one attribute, dense data, sequential reading, tabular comparison

**"Where should the primary CTA go?"**
- Always visible — never buried below the fold on landing pages
- After value proposition — never before user understands what they're signing up for
- Isolated — whitespace around it, no competing elements nearby

**"Should I use tabs or a sidebar?"**
- **Tabs:** Parallel content, same hierarchy level, ≤7 items, content comparison
- **Sidebar:** Deep hierarchy, many items, frequent switching, power-user context

**"Is this an error, warning, or info?"**
- **Error (red):** Something failed, data lost, action blocked, user needs to act NOW
- **Warning (amber):** Action could cause a problem, something may fail, user should be aware
- **Info (blue):** Neutral context, helpful information, nothing requires action

**"Should I use skeleton loading or a spinner?"**
- **Skeleton:** Content shape is predictable, loading 300ms+, list/card/page content
- **Spinner:** Short actions < 2s, small/unknown area, button loading state
- **Progress bar:** Duration is predictable (file upload, multi-step process)

---

## NAVIGATION DECISIONS

**"How many nav items is too many?"**
- Top nav: 7 items maximum before cognitive overload
- Bottom tab (mobile): 5 items maximum — every item must be a primary destination
- Sidebar: Can have more, but group with section headers at > 10 items

**"Does this belong in primary nav or settings?"**
- Primary nav: Destinations users visit frequently (daily/weekly)
- Settings: Configuration that users set once or rarely change

---

## FORM DECISIONS

**"Required or optional field marking?"**
- > 90% of fields required → Mark only OPTIONAL fields
- Many optional fields → Mark only REQUIRED fields
- Never mark both → pick the minority to label

**"Validation on change or on blur?"**
- On change: Password strength ONLY
- On blur: All other format/presence validation
- On submit: Full validation, show ALL errors at once

---

## DESIGN SYSTEM DECISIONS

**"Should this be a new component or a variant?"**
- New component: Structurally different, different ARIA role, fundamentally different purpose
- Variant: Same structure, same role, different visual presentation (size, color, outline vs. fill)

**"Token or hardcoded value?"**
- Token: Any value that might need to change globally or per theme
- Hardcoded: Never — if it could ever need to change, it needs a token

---

# QUICK REFERENCE: DESIGN LAWS CHEAT SHEET

```
HICK'S LAW:         More choices = slower decisions. Reduce options ruthlessly.
FITTS'S LAW:        Larger + closer = faster to hit. Big CTAs. Small destructive actions.
MILLER'S LAW:       Working memory holds 7±2 items. Group related content.
JAKOB'S LAW:        Users expect your site to work like all the others they know.
DOHERTY THRESHOLD:  Interactions > 400ms feel slow. Aim for < 100ms visual feedback.
PEAK-END RULE:      Users remember the worst moment and the final moment. Fix errors.
GESTALT PROXIMITY:  Close elements = related. Use spacing to group, not just borders.
GESTALT SIMILARITY: Similar appearance = same category. Break it intentionally for hierarchy.
ZEIGARNIK EFFECT:   Incomplete tasks remembered better. Use progress bars strategically.
AESTHETIC-USABILITY:Beautiful interfaces get more patience. Beauty supplements usability.
```

---

# DESIGN PRINCIPLES AT A GLANCE

```
ONE PRIMARY ACTION per screen (Law of One Thing)
PROGRESSIVE DISCLOSURE — reveal complexity on demand
ZERO FRICTION — every step costs the user energy; spend it wisely
FEEDBACK for every action — users must know their action was received
RECOGNITION over recall — show options, don't require memory
FORGIVENESS — undo, cancel, confirm before irreversible
CONSISTENCY — same things look and work the same everywhere
ACCESSIBILITY — design for everyone, including the 20% with disabilities
PERFORMANCE — speed is a feature; latency is UX debt
HONESTY — dark patterns destroy trust permanently
```

