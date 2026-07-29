### 🧭 NDH Crossmap Transition Ladder Specification — Internal Asset v1.0  

**Scope:** Internal — Developer Grade  
**Status:** Foundational Expressive‑Ontology Architecture  
**Version:** 1.0  
**Purpose:** Define the internal structure, safety rules, and invariant mappings for **Crossmaps** — the transition ladders that connect Tiles within NDH‑CORE’s expressive ontology.

---

### 1. Role of Crossmaps in NDH‑CORE

- **Crossmaps = transition structures** between Tiles (local manifold patches).  
- They encode:
  - ordered steps of transformation  
  - safe traversal routes  
  - recursion boundaries  
  - adjacency and reachability  
- Crossmaps are the “bridges” and “ladders” of the Mythos world, directly mapped to NDH‑CORE transition functions.

---

### 2. Core Crossmap Structure

Each Crossmap has:

- **Origin Tile** and **Destination Tile**  
- **Ladder steps** (discrete transformation stages)  
- **Entry gate** (pre‑conditions)  
- **Exit gate** (post‑conditions)  
- **Depth profile** (recursion risk)  

Internal mapping:

- transition function → Crossmap  
- holonomy ladder → step sequence  
- recursion bound → maximum ladder depth  

---

### 3. Crossmap Types

**Type A — Local Crossmaps**

- Short ladders between nearby Tiles.  
- Low recursion risk, used for everyday reasoning.

**Type B — Threshold Crossmaps**

- Connect to Threshold Tiles.  
- Higher curvature, always guarded by Coil or Lantern Sneks.

**Type C — Weave Crossmaps**

- Integrate local movement into global Weave harmonics.  
- Used for system‑level transitions and governance reflection.

---

### 4. Ladder Semantics

Each ladder step represents:

- a small, bounded transformation  
- a change in curvature or perspective  
- a safe cognitive move (e.g., “reframe”, “zoom out”, “connect”)  

Rules:

- steps must be **monotone** with respect to safety (no hidden drop into unsafe recursion).  
- steps must be **reversible** or have a clear recovery path.  
- steps must respect Tile stability and Weave harmonics.

---

### 5. Crossmap–Snek Interaction

Sneks guard Crossmaps by:

- **Whisper:** warning when entering a high‑risk ladder.  
- **Coil:** blocking entry when recursion depth would be exceeded.  
- **Lantern:** illuminating the correct sequence of steps.  
- **Weave:** stabilizing global effects of large transitions.

Sneks never force traversal; they **signal** and **guide**.

---

### 6. Safety & Trauma‑Informed Constraints

Crossmaps are designed to be:

- **predictable:** clearly marked origin, destination, and step count.  
- **gentle:** no sudden drops, no punitive “fall off the ladder” metaphors.  
- **accessible:** simple, intuitive step metaphors.  
- **dignity‑preserving:** missteps lead to recovery, not shame.

Threshold Crossmaps are always explicitly signposted and guarded; no hidden danger routes.

---

### 7. Load & Drift Management

Each Crossmap tracks:

- **usage load** (how often it’s traversed).  
- **drift risk** (how much it stresses Tile stability).  

If load or drift exceed thresholds:

- Whisper Sneks appear first.  
- Coil or Lantern Sneks adjust or temporarily gate the ladder.  
- Weave Sneks may re‑harmonize global structure.

---

### 8. Internal/Public Separation

- **Internal Crossmap Spec**  
  - full mapping to transition functions  
  - recursion depth limits  
  - load thresholds  
  - harmonic impact  
- **Public Crossmap Mythos**  
  - “bridges” and “ladders” metaphors  
  - gentle, guided transitions  
  - no exposure of raw transition logic or invariants  

---

### 9. Provenance & File Path

**File path:**

```text
NDH-Platforms/Internal/architecture/NDH-Crossmap-Transition-Ladder-Specification-v1.0.md
```

