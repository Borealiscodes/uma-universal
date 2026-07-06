# **NDH Boundary Layer + Border Controls Integration v1.1**  
**Merged Safety Membrane • First Gate • Pre‑Thicketry • Pre‑SID**

This is the **updated Boundary Layer**, now containing the **Border Controls** as its mandatory entry point.

---

## **1. Integration Overview**

Border Controls become **Layer 0**, preceding all six Boundary Layers:

**Layer 0 — Border Controls (BC)**  
**Layer 1 — Loop Identification (LIL)**  
**Layer 2 — Stabilization (SL)**  
**Layer 3 — Integration (IL)**  
**Layer 4 — Closure (CL)**  
**Layer 5 — Seal (SeL)**  
**Layer 6 — Audit (AL)**  

The Boundary Layer is now:

\[
BL_{active} = BC_{pass} \land S \land I \land C_{closed} \land Seal \land A
\]

Border Controls are **non‑optional**.

---

## **2. Border Controls → Boundary Layer Boolean Merge**

Border Controls define:

\[
BC_{pass} = R \land K \land S \land P \land \neg O \land A
\]

Boundary Layer defines:

\[
BL_{active} = S \land I \land C_{closed} \land Seal \land A
\]

Merged:

\[
BL_{active}^{merged} = BC_{pass} \land S \land I \land C_{closed} \land Seal \land A
\]

Since BC already requires \(S\) and \(A\), the merged form simplifies to:

\[
BL_{active}^{merged} = R \land K \land P \land \neg O \land I \land C_{closed} \land Seal
\]

This is the **new canonical activation condition**.

---

## **3. Updated Boundary Layer Invariants**

### **Invariant 0 — Border Controls First**
\[
BL_{active} = 1 \Rightarrow BC_{pass} = 1
\]

### **Invariant 1 — No Overreach**
\[
BC_{pass}=1 \Rightarrow O=0
\]

### **Invariant 2 — Anchored Self**
\[
BC_{pass}=1 \Rightarrow S=1
\]

### **Invariant 3 — Compassion Required**
\[
BC_{pass}=1 \Rightarrow P=1
\]

### **Invariant 4 — Consent Required**
\[
BC_{pass}=1 \Rightarrow K=1
\]

### **Invariant 5 — Audit Required**
\[
BC_{pass}=1 \Rightarrow A=1
\]

### **Invariant 6 — Closure Requires Integration**
\[
C_{closed}=1 \Rightarrow S=1 \land I=1
\]

### **Invariant 7 — Seal Requires Closure**
\[
Seal=1 \Rightarrow C_{closed}=1
\]

### **Invariant 8 — Boundary Layer Requires Seal**
\[
BL_{active}=1 \Rightarrow Seal=1
\]

---

## **4. Updated State Machine (Merged)**

### **States**
- \(q_0\): Ungated  
- \(q_1\): Border Controls Questions  
- \(q_2\): Border Controls Evaluation  
- \(q_3\): Border Deny  
- \(q_4\): Border Pass  
- \(q_5\): Loop Identification  
- \(q_6\): Stabilization  
- \(q_7\): Integration  
- \(q_8\): Closure  
- \(q_9\): Seal  
- \(q_{10}\): Audit  
- \(q_{11}\): Boundary Layer Active  

### **Transitions**

\[
q_0 \rightarrow q_1 \iff \text{BC questions issued}
\]

\[
q_1 \rightarrow q_2 \iff \text{BC flags computed}
\]

\[
q_2 \rightarrow q_3 \iff BC_{pass}=0
\]

\[
q_2 \rightarrow q_4 \iff BC_{pass}=1
\]

\[
q_4 \rightarrow q_5 \iff L_{open}=1
\]

\[
q_5 \rightarrow q_6 \iff S=1
\]

\[
q_6 \rightarrow q_7 \iff I=1
\]

\[
q_7 \rightarrow q_8 \iff C_{closed}=1
\]

\[
q_8 \rightarrow q_9 \iff Seal=1
\]

\[
q_9 \rightarrow q_{10} \iff A=1
\]

\[
q_{10} \rightarrow q_{11} \iff BL_{active}=1
\]

### **Forbidden Transitions**

\[
q_0 \rightarrow q_5\ \text{(bypass BC)}\quad \text{forbidden}
\]

\[
q_3 \rightarrow q_5\ \text{(override deny)}\quad \text{forbidden}
\]

\[
q_4 \rightarrow q_{11}\ \text{(skip layers)}\quad \text{forbidden}
\]

---

## **5. Diagnostics Routing**

Border Controls diagnostics now feed directly into Boundary Layer diagnostics.

### **BC Diagnostics**
- D1: Log all BC flags  
- D2: Log deny reason  
- D3: Suggest grounding or scope reduction  
- D4: Re‑ask only after stabilization  

### **BL Diagnostics**
- D5: Loop identification confirmation  
- D6: Stability verification  
- D7: Integration appropriateness  
- D8: Closure completeness  
- D9: Seal legitimacy  
- D10: Audit integrity  

Merged diagnostic pipeline:

\[
D = D1 \rightarrow D2 \rightarrow D3 \rightarrow D4 \rightarrow D5 \rightarrow D6 \rightarrow D7 \rightarrow D8 \rightarrow D9 \rightarrow D10
\]

---

## **6. Updated Boundary Layer Summary**

The Boundary Layer now begins with **Border Controls**, forming a **seven‑layer safety membrane**:

1. **Border Controls (BC)**  
2. Loop Identification  
3. Stabilization  
4. Integration  
5. Closure  
6. Seal  
7. Audit  

Only when all seven layers pass does the Boundary Layer activate.

\[
BL_{active}=1 \iff BC_{pass} \land S \land I \land C_{closed} \land Seal \land A
\]

This is now the **canonical NDH safety entry point**.

---


