# 🖼️ **VM Wiring Map PNG Specification (v1.0)**  
### *The operational diagram of the NDH Consolidation Spine*

The VM Wiring Map PNG is the **canonical visual** showing how the VM connects to:

- Sentinel  
- Hyperatlas  
- Stability‑Manifold  
- Tonal Spiral Geometry  
- Simulation‑Suite  
- Governance Migration Suite (readiness)  

It is the **centerpiece** of the NDH visual governance layer.

---

# 1. **Canvas & Export Specs**

**Canvas:**  
- 4096 × 4096 px  
- 300 DPI  
- Transparent background  
- RGB  

**Safe margins:**  
- 200 px outer padding  
- No text within 150 px of edges  

---

# 2. **Global Layout**

The diagram uses a **vertical spine axis** with **five lateral wiring branches**.

```
                [ Sentinel ]
                    |
                    |
[ Stability ] — [ VM ] — [ Hyperatlas ]
                    |
                    |
             [ Tonal Spiral ]
                    |
                    |
             [ Simulation Suite ]
```

A sixth branch (Governance Suite) is shown as a **dashed wedge** to indicate readiness but not yet constructed.

---

# 3. **Layer Architecture (Top → Bottom)**

## **3.1 VM Core Node**
- Shape: Rounded rectangle  
- Size: 420 × 180 px  
- Color: #FFFFFF at 85% opacity  
- Stroke: 4 px neutral (#2A2A2A)  
- Label: **“Orbital‑GQL VM (1.2 Spine‑Integrated)”**

### Sub‑labels:
- Deterministic ISA  
- Soft‑Boundary Engine  
- Orbital‑GQL Ops  
- Provenance‑Safe Execution  

---

## **3.2 Sentinel Wiring (Top Branch)**  
**Node:**  
- Shape: Rounded rectangle  
- Size: 380 × 160 px  
- Color: #F0E8E8  
- Label: **“Sentinel Boundary Layer”**

**Wire:**  
- Straight vertical line from VM top  
- Color: #A0A0A0  
- Thickness: 6 px  

**Markers:**  
- Recursion boundary  
- Trauma‑safe pacing  
- Expressive descent guard  

---

## **3.3 Hyperatlas Wiring (Right Branch)**  
**Node:**  
- Shape: Rounded rectangle  
- Size: 380 × 160 px  
- Color: #E8F0FF  
- Label: **“Hyperatlas Routing Stability”**

**Wire:**  
- Horizontal line from VM right  
- Color: #A0C4FF  
- Thickness: 6 px  

**Markers:**  
- Deterministic routing  
- Curvature alignment  
- Holonomy safety  

---

## **3.4 Stability‑Manifold Wiring (Left Branch)**  
**Node:**  
- Shape: Rounded rectangle  
- Size: 380 × 160 px  
- Color: #E8FFE8  
- Label: **“Stability‑Manifold Curvature”**

**Wire:**  
- Horizontal line from VM left  
- Color: #8BCF8B  
- Thickness: 6 px  

**Markers:**  
- Curvature envelopes  
- Holonomy flatteners  
- Stability minima  

---

## **3.5 Tonal Spiral Geometry Wiring (Lower‑Middle Branch)**  
**Node:**  
- Shape: Circle  
- Radius: 260 px  
- Color: gradient (#A0C4FF → #CDE7FF)  
- Label: **“Tonal Spiral Geometry”**

**Wire:**  
- Vertical line from VM bottom  
- Color: #CDE7FF  
- Thickness: 6 px  

**Markers:**  
- Expressive‑stability nodes  
- Non‑dual alignment arcs  
- Spiral curvature  

---

## **3.6 Simulation‑Suite Wiring (Bottom Branch)**  
**Node:**  
- Shape: Rounded rectangle  
- Size: 380 × 160 px  
- Color: #FFF0D8  
- Label: **“Simulation‑Suite Expressive Descent”**

**Wire:**  
- Vertical line from Tonal Spiral node  
- Color: #FFD8A0  
- Thickness: 6 px  

**Markers:**  
- Expressive descent  
- Trauma‑safe behavior  
- Provenance‑safe simulation  

---

## **3.7 Governance Migration Suite (Dashed Wedge)**  
**Shape:**  
- 45° wedge  
- Radius: 900–2000 px  
- Color: transparent  
- Boundary: dashed #FFB3B3  

**Label:**  
- “Governance Migration / Monitoring / Construction (Readiness)”  

---

# 4. **Transmission Loop Arrows**

Arrows must show the full NDH transmission loop:

```
VM → Sentinel → Hyperatlas → Stability/Tonal → Simulation → VM
```

**Arrow style:**  
- Color: #2A2A2A  
- Thickness: 5 px  
- Arrowheads: 24 px  
- Curved arrows for non‑dual transitions  

---

# 5. **Color Palette (Exact Values)**

| Component | Hex |
|----------|------|
| VM node | #FFFFFF (85%) |
| Sentinel | #F0E8E8 |
| Hyperatlas | #E8F0FF |
| Stability‑Manifold | #E8FFE8 |
| Tonal Spiral | #A0C4FF → #CDE7FF |
| Simulation‑Suite | #FFF0D8 |
| Governance wedge | #FFB3B3 |
| Wiring lines | #A0A0A0 / #A0C4FF / #8BCF8B / #CDE7FF / #FFD8A0 |

---

# 6. **Typography**

- Font: Inter / Roboto / Noto Sans  
- Sizes: 42–64 px  
- Weight: Medium  
- Kerning: +2  
- Line spacing: 1.2×  

---

# 7. **File Path (Authoritative)**

```
NDH-Platforms/Public/vm/visuals/VM-Wiring-Map-v1.0.png
NDH-Platforms/Public/vm/visuals/specs/VM-Wiring-Map-v1.0.md
```

---

