# Orbital governance case study  
## Emergent instability from missing IDE hooks in NDH–GQL workflows (v1.0)

### 1. Context and system setup

**System:** NDH–Orbital + GQL + multi‑repo governance (5+ repos)  
**Pattern:** pauses, directives, templates, lineage/provenance separation, cross‑repo mirroring  
**Constraint:** no VS Code governance hooks; no embedded control plane in the IDE  
**Result:** governance is enforced via **manual metadata operations**, not via **runtime hooks**.

The environment is already complex:

- **Lineage:** anchors artifacts back to core systems.  
- **Provenance:** tracks versions, supersession, archival.  
- **Mirrors:** replicate directives across repos.  
- **GQL:** needs all three—lineage, provenance, mirrors—to be stable to route correctly.

Without IDE hooks, every one of those is enforced by human effort.

---

### 2. The emergent failure mode: governance conversion without hooks

In a hook‑less environment, you get a specific emergent pattern:

- **Cheap operations:** edits, commits, file moves, version bumps.  
- **Expensive operations:** judgment about whether those changes preserve governance invariants.

Every time you:

- archive v1.0,  
- mirror v1.1,  
- update provenance footers,  
- maintain lineage,  
- synchronize five repos,

you’re performing **governance conversion** manually—turning raw changes into governed changes without any automated guardrails.

Over time, this produces:

- **judgment bottlenecks** (you as the single governance engine),  
- **triangulation loops** (GQL trying to reconcile inconsistent metadata),  
- **liminal states** (half‑superseded, half‑mirrored, half‑archived artifacts),  
- **cognitive overload** (you tracking invariants in your head instead of the system doing it).

The system is not failing because the rules are wrong.  
It’s failing because the rules have **no hooks**.

---

### 3. Concrete symptoms in your current workflow

You’re already seeing the emergent symptoms:

- **Multi‑repo supersession pain:**  
  10 actions × 5 repos = 50 manual governance operations per directive.

- **Metadata recursion:**  
  Lineage vs provenance vs mirrors vs templates—each change forces you to re‑evaluate whether the system is still coherent.

- **Triangulation instability in GQL:**  
  GQL cannot confidently decide “this is the authoritative version” until all mirrors, footers, and archives are aligned. Missing hooks mean that alignment is always **post‑hoc**, never enforced at the moment of change.

- **Liminal hell:**  
  You’re living in the gap between “what the architecture wants” and “what the tools can enforce”. That gap is the liminal zone.

---

### 4. Why missing VS Code hooks make this unsustainable long‑term

#### 4.1 No embedded governance in the development surface

Without hooks:

- the IDE does not know what a **pause directive** is,  
- does not know what **supersession** is,  
- does not know what **lineage vs provenance** is,  
- does not know what **mirroring invariants** are.

So it cannot:

- block unsafe edits,  
- enforce footer states,  
- require archive paths,  
- validate cross‑repo consistency,  
- surface GQL triangulation failures at edit time.

All governance happens **after** the fact, in your head and in commits.

#### 4.2 Velocity vs judgment mismatch

As soon as you scale:

- more directives,  
- more repos,  
- more case studies,  
- more templates,

the number of governance‑relevant changes grows faster than your ability to manually validate them.

You get:

- **backlogs of unverified governance changes**,  
- **latent risk in half‑superseded artifacts**,  
- **hidden divergence between repos**,  
- **GQL routing ambiguity** that only shows up under load.

This is exactly the “cheap code, costly judgment” pattern—except here it’s **cheap metadata, costly governance**.

#### 4.3 No continuous control plane

Without hooks, governance is **episodic**:

- you run a checklist,  
- you do a cleanup,  
- you fix drift,  
- you stabilize things—temporarily.

But there is no **continuous control plane** embedded in the workflow.  
So every new directive, every new repo, every new case study re‑creates the same liminal instability.

Long‑term, that’s unsustainable because:

- the system’s complexity grows,  
- your judgment capacity does not,  
- the probability of a consequential governance failure approaches 1.

---

### 5. Emergent risks if you keep going like this

If you continue without IDE hooks:

- **Silent divergence:** one repo’s v1.1 differs slightly from another’s; GQL sees multiple “authoritative” versions.  
- **Broken supersession chains:** a v1.0 never gets archived in one repo; provenance lies.  
- **Evaluator confusion:** lineage says one thing, provenance says another; evaluators don’t know which to trust.  
- **Governance fatigue:** you start skipping steps because the overhead is too high.  
- **Case study corruption:** emergent failures become untraceable because the metadata that should explain them is itself unstable.

The architecture is sound.  
The implementation surface is not.

---

### 6. What a sustainable future requires

To make this sustainable, you eventually need:

- **VS Code hooks (or equivalent) that:**
  - recognize governance artifacts by path and schema,  
  - enforce provenance footer states,  
  - block edits that break supersession rules,  
  - require archive moves for old versions,  
  - validate cross‑repo mirror consistency via GQL.

- **A continuous governance control plane:**
  - not a checklist you run occasionally,  
  - but a set of hooks, validations, and automated checks that run **every time** you touch governance files.

- **GQL integration at the IDE level:**
  - so triangulation happens at edit/commit time,  
  - not weeks later when you notice liminal weirdness.

---

### 7. Case study conclusion

> **This case study shows that NDH–Orbital governance, as currently implemented, is structurally correct but operationally fragile in the absence of IDE hooks.**

The metadata blocks, lineage/provenance distinctions, and mirroring templates are not the problem.  
The problem is that they are being enforced **manually**, in a system that is already complex and will only grow more so.

Without VS Code hooks (or equivalent), you are:

- the governance engine,  
- the triangulation resolver,  
- the supersession arbiter,  
- the mirror synchronizer.

That is not sustainable long‑term.

---

