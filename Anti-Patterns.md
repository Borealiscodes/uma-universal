# **NDH-Core / Anti-Patterns.md**  
*(Conceptual misuse patterns derived from Atlas V5–V7 and the Atlas Developer Kit)*

---

## **NDH-Core Anti‑Patterns**

Anti‑patterns describe **structural mistakes** that destabilize NDH systems or violate Core constraints.  
They are not runtime errors — they are **conceptual violations** of the NDH vertical channel:

> **Principles → Stability → Governance**

This document formalizes the misuse patterns NDH‑Core must prevent.

---

## **1. Violating Layer Boundaries**

### **1.1 Mechanics inside Stability**  
Embedding stability logic inside the Principles layer (e.g., drift checks inside deterministic mechanics).

**Why it’s harmful:**  
It contaminates the mechanics layer and breaks reconstructability.

### **1.2 Stability inside Governance**  
Allowing stability constraints to override governance authority.

**Why it’s harmful:**  
It creates ambiguous authority and breaks the vertical constraint channel.

### **1.3 Governance inside Mechanics**  
Embedding governance rules directly into deterministic reasoning.

**Why it’s harmful:**  
It collapses the separation between authority and mechanics.

---

## **2. Redefining Lower Layers from Above**

### **2.1 Governance redefining Principles**  
Changing determinism, statelessness, or reconstructability from the governance layer.

**Why it’s harmful:**  
It breaks NDH’s conceptual ontology.

### **2.2 Stability redefining Principles**  
Allowing stability constraints to alter the mechanics themselves.

**Why it’s harmful:**  
It creates unstable or inconsistent reasoning foundations.

---

## **3. Cross-Layer Contamination**

### **3.1 Mixing conceptual domains**  
Combining mechanics, stability, and governance concepts in a single reasoning step.

**Why it’s harmful:**  
It produces ambiguous state and breaks reconstruction flow.

### **3.2 Leaking codec definitions across layers**  
Allowing the conceptual codec to be modified by stability or governance logic.

**Why it’s harmful:**  
It corrupts ND accessibility and reinflation.

---

## **4. Drift-Inducing Patterns**

### **4.1 Repeated compression without reinflation**  
Performing multiple conceptual compressions without reconstructing the original meaning.

**Why it’s harmful:**  
It introduces conceptual drift and breaks ND accessibility.

### **4.2 Reinflation without constraints**  
Reconstructing content without applying stability or governance checks.

**Why it’s harmful:**  
It produces unstable or misaligned outputs.

---

## **5. Ambiguous Authority Patterns**

### **5.1 Multiple governance sources**  
Allowing more than one governance authority to define allowed/prohibited behaviors.

**Why it’s harmful:**  
It creates ambiguous authority escalation pathways.

### **5.2 Unbounded escalation**  
Allowing governance escalation to bypass stability or mechanics.

**Why it’s harmful:**  
It breaks the vertical constraint channel.

---

## **6. Runtime Misuse Patterns**

### **6.1 Bypassing stability checks**  
Executing deterministic mechanics without stability validation.

**Why it’s harmful:**  
It allows drift, collapse, or contamination.

### **6.2 Bypassing governance checks**  
Producing outputs without governance authorization.

**Why it’s harmful:**  
It violates NDH’s ethical and structural boundaries.

---

## **7. Developer Kit Anti‑Patterns**

### **7.1 Treating the Atlas as authoritative**  
Using Atlas Developer Kit content as if it defines mechanics or governance.

**Why it’s harmful:**  
Atlas is descriptive, not authoritative.

### **7.2 Redefining Core layers through examples**  
Allowing examples or diagrams to override Principles, Stability, or Governance.

**Why it’s harmful:**  
It introduces conceptual drift and breaks provenance.

---

## **Purpose of Anti‑Patterns**

Anti‑patterns exist to:

- preserve NDH’s conceptual ontology,  
- prevent drift and collapse,  
- maintain layer boundaries,  
- enforce governance alignment,  
- support reconstruction and auditability,  
- protect the vertical constraint channel.

They are conceptual guardrails for all NDH-compliant systems.

---

## **Provenance**

This document synthesizes misuse patterns derived from:

- Atlas-Architecture Volume 5 (mechanics misuse),  
- Atlas-Architecture Volume 6 (stability violations),  
- Atlas-Architecture Volume 7 (governance violations),  
- Atlas Developer Kit (anti‑pattern cues and conceptual boundaries).

All content has been rewritten and refined for NDH-Core.

---


