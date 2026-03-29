---
name: ultimate-ui-ux-design
description: >
  Master-level UI/UX Design expertise for creating exceptional digital experiences across all platforms.
  Specializes in strategic design thinking, information architecture, interaction design, visual systems,
  and platform-specific patterns (Web, Mobile iOS/Android, Desktop, Embedded Systems, Portals, Enterprise Software).
  Guides users through the complete design lifecycle from research to high-fidelity prototypes with
  psychological precision and business acumen. Handles responsive design, design systems, accessibility (WCAG),
  micro-interactions, and conversion optimization. NOT a graphic design or illustration tool—focuses on
  functional, user-centered interface architecture and experience strategy.
---

# Ultimate UI/UX Design Mastery

## Design Philosophy

UI/UX Design is the alchemy of **clarity**, **efficiency**, and **emotion**. The greatest challenge isn't adding features—it's deciding what to remove while maintaining power. Every pixel serves a purpose; every interaction tells a story.

### Core Principles

1. **Cognitive Load Management**: Never make users think. Reduce mental processing to instinct.
2. **Progressive Disclosure**: Reveal complexity only when needed. Layer information hierarchically.
3. **Affordance & Signifiers**: Every element must communicate its function without explanation.
4. **Consistency & Standards**: Leverage mental models. Deviations must be 10x better to justify breaking conventions.
5. **Feedback Loops**: Every action requires immediate, clear response (0.1s for instant, 1s for flow, 10s for progress).
6. **Error Prevention > Error Recovery**: Design so users cannot make mistakes, rather than helping them recover.
7. **Aesthetic-Usability Effect**: Beautiful interfaces are perceived as more usable—invest in visual polish.

---

## Platform-Specific Design Architecture

### 1. Web Applications (SaaS/Enterprise)

**Characteristics**: Complex workflows, data density, extended sessions, multi-tab behavior

**Design Strategy**:
- **Z-Pattern & F-Pattern**: Place CTAs along natural reading paths
- **Persistent Navigation**: Sticky headers with command palettes (Cmd+K) for power users
- **Data Density Gradients**: Dashboard → Detail → Edit (progressive complexity)
- **Responsive Breakpoints**: 
  - Mobile: <640px (single column, hamburger menu)
  - Tablet: 640-1024px (sidebar collapses, touch targets 44px+)
  - Desktop: 1024-1440px (optimal reading width 75ch, multi-pane)
  - Ultra-wide: >1440px (fluid grids, max-width containers)

**Key Patterns**:
- **Command Palette**: Universal search + action shortcuts
- **Breadcrumb Navigation**: Deep hierarchy wayfinding
- **Data Tables**: Sortable, filterable, column customization, sticky headers
- **Modal Layering**: Z-index management (Backdrop: 40, Modal: 50, Toast: 60, Tooltip: 70)
- **Auto-save Patterns**: Ghost indicators, conflict resolution UI

### 2. Mobile Applications (iOS & Android)

**iOS Design Language (Human Interface Guidelines)**:
- **Navigation**: Tab bars (primary), Navigation bars (hierarchical), Modals (self-contained tasks)
- **System Components**: SF Symbols, San Francisco font family, vibrancy effects
- **Interaction Model**: Direct manipulation, edge swipes, haptic feedback
- **Safe Areas**: Respect notch, home indicator, and status bar insets
- **Typography**: Dynamic Type support (scaling from 11pt to 53pt)

**Android Design Language (Material Design 3)**:
- **Navigation**: Navigation bar (primary), Navigation rail (large screens), Modal navigation drawer
- **System Components**: Material Symbols, Roboto/Roboto Flex, elevation shadows
- **Interaction Model**: Ripple effects, floating action buttons (FAB), snackbars
- **Foldables**: Multi-window states, continuity across screen changes

**Mobile-First Principles**:
- **Thumb Zone Mapping**: Primary actions in green zone (bottom 25%), destructive actions in red zone (top corners)
- **Touch Targets**: Minimum 44×44pt (iOS) or 48×48dp (Android)
- **Gestures**: Standardize (Swipe right = back/complete, Swipe left = actions, Pinch = zoom, Pull = refresh)
- **Bottom Sheets**: Mobile-native alternative to modals for complex selections
- **Skeleton Screens**: Perceived performance during loading (never use spinners for content)

### 3. Desktop Applications (macOS/Windows/Linux)

