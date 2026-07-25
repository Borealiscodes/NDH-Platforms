# 🛰️ **GQL Governance Shell (v1.0)**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-gql-governance-shell-v1.0.md
```

---

## **1. Purpose**

The GQL Governance Shell defines:

- the command‑line interface for GQL execution  
- how operators and CI/CD pipelines run governance queries  
- how governance artifacts are inspected, validated, and enforced  
- how bytecode, diagnostics, logs, telemetry, and safety signals are surfaced in terminal workflows  
- how governance automation integrates with NDH repos  
- how the Shell complements the **GQL Governance Console**  

It is the **automation‑first governance interface**.

---

## **2. Shell Architecture**

The Governance Shell consists of **six command groups**:

1. **Query Commands**  
2. **Bytecode Commands**  
3. **Execution Commands**  
4. **Diagnostics Commands**  
5. **Safety Commands**  
6. **Observability Commands**

Each command group maps directly to GQL subsystems.

---

## **3. Query Commands**

### **Run a GQL Query**
```
gql run <file.gql>
```

Outputs:

- results  
- provenance trails  
- naming clusters  
- enforcement summaries  
- temporal annotations  

### **Validate a GQL Query**
```
gql validate <file.gql>
```

Runs compiler + optimizer + linker checks.

### **Explain a GQL Query**
```
gql explain <file.gql>
```

Shows:

- AST  
- execution plan  
- bytecode lowering  
- safety constraints  

---

## **4. Bytecode Commands**

### **Inspect Bytecode**
```
gql bytecode inspect <file.gqlbc>
```

Shows:

- opcodes  
- operands  
- segments  
- safety blocks  

### **Disassemble Bytecode**
```
gql bytecode disasm <file.gqlbc>
```

Shows human‑readable instruction listing.

### **Verify Bytecode**
```
gql bytecode verify <file.gqlbc>
```

Runs loader + safety checks.

---

## **5. Execution Commands**

### **Execute Bytecode**
```
gql exec <file.gqlbc>
```

Runs the VM.

### **Step Through Execution**
```
gql exec step <file.gqlbc>
```

Shows:

- instruction fetch  
- decode  
- safety check  
- state transition  

### **Replay Execution**
```
gql exec replay <file.gqlbc>
```

Deterministic replay.

---

## **6. Diagnostics Commands**

### **Show Diagnostics**
```
gql diag show
```

Shows errors, warnings, traces, insights.

### **Filter Diagnostics**
```
gql diag show --domain naming
```

### **Export Diagnostics**
```
gql diag export <file.json>
```

Exports full diagnostic bundle.

---

## **7. Safety Commands (Critical)**

### **Check Safety**
```
gql safety check <file.gqlbc>
```

Runs full safety model.

### **Show Safety Violations**
```
gql safety violations
```

### **Explain Safety Context**
```
gql safety context
```

Shows:

- allowed naming families  
- allowed provenance boundaries  
- allowed structural volumes  
- allowed enforcement rules  
- allowed temporal ranges  

Safety commands integrate with:

- **Meta‑Document**  
- **Refinement Blueprint**  
- **Suite Index**  

---

## **8. Observability Commands**

### **Show Logs**
```
gql obs logs
```

### **Show Telemetry**
```
gql obs metrics
```

### **Show Execution Trace**
```
gql obs trace <file.gqlbc>
```

### **Show Governance Context**
```
gql obs context
```

---

## **9. CI/CD Integration**

The Shell is designed for CI/CD pipelines:

- pre‑merge governance checks  
- naming invariant enforcement  
- provenance boundary validation  
- structural volume validation  
- enforcement rule validation  
- temporal alignment validation  
- safety gate enforcement  

Example pipeline step:

```
gql validate naming.gql
gql safety check naming.gqlbc
```

If safety fails → merge blocked.

---

## **10. Deterministic Shell Guarantees**

The Governance Shell guarantees:

- identical output for identical input  
- identical ordering of diagnostics  
- identical safety behavior  
- identical execution replay  
- identical observability output  

This ensures governance reproducibility.

---

## **11. Machine‑Readable Shell Spec**

```
gql_governance_shell:
  version: "1.0"
  commands:
    - run
    - validate
    - explain
    - bytecode.inspect
    - bytecode.disasm
    - bytecode.verify
    - exec
    - exec.step
    - exec.replay
    - diag.show
    - diag.export
    - safety.check
    - safety.violations
    - safety.context
    - obs.logs
    - obs.metrics
    - obs.trace
    - obs.context
  deterministic: true
```

---

## **12. Placement Rules**

Place under:

```
NDH-Platforms/Orbital/governance/notes/
```

---

