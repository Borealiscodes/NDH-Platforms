# 🛰️ **GQL Diagnostics Specification (v1.0)**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-gql-diagnostics-spec-v1.0.md
```

---

## **1. Purpose**

The GQL Diagnostics Specification defines:

- diagnostic categories (errors, warnings, traces, insights)  
- how diagnostics are generated across the entire GQL pipeline  
- how diagnostics are structured, formatted, and surfaced  
- how governance context is included in diagnostic output  
- how safety‑related diagnostics are prioritized  
- how deterministic diagnostic behavior is guaranteed  
- how diagnostics integrate with the **GQL Error Model**  
- how diagnostics support maintainers, auditors, and automated governance tooling  

It is the **observability and introspection layer** of GQL.

---

## **2. Diagnostic Categories**

Diagnostics are grouped into **four categories**:

1. **Errors** — fatal issues halting execution  
2. **Warnings** — non‑fatal issues that may affect results  
3. **Traces** — step‑by‑step execution logs  
4. **Insights** — semantic, naming, provenance, structural, enforcement, and temporal analysis summaries  

Each category has:

- generation rules  
- propagation rules  
- reporting format  
- deterministic behavior guarantees  

---

## **3. Diagnostic Generation Pipeline**

Diagnostics are generated at **seven pipeline stages**:

1. **Lexing**  
2. **Parsing**  
3. **Semantic Analysis**  
4. **Compilation**  
5. **Optimization**  
6. **Linking**  
7. **Loading**  
8. **Execution**  

Each stage contributes its own diagnostic events.

---

## **4. Diagnostic Structure**

Every diagnostic event contains:

- diagnostic category  
- diagnostic code  
- message  
- governance domain (naming, provenance, structural, enforcement, temporal, safety)  
- bytecode location (if applicable)  
- AST location (if applicable)  
- execution step (if applicable)  
- relevant governance artifact (via guided link)  

Example:

```
Warning:
  code: NAM-W001
  domain: naming
  message: "Rhythm pattern canonicalized from CVCVC to CV-CV"
  artifact: Naming Invariant Ledger
```

---

## **5. Error Diagnostics**

Errors follow the **GQL Error Model**.

### Error Diagnostic Format
```
Error:
  code: <ERR-CODE>
  domain: <governance-domain>
  message: <description>
  location: <bytecode|AST|execution-step>
  artifact: <guided-link>
```

Errors always halt execution.

---

## **6. Warning Diagnostics**

Warnings indicate non‑fatal issues.

### Examples
- naming canonicalization  
- provenance pruning  
- structural flattening  
- enforcement consolidation  
- temporal compression  

### Warning Diagnostic Format
```
Warning:
  code: <WARN-CODE>
  domain: <governance-domain>
  message: <description>
  artifact: <guided-link>
```

Warnings never halt execution.

---

## **7. Trace Diagnostics**

Traces provide step‑by‑step execution visibility.

### Trace Events Include
- instruction fetch  
- instruction decode  
- safety check result  
- state transition  
- search engine invocation  
- result merge  
- ranking step  

### Trace Format
```
Trace:
  step: <execution-step>
  opcode: <opcode>
  operands: <operands>
  state_before: <context>
  state_after: <context>
```

Traces are deterministic and reproducible.

---

## **8. Insight Diagnostics**

Insights provide high‑level summaries of:

- semantic relevance  
- naming‑family clustering  
- provenance lineage  
- structural navigation  
- enforcement rule activation  
- temporal range evaluation  

### Insight Format
```
Insight:
  domain: <governance-domain>
  summary: <description>
  artifact: <guided-link>
```

Insights help maintainers understand governance behavior.

---

## **9. Diagnostic Prioritization**

Diagnostics must be prioritized:

1. **Safety Diagnostics**  
2. **Error Diagnostics**  
3. **Warning Diagnostics**  
4. **Trace Diagnostics**  
5. **Insight Diagnostics**

Safety always overrides everything else.

---

## **10. Diagnostic Propagation Rules**

Diagnostics propagate through the pipeline:

```
Compiler → Optimizer → Linker → Loader → VM
```

Rules:

- errors halt propagation  
- warnings propagate with context  
- traces propagate fully  
- insights propagate fully  

---

## **11. Diagnostic Determinism**

Diagnostics must be:

- identical for identical input  
- identical ordering  
- identical content  
- identical artifact references  

This ensures governance consistency.

---

## **12. Machine‑Readable Diagnostics Spec**

```
gql_diagnostics:
  version: "1.0"
  categories:
    - error
    - warning
    - trace
    - insight
  pipeline_stages:
    - lexing
    - parsing
    - semantic_analysis
    - compilation
    - optimization
    - linking
    - loading
    - execution
  prioritization:
    - safety
    - error
    - warning
    - trace
    - insight
  deterministic: true
```

---

## **13. Placement Rules**

The Diagnostics Specification must be placed under:

```
NDH-Platforms/Orbital/governance/notes/
```

---

