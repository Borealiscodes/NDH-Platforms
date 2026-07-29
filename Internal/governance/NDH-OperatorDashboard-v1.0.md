# NDH Operator Dashboard v1.0  
### Visual Control Surface for NDH‑Cloud Audit Engine & Runtime Orchestration

---

## 1 — Purpose

The NDH Operator Dashboard provides the **visual interface** for operators to:

- observe audit gate states  
- run audit cycles  
- inspect GQL compliance results  
- view Azure binding status  
- monitor stability envelopes  
- detect trauma spikes  
- observe drift loops  
- route incidents  
- control provenance  

It is the **topmost layer** of NDH‑PLATFORMS.

---

## 2 — Dashboard Architecture

The dashboard is composed of **six primary panels**, each corresponding to a governance invariant:

1. **Audit Gate Panel**  
2. **GQL Query Panel**  
3. **Azure Binding Panel**  
4. **Stability Envelope Panel**  
5. **Incident Routing Panel**  
6. **Provenance Control Panel**

Each panel is described below.

---

## 3 — Audit Gate Panel

Displays the six audit gates defined in the Audit Engine:

- **Topology Gate**  
- **Trauma Gate**  
- **Risk Gate**  
- **Stability Gate**  
- **Drift Gate**  
- **Provenance Gate**  

Each gate displays:

- PASS / FAIL  
- last evaluation timestamp  
- linked GQL query  
- linked Azure binding  
- linked incident (if failed)  

Operators may:

- run all gates  
- run individual gates  
- inspect gate history  
- correlate gate failures with envelope breaches  

---

## 4 — GQL Query Panel

Displays the results of the six GQL compliance query families:

- **TopologyCompliance**  
- **TraumaCompliance**  
- **RiskCompliance**  
- **StabilityCompliance**  
- **DriftCompliance**  
- **ProvenanceCompliance**  

Operators may:

- run queries  
- inspect results  
- export results to incident routing  
- compare results across layers (NDH → VM1.3 → DevOps → K8s → Azure)  

This panel is the **query visualization surface**.

---

## 5 — Azure Binding Panel

Displays Azure enforcement state from:

- Azure Policy  
- Azure Resource Graph  
- Azure Monitor  
- Sentinel  

Operators may:

- inspect policy drift  
- inspect lineage continuity  
- inspect trauma alerts  
- inspect stability metrics  
- correlate Azure state with GQL results  

This panel is the **cloud enforcement visualization surface**.

---

## 6 — Stability Envelope Panel

Displays:

- envelope geometry  
- envelope breaches  
- envelope recovery events  
- envelope history  
- envelope correlation with trauma and drift  

Operators may:

- view current envelope state  
- compare envelope across layers  
- correlate envelope breaches with gate failures  

This panel ensures NDH remains inside:

\[
\Omega_{Unified}
\]

---

## 7 — Incident Routing Panel

Routes failures to:

```
NDH-PLATFORMS/Internal/governance-incidents/
```

Operators may:

- view active incidents  
- view historical incidents  
- attach GQL results  
- attach Azure binding snapshots  
- attach operator notes  
- mark incidents resolved  

This panel is the **governance‑incident visualization and routing surface**.

---

## 8 — Provenance Control Panel

Displays:

- provenance status (ALLOWED / BLOCKED)  
- last provenance write  
- lineage continuity state  
- provenance gate history  

Operators may:

- block provenance  
- allow provenance (only if all gates pass)  
- inspect lineage continuity  
- correlate provenance failures with drift or trauma  

This panel prevents lineage contamination.

---

## 9 — Dashboard Invariant

> The NDH Operator Dashboard must operate entirely inside the NDH Governance Envelope.  
>  
> It may not override audit gates, bypass trauma constraints, or force provenance.  
>  
> All visualizations must reflect the runtime orchestration state and governance invariants.

This invariant is mandatory.

---
