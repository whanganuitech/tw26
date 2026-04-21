# Design System Document: Techweek 2026 Whanganui

## 1. Overview & Creative North Star: "The Neon Pulse"
This design system is engineered to transform a regional tech event into a high-end digital destination. Moving away from rigid corporate grids, "The Neon Pulse" centers on a **High-End Editorial** aesthetic that balances the depth of deep New Zealand nights with the high-energy fluorescence of the tech sector.

**Creative North Star: The Neon Pulse**
The experience should feel like a premium tech journal—authoritative yet vibrating with energy. We achieve this by breaking the "template" look through:
*   **Intentional Asymmetry:** Headlines and imagery should overlap and offset to create a sense of movement.
*   **Tonal Immersion:** Using deep navy as a canvas to make the vibrant pinks feel like light sources rather than mere accents.
*   **Breathing Room:** Oversized margins and generous vertical whitespace to signify luxury and professionalism.

---

## 2. Colors
The palette is derived from the collision of deep maritime blues and synthetic magentas, optimized for a professional-tech atmosphere.

### Core Tokens
*   **Primary (Navy):** `#000d25` – Our anchor. Use for high-contrast backgrounds and authoritative text.
*   **Secondary (Vibrant Pink):** `#b6005a` – Our pulse. Reserved for interaction points and critical data highlights.
*   **Tertiary (Midnight):** `#000f20` – Used for subtle depth shifts in dark-mode containers.

### The "No-Line" Rule
**Borders are prohibited for sectioning.** To separate a "Speakers" section from an "Agenda" section, do not use a 1px line. Instead, shift the background from `surface` (`#f8f9fa`) to `surface-container-low` (`#f3f4f5`). In dark layouts, shift from `primary` to `primary_container`. Let color change define the boundary.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Use the surface-container tiers to create nested depth:
1.  **Base:** `surface` (The floor)
2.  **Section:** `surface-container-low` (Subtle lift)
3.  **Card/Component:** `surface-container-lowest` (The highest point of focus)

### The "Glass & Gradient" Rule
To elevate the "tech-focus," use **Glassmorphism** for navigation bars and floating chips. 
*   **Formula:** `surface` at 70% opacity + `backdrop-blur: 12px`.
*   **Signature Texture:** Main CTAs or Hero sections should employ a subtle linear gradient from `secondary` (`#b6005a`) to `secondary_container` (`#e10f73`) at a 135-degree angle.

---

## 3. Typography
We utilize a dual-font strategy to balance technical precision with human-centric readability.

*   **Display & Headlines (Plus Jakarta Sans):** A high-performance sans-serif with a tech-leaning geometry. 
    *   *Usage:* Use `display-lg` (3.5rem) for hero statements with tight letter-spacing (-0.02em).
*   **Body & Titles (Manrope/Raleway):** Following the user's requirement for **Raleway**, we use it for body copy and titles to provide a clean, approachable, yet modern feel.
    *   *Usage:* `body-lg` for general content. Ensure `line-height` is set to 1.6 for maximum readability against high-contrast backgrounds.

The hierarchy is intentionally dramatic. A `display-lg` headline should sit near a `label-md` date tag to create an editorial, high-contrast visual rhythm.

---

## 4. Elevation & Depth
In "The Neon Pulse," depth is organic and light-based, not structural.

*   **The Layering Principle:** Avoid shadows on standard elements. Place a `surface-container-lowest` card on a `surface-container-low` background. The slight tonal shift provides all the "lift" needed.
*   **Ambient Shadows:** For floating elements like the "Register Now" FAB or a "Featured Event" card, use:
    *   **Shadow:** `0px 20px 40px rgba(0, 13, 37, 0.08)` (A tinted version of our primary navy). Large blur, very low opacity.
*   **The "Ghost Border" Fallback:** If accessibility requires a container edge, use `outline-variant` at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons
*   **Primary:** Gradient fill (`secondary` to `secondary_container`), white text, `md` (0.75rem) roundedness. No border.
*   **Secondary:** Ghost style. Transparent background, `secondary` text, and a `secondary` 1px border at 30% opacity.
*   **Tertiary:** Text-only, capitalized `label-md` with a vibrant pink arrow icon.

### Cards
Cards must never have visible borders.
*   **Style:** `surface-container-lowest` fill, `md` rounded corners, and a 4% ambient shadow.
*   **Layout:** Use asymmetrical padding (e.g., 2rem top, 1.5rem sides) to break the "standard box" look.

### Input Fields
*   **State:** Neutral state uses `surface-container-high` background.
*   **Focus:** Transition background to `white` and add a 2px `secondary` (Pink) bottom-border only. This mimics a "terminal" or tech-entry feel.

### Additional Component: "The Pulse Indicator"
A small, glowing dot using `secondary` with a CSS animation (scale/opacity) used next to "Live Events" or "Active Now" labels to reinforce the energetic tech theme.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use `secondary_fixed_dim` (light pink) for text on dark navy backgrounds to ensure high-end legibility without the harshness of pure white.
*   **Do** allow images to break the container. A speaker's head should overlap the top edge of a card.
*   **Do** use the `full` roundedness scale (9999px) for "Tech Tags" (Chips) to create a soft contrast against sharp typography.

### Don't:
*   **Don't** use black. Ever. Use `primary` (#000d25) for your darkest tones.
*   **Don't** use a standard grid for the hero. Offset the text to the left and the primary imagery to the right with a slight vertical stagger.
*   **Don't** use dividers between list items. Use 24px of vertical whitespace or a subtle background shift between items.