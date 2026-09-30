# handoff.md: Pique Dame Poster Generator Project

## 1. Project Overview & Objective
* **Goal:** Build an automated poster generator tool capable of generating layouts following the visual language of Jan Tschichold’s 1927 *Pique Dame* cinema poster[cite: 1, 2].
* **Core Paradigm:** The generator relies on declarative markdown instructions (`skills.md`) as its design engine, ensuring typography, hierarchy, geometry, and color inversions remain structurally consistent across runs.

---

## 2. Completed Work & Key Decisions

* **Typographic Identification & Selection:**
  * **Original Type:** Identified as *Venus Grotesk Bold / Fett* (Bauer Foundry, 1907)[cite: 1].
  * **Selected Open-Source Replacements:** Work Sans (Bold/Black), Epilogue, and Syne (Extra Bold) from Google Fonts, or VTF Grotesk from Velvetyne.
  * *Reasoning:* These faces replicate early European grotesque structural quirks (high-waisted bars on `P`, `E`, and `A`; prominent bowls; abrupt terminal cuts) that neutral neo-grotesques like Helvetica lack[cite: 1].

* **Visual Deconstruction & Iteration:**
  * **Global Slant:** Corrected initial assumptions regarding text orientation. All four tiers of typography share a uniform ascending angle of approximately +20° to +25° counter-clockwise[cite: 1, 2].
  * **Dynamic Color Inversion:** Identified and codified the knockout effect[cite: 2]. Letters passing through the diagonal gray stripe ("QUE" and "MIT JE") invert to white rather than staying black[cite: 2].
  * **Geometric Scaffolding:** Documented the slightly tilted vertical gray stripe (~ -5° to -7° from vertical) and its intersection with the circular portrait frame[cite: 2].

* **Specification Document (`skills.md`):**
  * Formulated and finalized the complete ruleset covering canvas borders, geometry, portrait halftone treatment, typographic tiers, tracking rules, and color codes[cite: 1, 2].

---

## 3. File Registry & Architecture

* **`skills.md`**: The master ruleset and prompt instruction file for the generator. Contains exact layout coordinates, angle constraints, hierarchy definitions, and palette values.
* **`handoff.md`**: This document; logs design decisions, technical specifications, and project continuity instructions.
* **Source Reference Assets:**
  * `image_274160.jpg`: Full view of the 1927 *Pique Dame* poster by Jan Tschichold for Phoebus-Palast[cite: 2].
  * `image_273217.jpg`: Close-up detail showing the headline typography and inverted color mechanics[cite: 1].

---

## 4. Next Steps for Implementation

1. **Scaffold the Generator Engine:**
   * Select the rendering target (e.g., HTML/Canvas, SVG, or a Python script using PIL/Cairo/Pillow).
   * Implement the outer border, cream base `#F4F0E8`, and the rotated background gray pillar.
2. **Implement Masking & Inversion Layers:**
   * Build the circular mask with its split-tone backing (pure white crescent overlapping the pillar, cream elsewhere).
   * Implement clipping/masking logic (such as CSS `mix-blend-mode: difference`, SVG `clipPath`, or duplicate layered text nodes) to automate the white knockout of text crossing the gray stripe[cite: 2].
3. **Build the Dynamic Typographic Layout:**
   * Load the selected open-source grotesque typeface.
   * Apply the universal +20° to +25° rotation matrix across all four text tiers[cite: 1, 2].
   * Set up input parameters (Title, Credits, Venue, Times, Portrait URL) so the tool can accept new inputs and output posters adhering to `skills.md`.
