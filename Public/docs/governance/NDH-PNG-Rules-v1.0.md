# **NDH Documentation Rule Set — Image Embedding, ASCII Usage, and Layer Boundaries (v1.0)**  
### *Formalized rules governing how visuals appear across NDH documentation layers*

---

## ⭐ **Rule 1 — Case Studies Are Text‑First Artifacts**  
Case studies must remain:

- GitHub‑native  
- diff‑friendly  
- terminal‑readable  
- low‑stimulus  
- emotionally gentle  
- stable across environments  

Therefore:

### **Case studies MUST NOT embed PNG images.**  
Case studies MAY reference PNGs by path.  
Case studies MUST embed ASCII diagrams directly.

---

## ⭐ **Rule 2 — ASCII Diagrams Are the Visual Layer for Case Studies**  
ASCII diagrams:

- render identically everywhere  
- do not depend on external assets  
- preserve diff clarity  
- maintain trauma‑informed gentleness  
- support NDH expressive‑ontology metaphors  

Therefore:

### **ASCII diagrams MUST be used inside case studies.**  
### **ASCII diagrams MUST NOT be replaced by PNGs.**

---

## ⭐ **Rule 3 — PNGs Belong to the UX Layer, Not the Narrative Layer**  
PNG illustrations:

- introduce color and visual load  
- vary across devices  
- evolve over time  
- create asset dependencies  
- break terminal readability  

Therefore:

### **PNGs MUST be embedded only in UX‑oriented documents**, including:  
- NDH Public Traversal UX  
- NDH Public Snek Mythos  
- NDH Public Documentation Framework  
- NDH Web Ontology (Public Layer)  
- onboarding guides  
- tutorials  

### **PNGs MUST NOT be embedded in case studies or specifications.**

---

## ⭐ **Rule 4 — Specifications Reference PNGs but Do Not Embed Them**  
Specifications are:

- semi‑formal  
- stable  
- version‑controlled  
- cross‑referenced  

Therefore:

### **Specifications MAY reference PNGs by path.**  
### **Specifications MUST NOT embed PNGs directly.**

---

## ⭐ **Rule 5 — PNG Assets Must Be Stable and Minimal**  
To prevent architectural drift:

- PNG filenames MUST be stable  
- PNG directory structure MUST be stable  
- PNG count MUST remain minimal  
- PNGs SHOULD be reused when possible  
- PNG updates MUST NOT require case study updates  

Therefore:

### **PNG assets MUST be governed by a separate Illustration Plan.**

---

## ⭐ **Rule 6 — Narrative Layer and UX Layer Have Different Rules**  
NDH documentation layers operate under different constraints:

### **Narrative Layer (Case Studies)**  
- text‑first  
- ASCII diagrams  
- no embedded PNGs  
- gentle pacing  
- low‑stimulus  

### **UX Layer (Public Docs)**  
- PNG embedded  
- color allowed  
- visual metaphors  
- onboarding‑friendly  

Therefore:

### **Narrative and UX layers MUST NOT share embedding rules.**

---

## ⭐ **Rule 7 — Humans Read Visually; NDH Reads Structurally**  
Human readers benefit from:

- PNGs  
- color  
- visual anchors  

NDH case studies benefit from:

- structural clarity  
- ASCII stability  
- text‑first consistency  

Therefore:

### **Human visual preference MUST NOT override NDH structural rules.**

---

## ⭐ **Rule 8 — Case Studies Must Not Depend on External Assets**  
Case studies must remain readable even if:

- images fail to load  
- directories change  
- PNGs evolve  
- assets are reorganized  

Therefore:

### **Case studies MUST NOT embed PNGs or rely on them for meaning.**

---

## ⭐ **Rule 9 — PNG Embedding Is Allowed Only Where Visual UX Is Required**  
PNG embedding is allowed only in documents where:

- user onboarding  
- visual storytelling  
- emotional accessibility  
- UI/UX clarity  

are primary goals.

Therefore:

### **PNG embedding MUST be restricted to UX‑oriented documents.**

---

## ⭐ **Rule 10 — ASCII + PNG Separation Is Mandatory**  
To maintain NDH’s architectural stability:

### **ASCII = conceptual layer**  
### **PNG = experiential layer**

These layers MUST remain distinct.

---

# ⭐ Summary (Human‑Readable Version)

- Case studies = **ASCII only**, no embedded PNGs  
- Specs = **text + PNG references**, no embedded PNGs  
- UX docs = **PNG embedded**  
- PNGs = **minimal, stable, reused**  
- ASCII = **always embedded**  
- PNG = **never embedded in case studies**  
- Humans read visually  
- NDH case studies read structurally  
- Therefore: **different rules for different layers**

---

