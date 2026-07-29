# NDH Dashboard State Machine v1.0  
### Governed State Model for NDH Operator Dashboard

---

## 1 — Purpose

The Dashboard State Machine defines:

- the **set of dashboard states**  
- the **permitted transitions** between those states  
- the **event‑flow mapping** from runtime to UI  
- the **reaction rules** for gate failures and envelope breaches  
- the **provenance‑lock behavior** under continuity or safety violations  

It ensures the dashboard cannot drift, misrepresent runtime, or allow unsafe operator behavior.

---

## 2 — State inventory

Canonical dashboard states:

- **IDLE**  
  Dashboard loaded; no active audit cycle.

- **INITIALIZING**  
  Runtime initialization and envelope checks in progress.

- **BINDING_EVAL**  
  Azure bindings being evaluated (Policy, Resource Graph, Monitor, Sentinel).

- **QUERY_RUNNING**  
  GQL compliance queries executing.

- **GATE_EVAL**  
  Audit gates evaluating (topology, trauma, risk, stability, drift, provenance).

- **PROVENANCE_PENDING**  
  All gates passed; provenance decision pending.

- **PROVENANCE_ALLOWED**  
  Provenance write permitted and in progress.

- **PROVENANCE_BLOCKED**  
  Provenance locked due to gate, continuity, or envelope failure.

- **INCIDENT_OPEN**  
  One or more governance incidents active.

- **CONTINUITY_BREACH**  
  Runtime continuity failure detected.

- **ENVELOPE_BREACH**  
  Governance or runtime safety envelope breach detected.

These states are exhaustive for the operator dashboard.

---

## 3 — State diagram (textual)

State transitions (simplified):

- `IDLE → INITIALIZING`  
  When operator triggers an audit cycle.

- `INITIALIZING → BINDING_EVAL`  
  When initialization completes without envelope or continuity breach.

- `BINDING_EVAL → QUERY_RUNNING`  
  When Azure bindings validated or incidents opened.

- `QUERY_RUNNING → GATE_EVAL`  
  When all GQL compliance queries complete.

- `GATE_EVAL → PROVENANCE_PENDING`  
  When all gates pass.

- `GATE_EVAL → PROVENANCE_BLOCKED`  
  When any gate fails.

- `PROVENANCE_PENDING → PROVENANCE_ALLOWED`  
  When continuity and safety invariants hold and operator confirms.

- `PROVENANCE_PENDING → PROVENANCE_BLOCKED`  
  When continuity or safety invariants fail.

- `ANY_STATE → INCIDENT_OPEN`  
  When an incident is created.

- `ANY_STATE → CONTINUITY_BREACH`  
  When continuity model detects a break.

- `ANY_STATE → ENVELOPE_BREACH`  
  When governance or runtime safety envelope is violated.

- `INCIDENT_OPEN → IDLE`  
  When all incidents resolved and no active cycle.

- `CONTINUITY_BREACH → INITIALIZING`  
  After restoration sequence and operator re‑start.

- `ENVELOPE_BREACH → INITIALIZING`  
  After remediation and envelope re‑validation.

No direct transition to `PROVENANCE_ALLOWED` is permitted from any state other than `PROVENANCE_PENDING`.

---

## 4 — Transition constraints

All transitions must respect:

- **Runtime Continuity Model v1.0**  
  No transition may bypass continuity checks.

- **Runtime Safety Envelope v1.0**  
  No transition may enter a state that implies unsafe execution.

- **Governance Envelope v1.0**  
  No transition may allow provenance outside governance bounds.

- **Dashboard Interaction Model v1.0**  
  Operator actions may only trigger permitted transitions.

Forbidden patterns:

- `IDLE → PROVENANCE_ALLOWED` (skips all gates)  
- `GATE_EVAL → PROVENANCE_ALLOWED` without `PROVENANCE_PENDING`  
- `PROVENANCE_BLOCKED → PROVENANCE_ALLOWED` without incident resolution and full re‑evaluation  
- `CONTINUITY_BREACH → PROVENANCE_ALLOWED` directly  
- `ENVELOPE_BREACH → PROVENANCE_ALLOWED` directly  

---

## 5 — Runtime event mapping

Runtime events drive dashboard transitions:

- **Initialization complete** → `INITIALIZING → BINDING_EVAL`  
- **Bindings evaluated** → `BINDING_EVAL → QUERY_RUNNING`  
- **Queries complete** → `QUERY_RUNNING → GATE_EVAL`  
- **All gates pass** → `GATE_EVAL → PROVENANCE_PENDING`  
- **Any gate fails** → `GATE_EVAL → PROVENANCE_BLOCKED` + `INCIDENT_OPEN`  
- **Continuity break** → `ANY_STATE → CONTINUITY_BREACH`  
- **Envelope breach** → `ANY_STATE → ENVELOPE_BREACH`  

Operator actions are **gated** by these runtime events and cannot force transitions that contradict them.

---

## 6 — Provenance lock behavior

Provenance is locked (`PROVENANCE_BLOCKED`) when:

- any gate fails  
- continuity invariants fail  
- runtime safety envelope breached  
- governance envelope breached  
- unresolved incidents exist that affect provenance safety  

Unlocking provenance requires:

- incident resolution  
- continuity restoration  
- envelope re‑validation  
- full re‑run of the orchestration cycle  
- successful gate evaluation  

Only then may the dashboard transition:

`PROVENANCE_PENDING → PROVENANCE_ALLOWED`.

---

## 7 — State machine invariant

> The NDH Operator Dashboard must follow the NDH Dashboard State Machine v1.0  
> exactly. No state skipping, no forced provenance, no bypass of continuity or  
> safety constraints is permitted. All transitions must reflect actual runtime  
> orchestration, continuity, and envelope state.

This invariant is mandatory.
