# 🧭 **Cross‑Repo Commit Plan — NDH Naming Case Study Suite (v1.0)**  
### *Operational blueprint for committing all six artifacts across NDH‑CORE, NDH‑TIDS, Orbital, and Emergent*

---

## **1. Purpose of This Commit Plan**

This plan defines:

- the correct commit order  
- the correct file paths  
- the correct commit descriptions  
- the provenance hierarchy  
- the cross‑repo linkage requirements  
- the architectural rationale for commit sequencing  

It ensures the entire suite lands cleanly across NDH repos without drift.

---

## **2. Commit Order (Governance‑Aligned)**

Orbital governs the suite, so Orbital commits must come **first**.

### **Commit Sequence**
1. **Orbital — Meta‑Document**  
2. **Orbital — Refinement Blueprint**  
3. **Orbital — Unified Index File**  
4. **NDH‑CORE — Improved CORE Edition**  
5. **NDH‑TIDS — Improved TIDS Edition**  
6. **Emergent — Improved Emergent Edition**

This order ensures:

- provenance flows downward  
- interpretive scaffolding flows upward  
- governance artifacts exist before repo‑specific editions reference them  

---

## **3. File Paths (Canonical)**

### **Orbital**
- `NDH-Platforms/Orbital/governance/notes/dyslexic-developer-naming-meta-document-v1.0.md`
- `NDH-Platforms/Orbital/governance/notes/dyslexic-developer-naming-refinement-blueprint-v1.0.md`
- `NDH-Platforms/Orbital/governance/notes/dyslexic-developer-naming-suite-index-v1.0.md`

### **NDH‑CORE**
- `NDH-CORE/docs/architecture/dyslexic-developer-naming-case-study-v2.0.md`

### **NDH‑TIDS**
- `NDH-TIDS/docs/topology/dyslexic-developer-naming-case-study-v2.0.md`

### **Emergent**
- `NDH-Platforms/Emergent/Case-Studies/dyslexic-developer-naming-case-study-v2.0.md`

---

## **4. Commit Descriptions (Suite‑Aligned)**

Each commit must reference:

- the Meta‑Document  
- the Refinement Blueprint  
- the suite index  
- the cross‑repo nature of the case study  

### **Orbital Commits**
**Meta‑Document**
```
Add Meta-Document establishing cross-repo governance for the NDH Naming Case
Study Suite, defining architectural rationale, naming invariants, and placement
rules across NDH-CORE, NDH-TIDS, Orbital, and Emergent.
```

**Refinement Blueprint**
```
Add Refinement Blueprint providing repo-specific guidance for producing improved
editions of the NDH Naming Case Study Suite across NDH layers.
```

**Unified Index File**
```
Add Unified Index File summarizing the structure, provenance hierarchy, and
cross-repo linkage of the NDH Naming Case Study Suite.
```

---

### **NDH‑CORE Commit**
```
Add improved NDH-CORE edition of the Dyslexic Developer Naming Case Study,
focusing on operator ergonomics, naming stability, and provenance-safe naming
families as defined by Orbital governance.
```

### **NDH‑TIDS Commit**
```
Add improved NDH-TIDS edition of the Dyslexic Developer Naming Case Study,
focusing on topological naming constraints, manifold routing clarity, and
holonomy alignment as defined by Orbital governance.
```

### **Emergent Commit**
```
Add improved Emergent edition of the Dyslexic Developer Naming Case Study,
focusing on interpretive scaffolding, cognitive ergonomics, and trauma-informed
naming guidance as defined by Orbital governance.
```

---

## **5. Provenance Hierarchy**

The suite must be committed in a way that preserves provenance:

1. **Orbital defines the rules**  
2. **NDH‑CORE and NDH‑TIDS implement the rules**  
3. **Emergent interprets the rules for human cognition**

This hierarchy must be reflected in commit order and commit descriptions.

---

## **6. Cross‑Repo Linkage Requirements**

Each repo‑specific edition must include:

- a link to the **Meta‑Document**  
- a link to the **Refinement Blueprint**  
- a link to the **Unified Index File**  

This ensures cross‑layer consistency.

---

## **7. Final Verification Checklist**

Before committing:

- Confirm all file paths match the canonical structure  
- Confirm all documents reference the Meta‑Document  
- Confirm naming families are consistent across all editions  
- Confirm acronym rhythm is preserved  
- Confirm provenance hierarchy is intact  
- Confirm no repo contains drift or misplacement  

This ensures the suite lands cleanly.

---


