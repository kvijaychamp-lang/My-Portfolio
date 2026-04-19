# Design System Document: The Neural Architect

## 1. Overview & Creative North Star
**Creative North Star: "The Digital Curator"**

This design system is built to reflect the precision of machine learning and the fluidity of artificial intelligence. We are moving away from the "template" look of generic developer portfolios. Instead, we embrace a **High-End Editorial** approach. 

The aesthetic is rooted in "The Digital Curator"—a style that treats code and data as high art. We achieve this through intentional asymmetry, massive typographic scales that bleed off the edges, and a sophisticated layering of dark surfaces. By prioritizing breathing room and tonal depth over rigid borders, we create an environment that feels less like a website and more like a high-tech terminal interface designed for a premium gallery.

---

## 2. Colors & The Tonal Philosophy

The palette is anchored in deep charcoal with hyper-saturated "data-stream" accents.

### The Palette (Material Design Convention)
- **Primary (Neon Blue):** `#c3f5ff` (Primary), `#00e5ff` (Container)
- **Secondary (Emerald Green):** `#40e56c` (Secondary), `#02c953` (Container)
- **Surface (The Charcoal Base):** `#131313` (Base), `#201f1f` (Container), `#0e0e0e` (Lowest)
- **Accents (Tertiary Gold):** `#ffeac0` (Tertiary)

### The "No-Line" Rule
Explicitly prohibit 1px solid borders for sectioning. Structural boundaries must be defined solely through background color shifts. For example, a project showcase section should transition from `surface` to `surface-container-low` to define its start. Lines are for grids; depth is for content.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—stacked sheets of frosted glass.
- **Nesting:** Place a `surface-container-highest` card inside a `surface-container` section to create a soft, natural lift. 
- **The "Glass & Gradient" Rule:** Floating elements (like navigation bars or hovering cards) must use Glassmorphism. Utilize a semi-transparent `surface` color with a `backdrop-blur` (12px–20px).
- **Signature Textures:** Use linear gradients for main CTAs, transitioning from `primary` (#c3f5ff) to `primary-container` (#00e5ff) at a 135-degree angle. This adds a "lithographic" soul to the interface.

---

## 3. Typography: Editorial Tech

We use a duo-font system to balance technical precision with high-fashion editorial impact.

- **Display & Headlines (Space Grotesk):** This is our "Tech-Forward" voice. Use `display-lg` (3.5rem) for hero statements. Don't be afraid to use `tight` letter-spacing (-0.02em) to make the type feel like a solid block of data.
- **Body & Labels (Inter):** Our "Functional" voice. Inter provides maximum legibility for project descriptions and code snippets.
- **Editorial Intent:** Use `headline-lg` for section titles, but place them asymmetrically—perhaps rotated 90 degrees or offset into the margin—to break the "F-pattern" grid and force the user to engage with the layout.

---

## 4. Elevation & Depth

We eschew traditional drop shadows for **Tonal Layering**.

- **The Layering Principle:** Depth is achieved by stacking. A `surface-container-lowest` element on a `surface-container-low` background creates a "recessed" look, perfect for code blocks.
- **Ambient Shadows:** When a "floating" effect is mandatory, shadows must be extra-diffused. Use a 32px blur with 6% opacity, tinted with the `on-surface` color.
- **The "Ghost Border" Fallback:** If a container needs more definition (e.g., in high-density data visualizations), use a **Ghost Border**. This is a 1px border using `outline-variant` at 15% opacity. Never use 100% opaque borders.
- **Glassmorphism:** Apply to any element that "hovers" over the main content (Modals, Dropdowns). This ensures the "deep charcoal" background always bleeds through, maintaining the dark-mode immersion.

---

## 5. Components

### Buttons
- **Primary:** High-contrast `primary-container` (#00e5ff) with `on-primary` text. Use `xl` (0.75rem) roundedness.
- **Secondary:** Transparent background with a `Ghost Border` and `primary` text.
- **Interaction:** On hover, the primary button should emit a soft glow (diffused shadow) using the `primary` color at 20% opacity.

### Project Cards (The Signature Component)
- **Visuals:** Use `surface-container-high`. No borders.
- **Effects:** Apply a subtle `backdrop-blur` and a 10% opacity `Ghost Border`.
- **Content:** Forbid divider lines. Use vertical white space (from the Spacing Scale) to separate the title from the metadata.

### Chips (Data Tags)
- **Style:** Small, `full` roundedness. 
- **Color:** Use `secondary-container` (#02c953) for "Success/Stable" AI models and `primary-container` (#00e5ff) for "In-Progress/Experimental" tech.

### Input Fields
- **Style:** Underline only or `surface-container-lowest` filled background.
- **Focus:** Transition the "Ghost Border" to a 100% opaque `primary` line on focus.

### Additional Suggestion: The "Code Terminal" List
Instead of standard list items, use a "Terminal" style list for technical skills. Use `surface-container-lowest` with a blinking cursor effect on the `primary` accent to reinforce the ML engineer persona.

---

## 6. Do's and Don'ts

### Do:
- **Use Intentional Asymmetry:** Overlap an image of a neural network over a text block.
- **Embrace Large Spacing:** Use double the expected white space between sections to create a "gallery" feel.
- **Use Tonal Transitions:** Shift background colors slightly to indicate new content areas.

### Don't:
- **No Divider Lines:** Never use a `<hr>` or a 1px solid border to separate list items or sections.
- **No Pure Black:** Stick to the defined `#131313` and its variants. Pure `#000000` kills the tonal depth of the charcoal.
- **No Default Shadows:** Avoid the "fuzzy grey" shadow. If it doesn't look like light hitting glass, don't use it.
- **No Standard Grids:** Avoid perfectly centered, symmetrical layouts. They feel like templates. Move elements off-center to create visual tension.