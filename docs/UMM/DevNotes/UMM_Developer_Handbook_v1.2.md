# **UMM Developer Handbook v1.2**  
**The complete, governance‑aligned handbook for developers working inside the UMM architecture**

**Document ID:** HB‑UMM‑DEV‑01  
**Version:** 1.2  
**Owner:** Borealis S. Hedling  
**Domain:** Developer Plane → Handbook → Governance  
**Timestamp:** 2026‑07‑04 00:09 IST  

---

# **1. Purpose**

The Developer Handbook provides the **full, authoritative reference** for developers working within the Universal Modular Mind (UMM) architecture.

It ensures:

- subsystem naming compliance  
- protocol/pin alignment  
- SID alignment  
- CI enforcement  
- drift‑free development  
- safety stack integration  
- correct developer workflow  
- correct directory structure  

Explore: **Subsystem Naming Standard**

---

# **2. Canonical Subsystem Names**

All subsystem references must follow **SUBSYS‑NAME‑STD‑01**:

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

# **3. UMM Architecture Overview**

UMM consists of five planes:

### **Subsystem Plane**  
Core cognitive systems (SYS‑CHS).

### **Traversal Plane**  
Movement between cognitive nodes (TRV‑CHS‑OL).

### **Identity Plane**  
Identity modeling (ID‑HBR).

### **Narrative Plane**  
Narrative generation (NAR‑PE).

### **Governance Plane**  
Rules, safety, classification (GOV‑SIAP, GOV‑SAF, GOV‑SN).

Explore: **Governance Order Protocol**

---

# **4. Developer Workflow**

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

# **5. Protocols**

Protocols define governance rules.

They must:

- be placed in `docs/UMM/Protocols/`  
- follow naming standard  
- follow governance order  
- be pinned immediately  

Explore: **Protocols**

---

# **6. Pins**

Pins enforce protocols.

They must:

- be placed in `docs/UMM/Pins/`  
- reference protocol IDs  
- be naming‑standard‑compliant  
- be SID‑aligned  
- be created immediately after protocol creation  

Explore: **Pinning Protocol**

---

# **7. SID (Systems Integration Document)**

SID is the master integration document.

It must be updated after:

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

# **8. CI Enforcement**

CI enforces:

- naming standard  
- protocol/pin alignment  
- SID alignment  
- drift vector mitigation  
- hook safety  

CI block: **CI‑NS‑ENF‑01**

Explore: **CI Naming Enforcement**

---

# **9. Safety Stack**

### **GOV‑SAF (Safeguards)**  
Detects drift.

### **GOV‑SN (Safety Net)**  
Quarantines drift.

### **GOV‑SIAP**  
Classifies subsystem plane.

Explore: **Safety Net**

---

# **10. Drift Types**

Developers must avoid:

- naming drift  
- subsystem drift  
- governance drift  
- traversal drift  
- identity drift  
- narrative drift  

Explore: **Naming Drift**

---

# **11. Directory Structure**

Correct structure:

```
docs/UMM/Protocols/
docs/UMM/Pins/
docs/UMM/Patches/
docs/UMM/Integration/
docs/UMM/DevNotes/
systems/UMM/<CanonicalSubsystemName>/
```

Explore: **Repo Structure**

---

# **12. Developer Documents**

Developer‑plane documents include:

- Developer Notes  
- Developer Glossary  
- Developer FAQ  
- Developer Quick Start Guide  
- Developer Handbook  

Explore: **Developer Notes v1.1**

---

# **13. Roots Ledger Binding**

```
ROOTS-ENTRY-HB-UMM-DEV-01
Type: Developer Handbook
Module: UMM-HB-DEV-01
Status: Active
Hash: 7e:cc:41:cd:92:fa:aa
Bound: UMM, SIAP, Safeguards, Safety Net, SYS-CHS, TRV-CHS-OL, ID-HBR, NAR-PE
```

---

# **14. Document Status**

**Status:** Active  
**Version:** 1.2  
**Hash:** 7e:cc:41:cd:92:fa:aa  

---