**Characteristics**: Power user features, keyboard shortcuts, window management, file system integration

**macOS**:
- **Human Interface**: Translucency, vibrancy, unified toolbar/search field
- **Window Management**: Sheets (document-modal), drawers (utility panels), full-screen optimization
- **Typography**: San Francisco, system font scaling
- **Shortcuts**: Cmd-based, menu bar integration, Touch Bar support (legacy)

**Windows**:
- **Fluent Design**: Acrylic material, reveal highlight, connected animations
- **Navigation**: NavigationView (top/left), CommandBar, teaching tips
- **Input**: Mouse precision (1px), keyboard accelerators (Alt+mnemonics), pen/touch hybrid
- **Windowing**: Snap layouts, multiple instances, title bar customization

**Cross-Desktop Patterns**:
- **Menu Bars**: File/Edit/View standards, context menus for right-click
- **Toolbars**: Customizable iconography, overflow handling
- **Keyboard Shortcuts**: Mnemonic consistency (Ctrl/Cmd+S, Ctrl/Cmd+Z, etc.)
- **Drag & Drop**: Visual feedback, ghost representations, drop zones
- **System Tray/Dock**: Background operation indicators, quick actions

### 4. Enterprise Software & Portals

**Characteristics**: Role-based access, workflow automation, high data volume, compliance requirements

**Design Approach**:
- **Role-Based Dashboards**: Admin, Manager, Operator views with permission-gated features
- **Workflow Visualization**: Step indicators, decision trees, approval chains
- **Data Grids**: Advanced filtering (facet search), bulk actions, inline editing
- **Audit Trails**: Version history, change tracking, undo capabilities
- **Help Integration**: Contextual tooltips, guided tours, inline documentation

**Enterprise Patterns**:
- **Master-Detail Views**: List selection updates detail pane without page reload
- **Configuration Wizards**: Step validation, progress saving, rollback points
- **Bulk Operations**: Selection checkboxes, action toolbars, confirmation dialogs for destructive actions
- **Advanced Search**: Query builders, saved filters, recent searches
- **Reporting Interfaces**: Date range selectors, export options, scheduled reports

### 5. Embedded Systems & Kiosks

**Characteristics**: Single-purpose, high contrast, touch-first, environmental constraints

**Design Constraints**:
- **High Contrast**: 4.5:1 minimum contrast ratio (WCAG AA), outdoor visibility
- **Large Touch Targets**: 60×60px minimum for industrial gloves
- **Simplified Navigation**: Flat information architecture, maximum 3 levels deep
- **Feedback**: Audio + visual + haptic for critical actions
- **Error Recovery**: Automatic reset to home screen after timeout

---

## Information Architecture (IA)

### The Architecture of Understanding

**Card Sorting Methodologies**:
- **Open Card Sorting**: Discover user mental models (labeling)
- **Closed Card Sorting**: Validate existing structures
- **Hybrid Card Sorting**: Combination for iterative refinement

**Navigation Patterns**:
- **Global Navigation**: Persistent, high-level sections (top bar or sidebar)
- **Local Navigation**: Contextual to current section (sub-menus, tabs)
- **Contextual Navigation**: Related content, "See also" links, smart recommendations
- **Utility Navigation**: User profile, settings, help (top-right convention)

**Content Organization**:
- **Hierarchical**: Tree structure (categories → subcategories → items)
- **Sequential**: Linear flows (checkout, onboarding, wizards)
- **Matrix**: Cross-referenced categories (filterable catalogs)
- **Organic**: Tag-based, associative (knowledge bases, blogs)

**Search Architecture**:
- **Search Scopes**: Global vs. contextual (current folder/category)
- **Auto-suggest**: Typo tolerance, synonyms, recent searches
- **Faceted Search**: Multi-dimensional filtering (Amazon-style sidebar)
- **Zero Results Pages**: Alternative suggestions, contact options, broadened criteria

---

## Interaction Design (IxD)

### The 5 Dimensions of Interaction

1. **Words**: Text buttons, labels—should be clear, actionable ("Save Changes" not "Submit")
2. **Visual Representations**: Icons, typography, spacing—universal recognition
3. **Physical Objects**: Device input methods (mouse, finger, stylus, voice)
4. **Time**: Motion, sound, feedback loops—temporal context
5. **Behavior**: Actions and reactions—system state changes

### Micro-interactions

**Trigger → Rules → Feedback → Loops & Modes**

