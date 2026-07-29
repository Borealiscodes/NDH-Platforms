# NDH Runtime Orchestration Spec v1.0  
### Execution Substrate for NDH‑Cloud Audit Engine

---

## 1 — Purpose

The NDH Runtime Orchestration Spec defines **how NDH executes governance cycles**, including:

- audit gate sequencing  
- GQL compliance query invocation  
- Azure binding evaluation  
- envelope enforcement  
- trauma‑vector monitoring  
- drift detection  
- provenance gating  
- incident routing  

It is the **runtime layer** beneath the Operator Console and the Governance Envelope.

---

## 2 — Orchestration Model

NDH runtime follows a **six‑phase orchestration cycle**:

1. Initialization Phase  
2. Binding Phase  
3. Query Phase  
4. Gate Evaluation Phase  
5. Routing Phase  
6. Provenance Phase

Each phase is mandatory and ordered.

---

## 3 — Phase Definitions

### 3.1 Initialization Phase

Runtime loads:

- governance envelope  
- audit engine configuration  
- GQL schema  
- Azure binding map  
- operator console state  

Runtime verifies:

- envelope integrity  
- configuration continuity  
- no active drift  
- no unresolved trauma spikes  

If any check fails → route to  
**governance-incidents**.

---

### 3.2 Binding Phase

Runtime queries Azure surfaces:

- Azure Policy  
- Azure Resource Graph  
- Azure Monitor  
- Sentinel  

Bindings are validated against:

- topology invariant  
- trauma invariant  
- risk invariant  
- stability invariant  
- holonomy invariant  
- provenance invariant  

Binding failures →  
**Azure Binding Incident**.

---

### 3.3 Query Phase

Runtime executes all GQL compliance queries:

- **TopologyCompliance**  
- **TraumaCompliance**  
- **RiskCompliance**  
- **StabilityCompliance**  
- **DriftCompliance**  
- **ProvenanceCompliance**  

Results are cached for gate evaluation.

---

### 3.4 Gate Evaluation Phase

Runtime evaluates all six audit gates:

- topology  
- trauma  
- risk  
- stability  
- drift  
- provenance  

Gate failures →  
**Audit Gate Incident**.

All gates must pass before provenance is allowed.

---

### 3.5 Routing Phase

If any gate fails:

- provenance is blocked  
- incident is created  
- operator console is updated  
- envelope is reinforced  
- runtime halts until operator resolves incident  

Routing target:

```
NDH-PLATFORMS/Internal/governance-incidents/
```

---

### 3.6 Provenance Phase

Executed only if:

- all gates pass  
- envelope is stable  
- no drift detected  
- no trauma spikes  
- Azure bindings are valid  
- GQL queries show continuity  

Runtime writes:

- lineage delta  
- audit cycle metadata  
- envelope state snapshot  

If continuity breaks →  
**Provenance Continuity Incident**.

---

## 4 — Orchestration Loop

Runtime repeats the orchestration cycle:

```
Initialization → Binding → Query → Gate Evaluation → Routing → Provenance
```

This loop is continuous and stateful.

---

## 5 — Operator Interaction Points

The Operator Console interacts with runtime at:

- cycle start  
- gate evaluation  
- incident routing  
- provenance gating  
- envelope monitoring  

Operators may:

- trigger cycles  
- inspect gate results  
- inspect GQL results  
- inspect Azure bindings  
- resolve incidents  
- unblock provenance  

All operator actions must remain inside the Governance Envelope.

---

## 6 — Runtime Invariants

The runtime must enforce:

- envelope geometry  
- trauma-informed traversal  
- holonomy identity  
- Azure binding validity  
- GQL compliance  
- provenance continuity  
- directory governance invariants  

These invariants cannot be overridden by operators.

---

## 7 — Runtime Failure Modes

Runtime may fail due to:

- topology drift  
- trauma spikes  
- misalignment scalar overflow  
- envelope breach  
- Azure misbinding  
- GQL schema mismatch  
- provenance discontinuity  

All failures route to governance-incidents.

---

## 8 — Runtime Invariant

> NDH runtime must execute all governance cycles inside the NDH Governance Envelope.  
>  
> No provenance may be written unless all gates pass.  
>  
> Runtime may not bypass trauma constraints, drift detection, or envelope geometry.

This invariant is mandatory.

---

