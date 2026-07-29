# NDH Dashboard Interaction Model v1.0  
### Operator Interaction Rules & Event Flow Mapping for NDH‑PLATFORMS

---

## 1 — Purpose

The Dashboard Interaction Model defines **how operators interact with the NDH Operator Dashboard**, including:

- permitted interactions  
- prohibited interactions  
- event‑flow mapping  
- gate‑trigger behavior  
- query invocation rules  
- envelope‑aware visual behavior  
- provenance control constraints  
- incident routing triggers  

It ensures all operator actions remain inside the **NDH Governance Envelope** and the **NDH Runtime Safety Envelope**.

---

## 2 — Interaction Architecture

Dashboard interactions are divided into six surfaces:

1. **Audit Gate Interaction Surface**  
2. **GQL Query Interaction Surface**  
3. **Azure Binding Interaction Surface**  
4. **Stability Envelope Interaction Surface**  
5. **Incident Routing Interaction Surface**  
6. **Provenance Control Interaction Surface**

Each surface maps directly to runtime orchestration primitives.

---

## 3 — Audit Gate Interaction Surface

Operators may:

- trigger full audit cycles  
- trigger individual gate evaluations  
- inspect gate history  
- open linked incidents  
- correlate gate failures with envelope breaches  

Operators may not:

- override gate results  
- bypass gate sequencing  
- force gate PASS states  
- suppress trauma or drift gate failures  

Gate interactions map to runtime orchestration:

```
Gate Trigger → Runtime Query Phase → Gate Evaluation Phase → Dashboard Update
```

---

## 4 — GQL Query Interaction Surface

Operators may:

- run individual GQL queries  
- run full query families  
- inspect query results  
- export results to incident routing  
- correlate query results across layers  

Operators may not:

- modify query definitions  
- bypass query ordering  
- run queries outside runtime safety boundaries  

Query interactions map to runtime orchestration:

```
Query Trigger → Runtime Query Phase → Dashboard Result Surface
```

---

## 5 — Azure Binding Interaction Surface

Operators may:

- inspect Azure Policy state  
- inspect Resource Graph lineage  
- inspect Monitor metrics  
- inspect Sentinel incidents  
- correlate Azure state with GQL results  

Operators may not:

- modify Azure bindings  
- suppress binding drift  
- override Azure enforcement states  

Binding interactions map to runtime orchestration:

```
Binding Inspection → Runtime Binding Phase → Dashboard Binding Surface
```

---

## 6 — Stability Envelope Interaction Surface

Operators may:

- view envelope geometry  
- inspect envelope breaches  
- correlate envelope breaches with trauma or drift  
- inspect envelope history  

Operators may not:

- override envelope geometry  
- force envelope PASS states  
- suppress envelope breach warnings  

Envelope interactions map to runtime orchestration:

```
Envelope Inspection → Runtime Stability Phase → Dashboard Envelope Surface
```

---

## 7 — Incident Routing Interaction Surface

Operators may:

- open incidents  
- attach GQL results  
- attach Azure binding snapshots  
- attach operator notes  
- mark incidents resolved  

Operators may not:

- delete incidents  
- suppress incident creation  
- bypass routing logic  

Incident interactions map to runtime orchestration:

```
Incident Trigger → Routing Phase → governance-incidents/
```

---

## 8 — Provenance Control Interaction Surface

Operators may:

- block provenance  
- allow provenance (only if all gates pass)  
- inspect lineage continuity  
- inspect provenance gate history  

Operators may not:

- force provenance writes  
- bypass provenance gate  
- override continuity checks  

Provenance interactions map to runtime orchestration:

```
Provenance Action → Provenance Phase → Dashboard Provenance Surface
```

---

## 9 — Interaction Invariants

The dashboard must enforce:

- Governance Envelope boundaries  
- Runtime Safety Envelope boundaries  
- trauma‑informed interaction constraints  
- holonomy identity conditions  
- stability envelope geometry  
- provenance continuity rules  

Operators must remain inside these boundaries at all times.

---

## 10 — Dashboard Interaction Invariant

> All operator interactions must remain inside the NDH Governance Envelope and  
> NDH Runtime Safety Envelope.  
>  
> No interaction may override audit gates, bypass trauma constraints, suppress  
> drift detection, or force provenance.  
>  
> Dashboard interactions must reflect runtime orchestration state exactly.

This invariant is mandatory.

---