**Essential Micro-interactions**:
- **Button States**: Default → Hover → Active → Loading → Success/Error
- **Input Validation**: Inline validation (on blur), password strength, format hints
- **Toggle Switches**: Immediate state change, clear on/off signification
- **Loading States**: Skeleton screens > spinners > progress bars (for >10s operations)
- **Toast Notifications**: Non-intrusive feedback, auto-dismiss (5s), action undo
- **Pull-to-Refresh**: Visual elasticity, release threshold, success haptic

### State Management

**Empty States**: 
- Zero data (first use): Welcome illustration + primary CTA + educational context
- Zero results (search/filter): Alternative suggestions + reset options
- Zero permission: Upgrade prompt or access request

**Error States**:
- **404**: Apologetic tone, search bar, popular links, home button
- **500**: Technical honesty, retry mechanism, support contact
- **Form Errors**: Inline indicators, field-level messages, summary at top
- **Network Errors**: Offline mode UI, retry queues, sync status

**Loading States**:
- **Instant (<100ms)**: No feedback needed
- **Fast (100ms-1s)**: Subtle transition, cursor change
- **Moderate (1-10s)**: Progress indicators, skeleton screens
- **Slow (>10s)**: Percentage progress, cancel option, estimated time

---

## Visual Design Systems

### Typography

**Type Scale (Major Third - 1.25 ratio)**:
- **Hero**: 48-72px (Marketing headlines)
- **H1**: 38px (Page titles)
- **H2**: 31px (Section headers)
- **H3**: 25px (Card titles)
- **H4**: 20px (Widget headers)
- **Body**: 16px (Primary content)
- **Small**: 13px (Captions, metadata)
- **Tiny**: 10px (Legal, timestamps)

**Line Heights**:
- Headings: 1.2 (tight)
- Body: 1.5-1.6 (readable)
- Captions: 1.4 (compact)

**Font Selection**:
- **Sans-serif**: UI elements, modern brands (Inter, SF Pro, Roboto)
- **Serif**: Long-form reading, editorial (Merriweather, Georgia)
- **Monospace**: Code, data tables (SF Mono, JetBrains Mono)

### Color Systems

**Primary Palette**: Brand color (60% of UI)
**Secondary Palette**: Accent actions (30% of UI)
**Neutral Palette**: Text, backgrounds, borders (10% of UI)

**Semantic Colors**:
- **Success**: Green hues (4.5:1 contrast on white)
- **Warning**: Orange/Amber (not red-green colorblind safe with error)
- **Error**: Red family, high contrast
- **Info**: Blue family, calming
- **Neutral**: Gray scale for non-emphasis

**Color Application**:
- **Background Layers**: Surface (base), Elevated (cards), Overlay (modals)
- **Text Hierarchy**: Primary (87% opacity), Secondary (60%), Disabled (38%)
- **Border Hierarchy**: Strong (dividers), Subtle (hover states), Ghost (layout guides)

### Spacing Systems (8-Point Grid)

**Base Unit**: 8px
- **4px**: Tight internal spacing, icon padding
- **8px**: Default element separation
- **16px**: Section padding, card internal spacing
- **24px**: Section breaks, form group spacing
- **32px**: Major section divisions
- **48px**: Page-level vertical rhythm
- **64px+**: Hero sections, major breaks

### Iconography

**System Icons**: 24×24px default, 1-2px stroke, 2px corner radius
**Product Icons**: 48×48px, filled style, brand color
**Platform Alignment**: Use SF Symbols (iOS), Material Icons (Android), Fluent Icons (Windows)

**Icon Usage Rules**:
- Always pair with text labels (unless universally recognized: Home, Search, Print)
- Maintain consistent stroke weight within sets
- Use filled variants for selected states
- Accessibility: aria-label or title tags for screen readers

---

## Design Systems & Component Libraries

### Atomic Design Methodology

1. **Atoms**: Colors, typography, spacing, icons (design tokens)
2. **Molecules**: Buttons, inputs, labels (simple components)
3. **Organisms**: Cards, navigation bars, forms (complex components)
4. **Templates**: Page layouts, wireframes (structure)
5. **Pages**: Real content, final UI (instances)

### Component Documentation

Each component requires:
- **Usage Guidelines**: When to use, when NOT to use
- **Anatomy**: Visual breakdown of parts
- **States**: Default, hover, active, disabled, loading, error
- **Variants**: Sizes, styles, configurations
- **Accessibility**: Keyboard navigation, ARIA labels, screen reader behavior
- **Code**: Props, events, methods
- **Examples**: Common use cases, edge cases

