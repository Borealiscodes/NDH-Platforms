# 🛰️ **GQL Logging Specification (v1.0)**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-gql-logging-spec-v1.0.md
```

---

## **1. Purpose**

The GQL Logging Specification defines:

- the persistent logging format for GQL  
- log levels and governance‑aware categories  
- retention and rotation rules  
- cross‑repo logging boundaries  
- safety‑critical logging requirements  
- how logs integrate with the **GQL Diagnostics** layer  
- how logs support governance audits, lineage reviews, and invariant enforcement  
- deterministic logging guarantees  

It is the **long‑term audit trail** of the GQL stack.

---

## **2. Logging Categories**

Logs are grouped into **five categories**, each with strict semantics:

1. **Safety Logs** — highest priority  
2. **Error Logs** — fatal conditions  
3. **Warning Logs** — non‑fatal anomalies  
4. **Execution Logs** — step‑level VM activity  
5. **Insight Logs** — semantic/naming/provenance summaries  

Each category has its own retention rules and required fields.

---

## **3. Log Levels**

The GQL logging system defines **six levels**:

| Level | Meaning |
|-------|---------|
| `CRITICAL` | Safety violation or fatal governance corruption risk |
| `ERROR` | Fatal error halting execution |
| `WARN` | Non‑fatal anomaly |
| `INFO` | High‑level execution information |
| `TRACE` | Step‑by‑step VM execution |
| `DEBUG` | Deep introspection for maintainers |

Safety logs always use `CRITICAL`.

---

## **4. Log Structure**

Every log entry contains:

- `timestamp` (ISO‑8601)  
- `level`  
- `category`  
- `message`  
- `governance_domain` (naming, provenance, structural, enforcement, temporal, safety)  
- `bytecode_location` (optional)  
- `ast_location` (optional)  
- `execution_step` (optional)  
- `context_snapshot` (optional)  
- `artifact_reference` (guided link)  

Example:

```
2026-07-25T16:22:14Z CRITICAL SAFETY
Violation: forbidden provenance boundary "CORE" in Emergent-only module
Artifact: Governance Constitution
```

---

## **5. Safety Logging Rules**

Safety logs are **mandatory**, **persistent**, and **never pruned**.

They must record:

- naming contamination attempts  
- provenance boundary violations  
- structural drift  
- enforcement contradictions  
- temporal contradictions  

Safety logs integrate with:

- **Meta‑Document**  
- **Refinement Blueprint**  
- **Suite Index**  

These define cross‑repo safety boundaries.

---

## **6. Error Logging Rules**

Error logs must record:

- error domain  
- error type  
- failing opcode  
- failing operand  
- failing segment  
- relevant governance artifact  

Errors always halt execution.

---

## **7. Warning Logging Rules**

Warnings must record:

- canonicalization  
- pruning  
- flattening  
- consolidation  
- compression  

Warnings never halt execution.

---

## **8. Execution Logging Rules**

Execution logs record:

- instruction fetch  
- instruction decode  
- safety check result  
- state transition  
- search engine invocation  
- merge and ranking steps  

Execution logs are deterministic and reproducible.

---

## **9. Insight Logging Rules**

Insights record:

- semantic relevance summaries  
- naming‑family clustering  
- provenance lineage summaries  
- structural navigation summaries  
- enforcement rule activation summaries  
- temporal range summaries  

Insights help maintainers understand governance behavior.

---

## **10. Log Retention & Rotation**

Retention rules:

| Category | Retention |
|----------|-----------|
| Safety | Permanent |
| Error | 5 years |
| Warning | 2 years |
| Execution | 1 year |
| Insight | 1 year |

Rotation rules:

- logs rotate daily  
- safety logs never rotate  
- rotation must preserve ordering  

---

## **11. Cross‑Repo Logging Boundaries**

Logs must respect repo boundaries defined by:

- Meta‑Document  
- Refinement Blueprint  
- Suite Index  

Rules:

- CORE logs cannot include TIDS context  
- TIDS logs cannot include Emergent context  
- Emergent logs cannot include Orbital context  
- Orbital logs may include all contexts  

This prevents cross‑repo leakage.

---

## **12. Deterministic Logging Guarantees**

The Logging Specification guarantees:

- identical logs for identical bytecode  
- identical ordering  
- identical safety behavior  
- identical retention behavior  

This ensures governance auditability.

---

## **13. Machine‑Readable Logging Spec**

```
gql_logging:
  version: "1.0"
  categories:
    - safety
    - error
    - warning
    - execution
    - insight
  levels:
    - CRITICAL
    - ERROR
    - WARN
    - INFO
    - TRACE
    - DEBUG
  retention:
    safety: permanent
    error: 5y
    warning: 2y
    execution: 1y
    insight: 1y
  rotation: daily
  deterministic: true
```

---

## **14. Placement Rules**

The Logging Specification must be placed under:

```
NDH-Platforms/Orbital/governance/notes/
```

---

