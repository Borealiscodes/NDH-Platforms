# **📄 NDH Expressive Suite Consolidated PDF Layout v1.0**  
### *NDH‑Platforms → Public → specs*

This specification defines the **canonical PDF layout** for presenting the entire NDH expressive suite — all eight PNGs, the SVG index, and their captions — on a single governed PDF surface.  
It ensures consistency, accessibility, trauma‑informed geometry, and non‑hierarchical presentation.

---

## **1 — Purpose**

The consolidated layout:

- Presents all expressive assets together  
- Preserves NDH trauma‑informed semantics  
- Ensures reversible, non‑hierarchical geometry  
- Provides a single‑surface onboarding reference  
- Supports enterprise docking documentation  
- Aligns with all render specs and the Expressive Suite Manifest  

This is the **master PDF layout** for NDH expressive documentation.

---

## **2 — Included Assets**

### **PNG Assets (8 total)**  
- Safety Envelope  
- Orbital Rings  
- Guardian Roles  
- Trans‑Orbital Flow  
- Public Interaction Flow  
- Soft Mistake Handling  
- Habitat Map  
- Constellation Activation

### **SVG Asset (1 total)**  
- Expressive Suite Index SVG

All assets must be embedded **directly**, not rasterized.

---

## **3 — Page Geometry**

### **Page Size**
- A4 or US Letter  
- Portrait orientation  
- 40–60 px margins  

### **Grid Layout**
A **three‑zone trauma‑informed grid**:

```
-------------------------------------------------------------
|                         Zone A                            |
|                 Expressive Suite Index SVG                |
|-----------------------------------------------------------|
|                         Zone B                            |
|         Traversal Ring PNGs (4 assets, 2×2 grid)          |
|-----------------------------------------------------------|
|                         Zone C                            |
|         Public Ring + Activation PNGs (4 assets)          |
-------------------------------------------------------------
```

Zones must be visually balanced and **non‑hierarchical**.

---

## **4 — Zone Specifications**

### **Zone A — Expressive Suite Index SVG**
- Centered  
- Width: 900–1200 px  
- Caption:  
  ```
  NDH Expressive Suite Index v1.0 — governed, reversible, non-hierarchical
  ```

### **Zone B — Traversal Ring PNGs**
- 2×2 grid  
- Equal spacing  
- No implied ordering  
- Captions centered under each PNG  
- PNG width: 350–450 px  

### **Zone C — Public Ring + Activation**
- 3 public PNGs + 1 activation PNG  
- 2×2 grid  
- Activation PNG must **not** be visually emphasized  
- PNG width: 350–450 px  

---

## **5 — Trauma‑Informed Constraints**

- No bold labels  
- No arrows  
- No urgency colors  
- No “core”, “primary”, “secondary” language  
- No center‑weighted hierarchy  
- All captions must be neutral and descriptive  
- All PNGs must be equal size  
- No asset may appear visually dominant  

---

## **6 — Accessibility Requirements**

### **Alt Text**
Each PNG must have alt text describing:

```
A trauma-informed diagram showing [asset name], using soft geometry, pastel colors, and reversible paths.
```

### **SVG Alt Text**
```
A trauma-informed index showing all NDH expressive assets arranged in traversal and public rings.
```

### **PDF Tagging**
- Each PNG → `<Figure>`  
- Each caption → `<Figcaption>`  
- SVG → `<Figure>`  
- All alt text embedded in metadata  

---

## **7 — Typography**

- Font: Rounded sans‑serif  
- Size: 18–22 px  
- Color: Soft gray (#6A6A6A)  
- No bold  
- No italics  
- Centered captions  

---

## **8 — Consolidated Layout ASCII Preview**

```text
-------------------------------------------------------------
|                                                           |
|                 [ Expressive Suite Index SVG ]            |
|                                                           |
|   NDH Expressive Suite Index v1.0 — governed, reversible  |
|                     and non-hierarchical                  |
|-----------------------------------------------------------|
|   [Safety Envelope]     [Orbital Rings]                   |
|   [Guardian Roles]      [Trans-Orbital Flow]              |
|-----------------------------------------------------------|
|   [Public Interaction Flow]   [Soft Mistake Handling]     |
|   [Habitat Map]               [Constellation Activation]  |
-------------------------------------------------------------
```

---

