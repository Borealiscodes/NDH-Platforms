# **NDH Documentation Rule Set — SVG Usage (v1.0)**  
### *Formal rules defining where SVGs are allowed, optional, or prohibited across NDH documentation layers*

---

# ⭐ **SVG Rule 1 — SVGs Are Optional, Not Required**  
SVGs MAY be used in NDH documentation, but they are NEVER required.

SVGs are considered an **optional enhancement layer**, not a core documentation layer.

---

# ⭐ **SVG Rule 2 — SVGs MUST NOT appear in Case Studies**  
Case studies follow strict text‑first rules.

Therefore:

### **SVGs MUST NOT be embedded in case studies.**  
### **SVGs MAY be referenced by path (same as PNGs).**

Case studies remain:

- ASCII‑first  
- text‑first  
- GitHub‑native  
- terminal‑readable  
- low‑stimulus  

SVG embedding violates these constraints.

---

# ⭐ **SVG Rule 3 — SVGs MAY be embedded in UX‑oriented documents**  
SVGs are allowed in documents where visual clarity is essential:

- NDH Public Traversal UX  
- NDH Web Ontology (Public Layer)  
- NDH Public Documentation Framework  
- NDH Public Snek Mythos  
- onboarding guides  
- tutorials  
- interactive docs  

SVGs are ideal for:

- scalable icons  
- clean line art  
- vector‑based diagrams  
- responsive visuals  

---

# ⭐ **SVG Rule 4 — SVGs MUST NOT replace ASCII diagrams**  
ASCII diagrams are mandatory in:

- case studies  
- specs  
- conceptual docs  

SVGs are optional enhancements in UX docs, but they **cannot replace ASCII** in narrative or spec layers.

ASCII remains the canonical conceptual representation.

---

# ⭐ **SVG Rule 5 — SVGs MUST NOT be used for emotionally intense visuals**  
SVGs are crisp, sharp, and high‑contrast.

NDH’s trauma‑informed design requires:

- soft edges  
- gentle gradients  
- low‑stimulus visuals  

Therefore:

### **SVGs MUST NOT be used for emotional metaphors, guardians, or snek characters.**  
Use PNGs for those.

SVGs MAY be used for:

- arrows  
- flow diagrams  
- icons  
- structural shapes  

---

# ⭐ **SVG Rule 6 — SVGs MUST remain minimal and stable**  
To avoid architectural drift:

- SVG filenames MUST be stable  
- SVG directory structure MUST be stable  
- SVG count MUST remain minimal  
- SVGs SHOULD be reused when possible  
- SVG updates MUST NOT require case study updates  

SVGs follow the same governance rules as PNGs.

---

# ⭐ **SVG Rule 7 — SVGs MUST NOT be used for complex illustrations**  
SVGs are ideal for:

- simple diagrams  
- icons  
- flow arrows  
- geometric shapes  

SVGs are NOT allowed for:

- Kawaii sneks  
- habitat maps  
- expressive metaphors  
- emotional guardians  
- narrative illustrations  

Those remain PNG‑only.

---

# ⭐ **SVG Rule 8 — SVGs MUST NOT be used where GitHub rendering is inconsistent**  
GitHub sometimes:

- strips SVG metadata  
- blocks inline scripts  
- sanitizes embedded SVGs  
- renders differently across devices  

Therefore:

### **SVGs MUST NOT be used for interactive or script‑based content.**  
### **SVGs MUST NOT rely on embedded animation.**

Only static, safe SVGs are allowed.

---

# ⭐ **SVG Rule 9 — SVGs MUST NOT be required for comprehension**  
SVGs are optional enhancements.

All NDH documentation MUST remain fully comprehensible without them.

Therefore:

### **SVGs MUST NOT carry essential meaning.**  
### **SVGs MUST NOT be the only representation of a concept.**

ASCII + text remain canonical.

---

# ⭐ **SVG Rule 10 — SVGs MUST be stored alongside PNGs**  
SVGs follow the same directory structure:

```
docs/public/img/
```

Examples:

```
docs/public/img/flow-diagram.svg
docs/public/img/ontology-icon.svg
docs/public/img/traversal-arrows.svg
```

This keeps repo governance clean.

---

# ⭐ **Summary — Where SVGs Fit**

### ✔️ **Allowed (optional)**  
- UX docs  
- Web Ontology  
- Traversal UX  
- Public documentation framework  
- Icons  
- Flow diagrams  
- Structural shapes  

### ✔️ **Referenced (not embedded)**  
- Specifications  
- Case studies (reference only)

### ❌ **Prohibited**  
- Case studies (embedding)  
- Emotional metaphors  
- Snek characters  
- Habitat maps  
- Guardians  
- Narrative illustrations  
- Anything requiring animation or scripts  

---
