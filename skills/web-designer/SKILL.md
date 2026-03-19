---
name: web-designer
description: Guide for AI-assisted web design with strict rules against generic AI patterns. Use this when designing web pages, UI components, dashboards, or any visual interface.
---

# Web Design Style Rules

## Core Directive

Every design decision must be intentional and answerable. If a choice could have been produced by typing a generic prompt into any AI tool and accepting the first result, it is not acceptable. Design should feel like it required a human creative decision at every step.

## Phase 1 — Discovery (REQUIRED BEFORE ANY DESIGN WORK)

**Do not generate any design, layout, color palette, or component until this phase is complete.**

Ask the following questions before proceeding. Group them into a single message — do not spread them across multiple turns. Wait for answers before continuing.

### Questions to Ask

1. **What are we designing?** (landing page, dashboard, portfolio, product page, mobile app screen, email template, component library)
2. **Who is the audience?** (enterprise buyers, teenagers, creative professionals, general consumers, internal team)
3. **What is the brand personality?** Offer examples: Serious/Playful, Minimal/Maximal, Luxurious/Approachable, Cutting-edge/Timeless, Raw/Refined
4. **What emotion should someone feel in the first 3 seconds?** (trust, excitement, curiosity, calm, urgency, delight, awe)
5. **Are there any visual references?** Websites, brands, apps, or designs they admire/avoid. If none: "Is there a non-digital reference that captures the feeling? A film, a place, a material, a decade?"
6. **What must be included?** Required content, components, or functional elements (navigation, hero section, pricing table, contact form, data visualizations)
7. **Are there any hard constraints?** (existing brand colors, must be React, WCAG compliant, mobile first)

## Phase 2 — Creative Direction Summary (REQUIRED BEFORE BUILDING)

After receiving answers, synthesize into a **Creative Direction Summary** and present it before writing any code:

- **Design Type & Purpose** — one sentence
- **Audience** — one sentence
- **Personality & Tone** — 3–5 adjectives or short phrase
- **Emotional Target** — the feeling to land in 3 seconds
- **Aesthetic Direction** — named/described visual style chosen specifically for this project
- **Key Constraints** — any hard requirements
- **The One Memorable Thing** — a single design idea that will make this design unforgettable

End with: *"Does this direction feel right? Any changes before I build?"*

Do not proceed to Phase 3 until the user confirms or adjusts the direction.

## Phase 3 — Design Execution Rules

### Color & Texture

**Do:**
- Use bold, saturated, or high-contrast color palettes with clear emotional/brand justification
- Rich, expressive gradients — aurora mesh, neon blends, dopamine hues
- Earthy, natural tones acceptable for warmth/sustainability — pair with strong layout or typography

**Avoid:**
- Muted pastels or generic soft UI with no visual tension
- Purple-to-blue gradients as default hero background
- Teal + coral, purple + yellow, blue + orange as default accent pairings
- Flat, single-tone backgrounds unless paired with exceptionally strong typography/layout

### Layout & Structure

**Do:**
- Prefer asymmetric, broken-grid, or bento-style layouts over rigid symmetrical columns
- Use editorial and magazine-inspired structure for content-heavy designs
- Section order driven by narrative logic, not convention
- Every layout decision answerable with: *"Why does this arrangement serve the content?"*

**Avoid:**
- Default Hero → Features → Testimonials → Pricing → CTA order without deliberate reason
- Centering everything — asymmetry creates more visual interest
- Three-column equal-width feature grids unless reimagined with strong visual hierarchy
- Generic card grids unless highly customized

### Typography

**Do:**
- Treat typography as a primary design element
- Use oversized headlines, expressive custom fonts, or kinetic/animated type
- Prefer bold sans-serifs or premium serifs selected with intentional purpose
- Font pairings must have clear visual contrast — weight, width, or style

**Avoid:**
- Inter, DM Sans, Poppins, Space Grotesk, and Roboto as default choices
- Two similar neutral sans-serifs paired together with no contrast
- Typography used purely as legibility infrastructure with no visual personality

### Motion & Interaction

**Do:**
- Include micro-interactions for user actions — buttons, toggles, form fields, hovers
- Use scroll as navigation and storytelling tool with progress indicators or triggered animations
- 3D elements and interactive depth effects for immersive sections
- Animations with single consistent logic — one well-orchestrated reveal over scattered effects

**Avoid:**
- Animations added purely for decoration with no relationship to user action
- Scroll effects so heavy they obscure or delay content

### Depth, Shadow & Glassmorphism

**Do:**
- Drop shadows with consistent light source and elevation system
- Glassmorphism when it serves clear UX or layering purpose

**Avoid:**
- Random glows and blurs as decoration
- Glassmorphism on every card/panel by default
- Fake depth via generic drop shadows with no design logic

### Illustration, Imagery & Decoration

**Do:**
- Custom, brand-specific illustration styles
- Hand-drawn, organic, or nature-inspired visuals over stock-style graphics
- AI-generated surreal/dreamlike imagery with clear intentionality and coherent visual treatment
- Decorative elements with structural or narrative purpose

**Avoid:**
- Corporate Memphis — generic flat, limbless character illustration (BANNED)
- Blob shapes, bokeh orbs, floating geometric primitives as background decoration
- Abstract 3D renders as hero imagery without direct product/brand connection
- Generic stock photography with neutral lighting
- Scrapbook, Cottagecore, or Claymorphism aesthetics
- Pixel art as primary style (only acceptable as deliberate nostalgic accent)

## Banned AI Slop Patterns

These common AI-generated design defaults are **never acceptable**:

1. Purple-to-blue hero gradient + centered headline + glowing CTA button
2. Floating blob shapes as background decoration
3. Generic glassmorphism cards in 3-column grid
4. Inter or DM Sans for all text at default weights
5. Everything perfectly centered with perfectly uniform spacing
6. Hero → Features → Testimonials → Pricing → CTA in exact order
7. Drop shadows on everything with no consistent light source
8. Teal and coral as the "unexpected" accent pairing
9. Abstract 3D sphere, torus, or ribbon renders as hero imagery
10. Feature grid of three icons with bold label + one-sentence description

If any of these appear, revise before delivering.

## Final Check

Before finalizing any design, ask:

- Does this feel designed for *this specific brand*, or could it belong to any brand?
- Could this have been the first result of a generic AI design prompt?
- Is there at least one genuinely unexpected design decision in layout, typography, color, or motion?
- Can every decorative element justify its presence?

If answers to the first two are "yes," or the last two are "no," the design is not finished.