### Design Tokens

**Global Tokens**: Brand colors, typography scale, spacing scale (platform-agnostic)
**Alias Tokens**: Semantic names (primary-color, border-radius-large)
**Component Tokens**: Button-specific, card-specific values

**Token Format**:
```json
{
  "color": {
    "primary": {
      "base": { "value": "#007AFF" },
      "hover": { "value": "#0056B3" },
      "disabled": { "value": "rgba(0,122,255,0.3)" }
    }
  },
  "spacing": {
    "xs": { "value": "4px" },
    "sm": { "value": "8px" },
    "md": { "value": "16px" }
  }
}
```

---

## User Psychology & Behavioral Design

### Cognitive Biases in UX

- **Hick's Law**: Reduce choices to speed decision-making
- **Fitts's Law**: Larger, closer targets are faster to reach
- **Jakob's Law**: Users spend 90% time on other sites—follow conventions
- **Miller's Law**: 7±2 items in working memory (chunk information)
- **Peak-End Rule**: Users remember the peak experience and the ending
- **Von Restorff Effect**: Isolated items are more likely remembered (CTAs)

### Behavioral Economics

- **Loss Aversion**: Frame features as "Don't lose progress" vs "Save progress"
- **Anchoring**: Show original price before discount
- **Social Proof**: User counts, ratings, testimonials near CTAs
- **Scarcity**: Limited availability indicators (truthful only)
- **Default Effect**: Pre-select the benign/safe option

### Flow States

**Achieving Flow**:
- Clear goals with immediate feedback
- Balance between challenge and skill
- Sense of control
- Distraction elimination

**Gamification Elements**:
- **Progress Indicators**: Checklists, completion percentages
- **Achievements**: Badges for milestones (meaningful only)
- **Streaks**: Consistency rewards
- **Leaderboards**: Social comparison (use cautiously)

---

## Accessibility (A11y) & Inclusive Design

### WCAG 2.1 Compliance

**Level A (Essential)**:
- Text alternatives for images
- Keyboard accessible
- Captions for video
- Color not sole information carrier

**Level AA (Industry Standard)**:
- Contrast ratio 4.5:1 for normal text
- 3:1 for large text (18pt+) and UI components
- Resizable text up to 200%
- Consistent navigation

**Level AAA (Enhanced)**:
- Contrast ratio 7:1 for normal text
- Sign language interpretation
- Extended audio descriptions

### Screen Reader Optimization

**ARIA Labels**:
- `aria-label`: Descriptive name for interactive elements
- `aria-describedby`: Additional context for complex controls
- `aria-live`: Announce dynamic content changes (polite vs assertive)
- `aria-expanded`: State of collapsible content
- `aria-hidden`: Hide decorative elements from readers

**Semantic HTML**:
- Use `<nav>`, `<main>`, `<article>`, `<aside>` over generic `<div>`
- Heading hierarchy (h1→h2→h3) without skipping levels
- `<button>` for actions, `<a>` for navigation
- `<label>` associated with every form input

**Keyboard Navigation**:
- Tab order follows visual order (logical flow)
- Focus indicators visible (2px outline minimum)
- Escape key closes modals/dropdowns
- Space/Enter activates buttons, arrows navigate lists

### Inclusive Design Considerations

- **Motor Disabilities**: Large touch targets, gesture alternatives
- **Cognitive Disabilities**: Simple language, consistent patterns, error prevention
- **Visual Impairments**: Screen reader support, high contrast modes, scalable text
- **Hearing Impairments**: Transcripts, visual alerts, haptic feedback
- **Photosensitive Epilepsy**: No flashing >3Hz, reduce motion option

---

## Responsive & Adaptive Design

### Breakpoint Strategy

**Mobile-First Approach**:
```css
/* Base: Mobile */
.container { width: 100%; padding: 16px; }

/* Tablet */
@media (min-width: 768px) {
  .container { max-width: 720px; margin: 0 auto; }
}

/* Desktop */
@media (min-width: 1024px) {
  .container { max-width: 960px; display: grid; grid-template-columns: 2fr 1fr; }
}

/* Large Desktop */
@media (min-width: 1440px) {
  .container { max-width: 1200px; }
}
```

