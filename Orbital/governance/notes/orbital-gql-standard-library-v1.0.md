# 🛰️ **GQL Standard Library (v1.0)**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-gql-standard-library-v1.0.md
```

---

## **1. Purpose**

The GQL Standard Library provides:

- reusable query functions  
- semantic macros  
- naming‑family shortcuts  
- provenance‑aware helpers  
- enforcement‑rule selectors  
- structural navigation helpers  
- temporal range utilities  
- cross‑repo lookup shortcuts  

It is the **developer‑facing ergonomic layer** for GQL.

---

## **2. Standard Library Structure**

The library is organized into **six modules**:

1. **Core Functions**  
2. **Naming Functions**  
3. **Provenance Functions**  
4. **Structural Functions**  
5. **Enforcement Functions**  
6. **Temporal Functions**

Each module contains reusable GQL constructs.

---

## **3. Core Functions**

### **`FIND_ARTIFACTS()`**  
Returns all governance artifacts.

### **`FIND_VOLUMES()`**  
Returns all Compendium volumes.

### **`SEARCH(term)`**  
Full‑text search across all governance artifacts.

### **`SEMANTIC(term)`**  
Semantic search using the **Governance Lexicon**.

---

## **4. Naming Functions**

These functions use naming families from the **Naming Invariant Ledger**.

### **`FAMILY(core|tids|orbital|emergent)`**  
Returns all artifacts referencing the given naming family.

### **`MATCH_RHYTHM(pattern)`**  
Finds artifacts referencing acronyms with a given rhythm.

### **`MATCH_SHAPE(pattern)`**  
Finds artifacts referencing acronyms with a given shape.

### **`NAMING_RULES()`**  
Returns all naming‑invariant rules.

### **`NAMING_DRIFT()`**  
Returns all artifacts discussing rhythm or shape drift.

---

## **5. Provenance Functions**

These functions use provenance concepts from the **Governance Constitution**.

### **`ANCESTORS(of)`**  
Returns all artifacts that are conceptual ancestors.

### **`DESCENDANTS(of)`**  
Returns all artifacts that derive from a given artifact.

### **`BOUNDARY(layer)`**  
Returns all provenance rules affecting CORE, TIDS, Emergent, or Orbital.

### **`LINEAGE(of)`**  
Returns the full provenance chain.

---

## **6. Structural Functions**

These functions use structural rules from the **Governance Style Guide**.

### **`IN_VOLUME(id)`**  
Returns all artifacts in a given Compendium volume.

### **`IN_SECTION(name)`**  
Returns all artifacts containing a given section.

### **`HAS_BANNER()`**  
Returns all artifacts requiring the governance banner.

### **`HAS_FOOTER()`**  
Returns all artifacts requiring the governance footer.

---

## **7. Enforcement Functions**

These functions use enforcement rules from:

- **Governance Schema**  
- **Governance Validator**  
- **Governance Automation Spec**  

### **`SCHEMA_RULES()`**  
Returns all schema rules.

### **`VALIDATOR_CHECKS()`**  
Returns all validator rules.

### **`AUTOMATION_GATES()`**  
Returns all CI/CD merge‑blocking rules.

### **`BLOCKS_MERGE()`**  
Returns all artifacts containing merge‑blocking enforcement.

---

## **8. Temporal Functions**

These functions use temporal artifacts:

- **Governance Calendar**  
- **Governance Almanac**  

### **`YEAR(y)`**  
Returns all governance events in a given year.

### **`QUARTER(q)`**  
Returns all governance events in a given quarter.

### **`AFTER(event)`**  
Returns all events after a given event.

### **`BEFORE(event)`**  
Returns all events before a given event.

---

## **9. Macro Library**

Macros provide ergonomic shortcuts.

### **`NAMING_OVERVIEW()`**  
Equivalent to:

```
SELECT naming_families
FROM NAMING
WHERE HAS_TERM("naming")
```

### **`PROVENANCE_OVERVIEW()`**  
Equivalent to:

```
SELECT provenance_rules
FROM FOUNDATIONS
WHERE HAS_TERM("provenance")
```

### **`ENFORCEMENT_OVERVIEW()`**  
Equivalent to:

```
SELECT enforcement_rules
FROM ENFORCEMENT
WHERE HAS_TERM("enforcement")
```

### **`TEMPORAL_OVERVIEW()`**  
Equivalent to:

```
SELECT temporal_events
FROM TEMPORAL
WHERE HAS_TERM("calendar") OR HAS_TERM("almanac")
```

---

## **10. Example GQL Queries Using the Standard Library**

### **1. Find all naming rules**
```
SELECT NAMING_RULES()
FROM NAMING
```

### **2. Find all artifacts referencing TIDS naming families**
```
SELECT FAMILY("tids")
FROM NAMING
```

### **3. Find all enforcement rules that block merges**
```
SELECT BLOCKS_MERGE()
FROM ENFORCEMENT
```

### **4. Find all governance events in 2026**
```
SELECT YEAR(2026)
FROM TEMPORAL
```

### **5. Find all artifacts in Volume IV**
```
SELECT IN_VOLUME("IV")
FROM STRUCTURE
```

---

## **11. Machine‑Readable Standard Library Definition**

```
gql_standard_library:
  version: "1.0"
  modules:
    core:
      - FIND_ARTIFACTS
      - FIND_VOLUMES
      - SEARCH
      - SEMANTIC
    naming:
      - FAMILY
      - MATCH_RHYTHM
      - MATCH_SHAPE
      - NAMING_RULES
      - NAMING_DRIFT
    provenance:
      - ANCESTORS
      - DESCENDANTS
      - BOUNDARY
      - LINEAGE
    structural:
      - IN_VOLUME
      - IN_SECTION
      - HAS_BANNER
      - HAS_FOOTER
    enforcement:
      - SCHEMA_RULES
      - VALIDATOR_CHECKS
      - AUTOMATION_GATES
      - BLOCKS_MERGE
    temporal:
      - YEAR
      - QUARTER
      - AFTER
      - BEFORE
```

---

## **12. Placement Rules**

The Standard Library must be placed under:

```
NDH-Platforms/Orbital/governance/notes/
```

---

