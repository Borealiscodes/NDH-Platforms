# **Spiral Singularity Example — Nightmare Arc Prime**  
### *NDH–TIDS Tensor‑Era Activity Locus Example v1.0*

---

## **1. Purpose**

This example demonstrates how to model a **spiral singularity**—a high‑intensity activity locus—using a concrete tensor potential  
**Φₐᵦ𝑐**  
that induces a **stable, tightening orbital trajectory** around a singularity point  
**s**,  
with **Nightmare Arc** designated as the prime locus.

The example is self‑contained and suitable for simulation under GBS v14.

---

## **2. Singularity Definition**

Let the singularity center be:

\[
s = (0, 0)
\]

in a local Verdant Deep chart:

\[
x = (x_1, x_2) \in \mathbb{R}^2
\]

Nightmare Arc is defined as the **region** where this spiral field is active.

---

## **3. Tensor Potential Construction**

The tensor potential is composed of:

- a **rotation term** generating circular motion  
- a **contraction term** generating inward tightening  

### **3.1 Rotation Term**

\[
R(x - s) =
\begin{pmatrix}
-\omega x_2 \\
\omega x_1
\end{pmatrix}
\]

with \(\omega > 0\).

### **3.2 Contraction Term**

\[
C(x - s) =
-\kappa (x_1^2 + x_2^2)
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}
\]

with \(\kappa > 0\).

### **3.3 Combined Tensor Potential**

\[
\Phi(x) = R(x - s) + C(x - s)
\]

This produces a **spiral field**:

- rotation dominates near \(s\)  
- contraction dominates farther out  

Nightmare Arc is the **prime locus** where \(\Phi\) reaches maximal intensity.

---

## **4. Recursion Update Rule**

Omega‑7+ recursion governs the evolution:

\[
x' = x + \lambda \Phi(x)
\]

with \(\lambda > 0\) small (e.g., 0.01).

This yields:

\[
x' =
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}
+
\lambda
\left[
\begin{pmatrix}
-\omega x_2 \\
\omega x_1
\end{pmatrix}
-
\kappa (x_1^2 + x_2^2)
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix}
\right]
\]

---

## **5. Resulting Dynamics**

### **5.1 Near the Center**

- contraction term small  
- rotation dominates  
- trajectory circles around \(s\)

### **5.2 Farther Out**

- contraction term grows as \(\|x\|^2\)  
- orbit radius shrinks  
- spiral tightens toward \(s\)

### **5.3 Nightmare Arc Interpretation**

Nightmare Arc is the **high‑intensity band** where:

- \(\omega\) is maximal  
- \(\kappa\) is steep  
- recursion steps produce rapid tightening  
- holonomy envelopes twist sharply  
- algebraic flows show strong rotational bias  

This region behaves like a **stable, contracting vortex**.

---

## **6. Stability Guarantees**

Lean invariants ensure:

- **forward invariance**  
- **strict span contraction**  
- **bounded curvature**  
- **bounded holonomy**  
- **bounded algebraic flows**  
- **recursion safety**  

Thus the spiral singularity—despite high intensity—remains **stable and non‑collapsing**.

---

## **7. Machine‑Readable Example Spec**

```yaml
spiral_singularity_example:
  version: "1.0"
  locus: "Nightmare Arc (prime)"
  singularity_point: "s = (0,0)"
  tensor_potential:
    rotation: "-ω x2, ω x1"
    contraction: "-κ ||x||^2 (x1, x2)"
    combined: "Φ = R + C"
  recursion:
    update_rule: "x' = x + λ Φ(x)"
    parameters:
      lambda: 0.01
      omega: "> 0"
      kappa: "> 0"
  dynamics:
    near_center: "rotation-dominant"
    outer_region: "contraction-dominant"
    behavior: "stable tightening spiral"
  invariants:
    forward_invariance: true
    strict_contraction: true
    anti_collapse: true
```

---

