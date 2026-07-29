# **📄 NDH Expressive Suite Index PDF Spec v1.0**  
### *NDH‑Platforms → Public → specs*

This specification defines how the **Expressive Suite Index SVG** must be embedded in NDH PDF documentation.  
It ensures consistent rendering, accessibility, trauma‑informed semantics, and stable layout across all NDH publications.

---

## **1 — Purpose**

The PDF Spec ensures:

- the SVG is embedded consistently  
- trauma‑informed geometry is preserved  
- no hierarchy or urgency is introduced by PDF formatting  
- accessibility and transparency remain intact  
- NDH expressive assets appear uniformly across all documentation  

This spec governs **PDF embedding**, not the SVG itself.

---

## **2 — Source Asset**

**SVG File:**  
```
NDH-Platforms/Public/img/NDH-Expressive-Suite-Index-v1.0.svg
```

This SVG is the *only* allowed source for PDF embedding.

---

## **3 — PDF Embedding Rules**

### **3.1 — Scaling**
- Embed at **100% scale** when possible  
- Minimum width: **900 px**  
- Maximum width: **1200 px**  
- Maintain aspect ratio at all times  
- No cropping, trimming, or clipping  

### **3.2 — Placement**
- Centered horizontally  
- 40–60 px top margin  
- 60–80 px bottom margin  
- No left‑aligned or right‑aligned placement  

### **3.3 — Background**
- PDF background must remain **white or transparent**  
- No colored frames  
- No drop shadows  
- No bounding boxes  

### **3.4 — Trauma‑Informed Constraints**
- No bolding of node labels  
- No added arrows or callouts  
- No emphasis colors  
- No annotations that imply hierarchy  
- No urgency cues (red, orange, flashing indicators)  

---

## **4 — Typography Rules**

### **4.1 — Caption**
- Font: Rounded sans‑serif  
- Size: 18–22 px  
- Color: Soft gray (#6A6A6A)  
- Alignment: Centered  
- Content:

```
NDH Expressive Suite Index v1.0 — governed, reversible, non-hierarchical
```

### **4.2 — Surrounding Text**
- Must not imply ranking  
- Must not describe traversal as “inner = core”  
- Must not describe public ring as “outer = secondary”  
- Must preserve NDH’s non‑hierarchical semantics  

---

## **5 — Accessibility Requirements**

### **5.1 — Alt Text**
Alt text must read:

```
A trauma-informed diagram showing the NDH traversal ring, public ring, and constellation activation node. All nodes are equal, reversible, and connected by soft arcs.
```

### **5.2 — PDF Tagging**
- SVG must be tagged as a **figure**  
- Caption must be tagged as **figcaption**  
- Alt text must be embedded in the PDF metadata  

### **5.3 — Screen Reader Semantics**
- No directional language  
- No evaluative language  
- No hierarchical language  

---

## **6 — PDF Layout Example (ASCII)**

```text
-------------------------------------------------------------
|                                                           |
|                 NDH Expressive Suite Index                |
|                                                           |
|                 [   Embedded SVG Here   ]                 |
|                                                           |
|   NDH Expressive Suite Index v1.0 — governed, reversible  |
|                     and non-hierarchical                  |
|                                                           |
-------------------------------------------------------------
```

---

