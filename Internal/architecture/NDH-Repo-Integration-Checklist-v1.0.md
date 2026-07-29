# 🛰️ **NDH Repo Integration Checklist (Internal Asset v1.0)**  
### *Authoritative rules for file placement, versioning, commit discipline, provenance, artifact lifecycle, and search‑engine alignment*

**Scope:** Internal — Developer Grade  
**Status:** Foundational Governance Asset  
**Version:** 1.0  
**Purpose:** Ensure every NDH artifact is placed correctly, versioned correctly, described correctly, and indexed correctly — preventing drift and guaranteeing architectural coherence.

---

# ⭐ 1 — Directory Structure Rules

All NDH internal artifacts must follow this structure:

```
NDH-Platforms/
    Internal/
        architecture/
        governance/
        telemetry/
        search/
        companions/
        reports/
    Public/
        docs/
        diagrams/
        companions/
        reports/
```

### Internal placement rules

- **architecture/**  
  Foundational system documents (registry, taxonomy, search engine model, GQL spec, dataset plan, repo checklist).

- **governance/**  
  Policy sets, invariants, compliance logic.

- **telemetry/**  
  Raw dataset schemas, ingestion rules, normalization logic.

- **search/**  
  Internal search engine configuration, indexing rules.

- **companions/**  
  Internal versions of all companions.

- **reports/**  
  Internal versions of Emergent, Meta, Meta‑Meta reports.

### Public placement rules

- **docs/**  
  Public‑safe explanations, conceptual summaries.

- **diagrams/**  
  Public architecture diagrams, flowcharts.

- **companions/**  
  Public companions (AI‑Zen, Accessibility/Snek, Ethics, Philosophy).

- **reports/**  
  Public Emergent/Meta/Meta‑Meta reports.

---

# ⭐ 2 — File Naming Rules

Every file must follow:

```
NDH-{Artifact-Name}-v{Major}.{Minor}.md
```

Examples:

- `NDH-Report-and-Companion-Registry-v1.0.md`
- `NDH-Public-Internal-Report-Taxonomy-v1.0.md`
- `NDH-Search-Engine-Creator-Model-v1.0.md`
- `NDH-GQL-Processing-Specification-v1.0.md`
- `NDH-Raw-Dataset-Population-Plan-v1.0.md`
- `NDH-Repo-Integration-Checklist-v1.0.md`

### Versioning rules

- **Major version increments**  
  Structural changes, schema changes, governance changes.

- **Minor version increments**  
  Clarifications, expansions, additional examples.

---

# ⭐ 3 — Commit Description Rules

Every commit must include:

### 3.1 Commit Title

Format:

```
internal-architecture: add/update {Artifact Name} v{Version}
```

### 3.2 Commit Body

Must include:

- purpose of the artifact  
- where it was placed  
- why it matters  
- dependencies  
- downstream impact  

This ensures search engines and governance systems can parse commit metadata.

---

# ⭐ 4 — Provenance & Citation Footer Rules

Every internal artifact must include a footer:

```
---
**NDH Provenance:** Internal Artifact  
**Scope:** Developer Grade  
**Layer:** {Telemetry | GQL | Internal | Public | Search | Repo}  
**Version:** v{Major}.{Minor}
```

Public artifacts use:

```
---
**NDH Provenance:** Public-Safe Summary  
**Scope:** External  
**Version:** v{Major}.{Minor}
```

This ensures search engines can classify artifacts correctly.

---

# ⭐ 5 — Artifact Lifecycle Rules

### Lifecycle stages:

1. **Draft**  
   - placed in `/Internal/architecture/drafts/`  
   - not indexed  

2. **Internal Release**  
   - placed in correct internal directory  
   - indexed by developer‑grade search engine  

3. **Public Release**  
   - sanitized  
   - placed in `/Public/`  
   - indexed by accessible search engine  

4. **Archived**  
   - moved to `/Internal/archive/`  
   - removed from active indexing  

### Rules:

- Internal artifacts must never be moved directly to public.  
- Public artifacts must never reference internal mechanics.  
- Archived artifacts must retain provenance.

---

# ⭐ 6 — Search Engine Integration Rules

### Developer‑Grade Search Engine indexes:

- internal reports  
- internal companions  
- GQL specs  
- telemetry schemas  
- governance math  
- repo governance rules  
- version metadata  
- provenance footers  

### Accessible Search Engine indexes:

- public reports  
- public companions  
- public diagrams  
- public summaries  
- public glossaries  

### Both engines require:

- correct file paths  
- correct versioning  
- correct provenance footers  
- correct artifact type declarations  

---

# ⭐ 7 — Drift Prevention Rules

To prevent drift:

- every artifact must declare its **type**  
- every artifact must declare its **scope**  
- every artifact must declare its **governance layer**  
- every artifact must declare its **epistemic lens**  
- every artifact must include a **provenance footer**  
- every artifact must follow **file naming rules**  
- every artifact must follow **directory placement rules**  
- every commit must follow **commit description rules**

This is the NDH invariant.

---

# ⭐ 8 — Repo Integration Checklist (Zen‑Clean Summary)

> **Place it correctly.  
> Name it correctly.  
> Version it correctly.  
> Describe it correctly.  
> Declare its scope.  
> Declare its layer.  
> Add provenance.  
> Commit cleanly.  
> Index correctly.  
> Prevent drift.**

This checklist ensures NDH’s entire knowledge architecture remains coherent.

---

