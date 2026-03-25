# Design System Document: The Scholastic Lab Aesthetic

## 1. Overview & Creative North Star: "The Digital Observatory"
This design system is built to reflect the intersection of elite academia and high-stakes venture building. The Creative North Star is **"The Digital Observatory"**—a visual language that feels like a high-end research interface: precise, expansive, and quietly powerful. 

We move beyond the "startup template" by rejecting standard boxed layouts. Instead, we utilize an intentional asymmetry and a "data-first" editorial approach. The interface should feel like a redacted intelligence report or a laboratory terminal—heavy on negative space, driven by rigorous typography, and defined by tonal depth rather than structural lines.

## 2. Colors: Tonal Sophistication
The palette is a monochromatic spectrum designed to evoke the materials of future technology: brushed aluminum, dark obsidian, and glowing screens.

- **Primary (`#ffffff`) & Secondary (`#c6c6cb`):** Used strictly for high-priority information and high-contrast interaction points.
- **Surface Hierarchy:** The "Dark Lab" environment is built using `surface` (`#131313`) as the base.
- **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Boundaries between content areas must be achieved solely through shifts in surface tokens. For example, a "Research Paper" section should transition from `surface` to `surface-container-low` to define its edge.
- **The "Glass & Gradient" Rule:** Floating elements (like navigation bars or hover-state cards) must use Glassmorphism. Apply `surface_container` with a 60% opacity and a `20px` backdrop-blur. 
- **Signature Textures:** Use a subtle radial gradient transitioning from `surface_bright` (#393939) at the top-left to `surface` (#131313) at the bottom-right in hero sections to create a sense of physical curvature and premium depth.

## 3. Typography: Editorial Authority
The type system pairs the technical precision of **Space Grotesk** for headlines with the ubiquitous clarity of **Inter** for data and body.

- **Display & Headline (Space Grotesk):** These should be tracked slightly tighter (-2% to -4%) to create a "dense" professional feel. Use `display-lg` (3.5rem) sparingly for high-impact statements.
- **Body & Labels (Inter):** Body copy should maintain a generous line-height (1.6) to ensure the "academic" feel remains readable. 
- **Hierarchy as Identity:** Use `label-md` (`#919191`) in all caps with `0.1rem` letter spacing for metadata (e.g., "RESEARCH PHASE // 01") to mimic technical schematics.

## 4. Elevation & Depth: Tonal Layering
In a "future tech" aesthetic, shadows do not exist in the traditional sense; they are represented by light emission or atmospheric occlusion.

- **The Layering Principle:** Depth is achieved by stacking. Place a `surface-container-highest` (`#353535`) element inside a `surface-container-low` (`#1b1b1b`) area to create a "lifted" interactive card.
- **Ambient Shadows:** For floating modals, use a shadow with a `48px` blur, 0px offset, and 8% opacity of the `on-surface` color. This creates a "glow" rather than a shadow.
- **The "Ghost Border" Fallback:** If a separator is required for accessibility, use the `outline-variant` token (`#474747`) at **15% opacity**. It should be felt, not seen.
- **Logo Integration:** Partner logos (YC, Fiserv, MassMutual, RTX) should be rendered in a monochromatic "Silver" (`#c6c6cb`) with a `0.6` opacity. On hover, they transition to `primary` (`#ffffff`) with 100% opacity.

## 5. Components: Precision Primitives

### Buttons
- **Primary:** `surface` text on a `primary` (#ffffff) background. 0.25rem (`DEFAULT`) corner radius. No border.
- **Secondary:** `on_surface` text with a "Ghost Border" (15% opacity `outline-variant`).
- **Interaction:** On hover, primary buttons should trigger a subtle `surface_tint` glow.

### Cards & Lists
- **The "No-Divider" Mandate:** Never use horizontal lines to separate list items. Use a `1rem` (4) spacing gap or a slight `surface-container` background shift on hover.
- **Research Cards:** Large vertical spacing (`spacing-12`) between headline and body text to emphasize the "Editorial" layout.

### Input Fields
- **Styling:** Minimalist bottom-stroke only or a subtle `surface-container-high` background. 
- **Focus State:** Transition the background to `surface-container-highest` and the label to `primary`.

### Specialized Components for dorm.network
- **The "Founder Grid":** A non-linear masonry layout for student profiles using varying `surface-container` tiers to distinguish between "Active" and "Alumni" founders.
- **The "Node Connector":** A visual graphic component using `outline-variant` lines (15% opacity) to connect related research topics, mimicking a neural network.

## 6. Do's and Don'ts

### Do:
- **Use Asymmetry:** Place a `display-lg` headline on the left and a small `body-sm` block of text on the far right.
- **Respect the Grid:** While elements can be asymmetric, they must align to the underlying grid columns to maintain "Academic" rigor.
- **Embrace Darkness:** Let the `surface` color breathe. Large areas of empty charcoal space signify premium quality.

### Don't:
- **Don't use pure black (#000000):** Use the `surface` token to keep the design "inky" and sophisticated, not "cheap" or "empty."
- **Don't use high-contrast borders:** This breaks the immersion of a futuristic, seamless interface.
- **Don't use standard icons:** Use "Thin" or "Light" weight iconography to match the `outline` weight. Avoid filled, bulky icons.

## 7. Spacing & Geometry
- **Corners:** Stick to the `DEFAULT` (0.25rem) or `sm` (0.125rem) for a sharp, engineered feel. Avoid `xl` or `full` except for specific status chips.
- **Rhythm:** Use `spacing-20` (5rem) between major sections to provide the "academic breathing room" required for a high-end research vibe.