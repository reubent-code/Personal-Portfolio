# Portfolio Design System: High-End Editorial Strategy

## 1. Overview & Creative North Star: "The Digital Curator"

This design system is built to transform a standard portfolio into a high-end editorial experience. Our Creative North Star is **The Digital Curator**: a philosophy that treats every project like a gallery installation rather than a list of links.

To break the "template" look, we move away from rigid, symmetrical grids. Instead, we utilize **Intentional Asymmetry**—where large-scale typography (Display-LG) creates a focal point that allows imagery to sit slightly off-center, creating a sense of motion and high-fashion layout. We prioritize "white space" as a functional element, using the `spacing.20` and `spacing.24` tokens to force the user to breathe between case studies.

## 2. Colors: Tonal Depth & The Accent

The palette is rooted in a "Dark Mode" luxury aesthetic, using deep charcoals to provide a canvas for the electric `primary` cyan.

* **Primary (`#c3f5ff`):** Use sparingly for "High-Impact" moments—CTAs, active navigation states, and key highlights.
* **Surface Hierarchy:** We utilize a "Nesting" strategy to create depth without borders.
  * **Level 0 (Base):** `surface` (`#131313`) for the main page background.
  * **Level 1 (Sections):** `surface_container_low` (`#1c1b1b`) for subtle section grouping.
  * **Level 2 (Interactive):** `surface_container_high` (`#2a2a2a`) for cards and floating elements.

### The "No-Line" Rule

**Explicit Instruction:** Do not use 1px solid borders to define sections. All boundaries must be established through color shifts. A case study section might sit on `surface`, while the "About" section below it shifts to `surface_container_low`. This creates a seamless, premium flow.

### The "Glass & Gradient" Rule

To add "soul" to the UI, use a subtle radial gradient on the Hero background: transitioning from `surface` at the edges to a faint `primary_container` (`#00e5ff`) at 5% opacity in the center. For floating navigation bars, use `surface_variant` at 60% opacity with a `backdrop-blur` of 20px.

## 3. Typography: The Editorial Scale

We pair the architectural strength of **Manrope** for headings with the functional clarity of **Inter** for body text.

* **Display-LG (Manrope, 3.5rem):** Reserved for hero headlines. Use a tight letter-spacing (-0.02em) to create a "locked" editorial feel.
* **Headline-MD (Manrope, 1.75rem):** Used for project titles. Pair this with `primary` color for high-contrast emphasis.
* **Body-LG (Inter, 1rem):** The workhorse for case study descriptions. Ensure a line-height of 1.6 to maintain readability against the dark background.
* **Label-MD (Inter, 0.75rem):** All-caps with increased letter-spacing (0.1em) for category tags (e.g., "UI/UX," "2024").

## 4. Elevation & Depth: Tonal Layering

Traditional shadows are often too "heavy" for a minimalist portfolio. We use **Tonal Layering** to define hierarchy.

* **The Layering Principle:** Place a `surface_container_highest` card on top of a `surface_container_low` section. This `12px` shift in hex value provides enough contrast for the human eye to perceive "lift" without visual clutter.
* **Ambient Shadows:** If a card must float (e.g., on hover), use a shadow tinted with `on_surface` at 4% opacity.
  * *Spec:* `box-shadow: 0 20px 40px rgba(229, 226, 225, 0.04);`
* **The "Ghost Border" Fallback:** If accessibility requires a stroke, use `outline_variant` (`#3b494c`) at 20% opacity. Never use 100% opaque outlines.

## 5. Components

### Elegant Project Cards

* **Layout:** No borders. The image should be the container.
* **Hover State:** Transition the image scale (1.05x) and shift the background from `surface_container` to `surface_bright`.
* **Typography:** Title in `headline-sm`, Category in `label-sm` (Primary color).

### Primary Buttons

* **Default:** `primary` background with `on_primary` text. Use `rounded.md` (0.375rem) for a modern, sharp look.
* **Style:** Instead of a flat fill, apply a subtle linear gradient from `primary` to `primary_fixed_dim`.

### Navigation

* **Style:** Floating centered dock or top-fixed bar.
* **Visual:** Use the Glassmorphism rule (60% `surface` + blur). Use `spacing.3` for vertical padding and `spacing.6` for horizontal padding.

### Contact Forms

* **Inputs:** Use `surface_container_highest` for the input field background.
* **Indicator:** Instead of a full-box border, use a 2px bottom-border of `outline` that transitions to `primary` on focus.
* **Error State:** Use `error` text for helper messages, never change the entire input background to red—keep it sophisticated.

## 6. Do's and Don'ts

### Do:

* **Use Massive Padding:** If you think there is enough space, add `spacing.8` more. High-end design thrives on "wasteful" space.
* **Animate Transitions:** Use a `cubic-bezier(0.2, 0, 0, 1)` curve for all hover states to create a "weighted," expensive feel.
* **Mix Type Alignments:** Try left-aligning your `Display-LG` headlines while center-aligning your `body-md` captions for an editorial look.

### Don't:

* **Don't Use Dividers:** Never use a `<hr>` or a 1px line to separate content. Use a `spacing.16` gap or a background color shift.
* **Don't Use Pure Black:** Always use `surface` (#131313). Pure black (#000) feels "dead" and reduces the effectiveness of our tonal layering.
* **Don't Overuse the Accent:** If everything is Electric Blue, nothing is. Reserve `primary` for the "Path to Conversion" (CTAs and Links).
