# **NDH Documentation Governance Charter v1.0**  
### *Foundational governance for all NDH public‑layer documentation artifacts*

---

## ⭐ 1 — Purpose of This Charter  
The NDH Documentation Governance Charter defines the **rules, constraints, and layer boundaries** that govern all documentation produced within the NDH ecosystem.

Its goals are:

- maintain architectural stability  
- prevent documentation drift  
- preserve trauma‑informed design principles  
- ensure clarity and accessibility  
- enforce consistent visual and narrative patterns  
- define how ASCII, PNG, and SVG assets are used  
- establish boundaries between narrative and UX layers  

This Charter is the **constitution** for NDH documentation.

---

## ⭐ 2 — Documentation Layer Model  
NDH documentation is divided into **three layers**, each with its own rules.

### **2.1 — Narrative Layer (Case Studies)**  
- text‑first  
- ASCII diagrams only  
- no embedded PNGs  
- no embedded SVGs  
- low‑stimulus  
- GitHub‑native  
- diff‑friendly  
- terminal‑readable  

Narrative artifacts include:

- NDH Case Studies  
- NDH Public Safety Envelope Case Study  
- NDH conceptual overviews  

### **2.2 — Specification Layer**  
- text‑first  
- ASCII diagrams required  
- PNGs referenced by path  
- SVGs referenced by path  
- no embedded images  

Specification artifacts include:

- NDH Public Safety Envelope Specification  
- NDH Web Ontology Specification  
- NDH Traversal Rules  

### **2.3 — UX Layer (Visual & Onboarding Docs)**  
- PNGs embedded  
- SVGs embedded (optional)  
- color allowed  
- visual metaphors allowed  
- Kawaii sneks allowed  
- expressive illustrations allowed  

UX artifacts include:

- NDH Public Traversal UX  
- NDH Public Snek Mythos  
- NDH onboarding guides  
- NDH visual documentation framework  

---

## ⭐ 3 — ASCII Governance Rules  
ASCII diagrams are the **canonical visual format** for conceptual NDH documentation.

### **ASCII MUST:**
- be embedded directly in case studies  
- be embedded directly in specifications  
- represent conceptual structures  
- remain stable across versions  
- remain low‑stimulus and gentle  

### **ASCII MUST NOT:**
- be replaced by PNGs  
- be replaced by SVGs  
- be omitted from conceptual documents  

ASCII is the **conceptual backbone** of NDH documentation.

---

## ⭐ 4 — PNG Governance Rules  
PNG illustrations are the **primary UX‑layer visual assets**.

### **PNG MUST:**
- be embedded only in UX‑layer documents  
- be referenced (not embedded) in specs  
- be referenced (not embedded) in case studies  
- remain minimal and stable  
- follow the PNG Illustration Plan  
- use soft, gentle, trauma‑informed aesthetics  

### **PNG MUST NOT:**
- be embedded in case studies  
- be embedded in specifications  
- replace ASCII diagrams  
- carry essential meaning (ASCII is canonical)  

PNG assets include:

- snek guardians  
- habitat maps  
- behavioral envelopes  
- traversal flow illustrations  

---

## ⭐ 5 — SVG Governance Rules  
SVGs are **optional vector assets** used only for structural UX diagrams.

### **SVG MAY:**
- be embedded in UX‑layer documents  
- be used for icons, arrows, flow diagrams  
- be referenced in specifications  

### **SVG MUST:**
- remain minimal  
- remain stable  
- avoid emotional content  
- avoid complex illustrations  
- avoid animation or scripting  

### **SVG MUST NOT:**
- be embedded in case studies  
- be used for snek characters  
- be used for expressive metaphors  
- replace ASCII diagrams  

SVGs are **structural**, not expressive.

---

## ⭐ 6 — Trauma‑Informed Documentation Principles  
NDH documentation must remain:

- gentle  
- predictable  
- low‑stimulus  
- emotionally safe  
- visually calm  
- non‑overwhelming  

Therefore:

### **Case studies MUST remain text‑first.**  
### **Specs MUST remain text‑first.**  
### **UX docs MAY use color and expressive visuals.**

This separation protects readers from cognitive overload.

---

## ⭐ 7 — Stability & Versioning Rules  
To prevent architectural drift:

### **All documentation artifacts MUST:**
- use versioned filenames  
- maintain stable directory structure  
- avoid embedding volatile assets  
- reference PNG/SVG paths consistently  
- avoid breaking changes without version increments  

### **PNG/SVG assets MUST:**
- be governed by the Illustration Plan  
- remain minimal  
- remain reusable  
- avoid proliferation  

---

## ⭐ 8 — AI Traversal Agents (Copilot, etc.)  
NDH documentation rules apply **only** to NDH repository artifacts.

They do **not** apply to:

- Copilot chat  
- inline images in conversation  
- multimodal responses  
- accessibility features  
- external AI agents  

Therefore:

> **AI traversal agents MAY render inline images, SVGs, or multimodal content in chat environments.  
> NDH documentation rules do not restrict conversational UX.**

This ensures accessibility and clarity for human readers.

---

## ⭐ 9 — Provenance & File Path  
This Charter must be stored at:

```
NDH-Platforms/Public/docs/governance/NDH-Documentation-Governance-Charter-v1.0.md
```

---

