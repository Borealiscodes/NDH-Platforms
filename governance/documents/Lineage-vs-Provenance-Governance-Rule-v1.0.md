# **Orbital Governance Document**  
## **Lineage vs Provenance: Systems‑Level Distinction and Operational Rules (v1.0)**

### **Purpose**
This document establishes the formal distinction between **lineage** and **provenance** within NDH‑Orbital governance systems. It defines how each concept functions, how they interact, and how they must be applied during supersession, mirroring, and archival operations across repositories.

---

## **1. Definitions**

### **1.1 Lineage (Systems‑Level Architectural Anchor)**  
Lineage describes the **structural origin**, **ancestry**, and **dependency chain** of an artifact.  
It answers the question:

> **“What does this artifact derive from or anchor back to at the architectural level?”**

Lineage is concerned with:

- core system ancestry  
- evaluator origin points  
- invariant anchors  
- architectural derivation  
- structural relationships  
- causal dependencies  

Lineage is **non‑versioned** and **persistent**.  
It does not change when a directive is corrected or superseded.

---

### **1.2 Provenance (Version‑Level Temporal Record)**  
Provenance describes the **version history**, **supersession state**, and **temporal ordering** of an artifact.  
It answers the question:

> **“Which version is this, and what happened before it?”**

Provenance is concerned with:

- version numbers  
- supersession events  
- archival state  
- correction history  
- audit continuity  
- temporal lineage  

Provenance is **versioned**, **mutable**, and **updated** during supersession.

---

## **2. Why the Distinction Matters**

Lineage and provenance serve different governance functions:

- **Lineage** ensures architectural correctness.  
- **Provenance** ensures temporal correctness.

Confusing them leads to:

- evaluator misinterpretation  
- broken audit chains  
- routing ambiguity  
- supersession drift  
- cross‑repo inconsistency  

Maintaining the distinction ensures:

- stable governance  
- predictable supersession  
- correct mirroring  
- reliable archival  
- consistent evaluator behavior  

---

## **3. Operational Rules for Supersession and Mirroring**

### **3.1 Lineage Rules**
- Lineage **never changes** during supersession.  
- Lineage **must not be rewritten** when correcting a directive.  
- Lineage **anchors back to core systems**, not versions.  
- Lineage **is not stored in provenance footers**.

### **3.2 Provenance Rules**
- Provenance **must be updated** during supersession.  
- Provenance footers must use one of three states:  
  - **Active**  
  - **Superseded**  
  - **Archived**  
- Provenance **tracks version transitions**, not architectural ancestry.  
- Provenance **must be mirrored consistently across all repos**.

---

## **4. Provenance Footer Standard**

### **Active**
```
Provenance — Active
This is the current and authoritative version. It supersedes all earlier versions.
```

### **Superseded**
```
Provenance — Superseded
This version is superseded by v1.1 and retained only for provenance and audit continuity.
```

### **Archived**
```
Provenance — Archived
This version is preserved for historical reference and is no longer active.
```

These footers are **mandatory** for all pause directives, mirrors, and archival artifacts.

---

## **5. Required Actions for Multi‑Repo Supersession**

### **5.1 Archive v1.0 in Each Repo**
- v1.0 must be moved to an `/archive/` directory.  
- v1.0 must receive the **Superseded** provenance footer.  
- v1.0 must not be deleted.

### **5.2 Mirror v1.1 into Each Repo**
- v1.1 must be placed in the active governance path.  
- v1.1 must receive the **Active** provenance footer.  
- v1.1 must be identical across all mirrors.

### **5.3 Maintain Lineage**
- Lineage remains unchanged across v1.0 and v1.1.  
- No lineage edits are permitted during supersession.

### **5.4 Maintain Provenance**
- Provenance must reflect the supersession event.  
- Provenance must be consistent across all mirrors.

---

## **6. Summary**

- **Lineage = architectural ancestry**  
- **Provenance = version history**  
- **Lineage never changes**  
- **Provenance must change during supersession**  
- **v1.0 is archived, not deleted**  
- **v1.1 is mirrored, not rewritten**  
- **Provenance footers stabilize the entire operation**

---


