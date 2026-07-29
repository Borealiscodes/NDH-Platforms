# **NDH Documentation Governance Charter v1.1**  
### *Includes ASCII diagrams + references to PNG/SVG assets per NDH visual governance*

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

# ⭐ 2 — NDH Documentation Layer Model  
NDH documentation is divided into **three layers**, each with its own rules.

### ASCII Diagram — Layer Model

```text
+------------------------------------------------------+
|                NDH Documentation Layers              |
+------------------------------------------------------+
|  Narrative Layer (Case Studies)                      |
|    - ASCII only                                      |
|    - No embedded PNG/SVG                             |
+------------------------------------------------------+
|  Specification Layer                                 |
|    - ASCII required                                  |
|    - PNG/SVG referenced only                         |
+------------------------------------------------------+
|  UX Layer (Visual Docs)                              |
|    - PNG embedded                                    |
|    - SVG embedded (optional)                         |
|    - Color + expressive visuals allowed              |
+------------------------------------------------------+
```

PNG reference (not embedded):

```
docs/public/img/public-interaction-flow.png
```

---

# ⭐ 3 — ASCII Governance Rules  
ASCII diagrams are the **canonical visual format** for conceptual NDH documentation.

### ASCII MUST:
- be embedded directly in case studies  
- be embedded directly in specifications  
- represent conceptual structures  
- remain stable across versions  
- remain low‑stimulus and gentle  

### ASCII MUST NOT:
- be replaced by PNGs  
- be replaced by SVGs  
- be omitted from conceptual documents  

ASCII is the **conceptual backbone** of NDH documentation.

---

# ⭐ 4 — PNG Governance Rules  
PNG illustrations are the **primary UX‑layer visual assets**.

### PNG MUST:
- be embedded only in UX‑layer documents  
- be referenced (not embedded) in specs  
- be referenced (not embedded) in case studies  
- remain minimal and stable  
- follow the PNG Illustration Plan  
- use soft, gentle, trauma‑informed aesthetics  

### PNG MUST NOT:
- be embedded in case studies  
- be embedded in specifications  
- replace ASCII diagrams  
- carry essential meaning (ASCII is canonical)  

PNG reference:

```
docs/public/img/snek-guardian-roles.png
```

---

# ⭐ 5 — SVG Governance Rules  
SVGs are **optional vector assets** used only for structural UX diagrams.

### SVG MAY:
- be embedded in UX‑layer documents  
- be used for icons, arrows, flow diagrams  
- be referenced in specifications  

### SVG MUST:
- remain minimal  
- remain stable  
- avoid emotional content  
- avoid complex illustrations  
- avoid animation or scripting  

### SVG MUST NOT:
- be embedded in case studies  
- be used for snek characters  
- be used for expressive metaphors  
- replace ASCII diagrams  

SVG reference:

```
docs/public/img/traversal-arrows.svg
```

---

# ⭐ 6 — Trauma‑Informed Documentation Principles  
NDH documentation must remain:

- gentle  
- predictable  
- low‑stimulus  
- emotionally safe  
- visually calm  
- non‑overwhelming  

Therefore:

### Case studies MUST remain text‑first.  
### Specs MUST remain text‑first.  
### UX docs MAY use color and expressive visuals.

ASCII Diagram — Trauma‑Informed Separation

```text
+---------------------------+
|  Trauma-Informed Rules    |
+---------------------------+
| Case Studies: ASCII only  |
| Specs: ASCII + references |
| UX Docs: PNG/SVG allowed  |
+---------------------------+
```

---

# ⭐ 7 — Stability & Versioning Rules  
To prevent architectural drift:

### All documentation artifacts MUST:
- use versioned filenames  
- maintain stable directory structure  
- avoid embedding volatile assets  
- reference PNG/SVG paths consistently  
- avoid breaking changes without version increments  

### PNG/SVG assets MUST:
- be governed by the Illustration Plan  
- remain minimal  
- remain reusable  
- avoid proliferation  

---

# ⭐ 8 — AI Traversal Agents (Copilot, etc.)  
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

---

# ⭐ 9 — Provenance & File Path  
This Charter must be stored at:

```
NDH-Platforms/Public/docs/governance/NDH-Documentation-Governance-Charter-v1.1.md
```

---