**Content-Based Breakpoints**: Break when design breaks, not at device widths

### Layout Patterns

**Responsive Patterns**:
- **Mostly Fluid**: Percentage-based widths, reflow at breakpoints
- **Column Drop**: Stack columns vertically on narrow screens
- **Layout Shifter**: Radically different layouts per breakpoint
- **Off-Canvas**: Hidden navigation revealed via toggle on mobile

**Images**:
- Responsive images (`srcset`, `sizes`) for resolution switching
- Art direction (`picture` element) for crop variations
- Vector graphics (SVG) for icons and illustrations

---

## UX Research & Validation

### Research Methods

**Generative (Discover)**:
- **User Interviews**: 1:1 deep dives, open-ended questions
- **Ethnographic Studies**: Contextual inquiry in user's environment
- **Diary Studies**: Longitudinal behavior tracking
- **Card Sorting**: Information architecture validation

**Evaluative (Test)**:
- **Usability Testing**: Task-based, think-aloud protocol
- **A/B Testing**: Statistical comparison of variants
- **First-Click Testing**: Navigation efficiency measurement
- **Eye-Tracking**: Visual attention heatmaps
- **Tree Testing**: IA findability without visual design

### Metrics & KPIs

**Behavioral Metrics**:
- **Task Success Rate**: % of users completing tasks
- **Time on Task**: Efficiency measurement
- **Error Rate**: Mistakes per task
- **Abandonment Rate**: Drop-off at specific steps

**Attitudinal Metrics**:
- **System Usability Scale (SUS)**: Standardized 10-question survey
- **Net Promoter Score (NPS)**: Loyalty measurement
- **Customer Satisfaction (CSAT)**: Immediate feedback
- **User Experience Questionnaire (UEQ)**: Modular assessment

### Heuristic Evaluation

**Nielsen's 10 Heuristics**:
1. Visibility of system status
2. Match between system and real world
3. User control and freedom (undo/redo)
4. Consistency and standards
5. Error prevention
6. Recognition rather than recall
7. Flexibility and efficiency (shortcuts)
8. Aesthetic and minimalist design
9. Help users recognize, diagnose, recover from errors
10. Help and documentation

---

## Prototyping & Handoff

### Fidelity Spectrum

**Low-Fidelity (Wireframes)**:
- Grayscale, placeholder content
- Focus on layout and hierarchy
- Rapid iteration, sketching
- Tools: Balsamiq, paper, Whimsical

**Mid-Fidelity**:
- Basic color, real content
- Interactions defined
- User testing ready
- Tools: Figma, Sketch, Adobe XD

**High-Fidelity (Pixel-Perfect)**:
- Production-ready visuals
- Micro-interactions animated
- Developer handoff specifications
- Tools: Figma (Dev Mode), Principle, ProtoPie

### Design Handoff Essentials

**Developer Specifications**:
- Exact spacing values (margin, padding)
- Typography: Font family, weight, size, line-height, letter-spacing
- Colors: Hex/RGBA values, opacity states
- Assets: Export @1x, @2x, @3x, SVG for vectors
- Interactions: Easing curves, duration (ms), triggers

**Documentation**:
- Redlining removed (use Figma Dev Mode)
- Component behavior specifications
- Edge cases and error states
- Responsive behavior rules

---

## AI-Augmented Design Practices

### Leveraging AI in UX

**Generative UI**:
- Use AI for rapid concept generation
- Maintain human oversight for final decisions
- Validate AI suggestions against usability heuristics

**Personalization**:
- Adaptive interfaces based on user behavior patterns
- Predictive next-actions (smart defaults)
- Dynamic content ordering by relevance

**Content Strategy**:
- AI-generated placeholder text (structured)
- Microcopy optimization for clarity
- Multi-language localization assistance

**Accessibility**:
- Automated contrast checking
- Alt-text generation for images
- Semantic structure validation

### AI Interface Patterns

**Conversational UI**:
- Chat interfaces: Message bubbles, typing indicators, suggested replies
- Voice UI: Wake words, confirmation dialogs, visual feedback for audio
- Hybrid: Context-aware switching between GUI and conversational

**AI Transparency**:
- **Confidence Indicators**: "I'm 90% sure..." for uncertain AI responses
- **Source Attribution**: Citations for generated content
- **Human Override**: Easy escape hatches from AI suggestions
- **Learning Indicators**: "Training in progress" for adaptive systems

---

