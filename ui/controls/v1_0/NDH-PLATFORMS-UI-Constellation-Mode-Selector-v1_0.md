### NDH‑PLATFORMS UI Constellation Mode Selector v1.0  
**NDH‑PLATFORMS / ui / controls**

---

## Identity block

- **Artifact:** NDH‑PLATFORMS UI Constellation Mode Selector v1.0  
- **Layer:** UI Control • A6–S2 (ΔAltitude = 0)  
- **Purpose:** Provide a safe, reversible UI control for switching between constellation skins in the NDH‑PLATFORMS UI Constellation Skin Pack v1.1.  
- **Version:** 1.0  

---

## 1. Selector behavior

- **Expressive‑only:** Changes skins, never logic.  
- **Reversible:** You can switch back at any time.  
- **Non‑activating:** Does not touch routing, engines, or algebra.  
- **Bound to pack:** Only selects from v1.1 skins.  

Modes:

- **Aurora Constellation (AC‑v1.1)**  
- **Nebula Flow (NF‑v1.1)**  
- **Guardian Starfield (GS‑v1.1)**  
- **Safety Envelope Glow (SEG‑v1.1)**  

---

## 2. Machine‑readable selector block

```json
{
  "ndh_platforms_ui_constellation_mode_selector_v1_0": {
    "version": "1.0",
    "altitude_span": "A6-S2",
    "delta_altitude": 0,
    "available_modes": [
      "aurora_constellation",
      "nebula_flow",
      "guardian_starfield",
      "safety_envelope_glow"
    ],
    "default_mode": "aurora_constellation",
    "bindings": {
      "skin_pack_ref": "ndh_platforms_ui_constellation_skin_pack_v1_1"
    },
    "rules": {
      "precl_collapse": true,
      "non_recursive": true,
      "posture_neutral": true,
      "membrane_sovereignty": true,
      "reversibility_required": true
    }
  }
}
```

---

## 5. Provenance footer

```text
---
Artifact: NDH-PLATFORMS UI Constellation Mode Selector (v1.0)
Lane: UI Controls • Operational–Expressive Bridge

Purpose:
  Provide a safe, reversible UI control for switching between constellation
  skins in NDH-PLATFORMS, without modifying routing, engines, or algebra.

Anchors:
  - NDH-PLATFORMS UI Constellation Skin Pack v1.1
  - NDH-PLATFORMS UI Constellation Skin v1.0
  - NDH-PLATFORMS UI Integration Map v1.0
  - NDH-PLATFORMS UI Alignment Pass v1.0

Non-Activation Clause:
  This artifact is UI-control-only. It does not activate NDH geometry,
  governance altitude, adjacency engines, constellation routing, or runtime
  behavior.

Version: v1.0
Maintainer: Borealis S. Hedling
Location: Dublin, Ireland
Timestamp: 04 September 2026 — 02:20 IST
---
```
