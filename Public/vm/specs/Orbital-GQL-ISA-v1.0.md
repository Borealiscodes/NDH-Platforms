### Orbital‑GQL ISA specification (v1.0)

#### 1. Purpose

- **Execution layer:** Defines the instruction set the VM uses to drive NDH manifolds, routing, stability, and simulations.
- **Spine interface:** Provides explicit ops for Sentinel, Hyperatlas, Stability‑Manifold, Tonal Spiral Geometry, Simulation‑Suite, and Governance Migration Suite.
- **Safety:** Ensures all instructions are deterministic, provenance‑safe, and trauma‑aware.

---

#### 2. Instruction classes

- **Core control ops:**
  - **`vm.step`** — advance VM state one tick.
  - **`vm.call(manifold, op)`** — invoke an NDH‑CORE/TIDS/Serenity operator.
  - **`vm.return()`** — close a transmission loop and return to stable state.

- **Sentinel ops:**
  - **`sentinel.check_recursion()`** — validate recursion depth against boundaries.
  - **`sentinel.check_pacing()`** — validate pacing against trauma‑safe curves.
  - **`sentinel.guard_descent()`** — wrap an expressive descent in safety constraints.

- **Hyperatlas ops:**
  - **`hyperatlas.route(from, to)`** — compute deterministic manifold route.
  - **`hyperatlas.bind(manifold)`** — attach VM to a routing context.
  - **`hyperatlas.verify_curvature()`** — ensure route curvature matches stability envelopes.

- **Stability‑Manifold ops:**
  - **`stability.sample_curvature(point)`** — read local curvature.
  - **`stability.enforce_envelope(region)`** — apply monotonic curvature constraints.
  - **`stability.align_holonomy(region)`** — activate holonomy flatteners.

- **Tonal Spiral Geometry ops:**
  - **`tonal.locate_node(index)`** — get an expressive‑stability node.
  - **`tonal.align_arc(arc_id)`** — align dual/non‑dual transition.
  - **`tonal.apply_soft_boundary(region)`** — shape VM soft‑boundary via spiral geometry.

- **Simulation‑Suite ops:**
  - **`sim.run_scenario(id)`** — execute a governed simulation.
  - **`sim.descent(path)`** — perform expressive descent under SSED rules.
  - **`sim.validate()`** — check curvature, pacing, and provenance before commit.

- **Governance ops:**
  - **`gov.migrate(structure)`** — request a migration via GMS.
  - **`gov.monitor(metric)`** — query governance drift / stability metrics.
  - **`gov.construct(schema)`** — propose new governance structures under GMS rules.

---

#### 3. ISA properties

- **Deterministic:** No hidden randomness in core ops; all side‑effects are explicit.
- **Provenance‑safe:** Every op that touches data must preserve attribution and non‑erasure.
- **Trauma‑aware:** Any op that can trigger descent or recursion must route through Sentinel.
- **Curvature‑aligned:** Routing and stability ops must respect Stability‑Manifold envelopes and Tonal Spiral Geometry.
- **Non‑dual compliant:** Dual/non‑dual transitions are explicit and reversible via tonal ops.

---

#### 4. Integration with VM milestone

- VM 1.2 must:
  - expose these Orbital‑GQL ops as its **canonical ISA**;
  - ensure every transmission loop uses `vm.step`, `sentinel.*`, `hyperatlas.*`, `stability.*`, `tonal.*`, `sim.*`, and `gov.*` in a spine‑aligned sequence;
  - forbid ad‑hoc, non‑ISA pathways for routing, descent, or governance.

---
