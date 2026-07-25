# 🛰️ **GQL Bytecode Specification (v1.0)**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-gql-bytecode-spec-v1.0.md
```

---

## **1. Purpose**

The GQL Bytecode Specification defines:

- the binary instruction encoding for GQL‑VM  
- the opcode table for all governance operations  
- the operand formats for semantic, naming, provenance, structural, enforcement, and temporal instructions  
- the memory addressing model  
- the execution semantics for each opcode  
- the deterministic ordering rules  
- the cross‑repo safety constraints  
- the compatibility rules with the **GQL Runtime**  

It is the **machine‑level representation** of governance queries.

---

## **2. Bytecode Design Principles**

GQL Bytecode must be:

- **deterministic** — identical results across environments  
- **portable** — identical behavior across VM hosts  
- **sandboxed** — safe cross‑repo traversal  
- **semantic‑aware** — integrates lexicon and naming families  
- **provenance‑aware** — enforces lineage boundaries  
- **enforcement‑aware** — integrates schema + validator + automation  
- **temporal‑aware** — integrates calendar + almanac  
- **structurally‑aware** — integrates compendium volumes  

Bytecode is not a general VM format — it is governance‑specific.

---

## **3. Bytecode Structure**

Each bytecode instruction has:

```
<opcode> <operand-count> <operand-1> <operand-2> ...
```

Bytecode is grouped into **segments**:

1. **Header Segment**  
2. **Instruction Segment**  
3. **Metadata Segment**  
4. **Safety Segment**  
5. **Footer Segment**

---

## **4. Opcode Table (GQL‑VM ISA → Bytecode)**

### **Semantic Opcodes**
| Opcode | Meaning |
|--------|---------|
| `0x10` | SEM_RESOLVE |
| `0x11` | SEM_MATCH |

### **Naming Opcodes**
| Opcode | Meaning |
|--------|---------|
| `0x20` | NAM_FAMILY |
| `0x21` | NAM_RHYTHM |
| `0x22` | NAM_SHAPE |

### **Provenance Opcodes**
| Opcode | Meaning |
|--------|---------|
| `0x30` | PROV_ANCESTOR |
| `0x31` | PROV_DESCENDANT |
| `0x32` | PROV_BOUNDARY |
| `0x33` | PROV_LINEAGE |

### **Structural Opcodes**
| Opcode | Meaning |
|--------|---------|
| `0x40` | STR_VOLUME |
| `0x41` | STR_SECTION |
| `0x42` | STR_BANNER |
| `0x43` | STR_FOOTER |

### **Enforcement Opcodes**
| Opcode | Meaning |
|--------|---------|
| `0x50` | ENF_SCHEMA |
| `0x51` | ENF_VALIDATOR |
| `0x52` | ENF_AUTOMATION |
| `0x53` | ENF_BLOCKS_MERGE |

### **Temporal Opcodes**
| Opcode | Meaning |
|--------|---------|
| `0x60` | TMP_YEAR |
| `0x61` | TMP_QUARTER |
| `0x62` | TMP_AFTER |
| `0x63` | TMP_BEFORE |

### **Search Engine Opcodes**
| Opcode | Meaning |
|--------|---------|
| `0x70` | SRCH_FULLTEXT |
| `0x71` | SRCH_SEMANTIC |
| `0x72` | SRCH_STRUCTURAL |
| `0x73` | SRCH_PROVENANCE |
| `0x74` | SRCH_ENFORCEMENT |
| `0x75` | SRCH_TEMPORAL |

---

## **5. Operand Formats**

Operands are encoded as:

### **1. Immediate Values**
```
0x01 <value-length> <value-bytes>
```

### **2. Naming Family IDs**
```
0x02 <family-id>
```

Family IDs come from the **Naming Invariant Ledger**.

### **3. Provenance Boundary IDs**
```
0x03 <boundary-id>
```

Boundary IDs come from the **Governance Constitution**.

### **4. Structural Volume IDs**
```
0x04 <volume-id>
```

Volume IDs come from the **Governance Compendium**.

### **5. Enforcement Rule IDs**
```
0x05 <rule-id>
```

Rule IDs come from:

- Schema  
- Validator  
- Automation Spec  

### **6. Temporal Values**
```
0x06 <year-or-quarter>
```

---

## **6. Bytecode Segments**

### **Header Segment**
Contains:

- bytecode version  
- VM version  
- checksum  
- execution flags  

### **Instruction Segment**
Contains:

- ordered list of opcodes  
- operands  
- segment boundaries  

### **Metadata Segment**
Contains:

- provenance markers  
- naming‑family markers  
- structural markers  
- enforcement markers  
- temporal markers  

### **Safety Segment**
Contains:

- cross‑repo traversal constraints  
- provenance boundary constraints  
- naming‑family isolation constraints  

Uses:

- **Meta‑Document**  
- **Refinement Blueprint**  
- **Suite Index**  

### **Footer Segment**
Contains:

- end‑of‑bytecode marker  
- final checksum  

---

## **7. Execution Semantics**

The GQL‑VM must execute bytecode:

- sequentially  
- deterministically  
- without reordering  
- without speculative execution  
- without cross‑segment jumps  

This ensures governance correctness.

---

## **8. Example Bytecode Program**

A query:

```
SELECT artifacts
FROM NAMING
WHERE MATCHES_FAMILY("tids")
```

Compiles to:

```
0x10 0x02 0x02 <tids-id>
0x71
```

Meaning:

- resolve naming family  
- run semantic search  

---

## **9. Machine‑Readable Bytecode Spec**

```
gql_bytecode:
  version: "1.0"
  opcodes:
    semantic: [0x10, 0x11]
    naming: [0x20, 0x21, 0x22]
    provenance: [0x30, 0x31, 0x32, 0x33]
    structural: [0x40, 0x41, 0x42, 0x43]
    enforcement: [0x50, 0x51, 0x52, 0x53]
    temporal: [0x60, 0x61, 0x62, 0x63]
    search: [0x70, 0x71, 0x72, 0x73, 0x74, 0x75]
  segments:
    - header
    - instruction
    - metadata
    - safety
    - footer
  operands:
    - immediate
    - naming_family
    - provenance_boundary
    - structural_volume
    - enforcement_rule
    - temporal_value
```

---

## **10. Placement Rules**

The Bytecode Specification must be placed under:

```
NDH-Platforms/Orbital/governance/notes/
```

---

