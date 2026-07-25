# 🛰️ **GQL State Transition Specification (v1.0)**  
### File Path  
```
NDH-Platforms/Orbital/governance/notes/orbital-gql-state-transition-spec-v1.0.md
```

---

## **1. Purpose**

The State Transition Specification defines:

- the formal state machine governing GQL execution  
- the transition rules for each governance context  
- the invariants that must hold across transitions  
- the interaction between contexts (naming ↔ provenance ↔ enforcement…)  
- the safety‑gated transition model  
- the deterministic evolution of governance state  
- the conditions under which transitions are allowed or forbidden  

It is the **mathematical semantics** of GQL.

---

## **2. Governance State Model**

The GQL‑VM maintains six independent but interlinked contexts:

1. **Naming Context**  
2. **Provenance Context**  
3. **Structural Context**  
4. **Enforcement Context**  
5. **Temporal Context**  
6. **Safety Context**

Each context has:

- **state variables**  
- **transition rules**  
- **invariants**  
- **cross‑context dependencies**

---

## **3. State Variables**

### **Naming Context**
- `current_family`  
- `allowed_families`  
- `rhythm_pattern`  
- `shape_pattern`  
- `naming_invariants`

### **Provenance Context**
- `current_lineage`  
- `allowed_boundaries`  
- `ancestry_chain`  
- `descendant_chain`

### **Structural Context**
- `current_volume`  
- `current_section`  
- `structural_requirements`

### **Enforcement Context**
- `schema_rules`  
- `validator_rules`  
- `automation_rules`  
- `merge_blockers`

### **Temporal Context**
- `year`  
- `quarter`  
- `range_start`  
- `range_end`

### **Safety Context**
- `allowed_naming_families`  
- `allowed_provenance_boundaries`  
- `allowed_structural_volumes`  
- `allowed_enforcement_rules`  
- `allowed_temporal_ranges`

---

## **4. Transition Model**

Each instruction triggers a **state transition**:

```
S_next = T(opcode, operands, S_current)
```

Where:

- `S_current` is the current governance state  
- `opcode` is the instruction  
- `operands` are instruction parameters  
- `T` is the transition function  
- `S_next` is the next governance state  

Transitions must be:

- deterministic  
- safety‑checked  
- context‑aware  
- provenance‑respecting  
- naming‑invariant‑preserving  

---

## **5. Transition Rules by Context**

### **Naming Context Transitions**

#### **NAM_FAMILY(f)**  
```
current_family := f
```
Allowed only if:
```
f ∈ allowed_naming_families
```

#### **NAM_RHYTHM(p)**  
```
rhythm_pattern := p
```

#### **NAM_SHAPE(p)**  
```
shape_pattern := p
```

Naming transitions must respect the **Naming Invariant Ledger**.

---

### **Provenance Context Transitions**

#### **PROV_ANCESTOR(x)**  
```
ancestry_chain := ancestry_chain ∪ {x}
```

#### **PROV_DESCENDANT(x)**  
```
descendant_chain := descendant_chain ∪ {x}
```

#### **PROV_BOUNDARY(b)**  
```
current_boundary := b
```
Allowed only if:
```
b ∈ allowed_provenance_boundaries
```

Provenance transitions must respect the **Governance Constitution**.

---

### **Structural Context Transitions**

#### **STR_VOLUME(v)**  
```
current_volume := v
```
Allowed only if:
```
v ∈ allowed_structural_volumes
```

#### **STR_SECTION(s)**  
```
current_section := s
```

Structural transitions must respect the **Governance Compendium**.

---

### **Enforcement Context Transitions**

#### **ENF_SCHEMA(r)**  
```
schema_rules := schema_rules ∪ {r}
```

#### **ENF_VALIDATOR(r)**  
```
validator_rules := validator_rules ∪ {r}
```

#### **ENF_AUTOMATION(r)**  
```
automation_rules := automation_rules ∪ {r}
```

#### **ENF_BLOCKS_MERGE**  
```
merge_blockers := merge_blockers ∪ {current_rule}
```

Enforcement transitions must respect:

- Schema  
- Validator  
- Automation Spec  

---

### **Temporal Context Transitions**

#### **TMP_YEAR(y)**  
```
year := y
```

#### **TMP_QUARTER(q)**  
```
quarter := q
year := infer_year(q)
```

#### **TMP_AFTER(e)**  
```
range_start := event_time(e)
```

#### **TMP_BEFORE(e)**  
```
range_end := event_time(e)
```

Temporal transitions must respect:

- **Governance Calendar**  
- **Governance Almanac**

---

### **Safety Context Transitions**

Safety context is **read‑only** during execution.

Transitions must check:

```
if not allowed(context_change):
    raise SafetyViolation
```

Safety rules come from:

- **Meta‑Document**  
- **Refinement Blueprint**  
- **Suite Index**  

---

## **6. Cross‑Context Dependencies**

### **Naming ↔ Provenance**
Naming families may imply provenance boundaries.

### **Structural ↔ Enforcement**
Certain volumes require specific enforcement rules.

### **Temporal ↔ Enforcement**
Temporal ranges may activate or deactivate enforcement rules.

### **Provenance ↔ Safety**
Cross‑boundary lineage transitions may violate safety.

---

## **7. Invariants**

The following must always hold:

### **Naming Invariant**
```
current_family ∈ allowed_naming_families
```

### **Provenance Invariant**
```
current_boundary ∈ allowed_provenance_boundaries
```

### **Structural Invariant**
```
current_volume ∈ allowed_structural_volumes
```

### **Enforcement Invariant**
```
validator_rules ⊆ allowed_enforcement_rules
```

### **Temporal Invariant**
```
range_start ≤ range_end
```

### **Safety Invariant**
```
∀ transitions: allowed(context_change)
```

---

## **8. Deterministic Transition Guarantees**

The State Transition Model guarantees:

- identical state evolution for identical bytecode  
- identical context values at each step  
- identical safety behavior  
- identical final results  

This ensures governance consistency across environments.

---

## **9. Machine‑Readable State Transition Spec**

```
gql_state_transition:
  version: "1.0"
  contexts:
    - naming
    - provenance
    - structural
    - enforcement
    - temporal
    - safety
  transition_rules:
    naming: NAM_FAMILY, NAM_RHYTHM, NAM_SHAPE
    provenance: PROV_ANCESTOR, PROV_DESCENDANT, PROV_BOUNDARY, PROV_LINEAGE
    structural: STR_VOLUME, STR_SECTION, STR_BANNER, STR_FOOTER
    enforcement: ENF_SCHEMA, ENF_VALIDATOR, ENF_AUTOMATION, ENF_BLOCKS_MERGE
    temporal: TMP_YEAR, TMP_QUARTER, TMP_AFTER, TMP_BEFORE
  invariants:
    - naming_invariant
    - provenance_invariant
    - structural_invariant
    - enforcement_invariant
    - temporal_invariant
    - safety_invariant
  deterministic: true
```

---

## **10. Placement Rules**

The State Transition Specification must be placed under:

```
NDH-Platforms/Orbital/governance/notes/
```

---

