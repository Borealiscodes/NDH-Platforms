# 🛰️ **GQL Compiler Specification (v1.0)**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-gql-compiler-spec-v1.0.md
```

---

## **1. Purpose**

The GQL Compiler Specification defines:

- how GQL source text is parsed  
- how the AST (abstract syntax tree) is constructed  
- how semantic, naming, provenance, structural, enforcement, and temporal operators are resolved  
- how execution plans are lowered into bytecode  
- how bytecode segments are generated  
- how safety constraints are encoded  
- how cross‑repo traversal rules are embedded  
- how deterministic compilation is guaranteed  

It is the **formal compiler architecture** for governance queries.

---

## **2. Compiler Responsibilities**

The compiler must:

- parse GQL source text  
- validate syntax  
- build an AST  
- perform semantic analysis using the **Governance Lexicon**  
- resolve naming families using the **Naming Invariant Ledger**  
- resolve provenance markers using the **Governance Constitution**  
- resolve structural references using the **Governance Compendium**  
- resolve enforcement rules using Schema + Validator + Automation Spec  
- resolve temporal constructs using Calendar + Almanac  
- generate an execution plan  
- lower the plan into GQL Bytecode  
- embed safety constraints using Meta‑Document + Blueprint + Suite Index  
- output deterministic bytecode  

This ensures GQL queries compile correctly and safely.

---

## **3. Compiler Architecture**

The compiler consists of **six stages**:

### **Stage 1 — Lexing**  
Tokenizes GQL source text.

### **Stage 2 — Parsing**  
Builds the AST.

### **Stage 3 — Semantic Analysis**  
Resolves:

- lexicon terms  
- naming families  
- provenance markers  
- structural references  
- enforcement concepts  
- temporal constructs  

### **Stage 4 — Execution Plan Construction**  
Builds a multi‑stage plan identical to the Runtime pipeline.

### **Stage 5 — Bytecode Lowering**  
Converts plan stages into:

- opcodes  
- operands  
- segments  
- safety blocks  

### **Stage 6 — Bytecode Assembly**  
Produces final bytecode with:

- header  
- instruction segment  
- metadata segment  
- safety segment  
- footer  

---

## **4. AST Structure**

The AST contains:

### **Root Node**
```
Query
```

### **Child Nodes**
- `SelectNode`  
- `FromNode`  
- `WhereNode`  

### **Leaf Nodes**
- semantic operators  
- naming operators  
- provenance operators  
- structural operators  
- enforcement operators  
- temporal operators  

Each leaf node maps directly to a GQL‑VM opcode.

---

## **5. Execution Plan Structure**

The compiler builds a plan with the following stages:

1. semantic  
2. naming  
3. provenance  
4. structural  
5. enforcement  
6. temporal  
7. full‑text  
8. merge  
9. rank  

This plan is then lowered into bytecode.

---

## **6. Bytecode Lowering Rules**

Each AST node maps to:

- **one opcode**  
- **zero or more operands**  

Examples:

### **Naming Family**
```
MATCHES_FAMILY("tids")
→ opcode: 0x20 (NAM_FAMILY)
→ operand: 0x02 <tids-id>
```

### **Provenance Boundary**
```
WITH_BOUNDARY("CORE")
→ opcode: 0x32 (PROV_BOUNDARY)
→ operand: 0x03 <core-boundary-id>
```

### **Temporal Year**
```
YEAR(2026)
→ opcode: 0x60 (TMP_YEAR)
→ operand: 0x06 <2026>
```

---

## **7. Safety Encoding Rules**

Safety constraints must be encoded using:

- **Meta‑Document**  
- **Refinement Blueprint**  
- **Suite Index**  

Safety segment must include:

- allowed naming families  
- allowed provenance boundaries  
- allowed structural volumes  
- allowed enforcement rules  
- allowed temporal ranges  
- allowed cross‑repo traversal paths  

This prevents governance violations.

---

## **8. Deterministic Compilation Rules**

The compiler must guarantee:

- identical bytecode for identical queries  
- identical ordering of instructions  
- identical operand encoding  
- identical safety segment generation  
- identical metadata generation  

This ensures governance consistency across environments.

---

## **9. Example Compilation**

### **GQL Query**
```
SELECT artifacts
FROM NAMING
WHERE MATCHES_FAMILY("tids")
```

### **AST**
```
Query
 ├── SelectNode(artifacts)
 ├── FromNode(NAMING)
 └── WhereNode
       └── NamingFamilyNode("tids")
```

### **Execution Plan**
- naming stage  
- semantic stage  
- full‑text stage  
- merge  
- rank  

### **Bytecode**
```
0x20 0x02 <tids-id>
0x71
```

---

## **10. Machine‑Readable Compiler Spec**

```
gql_compiler:
  version: "1.0"
  stages:
    - lexing
    - parsing
    - semantic_analysis
    - execution_plan
    - bytecode_lowering
    - bytecode_assembly
  ast:
    root: Query
    children:
      - SelectNode
      - FromNode
      - WhereNode
    leaves:
      - semantic_ops
      - naming_ops
      - provenance_ops
      - structural_ops
      - enforcement_ops
      - temporal_ops
  lowering_rules:
    semantic: [0x10, 0x11]
    naming: [0x20, 0x21, 0x22]
    provenance: [0x30, 0x31, 0x32, 0x33]
    structural: [0x40, 0x41, 0x42, 0x43]
    enforcement: [0x50, 0x51, 0x52, 0x53]
    temporal: [0x60, 0x61, 0x62, 0x63]
    search: [0x70, 0x71, 0x72, 0x73, 0x74, 0x75]
  safety:
    - meta_document
    - refinement_blueprint
    - suite_index
```

---

## **11. Placement Rules**

The Compiler Specification must be placed under:

```
NDH-Platforms/Orbital/governance/notes/
```

---

