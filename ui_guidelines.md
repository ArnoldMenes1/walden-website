# Walden Corp — Design System
> engineering ledger on a midnight canvas

**Theme:** light primary, dark inverted bands
**Version:** 2.0
**Status:** Official reference — binding for all internal and partner work
**Source synthesis:** Linear (hairline precision, surface stepping, single-accent restraint) · Stripe (whisper-weight headings, 4px geometry, no-shadow elevation) · Vercel (monochrome ledger, mono labels, triangle-as-mark discipline) · Raycast (key-tactile surfaces, neutral CTAs, glass nav) · Framer (discipline, card ladder, tight tracking) · Spline (atmospheric restraint, generous whitespace)

> **Contract of use.** This document is the single source of truth for every Walden Corp interface — marketing site, product dashboard, client portal, documentation, emails, and internal tools. Any person, AI agent, designer, developer, or partner producing work for Walden Corp must follow it without exception. When a rule here conflicts with a personal preference, this document wins. When two rules conflict, the more restrictive one wins.

---

## Table of Contents

1. [Brand Personality](#1-brand-personality)
2. [Design Tokens — Colors](#2-design-tokens--colors)
3. [Design Tokens — Typography](#3-design-tokens--typography)
4. [Design Tokens — Spacing, Shapes, Shadows](#4-design-tokens--spacing-shapes-shadows)
5. [Component Library](#5-component-library)
6. [Page Architecture](#6-page-architecture)
7. [Layout](#7-layout)
8. [Motion Guidelines](#8-motion-guidelines)
9. [UX Principles](#9-ux-principles)
10. [Responsive Rules](#10-responsive-rules)
11. [Accessibility](#11-accessibility)
12. [Iconography](#12-iconography)
13. [Illustration Style](#13-illustration-style)
14. [AI-Friendly Rules](#14-ai-friendly-rules)
15. [Do's and Don'ts](#15-dos-and-donts)
16. [Surfaces & Elevation](#16-surfaces--elevation)
17. [Imagery](#17-imagery)
18. [Agent Prompt Guide](#18-agent-prompt-guide)
19. [Similar Brands](#19-similar-brands)
20. [Quick Start — CSS & Tailwind](#20-quick-start--css--tailwind)
21. [Performance, SEO, Voice](#21-performance-seo-voice)
22. [The Walden Rule](#22-the-walden-rule)

---

## 1. Brand Personality

Walden Corp operates as a sober engineering instrument. The page opens on a paper-white canvas (#FFFFFF) with obsidian headings (#1C1C1E) — a light theme by default, honoring the brand charter's "Blanc = Fond." Depth is not cast as shadow but carved as a luminance ledger: white → #FAFAFA → #F2F2F4 → #E5E5E7, with a single midnight blue (#0F2D52) reserved for primary actions, link underlines, focus rings, and the rare accent border. Section rhythm is generous — 96px vertical islands — and content arrives in one of two registers: quiet typographic blocks or full-bleed inverted bands (#1C1C1E) that frame product screenshots and technical moments. There is no neon. There is no chromatic gradient. There is no bouncy motion. Color appears only when something must be acted upon, and even then it is the same midnight blue every time.

### 1.1 Who Walden is

| Trait | What it means in design |
|-------|--------------------------|
| **Premium** | Every detail is finished. No rough edges, no placeholder copy, no lorem ipsum in shipped work. |
| **Sober** | One accent color. One family. One radius per component class. Nothing decorative without purpose. |
| **Modern** | Typography and layout conventions current as of 2024–2026. No dated skeuomorphism, no drop shadows from 2014. |
| **Intelligent** | Information is structured, numbers are surfaced, evidence precedes adjectives. |
| **Elegant** | Generous whitespace. Restraint over ornament. Confidence through emptiness. |
| **Professional** | Dense-but-readable. Text-dominant. No emoji, no exclamations, no marketing exaggeration. |
| **Calm** | Motion is linear and atmospheric. Nothing pulses, nothing bounces, nothing demands attention twice. |
| **Minimalist** | Every element earns its place. If it can be removed, it should be. |
| **Robust** | Components hold their shape at every breakpoint. Nothing breaks under load, translation, or long content. |
| **High quality** | 1px hairlines are exactly 1px. Tracking is consistent. Contrast meets AA. |
| **Enterprise-first** | Designed for buyers who sign contracts, not for viral traffic. Dense data is welcome. |

### 1.2 Who Walden is not

❌ **Flashy** — no neon, no glow-for-glow's-sake, no gradient sweeps
❌ **Cyberpunk** — no terminal-green-on-black cliché, no glitch effects, no scanlines
❌ **Gaming** — no aggressive reds, no RGB, no angular futuristic chrome
❌ **Crypto** — no gold gradients, no 3D coins, no "web3" neon violet
❌ **Startup hype** — no "revolutionary", no "AI-powered", no exclamation marks
❌ **Experimental** — no unreadable type treatments, no scroll-jacking, no asymmetric grids that break the 1200px container
❌ **Corporate-sterile** — no clipart, no stock office photography, no blue-suit handshake imagery

### 1.3 Target perception

When a prospect lands on any Walden surface, within three seconds they should think: **"This company ships production software for serious businesses."** Not: "This is a startup," not "This is an agency," not "This is a tool I could also build myself." The design must speak to CTOs, VPs of Engineering, and procurement teams — people who have seen a hundred SaaS marketing pages and recognize restraint as a signal of competence.

### 1.4 Positioning rule

Walden is an **editor of professional solutions**, not an agency, not an ESN, not a consultancy. The design system must reflect that distinction: every page sells a **product capability** or a **measurable outcome**, never "services", never "our expertise", never "our team" as the hero. The product is the hero. The team is a footnote.

---

## 2. Design Tokens — Colors

| Name | Value | Token | Role |
|------|-------|-------|------|
| Paper | `#ffffff` | `--color-paper` | Default page canvas, card surfaces on light bands — the base the entire system sits on |
| Vellum | `#fafafa` | `--color-vellum` | Section banding, footer background, subtle surface separation without a visible line |
| Mist | `#f2f2f4` | `--color-mist` | Card border ring, hover backgrounds, input wells — the workhorse cool-neutral that divides content |
| Hairline | `#e5e5e7` | `--color-hairline` | 1px borders on cards, buttons, and dividers — visible at close range, invisible at speed |
| Silver | `#c0c0c0` | `--color-silver` | Brand silver — icon strokes on dark bands, disabled text, decorative rules |
| Fog | `#8e8e93` | `--color-fog` | Tertiary body text, placeholder copy, metadata captions |
| Stone | `#6e6e73` | `--color-stone` | Secondary body text, nav labels on light canvas, helper copy — where most reading happens |
| Slate | `#4a4a4e` | `--color-slate` | Body emphasis, dark nav labels, elevated paragraph text |
| Ink | `#2a2a2e` | `--color-ink` | Dark-band card surfaces one step above the inverted canvas |
| Obsidian | `#1c1c1e` | `--color-obsidian` | Primary headings, dark section canvas, inverted card fills — the brand's deep black |
| Carbon | `#0f0f10` | `--color-carbon` | Deepest surface — reserved for image backdrops and footer anchors |
| Bone | `#ffffff` | `--color-bone` | Primary text on dark bands, inverted button fills, the sole light source on obsidian |
| Pearl | `#e5e5e7` | `--color-pearl` | Body text on dark bands, nav labels on inverted sections |
| Midnight | `#0f2d52` | `--color-midnight` | Brand midnight blue — primary CTA fill, link color, focus ring, active nav indicator |
| Midnight Deep | `#0a1e38` | `--color-midnight-deep` | Shadow tint and atmospheric wash beneath midnight blue accents |
| Midnight Lift | `#1e56a0` | `--color-midnight-lift` | Hover state for midnight actions, brighter link accents on dark canvas |
| Midnight Wash | `#eaf0f8` | `--color-midnight-wash` | Lightest midnight tint — subtle section bands, tag pill backgrounds |
| Signal Green | `#2e7d4f` | `--color-signal-green` | Success indicator only — CLI checkmarks, confirmation states. Never a decorative wash |

---

## 3. Design Tokens — Typography

### 3.1 Inter
Sole interface and display typeface. The workhorse. Display sizes (44–64px) sit at weight 500 with aggressive negative tracking (-0.04em to -0.05em) — compressed, confident, still polite. Body sits at weight 400 with neutral tracking and 1.55 line-height for readability. Weights are capped at 600 (the wordmark only); nothing in the system shouts at 700. Substitute: Inter Variable, or system-ui as fallback. · `--font-inter`

- **Weights:** 400, 500, 600
- **Sizes:** 12, 13, 14, 15, 16, 18, 20, 24, 32, 44, 56, 64
- **Line height:** 1.00, 1.10, 1.20, 1.35, 1.50, 1.55, 1.60
- **Letter spacing:** -0.0500em at 64px, -0.0450em at 56px, -0.0400em at 44px, -0.0220em at 32px, -0.0120em at 24px, -0.0080em at 18px, -0.0030em at 16px, normal at 14px and below
- **OpenType features:** `"cv01", "cv05", "cv09", "cv11", "ss03"`, `"tnum"` on numeric blocks

### 3.2 IBM Plex Mono
Technical metadata typeface. Version strings (v1.0.0), deployment hashes, keyboard shortcuts, code blocks, uppercase eyebrow labels at 11–12px. Its slight mechanical warmth contrasts the Inter geometry to signal "this is structural, not prose". Substitute: JetBrains Mono, IBM Plex Mono, ui-monospace. · `--font-plex-mono`

- **Weights:** 400, 500
- **Sizes:** 11, 12, 13, 14
- **Line height:** 1.40, 1.50, 1.60
- **Letter spacing:** 0.0710em at 11px uppercase, 0.0300em at 12px uppercase, normal below
- **OpenType features:** `"tnum", "zero", "ss01"`

### 3.3 Type Scale

| Role | Family | Weight | Size | Line Height | Letter Spacing | Token |
|------|--------|--------|------|-------------|----------------|-------|
| eyebrow | IBM Plex Mono | 500 | 11px | 1.40 | 0.78px | `--text-eyebrow` |
| caption | Inter | 400 | 12px | 1.50 | -0.036px | `--text-caption` |
| body-sm | Inter | 400 | 14px | 1.55 | -0.042px | `--text-body-sm` |
| body | Inter | 400 | 16px | 1.55 | -0.048px | `--text-body` |
| body-lg | Inter | 400 | 18px | 1.50 | -0.144px | `--text-body-lg` |
| subheading | Inter | 500 | 20px | 1.35 | -0.240px | `--text-subheading` |
| heading-sm | Inter | 500 | 24px | 1.20 | -0.288px | `--text-heading-sm` |
| heading | Inter | 500 | 32px | 1.15 | -0.704px | `--text-heading` |
| heading-lg | Inter | 500 | 44px | 1.10 | -1.760px | `--text-heading-lg` |
| display | Inter | 500 | 56px | 1.05 | -2.520px | `--text-display` |
| display-xl | Inter | 500 | 64px | 1.00 | -3.200px | `--text-display-xl` |

---

## 4. Design Tokens — Spacing, Shapes, Shadows

**Base unit:** 4px
**Density:** compact

### 4.1 Spacing Scale

| Name | Value | Token |
|------|-------|-------|
| 4 | 4px | `--spacing-4` |
| 8 | 8px | `--spacing-8` |
| 12 | 12px | `--spacing-12` |
| 16 | 16px | `--spacing-16` |
| 20 | 20px | `--spacing-20` |
| 24 | 24px | `--spacing-24` |
| 32 | 32px | `--spacing-32` |
| 40 | 40px | `--spacing-40` |
| 48 | 48px | `--spacing-48` |
| 64 | 64px | `--spacing-64` |
| 80 | 80px | `--spacing-80` |
| 96 | 96px | `--spacing-96` |
| 128 | 128px | `--spacing-128` |

### 4.2 Border Radius

| Element | Value |
|---------|-------|
| badges | 4px |
| buttons | 6px |
| inputs | 6px |
| cards | 8px |
| largeCards | 12px |
| panels | 16px |
| pills | 9999px |
| iconContainers | 9999px |

### 4.3 Shadows

| Name | Value | Token |
|------|-------|-------|
| hairline | `rgba(0, 0, 0, 0.06) 0px 0px 0px 1px` | `--shadow-hairline` |
| hairline-light | `rgba(255, 255, 255, 0.06) 0px 0px 0px 1px inset` | `--shadow-hairline-light` |
| key | `rgba(255, 255, 255, 0.04) 0px 1px 0px 0px inset, rgba(0, 0, 0, 0.20) 0px -1px 0px 0px inset, rgba(0, 0, 0, 0.06) 0px 0px 0px 1px` | `--shadow-key` |
| card | `rgba(0, 0, 0, 0.04) 0px 1px 2px 0px` | `--shadow-card` |
| floating | `rgba(15, 45, 82, 0.08) 0px 4px 16px 0px` | `--shadow-floating` |
| accent-glow | `rgba(15, 45, 82, 0.20) 0px 4px 12px 0px` | `--shadow-accent-glow` |

### 4.4 Layout Constants

- **Page max-width:** 1200px
- **Section gap:** 96px
- **Card padding:** 32px
- **Element gap:** 12px
- **Nav height:** 64px

---

## 5. Component Library

Every component below is normative. Each entry specifies **description**, **usage**, **variants**, **spacing**, **responsive behavior**, **accessibility**, **do**, and **don't**. AI agents must be able to generate any component from this section alone, without interpretation.

---

### 5.1 Buttons

#### Primary Action Button (Midnight Filled)
**Description:** High-emphasis CTA — the only filled chromatic surface in the system.
**Usage:** Exactly one per view. Hero conversion, form submit, primary modal action.
**Variants:** default / hover / active / focus / disabled / loading.
**Spec:** Background #0F2D52, text #FFFFFF, 6px radius, padding 10px 20px, Inter 14px / weight 500, letter-spacing -0.011em.
**States:** hover → background #1E56A0 + `--shadow-accent-glow`; active → background #0A1E38; focus → 2px #0F2D52 ring offset 2px; disabled → background #C0C0C0, cursor not-allowed; loading → 16px spinner replacing trailing icon, text unchanged.
**Spacing:** vertical stack gap 12px when paired with secondary.
**Responsive:** full-width below 480px.
**Accessibility:** min-height 40px, min touch target 44px on mobile, `aria-disabled` on disabled.
**Do:** pair with a ghost secondary.
**Don't:** place two filled midnight buttons in the same viewport.

#### Neutral Filled Button (Bone Pill)
**Description:** Secondary filled action on dark bands.
**Usage:** Hero on inverted sections, dark-band forms.
**Spec:** Background #FFFFFF, text #1C1C1E, 6px radius, padding 10px 20px, Inter 14px / weight 500.
**States:** hover → background #E5E5E7; active → #C0C0C0.
**Responsive:** full-width below 480px.
**Accessibility:** contrast 15.8:1.

#### Ghost Outline Button
**Description:** Secondary action on light canvas.
**Spec:** Transparent background, text #1C1C1E, 1px #E5E5E7 ring, 6px radius, padding 10px 20px, Inter 14px / weight 500.
**States:** hover → border #C0C0C0, background #FAFAFA.

#### Midnight Ghost Button
**Description:** Secondary action on dark bands.
**Spec:** Transparent background, text #E5E5E7, 1px rgba(255,255,255,0.12) inset ring, 6px radius, padding 10px 20px.
**States:** hover → text #FFFFFF, ring rgba(255,255,255,0.20).

#### Text Link Button
**Description:** Inline action with trailing chevron (›).
**Spec:** No border, no background. Text #0F2D52 at 16px Inter weight 500 with a 14px chevron, 4px offset.
**States:** hover → 1px #0F2D52 underline.

#### Icon Button
**Description:** Compact icon-only action.
**Spec:** 36×36px, 6px radius, transparent background, 1.5px stroke icon at 16px, currentColor.
**States:** hover → background #F2F2F4 (light) / rgba(255,255,255,0.06) (dark).
**Accessibility:** mandatory `aria-label`.

---

### 5.2 Navigation & Chrome

#### Nav Top Bar
**Description:** Global navigation.
**Spec:** Height 64px, background rgba(255,255,255,0.80) + backdrop-filter blur(20px) saturate(180%), 1px hairline bottom border rgba(0,0,0,0.06).
**Structure:** logo left · nav links center-left (14px Inter 400, #6E6E73, 32px gap) · action cluster right (ghost "Sign in" + primary "Start a project").
**Responsive:** <1024px → hamburger, slide-in drawer.
**Accessibility:** `<nav>` landmark, skip-link before it.

#### Sidebar (Dashboard)
**Description:** Persistent left navigation in product surfaces.
**Spec:** Width 240px expanded / 56px collapsed. Background #FAFAFA (light) or #1C1C1E (dark). 1px right hairline border. Items at 14px Inter 500, 10px vertical padding, 12px horizontal, 6px radius, icon 16px.
**States:** hover → #F2F2F4; active → #EAF0F8 with midnight text.
**Responsive:** <1024px → drawer overlay.

#### Topbar (Dashboard)
**Description:** Content-area header inside product surfaces.
**Spec:** Height 56px, background #FFFFFF, 1px bottom hairline. Left: page title 20px Inter 500. Right: search trigger + notifications + user avatar.

#### Command Palette
**Description:** ⌘K search and action launcher.
**Spec:** Overlay backdrop rgba(28,28,30,0.40), panel 640px max-width, 12px radius, `--shadow-floating`. Input at top 48px, 16px Inter 400. Result list items 40px, 8px gap, keyboard navigation with visible focus.
**Accessibility:** focus trap, Escape closes, arrow keys navigate.

#### Modal
**Description:** Centered blocking dialog.
**Spec:** 12px radius, max-width 480px (sm) / 640px (md) / 800px (lg), `--shadow-floating`, padding 32px. Header 20px Inter 500 + description 15px #6E6E73 + actions footer aligned right with 12px gap.
**Accessibility:** focus trap, `role="dialog"`, `aria-modal="true"`, Escape closes.

#### Drawer
**Description:** Edge-anchored panel.
**Spec:** 480px max-width, full-height, 16px radius on the anchored edge only. Same shadow as Modal. Used for filters, detail views, mobile nav.

#### Toast
**Description:** Transient feedback.
**Spec:** Bottom-right desktop, top-center mobile. 8px radius, padding 12px 16px, max-width 360px, background #1C1C1E, text #FFFFFF, 14px Inter 400. Icon left (16px), dismiss action right. Auto-dismiss 4000ms. Stack max 3.
**Variants:** default / success (Signal Green icon) / error (#FF0022 icon) / warning (Silver icon).

#### Notification (Inline Banner)
**Description:** Persistent contextual message inside content.
**Spec:** 8px radius, padding 16px, 1px hairline ring, background #FAFAFA (or tinted: #EAF0F8 info, rgba(46,125,79,0.08) success, rgba(255,0,34,0.06) error). Icon 16px left, title 14px Inter 500, description 14px #6E6E73, optional action link right.

#### Footer
**Description:** Site anchor.
**Spec:** Full-bleed #1C1C1E band, 4-column link grid above 1px rgba(255,255,255,0.06) dividers, version line 12px IBM Plex Mono #8E8E93 separated by pipes.

---

### 5.3 Cards

#### Feature Card (Hairline)
**Description:** Content card on light canvas — defined by border, not shadow.
**Spec:** Background #FFFFFF, 8px radius, 1px rgba(0,0,0,0.06) ring via box-shadow, 32px padding. Content: 20px Inter 500 subheading + 15px Inter 400 #6E6E73 body.

#### Feature Card (Inverted)
**Description:** Content card on obsidian bands — key-tactile treatment.
**Spec:** Background #1C1C1E (or #2A2A2E for elevated), 8px radius, 32px padding, `--shadow-key`. Text #FFFFFF heading + #E5E5E7 body.

#### Product Showcase Card (Window Chrome)
**Description:** Framed product screenshot.
**Spec:** 12px radius, 1px hairline ring, 32px dark window chrome header (#0F0F10) with three monochrome dots (#C0C0C0, #8E8E93, #6E6E73) and 12px IBM Plex Mono title. Screenshot on #0F0F10 below.

#### Padded Feature Panel
**Description:** Large asymmetric feature block.
**Spec:** Background #FFFFFF or #1C1C1E, 12px radius, padding 64px vertical / 48px horizontal.

#### Analytics Card
**Description:** Metric-driven dashboard card.
**Spec:** Background #FFFFFF, 8px radius, 1px hairline, 24px padding. Header: 13px IBM Plex Mono uppercase #6E6E73 label. Value: 32px Inter 500 #1C1C1E. Delta: 13px Inter 500 with Signal Green (↑) or #FF0022 (↓) + arrow glyph. Sparkline area 64px height below, 1.5px stroke #0F2D52.

#### Metric Card
**Description:** Minimal numeric stat block.
**Spec:** No card chrome. Number at 56px Inter 500, #1C1C1E, tracking -0.045em. Label 14px Inter 400 #6E6E73, 8px gap.

#### Pricing Card
**Description:** Plan comparison block.
**Spec:** Background #FFFFFF, 8px radius, 1px hairline, 32px padding. Plan name 20px Inter 500, price 44px Inter 500 with trailing period-size unit (/mo) at 16px Inter 400 #6E6E73. Feature list items 14px Inter 400 with 16px check icon in #0F2D52. CTA full-width at bottom.
**Featured variant:** background #1C1C1E, text inverted, 1px midnight top border 2px.

#### CRM Card (Contact / Deal)
**Description:** Compact relationship record.
**Spec:** 8px radius, 1px hairline, 16px padding. Row 1: avatar 32px circle + name 14px Inter 500 + status badge right. Row 2: company 13px #6E6E73. Row 3: value 14px Inter 500 #1C1C1E + last activity 12px #8E8E93.

#### Timeline Card
**Description:** Activity feed block.
**Spec:** Vertical rail 1px #E5E5E7 at left, 16px gap. Each event: dot 8px circle (#0F2D52 for active, #C0C0C0 for past), timestamp 12px IBM Plex Mono #8E8E93, title 14px Inter 500 #1C1C1E, description 13px #6E6E73.

---

### 5.4 Data Display

#### Table
**Description:** Structured row-based data.
**Spec:** Header row 40px, background #FAFAFA, 13px Inter 500 #6E6E73 uppercase optional letter-spacing 0.02em. Body rows 52px, 1px bottom hairline. Cell padding 12px horizontal. Sortable column headers show chevron on hover. Row hover → #FAFAFA.
**Responsive:** <768px → card stack with label-above-value pairs.

#### Data Grid
**Description:** Dense editable matrix.
**Spec:** Same as Table with 40px rows, cell padding 8px, keyboard navigation (arrow keys, tab, enter to edit). Focus cell → 2px #0F2D52 inset ring. Frozen first column optional.

#### Charts
**Description:** Data visualization.
**Spec:** Line/area/bar chart, 1.5px stroke, #0F2D52 primary series, #C0C0C0 secondary, #E5E5E7 grid lines. Axis labels 12px IBM Plex Mono #8E8E93. Tooltips: 8px radius, #1C1C1E background, #FFFFFF text 12px, 12px padding. No 3D, no gradients, no drop shadows.

#### Empty State
**Description:** Zero-data placeholder.
**Spec:** Centered block, max-width 400px. Icon 48px line-art #C0C0C0, heading 20px Inter 500 #1C1C1E, description 15px #6E6E73, primary action below. 96px vertical padding.

#### Error State
**Description:** Failure feedback.
**Spec:** Same layout as Empty State with #FF0022 icon. Retry button secondary.

#### Success State
**Description:** Confirmation view.
**Spec:** Same layout with #2E7D4F checkmark icon. Optional primary "continue" action.

#### Loading Indicator
**Description:** Inline progress signal.
**Spec:** 16px spinner (2px stroke, #0F2D52 on light, #FFFFFF on dark) rotating 800ms linear infinite. For full-page: 32px centered spinner with 12px label below in #6E6E73.

#### Skeleton
**Description:** Content placeholder during load.
**Spec:** Background #F2F2F4, radius matching the replaced element, shimmer sweep 1.5s ease-in-out infinite (opacity 0.6 → 1.0 → 0.6). Never use spinner + skeleton on the same surface.

#### Pagination
**Description:** Multi-page navigation.
**Spec:** Row 40px height, gap 4px. Page buttons 32×32px, 6px radius, 13px Inter 500. Active page → background #0F2D52, text #FFFFFF. Disabled → #C0C0C0.

#### Filter Bar
**Description:** Faceted filtering controls.
**Spec:** Horizontal row, wrap below 768px. Filter chips use Pill spec (see below). Active filters show count badge. "Clear all" text link right-aligned.

#### Search Input
**Description:** Text query input.
**Spec:** Same as Input Field with 16px leading magnifier icon. On focus, ring 2px #0F2D52.

---

### 5.5 Forms

#### Input Field
**Description:** Text inputs, search, form fields.
**Spec:** Background #FAFAFA (light) or rgba(255,255,255,0.04) (dark), 6px radius, 1px #E5E5E7 ring, padding 10px 14px, Inter 14px 400, #1C1C1E text. Placeholder #8E8E93. Focus → border #0F2D52 + 2px rgba(15,45,82,0.12) ring offset 1px.
**Variants:** text / email / password / number / textarea / select.
**Accessibility:** every input has an associated `<label>`; error uses `aria-describedby`.

#### Label
**Description:** Input label.
**Spec:** 13px Inter 500 #1C1C1E, 6px margin-bottom. Optional helper text below in 12px #6E6E73.

#### Checkbox / Radio
**Description:** Binary or single-select control.
**Spec:** 16×16px, 4px radius (checkbox) or 9999px (radio), 1px #C0C0C0 ring. Checked → #0F2D52 fill, white glyph. Focus → 2px #0F2D52 ring.

#### Toggle / Switch
**Description:** Binary on/off.
**Spec:** 36×20px track, 16px thumb. Off → #E5E5E7 track, #FFFFFF thumb. On → #0F2D52 track. Transition 200ms `--ease-standard`.

#### Upload
**Description:** File drop zone.
**Spec:** Dashed 1.5px #C0C0C0 border, 8px radius, padding 32px, centered icon 24px + label 14px Inter 500 + helper 12px #6E6E73. Drag active → border #0F2D52, background #EAF0F8.

#### Wizard (Stepper)
**Description:** Multi-step form flow.
**Spec:** Horizontal step list at top, 32px gap. Step dot 24px circle, number 12px Inter 500. Active → #0F2D52 fill + white number. Completed → #0F2D52 fill + check. Upcoming → #E5E5E7 fill + #8E8E93 number. Connector line 1px #E5E5E7 between dots.

#### Settings Panel
**Description:** Grouped form sections.
**Spec:** Vertical stack, 32px gap between groups. Group header 16px Inter 500 #1C1C1E + 4px subtitle 13px #6E6E73. Field rows 1px hairline separated. Save action sticky at bottom right.

---

### 5.6 Feedback & Overlays

#### Badge / Status Tag
**Description:** Inline metadata.
**Spec:** Background #F2F2F4 (light) / rgba(255,255,255,0.06) (dark), text #4A4A4E 12px Inter 500, 4px radius, padding 2px 8px.
**Variants:** default / info (#EAF0F8) / success (rgba(46,125,79,0.10)) / warning (rgba(255,187,0,0.14)) / error (rgba(255,0,34,0.08)).

#### Pill Tag
**Description:** Filter chips, category pills.
**Spec:** Transparent, 1px #E5E5E7 ring, text #4A4A4E 13px Inter 500, 9999px radius, padding 6px 14px. Hover → ring #C0C0C0, text #1C1C1E. Active → background #0F2D52, text #FFFFFF, no ring.

#### Calendar
**Description:** Date picker / scheduler.
**Spec:** Grid 7 columns, cells 40px, 6px radius. Selected day → #0F2D52 fill. Today → 1px #0F2D52 ring. Out-of-month → #C0C0C0. Header 16px Inter 500 + prev/next icon buttons.

#### Tooltip
**Description:** Contextual hover hint.
**Spec:** Background #1C1C1E, text #FFFFFF 12px Inter 400, 6px radius, padding 6px 10px, max-width 240px. 200ms fade-in, no arrow or a 6px CSS arrow.

---

### 5.7 Composite / Product Patterns

#### Dashboard Shell
**Description:** Standard product layout.
**Structure:** Sidebar (240px) + Topbar (56px) + Content (fluid, max 1280px inside) + optional Right panel (320px).
**Background:** Content on #FAFAFA; cards on #FFFFFF.

#### KPI Row
**Description:** Top-of-dashboard metric strip.
**Spec:** 3–4 metric cards in a row, 24px gap, responsive to 2-up at 1024px, 1-up at 640px.

#### Empty Dashboard State
**Description:** First-run experience.
**Spec:** Centered, 640px max-width. Icon 64px, headline 32px Inter 500, description 16px #6E6E73, primary CTA + ghost documentation link.

#### Client Portal Shell
**Description:** External-facing authenticated area.
**Structure:** Simplified topbar only (no sidebar). Content max 960px. Warmer spacing (32px card padding, 48px gaps).

#### Developer Portal Shell
**Description:** API/docs area.
**Structure:** Left sidebar of topics + main content + right "on this page" nav. Code blocks use CLI Panel spec.

---

## 6. Page Architecture

Every page follows a canonical vertical rhythm. AI agents must respect these sequences.

### 6.1 Homepage

```
Nav (glass, 64px)
↓
Hero — asymmetric, left headline + right empty 40%
↓
Trust strip — customer logos, monochrome
↓
Solutions — 3-column feature cards (light)
↓
Process — numbered steps with timeline layout
↓
Case Studies — 2-column product showcase cards
↓
Testimonials — 3-up quote cards
↓
Metrics — 4-stat strip
↓
Full-bleed CTA band (obsidian, 64px vertical padding)
↓
Footer
```

### 6.2 Product Page

```
Nav
↓
Hero — product name + one-line outcome + CTA pair
↓
Problem → Solution — 2-column, text left, screenshot right
↓
Capabilities — tabbed feature explorer
↓
Integrations — logo grid, 6-column
↓
Pricing Preview — single card with "see pricing" link
↓
FAQ — 12-item accordion
↓
CTA band
↓
Footer
```

### 6.3 Pricing

```
Nav
↓
Hero — headline + subhead, centered
↓
Billing toggle (monthly / yearly)
↓
Pricing cards — 3-up, featured middle
↓
Comparison table — full feature matrix
↓
FAQ — billing-specific
↓
CTA band
↓
Footer
```

### 6.4 Documentation

```
Nav
↓
Layout: left sidebar (topics) + main content + right TOC
↓
Content: H1 + intro paragraph + anchors
↓
Code blocks, callouts, tables
↓
Prev / Next footer nav
```

### 6.5 Dashboard

```
Sidebar (240px) + Topbar (56px)
↓
KPI Row (3–4 metric cards)
↓
Primary chart panel (full-width)
↓
Two-column: recent activity table + secondary chart
↓
Footer meta strip (version, environment, latency)
```

### 6.6 Blog

```
Nav
↓
Hero — featured post, large
↓
Grid — 3-column of recent posts
↓
Category filter pills
↓
Pagination
↓
Newsletter CTA band
↓
Footer
```

### 6.7 Support

```
Nav
↓
Hero — search input, prominent
↓
Category grid — 6 cards
↓
Popular articles — 10-row list
↓
Contact options — 3-up cards (chat / email / docs)
↓
Footer
```

### 6.8 Contact

```
Nav
↓
Two-column: form left (60%) + info right (40%)
↓
Form: name, email, company, message, submit
↓
Info: address, email, phone, hours
↓
Map or office photo (documentary, not stock)
↓
Footer
```

### 6.9 Authentication

```
Centered card, 400px max-width
↓
Logo mark + wordmark
↓
H1 — "Sign in to Walden"
↓
Inputs: email, password
↓
Primary CTA full-width
↓
Secondary: SSO, magic link
↓
Footer links: privacy, terms
```

### 6.10 Admin

```
Sidebar (collapsed by default, 56px) + Topbar
↓
Section tabs
↓
Data Grid primary
↓
Bulk action bar (contextual)
↓
Audit log below
```

### 6.11 CRM

```
Sidebar + Topbar
↓
Pipeline view (kanban, 4–6 columns)
↓
Deal cards use CRM Card spec
↓
Right drawer for detail on click
↓
Activity timeline inside drawer
```

### 6.12 Client Portal

```
Topbar (simplified, no sidebar)
↓
Welcome block — client name + project status
↓
Deliverables list
↓
Invoices table
↓
Support contact block
↓
Footer (minimal)
```

### 6.13 Developer Portal

```
Nav
↓
Sidebar (API topics) + Content + TOC
↓
Getting started
↓
API reference
↓
Code samples (CLI panel)
↓
SDKs and libraries
↓
Changelog
```

---

## 7. Layout

Max-width 1200px centered container with 24–48px responsive horizontal padding. Full-bleed sections extend to viewport edges on both white and obsidian bands. The hero is an asymmetric two-zone composition: left-aligned oversized headline (56–64px) + sub-paragraph + CTA pair, with the right 40% left intentionally empty. Below the hero, content alternates between type-only blocks (eyebrow + heading + paragraph) and product showcase bands (full-bleed obsidian with a framed screenshot). Sections are separated by 96px vertical gaps, with 1px #E5E5E7 dividers between major content shifts. Card grids use 2-column or 3-column layouts at desktop with 24px column gaps, collapsing to single column at 767px. Navigation is a single 64px sticky top bar with a glass-blur treatment; no sidebar, no mega-menu, no hover dropdowns. The overall density is compact and text-dominant.

---

## 8. Motion Guidelines

Motion is deliberate and atmospheric — never decorative. It exists to clarify state changes, never to entertain.

### 8.1 Allowed primitives

| Primitive | Use case |
|-----------|----------|
| **Fade** | Modal / tooltip / toast appearance, section reveal on scroll |
| **Slide** | Drawer enter/exit, toast position, mobile nav |
| **Scale** | Modal open (0.98 → 1.00 only), button press feedback (1.00 → 0.98) |
| **Opacity** | Link hover, disabled transitions |
| **Color** | Border, background, text — the dominant transition property |
| **Blur** | Nav backdrop-filter appearance on scroll |
| **Translate** | Scroll reveal 2px upward only |

### 8.2 Durations

| Category | Duration |
|----------|----------|
| Micro (hover, focus, small color shifts) | 150–200ms |
| Standard (button press, toggle, dropdown) | 200–250ms |
| Surface (modal, drawer, toast) | 300–400ms |
| Reveal (scroll-triggered section fade) | 500–600ms |

**Hard ceiling:** 600ms. Anything longer is forbidden.

### 8.3 Easing

- **Standard:** `cubic-bezier(0.4, 0, 0.2, 1)` — all interactive state changes
- **Enter:** `cubic-bezier(0, 0, 0.2, 1)` — elements appearing
- **Exit:** `cubic-bezier(0.4, 0, 1, 1)` — elements leaving
- **Linear:** only for spinner rotation

**Forbidden:** `ease-in-out` on scroll reveals, bouncy `cubic-bezier` with overshoot, spring physics.

### 8.4 Micro-interactions

- **Button hover:** background-color shift, 200ms standard easing
- **Button press:** `transform: scale(0.98)`, 150ms
- **Link hover:** color shift + underline fade-in 200ms
- **Input focus:** border brighten + 2px ring fade-in 200ms
- **Checkbox check:** stroke draw 200ms
- **Toggle switch:** thumb translate 200ms
- **Accordion:** height auto transition 300ms enter / 250ms exit, chevron rotate 200ms
- **Modal:** opacity 0→1 + translateY(8px→0) over 300ms enter / 200ms exit
- **Toast:** translateX(24px→0) + fade 300ms enter, reverse 200ms exit
- **Scroll reveal:** opacity 0→1 + translateY(2px→0) 600ms, trigger at 20% viewport entry

### 8.5 Strict limits

- No motion above 600ms — ever
- No rotation, no 3D transforms, no skew
- No animation on page load that delays content (no hero fade-in that blocks reading)
- No parallax scrolling
- No scroll-jacking
- No looping animation except spinners and skeleton shimmer
- No animation on data tables, charts, or dense information
- `prefers-reduced-motion: reduce` disables all non-essential motion

### 8.6 Reduced motion

When `@media (prefers-reduced-motion: reduce)` is active:
- All scroll reveals become instant (`opacity: 1`, no transform)
- Modal and drawer appear instantly (no transition duration)
- Hover states remain (color only, no transform)
- Spinners continue (necessary)
- Skeleton shimmer becomes static opacity

---

## 9. UX Principles

### 9.1 Navigation

Every page reachable in ≤3 clicks from the homepage. Persistent navigation on authenticated surfaces. Breadcrumbs on nested documentation and admin pages. No mega-menus, no nested hover dropdowns. Command palette (⌘K) available in all product surfaces.

### 9.2 Visual Hierarchy

One H1 per page. Heading levels never skipped. The most important element on any screen is 2× the size of the next-most-important. Whitespace increases with hierarchy importance. Every screen must answer "what should I look at first?" without ambiguity.

### 9.3 Readability

Minimum body size: 14px on light, 13px on dark. Line length 45–75 characters. Line height 1.55 for body, 1.20 for headings. Never justify text. Never set body copy below #6E6E73 on light canvas for anything longer than a caption.

### 9.4 Accessibility

Non-negotiable. See section 11.

### 9.5 Performance

First Contentful Paint < 1.2s, Largest Contentful Paint < 2.0s, Interaction to Next Paint < 200ms, Cumulative Layout Shift < 0.05. Any deviation is a design failure, not just an engineering one.

### 9.6 Responsive

Mobile-first. Every screen designed at 375px before 1440px. No horizontal scroll at any breakpoint. Touch targets ≥44×44px. See section 10.

### 9.7 User feedback

Every action produces feedback within 100ms — either visual state change, spinner, or optimistic update. No silent actions. No ambiguous states. Errors are specific, not "something went wrong".

### 9.8 Error handling

Errors explain what happened, why, and what to do next — in that order, in one sentence each. Never blame the user. Never expose stack traces. Provide a retry or escape action on every error surface.

### 9.9 Confirmation

Destructive actions require explicit confirmation with the object named in the dialog title. Multi-step destructive flows require typing the object name. No confirmation for reversible actions.

### 9.10 Loading times

- <100ms: no indicator
- 100–1000ms: inline spinner or optimistic UI
- >1000ms: skeleton or progress bar
- >10s: background task with notification on completion

---

## 10. Responsive Rules

Mobile-first. All layouts are designed at the smallest breakpoint first, then progressively enhanced.

| Breakpoint | Range | Target | Key adjustments |
|------------|-------|--------|-----------------|
| Mobile | 320–767px | Smartphone | Single column. `display-xl` → 40px. Section gap → 64px. Card padding → 24px. Nav → 56px bar with slide-in drawer. Hero left-aligned, no empty right zone. |
| Tablet | 768–1023px | Tablet portrait | Two-column card grids. `display-xl` → 52px. Section gap → 80px. Card padding → 28px. Nav → 60px with drawer at <900px. |
| Laptop | 1024–1439px | Laptop | Full 1200px container. All scales at spec. Hero asymmetric split active. |
| Desktop | 1440px+ | Desktop / ultrawide | Same as laptop, content capped at 1200px. Margins grow symmetrically. Max readable content width never exceeds 720px inside the container. |

Rules:
- No horizontal scroll at any breakpoint
- Fluid grids via `minmax()` and `clamp()` for typography
- Touch targets minimum 44×44px
- Images served as WebP / AVIF with `loading="lazy"` below the fold
- Nav collapses to a full-screen overlay drawer below 1024px
- Tables switch to card stacks below 768px
- Data grids become horizontally scrollable below 1024px with sticky first column

---

## 11. Accessibility

**Contrast:**
- Body text ≥ 4.5:1 against its canvas
- Large display type (≥24px) ≥ 3:1
- Interactive elements (borders, focus rings, icons) ≥ 3:1
- Never use color alone to convey information — pair with icon, text, or shape

**Focus:**
- Every interactive element shows a visible 2px `#0F2D52` ring at 2px offset on `:focus-visible` only
- Never `outline: none` without a replacement
- Focus ring must be visible on both light and dark surfaces

**Keyboard:**
- All navigation, forms, and modals operable via keyboard
- No keyboard trap — Escape exits every overlay
- Logical tab order
- Skip-to-content link as first focusable element

**Screen readers:**
- Semantic HTML first (`<nav>`, `<main>`, `<button>`, `<label>`)
- ARIA only when native semantics fall short
- Every icon-only button has `aria-label`
- Every form input has an associated `<label>`
- Errors use `aria-live="polite"` and `aria-describedby`
- Modal: `role="dialog"`, `aria-modal="true"`, focus trap

**Motion:**
- Respect `prefers-reduced-motion: reduce`
- No autoplay video
- No flashing content above 3Hz

**Text:**
- Minimum 14px on light, 13px on dark
- Supports 200% browser zoom without loss
- Language attribute on `<html>` per locale

---

## 12. Iconography

**Choice:** Line-art only. 24×24 grid, 1.5px stroke, geometric construction, single-color `currentColor`. Drawn specifically for Walden; never mixed with third-party icon sets without redrawing to match weight and corner radius.

**Style:**
- Stroke-cap: round
- Stroke-join: round
- Corners: 2px radius on outer paths
- Grid: 24×24 with 2px internal padding (content lives in 20×20)
- Fills: none, except for status indicators

**Sizes:**
- 16px — inline within text, dense UI
- 20px — buttons, nav items
- 24px — standalone, feature cards
- 32px — empty states, hero decorative
- 48px — empty state primary
- Never scale icons non-proportionally

**Color:**
- On light canvas: `#1C1C1E` primary, `#6E6E73` secondary, `#C0C0C0` decorative
- On dark canvas: `#FFFFFF` primary, `#E5E5E7` secondary, `#C0C0C0` decorative
- Midnight accent `#0F2D52` only for active states and single-point emphasis
- Signal Green `#2E7D4F` only for success indicators

**Spacing:**
- 8px between icon and label at 16–20px sizes
- 12px between icon and label at 24px+
- Icons in buttons: 8px gap to label
- Icons in nav items: 12px gap to label

**Forbidden:** filled icons (except status dots and avatars), multi-color icons, cartoon style, 3D icons, icons with drop shadows, any icon resembling robots, brains, circuits, or crowns.

---

## 13. Illustration Style

Walden uses illustration sparingly, and only when a concept cannot be communicated with typography, real product UI, or a geometric diagram.

### 13.1 3D
**Not used.** No 3D renders, no isometric illustrations, no extruded shapes. If a diagram is needed, use 2D geometry.

### 13.2 Gradients
**Forbidden** on UI, cards, buttons, and text. A single subtle gradient is permitted only in the CLI panel background (barely perceptible #0F0F10 → #1C1C1E at 10% range) and never elsewhere.

### 13.3 Glassmorphism
Permitted only on the nav bar (backdrop-blur 20px). Nowhere else. No frosted cards, no translucent panels, no blurred backgrounds.

### 13.4 Images
Documentary and product-first. Real product UI screenshots dominate. Photography permitted only as documentary (offices, architecture, teams at work), never stock, never staged, never with artificial lighting. Always shot from a natural angle, never eye-level corporate cliché.

### 13.5 Photography
When photography is used:
- Natural light only
- Documentary framing
- Cool color grade (never warm, never filtered)
- Human subjects shown mid-action, never posed
- Never stock photography with obvious artifice
- Never AI-generated imagery
- Never generic "tech office" imagery

### 13.6 Icons
See section 12.

### 13.7 Illustrations
Only when necessary. Abstract geometry only: grids, axes, line charts, node graphs, structural diagrams, flow arrows. All rendered in the palette (Midnight, Silver, Hairline, Obsidian). Never literal, never figurative, never narrative.

### 13.8 When to use each

| Situation | Use |
|-----------|-----|
| Explaining a workflow | Geometric diagram |
| Showing a capability | Real product screenshot |
| Establishing trust | Customer logos, testimonial photos (documentary only) |
| Filling an empty state | Simple line-art icon at 48px |
| Marketing a concept | Large compressed headline + sub-paragraph (typography, no illustration) |
| Documentation | Code blocks, CLI panels, geometric diagrams |

**Never:** robots, brains, circuit boards, crowns, eagles, sci-fi scenes, neon diagrams, glitch art, particle effects, WebGL backgrounds.

---

## 14. AI-Friendly Rules

This document is designed to be consumed by AI agents (Cline, ChatGPT, Copilot, Claude, Cursor) without human interpretation. The following rules make this possible.

### 14.1 Explicitness

Every rule is stated in plain language. Where a rule could be ambiguous, an example or a negation is provided. AI agents must not infer — they must read.

### 14.2 Non-ambiguity

- Colors are given as hex values, always
- Sizes are given as pixel values, always
- Fonts are named by family and weight, always
- Every "do" has a matching "don't" where a common mistake exists
- Every component has a complete spec — no "styles follow the pattern above"

### 14.3 Structured generation

To generate any component, an AI agent follows this exact sequence:

1. Read section 5 for the component entry
2. Apply the exact spec (background, text, radius, padding, font)
3. Apply states (hover, focus, active, disabled, loading) per section 5
4. Apply spacing per section 4.4
5. Apply responsive behavior per section 10
6. Apply accessibility per section 11
7. Cross-check with section 15 (Do's and Don'ts)
8. Emit HTML/CSS using tokens from section 20

### 14.4 Tokens are mandatory

AI agents must use the CSS custom properties from section 20 — never hard-coded hex values, never magic numbers. Every pixel, every color, every shadow comes from a token. This makes global changes possible without hunting raw values.

### 14.5 Component generation template

For any new component, produce:

```
Component name: [name]
Purpose: [one-line description]
Structure: [semantic HTML outline]
Spec: [exact values from section 5, or the pattern it extends]
States: [list of states and their exact style deltas]
Spacing: [padding, gap, margin from section 4.4]
Responsive: [behavior at each breakpoint from section 10]
Accessibility: [role, aria attributes, keyboard behavior]
Tokens: [exact CSS custom properties used]
```

### 14.6 Forbidden AI behaviors

- Inventing colors, sizes, radii, shadows, or fonts not in this document
- Using a hard-coded hex value where a token exists
- Creating a component variant not listed in section 5 without human approval
- Interpreting "minimal" as "empty" or "premium" as "add a gradient"
- Adding motion not listed in section 8
- Using a font weight above 600
- Introducing a second accent color
- Generating illustrations, icons, or imagery that violate section 13

### 14.7 Required AI behaviors

- Always ask: which of the 5 Walden questions (section 22) does this pass?
- Always emit tokens, not raw values
- Always include responsive rules
- Always include focus states and ARIA where interactive
- Always cross-reference section 15 before emitting
- If a request conflicts with this document, refuse and explain why

### 14.8 Reference resolution order

When two rules conflict, resolve in this order (highest priority first):

1. Accessibility (section 11)
2. Brand personality (section 1)
3. Do's and Don'ts (section 15)
4. Component specs (section 5)
5. Tokens (sections 2–4)
6. Layout (section 7)
7. Motion (section 8)
8. UX Principles (section 9)

---

## 15. Do's and Don'ts

### Do
- Use #1C1C1E exclusively for headings and inverted bands — never pure #000000, never a warm near-black
- Use #0F2D52 (Midnight) exclusively for the single primary CTA per view, link text, and focus rings — never as a decorative fill
- Set all display headings at Inter weight 500 with -0.04em to -0.05em tracking — the compression and restraint are non-negotiable
- Build depth with hairline 1px borders (rgba(0,0,0,0.06) on light, rgba(255,255,255,0.06) on dark) — never with drop-shadows
- Use 6px radius for buttons and inputs, 8px for cards, 12px for large cards, 4px for badges, 9999px for pills — five radii is the entire vocabulary
- Set section gaps at 96px and element gaps at 12px — the 4/8/12/24/32/64/96 ladder is the rhythm
- Use IBM Plex Mono uppercase at 11–12px with 0.071em tracking for all eyebrow labels, version strings, and technical metadata
- Use the keyboard-key shadow stack (rgba(255,255,255,0.04) inset top + rgba(0,0,0,0.20) inset bottom + rgba(0,0,0,0.06) outer ring) on dark-band feature cards only
- Keep one filled chromatic button per view — the midnight CTA. Every other button is neutral (bone filled) or ghost.
- Pair every filled CTA with a ghost secondary — never present a lone filled button
- Respect the reference resolution order (14.8) when rules conflict

### Don't
- Don't introduce any chromatic accent beyond Midnight (#0F2D52) — no greens, oranges, pinks, or additional blues anywhere
- Don't use #FFFFFF as a card fill on light canvas — white is the canvas itself; cards are defined by hairlines, not fills
- Don't apply drop-shadows to cards, panels, or buttons — the Raycast key stack and Linear hairlines are the entire depth vocabulary
- Don't use font weights above 600 — the system speaks at 400 (body), 500 (display and buttons), and 600 (wordmark only). Nothing bolder.
- Don't set body text below 14px on light canvas or below 13px on dark canvas — Walden's minimum size protects readability
- Don't use warm grays, chromatic neutrals, or gradients — the palette is strictly cool/achromatic with midnight blue as the only chromatic direction
- Don't pill-shape buttons — 9999px radius belongs to tags and chips only
- Don't use glassmorphism beyond the nav bar's backdrop-blur — translucent panels elsewhere break the ledger aesthetic
- Don't mix Inter and IBM Plex Mono within a single text block — Inter for prose, Mono for stamps, never together
- Don't center body copy or headings — Walden text blocks are always left-aligned within their column
- Don't use border-radius values outside the defined scale (4, 6, 8, 12, 16, 9999) — every radius in the system maps to a specific component type
- Don't animate with bounce, spring, or overshoot — motion is linear and atmospheric, never playful
- Don't introduce a second brand color, a gradient sweep, or a "spectrum" accent of any kind
- Don't create variants of any component without explicit human approval

---

## 16. Surfaces & Elevation

### 16.1 Surfaces

| Level | Name | Value | Purpose |
|-------|------|-------|---------|
| 0 | Paper | `#ffffff` | Default page canvas on light bands |
| 1 | Vellum | `#fafafa` | Section banding and quiet footer separators — a barely-perceptible cool wash |
| 2 | Mist | `#f2f2f4` | Card ring borders, hover backgrounds, input wells |
| 3 | Hairline | `#e5e5e7` | 1px structural borders and dividers |
| 4 | Obsidian | `#1c1c1e` | Dark section canvas, inverted card fills, footer anchor |
| 5 | Ink | `#2a2a2e` | Elevated surfaces one step above obsidian — dark-band cards |
| 6 | Carbon | `#0f0f10` | Deepest surface — image backdrops, CLI panels, terminal chrome |
| 7 | Midnight Wash | `#eaf0f8` | Atmospheric midnight-tinted section bands and tag pills |

### 16.2 Elevation

Walden's system borrows Linear's border-first elevation discipline. Depth is achieved through surface-level luminance stepping (Paper → Vellum → Mist → Hairline on light; Obsidian → Ink → Carbon on dark), 1px hairline borders, and on dark-band cards only, the Raycast keyboard-key inner shadow stack. There are exactly three shadow primitives in the entire system:

- **Hairline ring:** `rgba(0, 0, 0, 0.06) 0px 0px 0px 1px` (light) / `rgba(255, 255, 255, 0.06) 0px 0px 0px 1px` (dark)
- **Keyboard key:** `rgba(255, 255, 255, 0.04) 0px 1px 0px 0px inset, rgba(0, 0, 0, 0.20) 0px -1px 0px 0px inset, rgba(0, 0, 0, 0.06) 0px 0px 0px 1px` — dark cards only
- **Floating:** `rgba(15, 45, 82, 0.08) 0px 4px 16px 0px` — modals, dropdowns, and the hero nav only

No card has a drop-shadow. No button has a shadow on hover. The single chromatic shadow is the midnight accent glow, `rgba(15, 45, 82, 0.20) 0px 4px 12px 0px`, applied only to the hovered primary CTA.

---

## 17. Imagery

The visual language is product-first and documentary-adjacent. Hero and section imagery is dominated by real product UI — dashboards, deployment consoles, workflow editors, API responses — captured at full fidelity and framed in simulated window chrome with monochrome traffic-light dots. No stock photography, no lifestyle imagery, no abstract 3D renders. Where abstract imagery is needed (rare), it stays geometric: grid systems, axis lines, deterministic charts, structural diagrams — never nebulous neon forms. Customer logos appear in a single horizontal rail, rendered in each brand's actual wordmark, desaturated to #8E8E93 on light bands or #C0C0C0 on dark. Icons are uniform 1.5px stroke line-art, geometric and single-color, drawn at 16–24px. No illustration. No decorative background imagery. The product is the visual content.

---

## 18. Agent Prompt Guide

### 18.1 Quick Color Reference

- **Background (light):** `#ffffff`
- **Background (dark band):** `#1c1c1e`
- **Text primary:** `#1c1c1e` (light) / `#ffffff` (dark)
- **Text secondary:** `#6e6e73`
- **Text muted:** `#8e8e93`
- **Border / divider:** `#e5e5e7`
- **Accent / CTA / link:** `#0f2d52`
- **Accent hover:** `#1e56a0`
- **Card surface (light):** `#ffffff` with hairline ring
- **Card surface (dark):** `#2a2a2e` with keyboard-key stack
- **primary action:** `#0f2d52` (filled action)

### 18.2 Example Component Prompts

**1. Hero headline block**
Full-bleed white (#ffffff) canvas. Eyebrow label above in IBM Plex Mono 11px weight 500, uppercase, #6e6e73, letter-spacing 0.78px. Headline at 64px Inter weight 500, color #1c1c1e, letter-spacing -3.2px, line-height 1.0. Sub-paragraph at 18px Inter weight 400, color #6e6e73, max-width 480px, line-height 1.50. Below: primary midnight CTA (#0f2d52 fill, #ffffff text, 6px radius, 10px 20px padding, Inter 14px weight 500) + ghost outline button (transparent fill, #1c1c1e text, 1px #e5e5e7 ring, 6px radius), 12px gap. Right 40% of the layout stays empty.

**2. Product showcase card**
Background #1c1c1e, border-radius 12px, 1px hairline ring rgba(255,255,255,0.08). 32px dark window chrome header (#0f0f10) at the top with three monochrome dots (#c0c0c0, #8e8e93, #6e6e73) and a 12px title in IBM Plex Mono #e5e5e7. Below: embedded product screenshot on #0f0f10. No outer shadow.

**3. Feature card (dark band)**
Background #2a2a2e, border-radius 8px, 32px padding, keyboard-key stack: rgba(255,255,255,0.04) 0 1px 0 0 inset, rgba(0,0,0,0.20) 0 -1px 0 0 inset, rgba(0,0,0,0.06) 0 0 0 1px. Inside: 20px Inter weight 500 subheading in #ffffff at -0.24px tracking, then 15px Inter weight 400 body in #e5e5e7.

**4. Section heading + stat block**
96px top padding. Eyebrow label at 11px IBM Plex Mono weight 500, uppercase, #6e6e73, letter-spacing 0.78px. Heading at 44px Inter weight 500, #1c1c1e, letter-spacing -1.76px. Below: 32px gap, then a large stat — number at 56px Inter weight 500, #1c1c1e, tracking -2.52px — with a #6e6e73 14px label below it.

**5. CLI output panel**
Background #0f0f10, border-radius 8px, 1px hairline ring rgba(255,255,255,0.06), 24px padding. All text in IBM Plex Mono 13px weight 400, #e5e5e7. Commands prefixed with "›" in #c0c0c0; successful lines prefixed with "✓" in #2e7d4f. line-height 1.60.

**6. Nav top bar**
Height 64px, background rgba(255,255,255,0.80) with backdrop-filter blur(20px) saturate(180%), 1px hairline bottom border rgba(0,0,0,0.06). Left: 12×12px geometric glyph in #1c1c1e + "Walden" wordmark in Inter 16px weight 600, tracking -0.022em, #1c1c1e. Center-left: nav links at 14px Inter weight 400, #6e6e73, 32px gap. Right: ghost "Sign in" (6px radius, 1px #e5e5e7 ring, #1c1c1e text) + primary "Start a project" (#0f2d52 fill, #ffffff text, 6px radius).

**7. Eyebrow label**
IBM Plex Mono 11px weight 500, uppercase, letter-spacing 0.78px, color #6e6e73. Pair with 12px margin-bottom before the heading it introduces.

**8. Dashboard KPI row**
3-up grid, 24px gap. Each card: background #ffffff, 8px radius, 1px hairline, 24px padding. Header: 13px IBM Plex Mono uppercase #6e6e73 label. Value: 32px Inter 500 #1c1c1e. Delta: 13px Inter 500 in #2e7d4f (↑) or #ff0022 (↓) with arrow glyph. Sparkline 64px height, 1.5px #0f2d52 stroke.

**9. Pricing card**
Background #ffffff, 8px radius, 1px hairline, 32px padding. Plan name 20px Inter 500 #1c1c1e. Price 44px Inter 500 with trailing "/mo" at 16px Inter 400 #6e6e73. Feature list: 14px Inter 400 with 16px check icon in #0f2d52, 8px vertical gap. CTA full-width at bottom. Featured variant: background #1c1c1e, text inverted, 2px #0f2d52 top border.

**10. Modal**
12px radius, max-width 480px, `--shadow-floating`, padding 32px. Header 20px Inter 500 #1c1c1e + description 15px #6e6e73 + footer actions right-aligned with 12px gap. Backdrop rgba(28,28,30,0.40). Focus trap active. Escape closes.

---

## 19. Similar Brands

- **Linear** — Same hairline-border depth model, same single-accent-on-monochrome discipline, same compressed Inter-weight display type, same 96px section rhythm. Walden is Linear sobered to midnight blue and given a light primary mode.
- **Vercel** — Same paper-white ledger canvas, same mono-stamp labels, same refusal of chromatic decoration, same product-screenshot-as-hero approach. Walden trades Vercel's pure black for obsidian and its Geist family for Inter + IBM Plex Mono.
- **Stripe** — Same whisper-weight display headings, same 4px-to-6px button geometry, same trust in whitespace over chrome, same left-aligned text-block layout. Walden borrows the restraint without sohne-var's corporate warmth.
- **Raycast** — Same keyboard-key tactile treatment on dark-band cards, same neutral filled CTAs, same glass nav bar discipline, same terminal-as-marketing pattern. Walden replaces Raycast's coral with midnight and its dramatic hero gradient with literal emptiness.
- **Framer** — Same asymmetric hero composition, same card-radius ladder, same compressed display tracking. Walden removes Framer's neon blue entirely and replaces its luminance-stepping cards with hairline borders.
- **Arc Browser** — Same midnight-on-dark atmosphere, same restrained accent use, same product-as-artifact aesthetic. Walden is Arc stripped of its playful color moments.

---

## 20. Quick Start — CSS & Tailwind

### 20.1 CSS Custom Properties

```css
:root {
  /* Colors — Light canvas */
  --color-paper: #ffffff;
  --color-vellum: #fafafa;
  --color-mist: #f2f2f4;
  --color-hairline: #e5e5e7;
  --color-silver: #c0c0c0;
  --color-fog: #8e8e93;
  --color-stone: #6e6e73;
  --color-slate: #4a4a4e;

  /* Colors — Dark canvas */
  --color-ink: #2a2a2e;
  --color-obsidian: #1c1c1e;
  --color-carbon: #0f0f10;
  --color-bone: #ffffff;
  --color-pearl: #e5e5e7;

  /* Colors — Accent */
  --color-midnight: #0f2d52;
  --color-midnight-deep: #0a1e38;
  --color-midnight-lift: #1e56a0;
  --color-midnight-wash: #eaf0f8;

  /* Colors — Signal */
  --color-signal-green: #2e7d4f;

  /* Typography — Font Families */
  --font-inter: 'Inter', ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-plex-mono: 'IBM Plex Mono', ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;

  /* Typography — Scale */
  --text-eyebrow: 11px;
  --leading-eyebrow: 1.40;
  --tracking-eyebrow: 0.78px;
  --text-caption: 12px;
  --leading-caption: 1.50;
  --tracking-caption: -0.036px;
  --text-body-sm: 14px;
  --leading-body-sm: 1.55;
  --tracking-body-sm: -0.042px;
  --text-body: 16px;
  --leading-body: 1.55;
  --tracking-body: -0.048px;
  --text-body-lg: 18px;
  --leading-body-lg: 1.50;
  --tracking-body-lg: -0.144px;
  --text-subheading: 20px;
  --leading-subheading: 1.35;
  --tracking-subheading: -0.240px;
  --text-heading-sm: 24px;
  --leading-heading-sm: 1.20;
  --tracking-heading-sm: -0.288px;
  --text-heading: 32px;
  --leading-heading: 1.15;
  --tracking-heading: -0.704px;
  --text-heading-lg: 44px;
  --leading-heading-lg: 1.10;
  --tracking-heading-lg: -1.760px;
  --text-display: 56px;
  --leading-display: 1.05;
  --tracking-display: -2.520px;
  --text-display-xl: 64px;
  --leading-display-xl: 1.00;
  --tracking-display-xl: -3.200px;

  /* Typography — Weights */
  --font-weight-regular: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 600;

  /* Spacing */
  --spacing-4: 4px;
  --spacing-8: 8px;
  --spacing-12: 12px;
  --spacing-16: 16px;
  --spacing-20: 20px;
  --spacing-24: 24px;
  --spacing-32: 32px;
  --spacing-40: 40px;
  --spacing-48: 48px;
  --spacing-64: 64px;
  --spacing-80: 80px;
  --spacing-96: 96px;
  --spacing-128: 128px;

  /* Layout */
  --page-max-width: 1200px;
  --section-gap: 96px;
  --card-padding: 32px;
  --element-gap: 12px;
  --nav-height: 64px;

  /* Border Radius */
  --radius-badge: 4px;
  --radius-button: 6px;
  --radius-input: 6px;
  --radius-card: 8px;
  --radius-largecard: 12px;
  --radius-panel: 16px;
  --radius-pill: 9999px;
  --radius-circle: 9999px;

  /* Shadows */
  --shadow-hairline: rgba(0, 0, 0, 0.06) 0px 0px 0px 1px;
  --shadow-hairline-light: rgba(255, 255, 255, 0.06) 0px 0px 0px 1px inset;
  --shadow-key: rgba(255, 255, 255, 0.04) 0px 1px 0px 0px inset, rgba(0, 0, 0, 0.20) 0px -1px 0px 0px inset, rgba(0, 0, 0, 0.06) 0px 0px 0px 1px;
  --shadow-card: rgba(0, 0, 0, 0.04) 0px 1px 2px 0px;
  --shadow-floating: rgba(15, 45, 82, 0.08) 0px 4px 16px 0px;
  --shadow-accent-glow: rgba(15, 45, 82, 0.20) 0px 4px 12px 0px;

  /* Surfaces */
  --surface-paper: #ffffff;
  --surface-vellum: #fafafa;
  --surface-mist: #f2f2f4;
  --surface-hairline: #e5e5e7;
  --surface-obsidian: #1c1c1e;
  --surface-ink: #2a2a2e;
  --surface-carbon: #0f0f10;
  --surface-midnight-wash: #eaf0f8;

  /* Motion */
  --ease-standard: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-enter: cubic-bezier(0, 0, 0.2, 1);
  --ease-exit: cubic-bezier(0.4, 0, 1, 1);
  --duration-fast: 200ms;
  --duration-base: 300ms;
  --duration-slow: 600ms;
}
```

### 20.2 Tailwind v4

```css
@theme {
  /* Colors */
  --color-paper: #ffffff;
  --color-vellum: #fafafa;
  --color-mist: #f2f2f4;
  --color-hairline: #e5e5e7;
  --color-silver: #c0c0c0;
  --color-fog: #8e8e93;
  --color-stone: #6e6e73;
  --color-slate: #4a4a4e;
  --color-ink: #2a2a2e;
  --color-obsidian: #1c1c1e;
  --color-carbon: #0f0f10;
  --color-bone: #ffffff;
  --color-pearl: #e5e5e7;
  --color-midnight: #0f2d52;
  --color-midnight-deep: #0a1e38;
  --color-midnight-lift: #1e56a0;
  --color-midnight-wash: #eaf0f8;
  --color-signal-green: #2e7d4f;

  /* Typography */
  --font-inter: 'Inter', ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-plex-mono: 'IBM Plex Mono', ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;

  /* Typography — Scale */
  --text-eyebrow: 11px;
  --leading-eyebrow: 1.40;
  --tracking-eyebrow: 0.78px;
  --text-caption: 12px;
  --leading-caption: 1.50;
  --tracking-caption: -0.036px;
  --text-body-sm: 14px;
  --leading-body-sm: 1.55;
  --tracking-body-sm: -0.042px;
  --text-body: 16px;
  --leading-body: 1.55;
  --tracking-body: -0.048px;
  --text-body-lg: 18px;
  --leading-body-lg: 1.50;
  --tracking-body-lg: -0.144px;
  --text-subheading: 20px;
  --leading-subheading: 1.35;
  --tracking-subheading: -0.240px;
  --text-heading-sm: 24px;
  --leading-heading-sm: 1.20;
  --tracking-heading-sm: -0.288px;
  --text-heading: 32px;
  --leading-heading: 1.15;
  --tracking-heading: -0.704px;
  --text-heading-lg: 44px;
  --leading-heading-lg: 1.10;
  --tracking-heading-lg: -1.760px;
  --text-display: 56px;
  --leading-display: 1.05;
  --tracking-display: -2.520px;
  --text-display-xl: 64px;
  --leading-display-xl: 1.00;
  --tracking-display-xl: -3.200px;

  /* Spacing */
  --spacing-4: 4px;
  --spacing-8: 8px;
  --spacing-12: 12px;
  --spacing-16: 16px;
  --spacing-20: 20px;
  --spacing-24: 24px;
  --spacing-32: 32px;
  --spacing-40: 40px;
  --spacing-48: 48px;
  --spacing-64: 64px;
  --spacing-80: 80px;
  --spacing-96: 96px;
  --spacing-128: 128px;

  /* Border Radius */
  --radius-badge: 4px;
  --radius-button: 6px;
  --radius-input: 6px;
  --radius-card: 8px;
  --radius-largecard: 12px;
  --radius-panel: 16px;
  --radius-pill: 9999px;

  /* Shadows */
  --shadow-hairline: rgba(0, 0, 0, 0.06) 0px 0px 0px 1px;
  --shadow-hairline-light: rgba(255, 255, 255, 0.06) 0px 0px 0px 1px inset;
  --shadow-key: rgba(255, 255, 255, 0.04) 0px 1px 0px 0px inset, rgba(0, 0, 0, 0.20) 0px -1px 0px 0px inset, rgba(0, 0, 0, 0.06) 0px 0px 0px 1px;
  --shadow-card: rgba(0, 0, 0, 0.04) 0px 1px 2px 0px;
  --shadow-floating: rgba(15, 45, 82, 0.08) 0px 4px 16px 0px;
  --shadow-accent-glow: rgba(15, 45, 82, 0.20) 0px 4px 12px 0px;
}
```

---

## 21. Performance, SEO, Voice

### 21.1 Performance Contract

- First Contentful Paint < 1.2s on 4G; Largest Contentful Paint < 2.0s
- Images: WebP primary, AVIF where supported, `srcset` with 3 widths, `loading="lazy"` below fold, explicit `width`/`height` to prevent layout shift
- Fonts: Inter and IBM Plex Mono loaded via `font-display: swap`, subset to Latin + Latin Extended, `preconnect` to the font host
- JS: route-level code splitting, no runtime CSS-in-JS, critical CSS inlined for first paint, everything else deferred
- Icons: inline SVG only — no icon font, no sprite network request
- Core Web Vitals: LCP < 2.0s, CLS < 0.05, INP < 200ms

### 21.2 SEO Contract

- Every page ships with a unique `<title>`, `<meta name="description">`, canonical URL, and Open Graph image (1200×630)
- Structured data: `Organization` on the homepage, `SoftwareApplication` on product pages, `BreadcrumbList` on documentation
- Semantic `<h1>`–`<h6>` hierarchy — never skip a level, never use headings for visual styling alone
- Clean URLs (lowercase, hyphens, no query strings on canonical content)
- `sitemap.xml` and `robots.txt` generated at build time
- Language attribute on `<html>` set per locale; `hreflang` on international variants

### 21.3 Voice & Content Rules

Headlines state a capability or outcome — never a slogan. Body copy is factual, specific, and free of marketing adjectives. Numbers are preferred over adjectives ("0.4s" beats "blazing fast"; "99.98% uptime" beats "rock solid"). Every claim must be verifiable or removed. No exclamation marks. No emoji. No "revolutionary", "game-changing", "next-generation", "AI-powered", "cutting-edge", or "world-class". Product names are set in Inter weight 500, not italics, not quotes. The brand name is always "Walden Corp" on first mention and "Walden" thereafter — never "WaldenCorp", never "WALDEN CORP" in body copy.

---

## 22. The Walden Rule

Before any design or code decision ships, five questions must be answered yes:

1. Is it simpler than the alternative?
2. Is it more legible than the alternative?
3. Is it more professional than the alternative?
4. Is it more consistent with this system than the alternative?
5. Is it more performant than the alternative?

If any answer is no, the decision is revised. This rule is the charte's own clause 25, applied to every commit.

> **Walden Corp construit des logiciels qui inspirent confiance, durent dans le temps et produisent des résultats concrets. Chaque détail, du design à la dernière ligne de code, doit refléter cette exigence.**

---

**End of document — Version 2.0**
**Next review:** 12 months from adoption, or upon a material change in brand positioning.
