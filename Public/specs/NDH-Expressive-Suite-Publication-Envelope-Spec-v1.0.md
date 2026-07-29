# **📐 NDH Expressive Suite Publication Envelope Spec v1.0**  
### *NDH‑Platforms → Public → specs*

The **Publication Envelope Spec** defines the technical invariants, geometry rules, accessibility requirements, and trauma‑informed constraints governing the NDH Expressive Suite Publication Envelope.  
It ensures that all expressive‑layer PDFs follow a consistent, reversible, non‑hierarchical structure.

---

## **1 — Specification Scope**

This specification governs:

- Envelope geometry  
- Surface ordering  
- Trauma‑informed invariants  
- Accessibility metadata  
- Tagging requirements  
- Export constraints  
- Validation rules  

It applies to **all expressive‑layer PDFs** produced within NDH‑Platforms.

---

## **2 — Envelope Components (Required)**

The envelope must contain **exactly five governed surfaces**:

1. **Cover Page**  
2. **Consolidated Layout**  
3. **Back Page**  
4. **Publication Metadata Block**  
5. **PDF Export Checklist**

Each surface must be present, complete, and compliant with its own spec.

---

## **3 — Envelope Geometry Specification**

### **3.1 — Page Order (Invariant)**

```
1. Cover Page
2. Consolidated Layout
3. Back Page
4. Metadata Block
5. Export Checklist
```

This order is **fixed** and must not be altered.

### **3.2 — Margins**

- 40–60 px on all sides  
- No element may touch page edges  
- No asymmetry implying hierarchy  

### **3.3 — Alignment**

- All content centered  
- No left‑aligned or right‑aligned blocks  
- No directional flow  
- No visual emphasis on any surface  

### **3.4 — Color & Tone**

- Soft gray (#6A6A6A) for text  
- Pastel palette only  
- No saturated colors  
- No urgency cues  

---

## **4 — Trauma‑Informed Invariants (Mandatory)**

The envelope must comply with NDH trauma‑informed design rules:

- **Non‑hierarchical geometry**  
- **Reversible paths**  
- **Emotionally neutral surfaces**  
- **No arrows**  
- **No evaluative symbolism**  
- **No urgency colors**  
- **No “primary/secondary” language**  
- **No “final/end” terminology**  
- **Equal visual weight across surfaces**  

These invariants are **non‑negotiable**.

---

## **5 — Accessibility Specification**

### **5.1 — Global Alt Text**

The envelope must embed:

```
A trauma-informed publication envelope containing the NDH Expressive Suite,
including cover, layout, back page, metadata, and export checklist surfaces.
All geometry is reversible and non-hierarchical.
```

### **5.2 — Tagging Requirements**

- `<Section>` for each surface  
- `<Figure>` for all images  
- `<Figcaption>` for captions  
- Metadata embedded in PDF properties  

### **5.3 — Screen Reader Semantics**

Avoid:

- ranking  
- ordering language  
- directional cues  
- evaluative descriptors  

Use neutral, reversible phrasing.

---

## **6 — Metadata Requirements**

The envelope must embed:

- Title  
- Subtitle  
- Description  
- Keywords  
- Version  
- Publication date  
- Trauma‑Informed Semantics Block  
- Rights & Governance Block  

All metadata must match the **Publication Metadata Block v1.0**.

---

## **7 — Export Constraints**

The final PDF must:

- preserve SVG vector format  
- preserve PNG transparency  
- avoid rasterization  
- avoid compression artifacts  
- avoid font substitution  
- preserve all accessibility tags  
- preserve all metadata  
- render identically across major PDF viewers  

Export must follow the **PDF Export Checklist v1.0**.

---

## **8 — Envelope Validation Rules**

Before export, validate:

- All five surfaces present  
- All trauma‑informed invariants satisfied  
- All accessibility metadata embedded  
- All PNGs equal size  
- SVG embedded as vector  
- No hierarchy introduced  
- No urgency cues  
- No saturated colors  
- No directional arrows  
- No evaluative language  
- All geometry reversible  
- All text centered  
- All margins correct  

Only after all checks pass may the envelope be exported.

---

## **9 — ASCII Structural Preview**

```text
=============================================================
|                                                           |
|                 [ NDH Expressive Suite Cover ]            |
|-----------------------------------------------------------|
|                 [ Consolidated Layout ]                   |
|-----------------------------------------------------------|
|                 [ Back Page ]                             |
|-----------------------------------------------------------|
|                 [ Metadata Block ]                        |
|-----------------------------------------------------------|
|                 [ Export Checklist ]                      |
|                                                           |
=============================================================
```

This preview reflects the envelope’s governed surface order.

---

