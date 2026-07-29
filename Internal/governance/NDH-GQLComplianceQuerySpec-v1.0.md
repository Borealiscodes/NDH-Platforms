### 🟣 NDH GQL Compliance Query Spec v1.0  
*Unified Compliance Query Layer for NDH-Cloud Audit Engine*

#### 1 — Purpose

- **Goal:** Provide a single GQL-based query surface for the NDH‑Cloud Audit Engine.  
- **Scope:** NDH, VM 1.3, DevOps, Kubernetes, Azure (Policy, Resource Graph, Monitor, Sentinel).  
- **Function:** Evaluate compliance for:
  - topology  
  - trauma  
  - risk  
  - stability  
  - drift  
  - provenance  

---

#### 2 — Core GQL schema (conceptual)

**2.1 Entities**

- **Resource**  
  - fields: `id`, `type`, `layer`, `tags`, `topologyState`, `stabilityState`
- **Event**  
  - fields: `id`, `timestamp`, `layer`, `kind`, `severity`, `traumaSignal`
- **PolicyBinding**  
  - fields: `id`, `azurePolicyId`, `ndhVector`, `status`
- **LineageEdge**  
  - fields: `fromId`, `toId`, `kind`, `timestamp`

---

#### 3 — Compliance query families

**3.1 Topology Compliance Query**

- **Intent:** Detect topology violations across NDH → VM 1.3 → DevOps → K8s → Azure.  
- **Example (conceptual):**

```gql
query TopologyCompliance {
  resources(where: { topologyState: { neq: "Valid" } }) {
    id
    layer
    type
    topologyState
  }
}
```

---

**3.2 Trauma Compliance Query**

- **Intent:** Surface trauma vector spikes and unresolved incidents.  

```gql
query TraumaCompliance {
  events(where: { traumaSignal: { gt: "Threshold" } }) {
    id
    timestamp
    layer
    kind
    traumaSignal
    severity
  }
}
```

---

**3.3 Risk (Misalignment Scalar) Compliance Query**

- **Intent:** Check misalignment scalar against allowed bounds.  

```gql
query RiskCompliance {
  resources(where: { riskScalar: { gt: "MaxAllowed" } }) {
    id
    layer
    riskScalar
  }
}
```

---

**3.4 Stability Envelope Compliance Query**

- **Intent:** Ensure all active resources are inside ΩUnified.  

```gql
query StabilityCompliance {
  resources(where: { stabilityState: { neq: "InsideEnvelope" } }) {
    id
    layer
    stabilityState
  }
}
```

---

**3.5 Holonomy Drift Compliance Query**

- **Intent:** Detect governance loops where holonomy is non‑identity.  

```gql
query DriftCompliance {
  loops(where: { holonomyState: { neq: "Identity" } }) {
    loopId
    layer
    holonomyState
  }
}
```

---

**3.6 Provenance Continuity Compliance Query**

- **Intent:** Verify lineage continuity before provenance write.  

```gql
query ProvenanceCompliance {
  lineageBreaks {
    fromId
    toId
    kind
    timestamp
  }
}
```

---

#### 4 — Audit engine integration

- Each query family maps directly to one audit gate:
  - Topology → Topology Gate  
  - Trauma → Trauma Gate  
  - Risk → Risk Gate  
  - Stability → Stability Gate  
  - Drift → Drift Gate  
  - Provenance → Provenance Gate  
- The NDH‑Cloud Audit Engine:
  - runs these GQL queries  
  - aggregates results  
  - blocks provenance if any gate fails  
  - routes incidents to `Internal/governance-incidents/`.

---


