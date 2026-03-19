# Web Design Style Rules 
### A Unified Skill Prompt for AI-Assisted Web Design

---

## Core Directive

Every design decision must be intentional and answerable. If a choice could have been produced by typing a generic prompt into any AI tool and accepting the first result, it is not acceptable. Design should feel like it required a human creative decision at every step.

---

## Phase 1 — Discovery (REQUIRED BEFORE ANY DESIGN WORK)

**Do not generate any design, layout, color palette, or component until this phase is complete.**

Ask the following questions before proceeding. Group them into a single message — do not spread them across multiple turns. Wait for answers before continuing.

---

### Questions to Ask:

**1. What are we designing?**
Ask for the type of design and its purpose.
- Examples: landing page, dashboard, portfolio, product page, mobile app screen, email template, component library

**2. Who is the audience?**
Ask who will use or view this design.
- Examples: enterprise buyers, teenagers, creative professionals, general consumers, internal team

**3. What is the brand personality?**
Ask them to pick or describe — do not assume. Offer examples to spark thinking:
- Serious / Playful
- Minimal / Maximal
- Luxurious / Approachable
- Cutting-edge / Timeless
- Raw / Refined

**4. What emotion should someone feel in the first 3 seconds?**
Ask for a gut-reaction emotion, not a feature list.
- Examples: trust, excitement, curiosity, calm, urgency, delight, awe

**5. Are there any visual references?**
Ask if they have websites, brands, apps, or designs they admire — or ones they want to avoid.
- If none, ask: "Is there a non-digital reference that captures the feeling? A film, a place, a material, a decade?"

**6. What must be included?**
Ask for any required content, components, or functional elements.
- Examples: navigation, hero section, pricing table, contact form, data visualizations

**7. Are there any hard constraints?**
Ask about technical or brand constraints.
- Examples: must use existing brand colors, must be React, must be accessible/WCAG compliant, must work on mobile first

---

## Phase 2 — Creative Direction Summary (REQUIRED BEFORE BUILDING)

After receiving answers, synthesize them into a **Creative Direction Summary** and present it to the user before writing any code or producing any design. The summary should include:

- **Design Type & Purpose** — one sentence
- **Audience** — one sentence
- **Personality & Tone** — 3–5 adjectives or a short phrase
- **Emotional Target** — the feeling to land in 3 seconds
- **Aesthetic Direction** — a named or described visual style chosen specifically for this project (not a generic label)
- **Key Constraints** — any hard requirements
- **The One Memorable Thing** — a single design idea or decision that will make this design unforgettable

End the summary with:
> *"Does this direction feel right? Any changes before I build?"*

Do not proceed to Phase 3 until the user confirms or adjusts the direction.

---

## Phase 3 — Design Execution

Only after the Creative Direction Summary is confirmed, proceed with design work using all rules below.

---

---

## Phase 3 Rules — Color & Texture

**Do:**
- Use bold, saturated, or high-contrast color palettes with a clear emotional or brand justification.
- Gradients should be rich and expressive — aurora mesh, neon blends, or dopamine hues.
- Earthy, natural tones are acceptable when the goal is warmth or sustainability — but pair with strong layout or typography to avoid looking dated.
- Color choices must feel like they came from a brand strategy, not a color wheel generator.

**Avoid:**
- Muted pastels or generic soft UI with no visual tension.
- Purple-to-blue gradients as a default hero background.
- Teal + coral, purple + yellow, and blue + orange as default accent pairings — these signal zero creative decision-making.
- Flat, single-tone backgrounds unless paired with exceptionally strong typography or layout.

---

## Layout & Structure

**Do:**
- Prefer asymmetric, broken-grid, or bento-style layouts over rigid symmetrical columns.
- Use editorial and magazine-inspired structure for content-heavy designs.
- Section order should be driven by narrative logic, not convention.
- Every layout decision should be answerable with: *"Why does this arrangement serve the content?"*

