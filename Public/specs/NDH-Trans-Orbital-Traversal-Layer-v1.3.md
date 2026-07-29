### NDH Trans‑Orbital Traversal Layer v1.3  
#### *SVG Structural Diagrams Edition — Public Specification*

---

## 1 — Purpose

Version 1.3 extends the Trans‑Orbital Traversal Layer by:

- defining **SVG structural diagrams** for traversal,
- mapping orbital geometry into vector‑friendly shapes,
- specifying constraints for SVG usage (no emotional content),
- preparing the UX layer to render traversal flows consistently.

This version does **not** embed SVGs; it defines their structure and behavior.

---

## 2 — SVG Design Principles for Trans‑Orbital Traversal

- **Structural only:** SVGs represent orbits, paths, arrows, and boundaries.
- **No emotional content:** no faces, characters, or expressive metaphors.
- **Stable geometry:** shapes must remain consistent across versions.
- **Low stimulus:** minimal color, no animation, no flashing.
- **Reference‑only in specs:** SVGs are referenced by path, embedded only in UX docs.

---

## 3 — Core SVG Artifacts

**3.1 — Orbital Rings Diagram**

- **File:**  
  `docs/public/img/trans-orbital-rings.svg`

- **Content:**  
  - three concentric rings:
    - outer: Shallow Orbit  
    - middle: Medium Orbit  
    - inner: Deep Orbit  
  - labeled text for each orbit.
  - optional subtle arrows indicating allowed transitions (S→M→D, D→M→S).

---

**3.2 — Traversal Flow Diagram**

- **File:**  
  `docs/public/img/trans-orbital-flow.svg`

- **Content:**  
  - linear flow: Entry Gate → Orbital Selector → Depth & Pace → Guardian → Exit.
  - arrows between nodes.
  - rectangular nodes with labels:
    - Entry Gate  
    - Orbital Path Selector  
    - Depth & Pace Controller  
    - Guardian Interventions  
    - Exit / Soft Landing  

---

**3.3 — Recursion Map Diagram**

- **File:**  
  `docs/public/img/trans-orbital-recursion-map.svg`

- **Content:**  
  - stacked layers:
    - Shallow (R0)  
    - Medium (R1)  
    - Deep (R2)  
  - arrows showing recursion allowed only in Medium/Deep.
  - visual indication that Shallow has no recursion.

---

## 4 — SVG Usage Constraints

- **In specs:**
  - SVGs are referenced by path only.
  - No inline embedding.
  - ASCII remains canonical.

- **In UX docs:**
  - SVGs may be embedded.
  - Used for:
    - diagrams,
    - flow charts,
    - structural maps.
  - Must remain non‑overwhelming and trauma‑informed.

---

## 5 — Relationship to PNG Assets

- **PNG:** expressive, gentle visuals (Sneks, habitats, envelopes).
- **SVG:** structural diagrams (rings, arrows, flow).

Both are governed by:

- trauma‑informed design,
- minimalism,
- stability,
- clear separation of roles.

---

## 6 — Summary

Trans‑Orbital v1.3:

- keeps ASCII as canonical,
- introduces SVG structural diagrams as optional UX‑layer assets,
- defines file paths and constraints,
- prepares the traversal system for visual rendering without breaking NDH governance.

---

