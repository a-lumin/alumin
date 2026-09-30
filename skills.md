# skills.md: Pique Dame Poster Generation Protocol

## 0. Meta-Information
This file serves as the definitive specification for the programmatic poster generator tool. It encodes the visual grammar, spatial geometry, typographic rules, and contrast systems derived from Jan Tschichold’s 1927 *Pique Dame* cinema poster. Any poster output produced by this tool must adhere strictly to these rules to maintain historical and structural integrity.

---

## 1. Canvas & Framing
* **Aspect Ratio:** Standard portrait format (approximately 1:1.41 to 1:1.5).
* **Outer Margin / Border:** Generous, uniform unprinted border around all four edges (paper margin effect), enclosing the active visual field.
* **Canvas Substrate:** Warm off-white, light cream, or unbleached newsprint tone across the base.

---

## 2. Geometric Scaffolding & Asymmetry
* **The Slanted Pillar (Gray Band):**
  * A broad, translucent or screen-printed gray stripe traverses the composition vertically from top to bottom.
  * **Tilt Angle:** Slanted slightly counter-clockwise (approximately -5° to -7° from vertical).
  * **Horizontal Position:** Offset into the left-to-middle third of the composition.
* **The Circle Composite:**
  * Positioned in the upper half of the poster, anchored to the right of the vertical centerline.
  * The left portion of the circle intersects the slanted gray pillar.
  * **Split-Tone Background:** The circle ring is split into two halves:
    * The left crescent (overlapping the gray pillar) has a clean, solid white background field.
    * The right semicircle frames the photographic element directly on the cream field.

---

## 3. Photographic Element (The Portrait)
* **Cropping & Masking:** Masked cleanly within the upper circular zone.
* **Tonal Treatment:** High-contrast, monochromatic black-and-white photogravure/halftone reproduction with heavy ink density in dark areas (shadows around eyes, hair, lips).
* **Subject Demeanor:** Dramatic side-angle gaze directed downward and rightward, establishing a dynamic diagonal axis that counters the ascending diagonal of the typography.

---

## 4. Typographic Hierarchy & Layout Rules

### 4.1 Global Angle of Text
* **Universal Slant:** Unlike conventional layouts, **all four text tiers are set on an identical ascending diagonal angle** (approximately +20° to +25° counter-clockwise from the horizontal baseline), rising sharply from lower-left to upper-right.

### 4.2 Hierarchy Tiers
1. **Tier 1 — Main Title ("PIQUEDAME"):**
   * **Font Style:** Bold, early German Grotesque (Venus Grotesk archetype / Work Sans Black / Epilogue Bold).
   * **Scale:** Dominant, ultra-large display scale.
   * **Position:** Sweeps across the lower half of the poster, cutting straight through the gray band.
2. **Tier 2 — Secondary Credits ("MIT JENNY JUGO UND RUD. FORSTER"):**
   * **Scale:** Small, single-line caption directly tucked beneath the baseline of the main title.
   * **Position:** Aligned under the second half of the title ("DAME").
3. **Tier 3 — Venue ("PHOEBUSPALAST"):**
   * **Scale:** Medium display, approximately 35–40% scale of Tier 1.
   * **Position:** Bottom-right quadrant, staggered below Tier 2 along the same diagonal axis.
4. **Tier 4 — Screening Details / Times ("ANFANG: 4.00..."):**
   * **Scale:** Micro-caption, light/medium weight, tracked wide, set directly below the venue title.

### 4.3 Overprint & Tonal Inversion Rule (Crucial Mechanism)
* The typography dynamically interacts with the background layers:
  * **Over the Cream Field:** Letters are solid, deep black ink.
  * **Over the Gray Pillar:** Letters crossing the gray vertical band drop out to white (knockout/negative reverse) or tint to a lighter tone, creating visual vibration across the seam.
  * Specifically seen in:
    * The letters **"QUE"** in `PIQUEDAME` invert to white against the gray band.
    * The prefix **"MIT JE"** in the credits subline drops to white against the gray band.

---

## 5. Color Palette & Ink Specification
* **Base Paper:** `#F4F0E8` (Aged cream / off-white)
* **Gray Pillar:** `#9C9993` (Cool/neutral mid-gray, ~40% ink density)
* **Primary Ink:** `#1A1817` (Deep carbon black)
* **Knockout / Highlight:** `#FFFFFF` (Pure white reserved for inversions and the circular crescent highlight)
