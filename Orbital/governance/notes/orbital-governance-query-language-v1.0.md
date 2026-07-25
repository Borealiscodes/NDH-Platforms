# 🛰️ **Governance Query Language (GQL) — Specification v1.0**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-governance-query-language-v1.0.md
```

---

## **1. Purpose**

GQL defines:

- the syntax for governance queries  
- the semantics for interpreting naming families  
- the grammar for provenance‑aware queries  
- the operators for structural and temporal search  
- the filters for enforcement rules  
- the selectors for governance volumes and artifacts  
- the integration contract with the **Governance Search Engine Spec**  
- the mapping rules to the **Governance Library Index**  

It is the **governance DSL** for NDH.

---

## **2. GQL Design Principles**

GQL is designed to be:

- **semantic** — uses the **Governance Lexicon**  
- **structural** — aware of the **Governance Compendium**  
- **provenance‑aware** — uses lineage markers  
- **naming‑aware** — uses naming families from the **Naming Invariant Ledger**  
- **enforcement‑aware** — integrates Schema + Validator + Automation Spec  
- **temporal** — integrates Almanac + Calendar  
- **cross‑repo** — integrates Meta‑Document + Blueprint + Suite Index  

GQL is not a general search language — it is a governance‑specific one.

---

## **3. GQL Query Structure**

A GQL query has three layers:

```
SELECT <targets>
FROM <governance-domain>
WHERE <constraints>
```

### **SELECT Layer**  
Defines what the user wants:

- artifacts  
- naming families  
- provenance markers  
- enforcement rules  
- temporal events  
- structural sections  

Examples:

- `SELECT artifacts`  
- `SELECT naming_families`  
- `SELECT provenance_anchors`  
- `SELECT validator_rules`

### **FROM Layer**  
Defines the governance domain:

- `FOUNDATIONS` — Constitution + Charter  
- `NAMING` — Ledger + Lexicon  
- `STRUCTURE` — Style Guide + Banner + Footer  
- `ENFORCEMENT` — Schema + Validator + Automation  
- `SPATIAL` — Atlas + Cartography Supplement  
- `TEMPORAL` — Almanac + Calendar  
- `INFRASTRUCTURE` — Suite Index + Manifest + Changelog + README  

### **WHERE Layer**  
Defines constraints using:

- naming families  
- provenance markers  
- rhythm/shape rules  
- enforcement concepts  
- temporal ranges  
- structural sections  

---

## **4. GQL Operators**

### **Semantic Operators**
- `HAS_TERM("…")`  
- `MATCHES_FAMILY("RTO")`  
- `MATCHES_RHYTHM("CV-CV")`  
- `MATCHES_SHAPE("XXY")`

### **Provenance Operators**
- `ANCESTOR_OF("…")`  
- `DESCENDANT_OF("…")`  
- `WITH_LINEAGE("…")`  
- `WITH_BOUNDARY("CORE")`

### **Structural Operators**
- `IN_VOLUME("IV")`  
- `IN_SECTION("requirements")`  
- `HAS_BANNER`  
- `HAS_FOOTER`

### **Enforcement Operators**
- `REQUIRES_SCHEMA("…")`  
- `ENFORCED_BY("validator")`  
- `BLOCKS_MERGE`

### **Temporal Operators**
- `YEAR(2026)`  
- `QUARTER(3)`  
- `AFTER("Almanac-2025")`  
- `BEFORE("Calendar-2027")`

---

## **5. Example GQL Queries**

### **1. Find all artifacts that enforce naming invariants**
```
SELECT artifacts
FROM ENFORCEMENT
WHERE ENFORCED_BY("validator") AND REQUIRES_SCHEMA("naming_invariants")
```

### **2. Find all documents referencing the CORE naming family**
```
SELECT artifacts
FROM NAMING
WHERE MATCHES_FAMILY("RTO")
```

### **3. Find provenance rules affecting NDH‑TIDS**
```
SELECT provenance_rules
FROM FOUNDATIONS
WHERE WITH_BOUNDARY("TIDS")
```

### **4. Find all temporal governance events in 2026**
```
SELECT events
FROM TEMPORAL
WHERE YEAR(2026)
```

### **5. Find all artifacts in Volume IV of the Compendium**
```
SELECT artifacts
FROM STRUCTURE
WHERE IN_VOLUME("IV")
```

### **6. Find enforcement rules that block merges**
```
SELECT enforcement_rules
FROM ENFORCEMENT
WHERE BLOCKS_MERGE
```

---

## **6. Machine‑Readable GQL Grammar**

```
gql:
  select_clause:
    - artifacts
    - naming_families
    - provenance_rules
    - enforcement_rules
    - temporal_events
    - structural_sections

  from_clause:
    - FOUNDATIONS
    - NAMING
    - STRUCTURE
    - ENFORCEMENT
    - SPATIAL
    - TEMPORAL
    - INFRASTRUCTURE

  where_clause:
    operators:
      semantic:
        - HAS_TERM
        - MATCHES_FAMILY
        - MATCHES_RHYTHM
        - MATCHES_SHAPE
      provenance:
        - ANCESTOR_OF
        - DESCENDANT_OF
        - WITH_LINEAGE
        - WITH_BOUNDARY
      structural:
        - IN_VOLUME
        - IN_SECTION
        - HAS_BANNER
        - HAS_FOOTER
      enforcement:
        - REQUIRES_SCHEMA
        - ENFORCED_BY
        - BLOCKS_MERGE
      temporal:
        - YEAR
        - QUARTER
        - AFTER
        - BEFORE
```

This grammar defines the GQL language contract.

---

## **7. Cross‑Repo Linkage**

GQL must reference:

- **Meta‑Document**  
- **Refinement Blueprint**  
- **Suite Index**  

These define cross‑repo query boundaries.

---

## **8. Placement Rules**

The GQL specification must be placed under:

```
NDH-Platforms/Orbital/governance/notes/
```

---

