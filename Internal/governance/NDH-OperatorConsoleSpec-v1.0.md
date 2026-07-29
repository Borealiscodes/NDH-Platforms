# NDH Operator Console Spec v1.0  
### Operator Control Plane for NDH‑Cloud Audit Engine

---

## 1 — Purpose

The NDH Operator Console provides the **human control surface** for:

- running audit cycles  
- invoking GQL compliance queries  
- viewing Azure binding states  
- monitoring stability envelopes  
- detecting trauma spikes  
- observing drift loops  
- routing governance incidents  
- blocking or allowing provenance  

It is the **operator‑facing layer** of NDH‑PLATFORMS.

---

## 2 — Console Architecture

The console is divided into six panels:

1. **Audit Gate Panel**  
2. **GQL Query Panel**  
3. **Azure Binding Panel**  
4. **Stability Envelope Panel**  
5. **Incident Routing Panel**  
6. **Provenance Control Panel**

Each panel corresponds to a governance invariant.

---

## 3 — Audit Gate Panel

Displays the six audit gates:

- **Topology Gate**  
- **Trauma Gate**  
- **Risk Gate**  
- **Stability Gate**  
- **Drift Gate**  
- **Provenance Gate**  

Each gate shows:

- PASS / FAIL  
- last run timestamp  
- linked incident (if failed)  
- GQL query used  
- Azure binding used  

Operators may:

- run all gates  
- run a single gate  
- view gate history  
- view gate dependencies  

---

## 4 — GQL Query Panel

Provides direct operator access to:

- **TopologyCompliance**  
- **TraumaCompliance**  
- **RiskCompliance**  
- **StabilityCompliance**  
- **DriftCompliance**  
- **ProvenanceCompliance**

Operators may:

- run queries  
- inspect results  
- export results to the incident panel  
- compare query results across layers  

This panel is the **query surface** of the console.

---

## 5 — Azure Binding Panel

Displays Azure enforcement state from:

- Azure Policy  
- Azure Resource Graph  
- Azure Monitor  
- Sentinel  

Operators may:

- view binding status  
- inspect policy drift  
- inspect lineage continuity  
- inspect trauma alerts  
- inspect stability metrics  

This panel is the **cloud enforcement surface**.

---

## 6 — Stability Envelope Panel

Displays:

- envelope geometry  
- envelope breaches  
- envelope history  
- envelope recovery events  

Operators may:

- view envelope state  
- compare envelope across layers  
- correlate envelope breaches with trauma spikes  
- correlate envelope breaches with drift loops  

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

This panel is the **governance‑incident control surface**.

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

## 9 — Console Invariant

> The NDH Operator Console must operate entirely inside the NDH Governance Envelope.  
>  
> It may not override audit gates, bypass trauma constraints, or force provenance.  
>  
> All operator actions must respect envelope geometry and governance invariants.

This invariant is mandatory.

---

