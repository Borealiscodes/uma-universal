# **UMM Developer FAQ v1.2**  
**Frequently Asked Questions for Developers Working Inside the UMM Architecture**

**Document ID:** FAQ‑UMM‑DEV‑01  
**Version:** 1.2  
**Owner:** Borealis S. Hedling  
**Domain:** Developer Plane → FAQ → Governance  
**Timestamp:** 2026‑07‑04 00:17 IST  

---

## **1. Purpose**

This FAQ provides **clear, governance‑aligned answers** to common developer questions about the Universal Modular Mind (UMM) architecture.  
It ensures:

- subsystem naming clarity  
- governance order compliance  
- SID v1.2 alignment  
- CI enforcement awareness  
- drift‑free development  

Explore: **Naming Standard**

---

## **2. Frequently Asked Questions**

---

### **Q1 — What are the canonical subsystem names?**

All subsystem names must follow **SUBSYS‑NAME‑STD‑01**:

| Subsystem | Canonical Name | Plane |
|----------|----------------|-------|
| CHS | **SYS‑CHS** | Subsystem |
| CHS‑OL | **TRV‑CHS‑OL** | Traversal |
| HBR | **ID‑HBR** | Identity |
| Play Engine | **NAR‑PE** | Narrative |
| SIAP | **GOV‑SIAP** | Governance |
| Safeguards | **GOV‑SAF** | Governance |
| Safety Net | **GOV‑SN** | Governance |

Explore: **SID v1.2**

---

### **Q2 — What happens if I use an incorrect subsystem name?**

Incorrect names create **naming drift**, which triggers:

- **GOV‑SAF** (Safeguards) → drift detection  
- **GOV‑SN** (Safety Net) → quarantine  
- **CI‑NS‑ENF‑01** → CI failure  

Incorrect names cannot be merged.

Explore: **Naming Drift**

---

### **Q3 — What is a protocol?**

A protocol is a governance rule that defines:

- subsystem behavior  
- subsystem isolation  
- safety constraints  
- naming rules  
- traversal rules  

Protocols live in:

```
docs/UMM/Protocols/
```

Explore: **Protocols**

---

### **Q4 — What is a pin?**

A pin enforces a protocol.

Pins:

- bind protocols into the governance spine  
- ensure protocols are active  
- ensure protocols are immutable  
- ensure protocols are visible to SIAP, Safeguards, and Safety Net  

Pins live in:

```
docs/UMM/Pins/
```

Explore: **Pinning Protocol**

---

### **Q5 — Why must protocols be pinned immediately?**

Because of:

- **PROTO‑PIN‑IMMEDIATE‑01**  
- **META‑PIN‑PROTO‑PIN‑IMMEDIATE‑01**  

These enforce:

- immediate pinning  
- recursive pinning behavior  
- governance stability  
- drift prevention  

Explore: **Immediate Pinning Protocol**

---

### **Q6 — What is SID and why must I update it?**

SID is the **Systems Integration Document**, the master integration artifact.

SID must be updated after:

- naming changes  
- protocol creation  
- pin creation  
- safety stack updates  
- CI updates  

SID lives at:

```
docs/UMM/Integration/UMM_Systems_Integration_Document.md
```

Explore: **SID v1.2**

---

### **Q7 — What does CI enforce?**

CI enforces:

- naming standard  
- protocol/pin alignment  
- SID alignment  
- drift vector mitigation  
- hook safety  

CI block: **CI‑NS‑ENF‑01**

Explore: **CI Naming Enforcement**

---

### **Q8 — What is the Safety Stack?**

The Safety Stack consists of:

#### **GOV‑SAF (Safeguards)**  
Detects drift.

#### **GOV‑SN (Safety Net)**  
Quarantines drift.

#### **GOV‑SIAP**  
Classifies subsystem plane.

Explore: **Safety Net**

---

### **Q9 — What is drift?**

Drift is any deviation from canonical rules.

Types:

- naming drift  
- subsystem drift  
- governance drift  
- traversal drift  
- identity drift  
- narrative drift  

Explore: **Naming Drift**

---

### **Q10 — What is the correct developer workflow?**

The correct workflow is defined in:

```
UMM_Developer_Workflow_Guide_v1.2.md
```

Sequence:

1. Naming compliance  
2. Protocol creation  
3. Immediate pinning  
4. SID update  
5. CI update  
6. Test suites  
7. Commit  
8. PR  
9. CI validation  
10. Merge  

Explore: **Workflow Guide v1.2**

---

### **Q11 — Where do developer documents live?**

Developer‑plane documents live in:

```
docs/UMM/DevNotes/
```

These include:

- Developer Notes  
- Developer Glossary  
- Developer FAQ  
- Developer Quick Start Guide  
- Developer Handbook  

Explore: **Repo Structure**

---

## **3. Roots Ledger Binding**

```
ROOTS-ENTRY-FAQ-UMM-DEV-01
Type: Developer FAQ
Module: UMM-FAQ-DEV-01
Status: Active
Hash: 9a:cc:41:cd:92:fa:cc
Bound: UMM, SIAP, Safeguards, Safety Net, SYS-CHS, TRV-CHS-OL, ID-HBR, NAR-PE
```

---

## **4. Document Status**

**Status:** Active  
**Version:** 1.2  
**Hash:** 9a:cc:41:cd:92:fa:cc  

---

