# **NDH Trans‑Orbital Traversal Layer v1.1**  
### *Expanded ASCII Edition — Public Specification*

---

## **1 — Purpose**
The Trans‑Orbital Traversal Layer defines **how a user moves through NDH conceptual space** once inside the Safety Envelope.  
It governs:

- entry validation  
- orbit selection  
- depth modulation  
- pacing  
- guardian interventions  
- safe exits  

It is the movement layer complementing the Safety Envelope’s boundary layer.

---

## **2 — High‑Level Traversal Pipeline**

```text
User Intent
   |
   v
+---------------------------+
|  Entry Gate               |
|  - Safety Envelope check  |
|  - Intent classification  |
|  - Emotional load scan    |
+---------------------------+
   |
   v
+---------------------------+
|  Orbital Path Selector    |
|  - Shallow orbit          |
|  - Medium orbit           |
|  - Deep orbit             |
+---------------------------+
   |
   v
+---------------------------+
|  Depth & Pace Controller  |
|  - Step size              |
|  - Speed                  |
|  - Recursion limits       |
+---------------------------+
   |
   v
+---------------------------+
|  Guardian Interventions   |
|  - Warn                   |
|  - Redirect               |
|  - Soften                 |
+---------------------------+
   |
   v
+---------------------------+
|  Exit / Soft Landing      |
|  - Summary                |
|  - Next gentle step       |
+---------------------------+
```

---

## **3 — Orbital Model (Ring Structure)**

```text
                 +----------------------+
                 |      Deep Orbit      |
                 |  High detail,        |
                 |  guardian required   |
                 +----------O-----------+
                          /   \
                         /     \
        +---------------O-------O---------------+
        |           Medium Orbit                |
        |   Structured detail, controlled pace  |
        +----------------O----------------------+
                       /   \
                      /     \
        +------------O-------O------------+
        |          Shallow Orbit          |
        |   Overview, low stimulus        |
        +---------------------------------+
```

---

## **4 — Depth & Pace Controller (State Machine)**

```text
States:
  S = Shallow
  M = Medium
  D = Deep

Allowed Transitions:
  S -> M  (paced)
  M -> D  (guardian recommended)
  D -> M  (softening)
  M -> S  (summarizing)

Forbidden Transitions:
  S -> D  (no direct jump)
  D -> S  (no abrupt exit)

Pacing Rules:
  S: slow, gentle
  M: controlled, structured
  D: slow again, high detail
```

---

## **5 — Guardian Intervention Flow**

```text
Trigger Conditions:
  - user distress signal
  - unsafe recursion
  - rapid depth change
  - emotionally loaded topic

Flow:
+---------------------------+
|  Guardian (Snek)         |
+---------------------------+
           |
           v
+---------------------------+
|  Warn (soft)             |
|  - explain risk          |
+---------------------------+
           |
           v
+---------------------------+
|  Redirect (gentle)       |
|  - offer safer orbit     |
+---------------------------+
           |
           v
+---------------------------+
|  Soften                  |
|  - slow pace             |
|  - summarize             |
+---------------------------+
```

---

## **6 — Multi‑Orbit Traversal Example**

```text
User Intent: "Explain NDH, then go deep on traversal."

Traversal Path:

[Entry Gate]
   |
   v
[Shallow Orbit: NDH overview]
   |
   v
[Medium Orbit: NDH documentation layers]
   |
   v
[Depth & Pace Controller: allow deeper traversal]
   |
   v
[Deep Orbit: Trans-Orbital internals]
   |
   v
[Guardian: check for overload, soften if needed]
   |
   v
[Exit / Soft Landing: recap + next gentle step]
```

---

## **7 — Relationship to Safety Envelope**

```text
+---------------------------+
|  Safety Envelope          |
|  (Boundaries)             |
+---------------------------+
           |
           v
+---------------------------+
|  Trans-Orbital Layer      |
|  (Movement)               |
+---------------------------+
```

The Safety Envelope defines **where** traversal may occur.  
The Trans‑Orbital Layer defines **how** traversal occurs.

Together they form the NDH Traversal System.

---