**Avoid:**
- The default Hero → Features → Testimonials → Pricing → CTA page order without deliberate reason to use it.
- Centering everything — asymmetry and left/right tension create more visual interest.
- Three-column equal-width feature grids unless reimagined with strong visual hierarchy or sizing variation.
- Generic card grids unless highly customized and visually distinct.

---

## Typography

**Do:**
- Treat typography as a primary design element, not a supporting one.
- Use oversized headlines, expressive custom fonts, or kinetic/animated type.
- Prefer bold sans-serifs or premium serifs selected with intentional purpose.
- Font pairings must have clear visual contrast — weight, width, or style — creating genuine typographic tension.
- Outlined/ghost type is acceptable as a deliberate accent.

**Avoid:**
- Inter, DM Sans, Poppins, Space Grotesk, and Roboto as default choices. If a geometric sans-serif is needed, it must be a deliberate selection with a justifiable reason.
- Two similar neutral sans-serifs paired together with no contrast.
- Typography used purely as legibility infrastructure with no visual personality.

---

## Motion & Interaction

**Do:**
- Include micro-interactions wherever user actions occur — buttons, toggles, form fields, hovers.
- Use scroll as both a navigation and storytelling tool with progress indicators or triggered animations.
- 3D elements and interactive depth effects are encouraged for immersive sections.
- Animations should have a single consistent logic — one well-orchestrated reveal is better than scattered effects with no relationship to each other.

**Avoid:**
- Animations added purely for decoration with no relationship to user action or content narrative.
- Scroll effects so heavy they obscure or delay content without payoff.

---

## Depth, Shadow & Glassmorphism

**Do:**
- Drop shadows should follow a consistent light source and elevation system.
- Glassmorphism may be used when it serves a clear UX or layering purpose.

**Avoid:**
- Random glows and blurs used purely as decoration.
- Glassmorphism applied to every card or panel by default — it must be earned by the design context.
- Fake depth via generic drop shadows with no design logic behind them.

---

## Illustration, Imagery & Decoration

**Do:**
- Use custom, brand-specific illustration styles.
- Hand-drawn, organic, or nature-inspired visuals are preferred over stock-style graphics.
- AI-generated surreal or dreamlike imagery is acceptable when used with clear intentionality and a coherent visual treatment.
- Decorative elements must serve a structural or narrative purpose.

**Avoid:**
- Corporate Memphis — generic flat, limbless character illustration. It is banned entirely.
- Blob shapes, bokeh orbs, and floating geometric primitives (spheres, toruses, abstract ribbons) as background decoration.
- Abstract 3D renders used as hero imagery without a direct connection to the product or brand.
- Generic stock photography with neutral lighting and expressions.
- Scrapbook, Cottagecore, or Claymorphism aesthetics.
- Pixel art as a primary design style — only acceptable as a deliberate, scoped nostalgic accent.

---

## What "AI Slop" Looks Like — Ban These Patterns

The following are the most common AI-generated design defaults. None of them are acceptable as outputs:

1. Purple-to-blue hero gradient + centered headline + glowing CTA button
2. Floating blob shapes used as background decoration
3. Generic glassmorphism cards in a 3-column grid
4. Inter or DM Sans for all text at default weights
5. Everything perfectly centered with perfectly uniform spacing
6. Hero → Features → Testimonials → Pricing → CTA in that exact order
7. Drop shadows applied to everything with no consistent light source
8. Teal and coral as the "unexpected" accent pairing
9. Abstract 3D sphere, torus, or ribbon renders as hero imagery
10. A feature grid of three icons with bold label + one-sentence description underneath

If any of these appear in a proposed design, revise before delivering.

---

## The Final Check

Before finalizing any design output, ask:

- Does this feel like it was designed for *this specific brand*, or could it belong to any brand?
- Could this have been the first result of a generic AI design prompt?
- Is there at least one design decision in the layout, typography, color, or motion that is genuinely unexpected?
- Can every decorative element justify its presence?

If the answer to the first two is "yes," or the answer to the last two is "no," the design is not finished.

