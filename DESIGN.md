# Design System Document: High-Performance Nutrition & Vitality

## 1. Overview & Creative North Star: "Kinetic Precision"

The Creative North Star for this design system is **Kinetic Precision**. In the world of elite fitness and nutrition, success is found at the intersection of raw energy and scientific accuracy. This system moves away from the "soft and organic" tropes of wellness and instead embraces a high-octane, editorial aesthetic. 

We break the "template" look through **intentional asymmetry** and **high-contrast typography scales**. Imagine a premium sports editorial: large, aggressive headlines paired with ultra-clean, technical data. Layouts should feel like they are in motion, utilizing overlapping elements (e.g., an image bleeding into a `primary_container` section) and expansive white space to create a sense of breathing room and elite performance.

---

## 2. Colors: The High-Contrast Pulse

The color palette is built on a foundation of "Deep Charcoal" (`on_background`) and "Acidic Energy" (`primary`). This contrast mimics the environment of a high-end training facility—dark, focused, and punctuated by bursts of vibrant light.

### Surface Hierarchy & Nesting
We reject the flat grid. Hierarchy is achieved through **Tonal Layering**.
*   **Base Layer:** Use `surface` (#f6f6f9) for the global canvas.
*   **Intermediate Depth:** Use `surface_container_low` (#f0f0f3) for secondary content areas like sidebar backgrounds or content transitions.
*   **Prominent Floating Layers:** Use `surface_container_lowest` (#ffffff) for primary cards or interactive modules to create a "lifted" effect.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. All structural boundaries must be defined by shifts in background tokens (e.g., a `surface_container` section adjacent to a `surface` section). This creates a sophisticated, seamless flow rather than a boxy, fragmented UI.

### The "Glass & Gradient" Rule
To inject "soul" into the technical layout:
*   **Signature Gradients:** For Hero CTAs and high-impact moments, use a linear gradient (135°) transitioning from `primary` (#4e6300) to `primary_fixed` (#cafd00).
*   **Glassmorphism:** For floating navigation bars or overlay modals, use `surface` at 80% opacity with a `20px` backdrop-blur. This ensures the vibrant "Acid Green" energy of the background bleeds through, keeping the UI integrated.

---

## 3. Typography: Editorial Authority

The typography strategy pairs **Space Grotesk** (a technical, quirky Sans-serif) with **Manrope** (a modern, highly legible Sans-serif).

*   **Display & Headlines (Space Grotesk):** These are your "shout" moments. Use `display-lg` (3.5rem) with a negative letter-spacing of `-0.04em` to create a dense, powerful brand presence. Headlines should drive the "Kinetic" feel—don't be afraid to let a headline overlap a container boundary.
*   **Titles & Body (Manrope):** Use `title-lg` for sub-headers to maintain a clean, professional tone. `body-md` (0.875rem) is the workhorse for nutritional data and meal plans, providing a technical, "data-sheet" feel that builds client trust.
*   **Labels (Manrope):** All-caps `label-md` with `0.1em` letter-spacing should be used for categories (e.g., "MACRONUTRIENTS") to mimic the labeling on high-end supplement packaging.

---

## 4. Elevation & Depth: Tonal Dimension

Traditional drop shadows are too "heavy" for a system focused on speed and health. We use light and tone to create depth.

*   **The Layering Principle:** Stack `surface_container_lowest` cards on top of `surface_container_low` sections. The subtle shift from `#f0f0f3` to `#ffffff` provides all the separation required for a premium feel.
*   **Ambient Shadows:** If a floating action button or modal requires a shadow, use the `on_surface` color at 6% opacity with a 32px blur and 16px Y-offset. This mimics natural light, preventing the UI from looking "muddy."
*   **The Ghost Border Fallback:** For input fields or essential containment, use the `outline_variant` (#acadaf) at **20% opacity**. It should be felt, not seen.

---

## 5. Components: The Performance Kit

### Buttons: The "Energy" Variant
*   **Primary:** `primary_container` background with `on_primary_container` text. Use `rounded-md` (0.375rem). The slightly sharp corners feel more "precision-engineered" than full rounds.
*   **Secondary:** Ghost style. No background, `outline` border at 20% opacity, `on_surface` text.

### Cards: The "Editorial" Card
*   **Rule:** Forbid divider lines. Use `spacing-6` (2rem) of vertical white space to separate the image, title, and body text.
*   **Background:** Use `surface_container_lowest`.

### Chips: The "Metric" Chip
*   Used for "High Protein" or "Keto" tags. Use `tertiary_container` (#fcdc43) with `on_tertiary_container` (#5c4e00). These should be `rounded-full` to contrast against the sharper angles of the primary buttons.

### Data Inputs
*   **States:** Default state should use `surface_container_high` background with no border. On focus, transition to a 1px `primary` border to signal "Active/High Performance."

### Performance Specialized Components:
*   **Macro-Trackers:** Use "thick" progress bars (height: `0.5rem`) with `primary` and `secondary_container` colors. No rounded caps; use flat ends for a more "scientific instrument" look.
*   **The "Vibe" Divider:** Instead of a line, use a `32px` vertical gap (Spacing Scale `8`) to denote a change in context.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical margins. For example, give a Hero headline a 10% left margin while the body text stays at 15%.
*   **Do** use the `tertiary` (Gold/Yellow) sparingly for "Success" or "Elite" achievements.
*   **Do** lean into high-contrast "Dark Mode" sections using `inverse_surface` (#0c0e10) to break up a long scrolling page.

### Don't:
*   **Don't** use 100% black. Use `on_background` (#2d2f31) to maintain a sophisticated charcoal depth.
*   **Don't** use standard "Success Green." Use the system's `primary` lime (#4e6300) to keep the brand identity consistent.
*   **Don't** use soft, bubbly corners. Stick to the `md` (0.375rem) scale to maintain the "Precision" aspect of the brand.
*   **Don't** clutter the screen. If a piece of information isn't driving performance, remove it. Use the Spacing Scale `12` (4rem) to let key metrics breathe.