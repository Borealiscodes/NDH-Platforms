# 🛰️ **NDH Raw Dataset Population Plan (Internal Asset v1.0)**  
### *How NDH captures, validates, structures, and governs telemetry before GQL ingestion*

**Scope:** Internal — Developer Grade  
**Status:** Foundational Telemetry Plan  
**Version:** 1.0  
**Purpose:** Define how NDH populates its raw dataset layer so GQL can operate consistently, safely, and without drift.

---

## ⭐ 1 — Purpose of the Raw Dataset Population Plan

NDH governance depends on **raw telemetry**.  
Telemetry must be:

- captured  
- validated  
- normalized  
- stored  
- versioned  
- governed  
- mapped into canonical JSON schemas  
- fed into GQL  

This plan ensures the raw dataset is:

- stable  
- non‑drifting  
- provenance‑safe  
- GQL‑ready  
- searchable by the developer‑grade engine  
- never exposed to the public engine  

---

## ⭐ 2 — Telemetry Capture Model

### 2.1 Capture Sources  
NDH captures telemetry from:

- configuration systems  
- deployment pipelines  
- runtime infrastructure  
- policy engines  
- compliance evaluators  
- access control systems  
- resource health monitors  
- CI/CD events  
- governance workflows  

### 2.2 Capture Modes  
Telemetry enters NDH via:

- **push** (systems emit events)  
- **pull** (NDH queries systems)  
- **hybrid** (scheduled polling + event streams)  

### 2.3 Capture Envelope  
All telemetry must conform to the envelope:

- `id`  
- `timestamp`  
- `source`  
- `type`  
- `payload`  
- `provenance`  
- `severity`  

Telemetry failing envelope validation is:

- rejected  
- logged  
- quarantined  

---

## ⭐ 3 — Validation Pipeline

### 3.1 Structural Validation  
Checks:

- envelope completeness  
- JSON schema conformity  
- type correctness  
- required fields present  

### 3.2 Provenance Validation  
Ensures:

- trusted origin  
- integrity  
- no tampering  
- correct signing (if applicable)  

### 3.3 Semantic Validation  
Ensures:

- event type matches payload  
- environment identifiers are valid  
- policy sets exist  
- resource identifiers resolve  

Invalid telemetry is:

- rejected  
- logged  
- optionally reprocessed  

---

## ⭐ 4 — Canonical Dataset Schema

Raw telemetry is mapped into a **canonical dataset schema** before GQL ingestion.

### 4.1 Canonical Fields  
- `entity_id`  
- `environment`  
- `policy_set`  
- `event_type`  
- `governance_dimension`  
- `raw_payload`  
- `normalized_payload`  
- `provenance`  
- `severity`  
- `timestamp`  

### 4.2 Canonical Dimensions  
- **Compliance**  
- **Configuration Drift**  
- **Stability**  
- **Access & Permissions**  
- **Resource Health**  
- **Deployment Events**  

### 4.3 Canonical Storage Format  
- JSON  
- versioned  
- immutable  
- append‑only  

---

## ⭐ 5 — Storage & Versioning Model

### 5.1 Storage Requirements  
Raw dataset storage must be:

- durable  
- append‑only  
- versioned  
- provenance‑preserving  
- searchable  
- GQL‑accessible  

### 5.2 Versioning Rules  
- every telemetry event gets a version  
- every normalized payload gets a version  
- every canonical dataset snapshot gets a version  

### 5.3 Retention  
Retention is governed by:

- compliance requirements  
- operational needs  
- governance analysis windows  

---

## ⭐ 6 — Dataset Governance

### 6.1 Safety  
Raw dataset is **internal only**.

### 6.2 Access Control  
Only:

- GQL  
- internal NDH reports  
- internal companions  
- developer‑grade search engine  

may access raw dataset.

### 6.3 Public Safety  
Public artifacts receive:

- summaries  
- aggregates  
- conceptual diagrams  

Never raw data.

---

## ⭐ 7 — Integration with GQL

Raw dataset feeds GQL:

- ingestion  
- normalization  
- evaluation  
- governance signal formation  
- governance state emission  

GQL depends on:

- canonical schema  
- stable versioning  
- provenance integrity  
- non‑drifting dataset  

---

## ⭐ 8 — Integration with Search Engines

### Developer‑Grade Search Engine  
Indexes:

- raw dataset metadata  
- canonical schema  
- provenance  
- versioning  
- GQL outputs  

### Accessible Search Engine  
Indexes:

- public summaries  
- conceptual diagrams  
- sanitized governance explanations  

Never raw data.

---

## ⭐ 9 — Repo Integration

**File path:**

```
NDH-Platforms/Internal/architecture/NDH-Raw-Dataset-Population-Plan-v1.0.md
```

---

## ⭐ 10 — Summary (zen‑clean)

> Raw telemetry → validated → normalized → canonical dataset → GQL → internal reports → public summaries.  
>  
> Raw dataset is internal only.  
>  
> GQL depends on this plan.  
>  
> Search engines depend on this plan.  
>  
> Repo governance depends on this plan.  
>  
> This is the backbone of NDH telemetry architecture.

---

