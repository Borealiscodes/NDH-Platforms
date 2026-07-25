# 🛰️ **Orbital Governance Validator (v1.0)**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-governance-validator-v1.0.md
```

---

## **1. Purpose**

The Governance Validator defines:

- how to check structural compliance  
- how to enforce naming invariants  
- how to validate provenance markers  
- how to detect rhythm and shape drift  
- how to ensure cross‑repo linkage  
- how to verify accessibility rules  
- how to apply the Governance Schema programmatically  

Orbital maintains this validator as part of its enforcement authority.

---

## **2. Validator Responsibilities**

The validator must confirm that every Orbital governance document:

- includes the **Governance Banner**  
- follows the required section ordering  
- includes the **Governance Footer**  
- references the Meta‑Document, Blueprint, and Suite Index  
- uses naming families defined in the **Naming Invariant Ledger**  
- avoids rhythm drift and shape drift  
- includes provenance anchors  
- follows accessibility rules  
- is placed in the correct directory  

This ensures structural and semantic stability.

---

## **3. Validation Workflow**

### **Step 1 — Structural Validation**  
Check for:

- banner present  
- footer present  
- required sections present  
- correct section order  
- correct header levels  
- correct placement path  

### **Step 2 — Naming Validation**  
Check that:

- all acronyms belong to canonical naming families  
- no naming outliers exist  
- acronym rhythm is stable  
- acronym shape is consistent  
- no cross‑layer naming contamination occurs  

### **Step 3 — Provenance Validation**  
Confirm:

- provenance scope is declared  
- lineage markers are present  
- provenance anchors match the Meta‑Document  
- cross‑repo boundaries are respected  

### **Step 4 — Accessibility Validation**  
Ensure:

- rhythm stability  
- no dense acronym clusters  
- no stress‑triggering naming patterns  
- predictable section flow  
- dyslexia‑aware formatting  

### **Step 5 — Cross‑Repo Linkage Validation**  
Verify references to:

- **Meta‑Document**  
- **Refinement Blueprint**  
- **Suite Index**  

### **Step 6 — Schema Compliance**  
Validate against the **Governance Schema**:

- required fields  
- required references  
- required provenance markers  
- required naming invariants  
- required accessibility rules  

---

## **4. Validator Output**

The validator must produce:

### **Pass Report**  
If all checks succeed:

- “Document is governance‑compliant.”  
- List of validated invariants  
- No warnings  

### **Warning Report**  
If non‑critical issues exist:

- rhythm drift  
- minor naming inconsistencies  
- missing optional references  

### **Failure Report**  
If critical issues exist:

- missing banner/footer  
- missing required sections  
- naming outliers  
- provenance violations  
- schema non‑compliance  

Failures must block commit until resolved.

---

## **5. Enforcement Rules**

- No Orbital governance document may be committed without passing validation.  
- Repo‑specific documents (CORE, TIDS, Emergent) may be committed even if they fail Orbital validation — but their governance references must pass.  
- The validator must run automatically on PR creation.  
- Human reviewers must check validator output before approving merges.  

---

## **6. Placement Rules**

The validator specification must be placed under:

```
NDH-Platforms/Orbital/governance/notes/
```

This ensures structural consistency.

---