## Cross-Platform Consistency

### Brand Cohesion Across Platforms

**Core Identity**:
- Logo usage consistent but adapted (simplified for favicon, responsive logo)
- Color palette unified with platform-specific accent adjustments
- Typography: Web-safe fallbacks that match brand personality
- Voice & Tone: Consistent microcopy across iOS, Android, Web

**Platform Adaptation**:
- **iOS**: Follow HIG for navigation patterns, use SF Symbols
- **Android**: Material Design components, Roboto typography
- **Web**: Custom design system, responsive flexibility
- **Desktop**: Native menu bars, window controls, shortcuts

### Design-to-Development Workflow

**Version Control**:
- Branching strategies for design (Git for design files)
- Design system versioning (semantic versioning)
- Change logs for component updates

**Collaboration**:
- Design critiques: Structured feedback sessions
- Design QA: Pixel-perfect implementation review
- DesignOps: Automation of repetitive design tasks

---

## Common Anti-Patterns (What NOT to Do)

**Dark Patterns** (Avoid ethically):
- Roach Motel: Easy in, hard out (subscriptions)
- Sneak into Basket: Added items without consent
- Confirmshaming: Guilt-inducing opt-out language
- Dark Patterns in AI: Fake urgency, hidden costs, forced continuity

**Usability Anti-Patterns**:
- Mystery Meat Navigation: Icons without labels
- Carousel/Slider: Hidden content, low engagement
- Infinite Scroll: Lost footer, difficult to find specific items
- Hamburger Menu on Desktop: Hiding primary navigation unnecessarily
- Input Masking: Over-aggressive formatting causing errors
- Autoplay: Video/audio without user initiation
- Pop-up Overlays: Interrupting user flow for non-critical information

**Visual Anti-Patterns**:
- Low Contrast Text: Gray on gray for "aesthetic"
- Overuse of Modals: Disrupting flow for non-urgent actions
- Inconsistent Icons: Mixing filled/outline styles arbitrarily
- Centered Text Blocks: Hard to read beyond 2-3 lines
- Excessive White Space: Scrolling fatigue on content-heavy pages

---

## Design Critique Framework

### The 4 Ls Method

When reviewing designs, evaluate:

1. **Look**: Visual hierarchy, aesthetics, brand alignment
2. **Use**: Usability, task completion efficiency, error prevention
3. **Feel**: Emotional response, delight, trustworthiness
4. **Build**: Technical feasibility, scalability, maintenance

### Articulating Design Decisions

**The Pyramid Principle**:
- **Conclusion First**: "This layout increases conversion by 15%"
- **Supporting Arguments**: "Eye-tracking shows F-pattern reading"
- **Data Evidence**: "Heatmaps indicate drop-off at previous CTA location"

---

## Emergency UX Patterns

**Crisis Mode UI**:
- High-contrast alerts for system failures
- Simplified interfaces for emergency tasks
- Offline mode indicators with queued action visibility

**Data Loss Prevention**:
- Auto-save indicators (Last saved: 2s ago)
- Browser close warnings for unsaved changes
- Session timeout warnings with extend options

---

## Conclusion

Master UI/UX Design requires balancing **user needs**, **business goals**, and **technical constraints**. The ultimate interface is invisible—users accomplish their goals without noticing the design. Strive for intuitive elegance: complex capabilities delivered through simple interactions.

Remember: **Good design is obvious. Great design is transparent.**

## Usage Instructions

When the user requests UI/UX design assistance:

1. **Identify the Platform**: Web, iOS, Android, Desktop, or Embedded
2. **Assess User Context**: Novice vs. Expert users, task criticality
3. **Apply Principles**: Progressive disclosure, cognitive load management
4. **Specify Details**: Exact dimensions, colors, spacing, typography
5. **Address Accessibility**: WCAG compliance, keyboard navigation, screen readers
6. **Provide Rationale**: Explain WHY behind design decisions using psychological principles
7. **Iterate**: Start with low-fidelity, validate, then polish

**Design Checklist**:
- [ ] Information architecture validated
- [ ] 8-point spacing system applied
- [ ] Typography scale established
- [ ] Color contrast checked (4.5:1 minimum)
- [ ] Touch targets 44px/48dp minimum
- [ ] Loading states designed
- [ ] Error states with recovery paths
- [ ] Keyboard navigation tested
- [ ] Responsive breakpoints defined
- [ ] Micro-interactions specified
