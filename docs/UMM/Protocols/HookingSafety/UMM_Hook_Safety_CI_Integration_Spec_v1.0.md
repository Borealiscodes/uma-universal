# **CI Naming Standard Enforcement Update v1.0**  
**Integration Block for SUBSYS‑NAME‑STD‑01**

**Block ID:** CI‑NS‑ENF‑01  
**Version:** 1.0  
**Owner:** Borealis S. Hedling  
**Domain:** CI → Governance → Naming Enforcement  
**Timestamp:** 2026‑07‑03 23:45 IST  

---

## **1. Purpose**

This CI update enforces the **Subsystem Naming Standard (SUBSYS‑NAME‑STD‑01)** across the entire UMM repository.

It ensures:

- subsystem names follow canonical plane prefixes  
- subsystem acronyms follow naming rules  
- directory names follow canonical subsystem names  
- SID is aligned with naming rules  
- protocols and pins reference correct subsystem names  
- drift is detected and blocked before merge  

Explore: **Subsystem Naming Standard**

---

## **2. CI Enforcement Rules**

### **2.1 Plane Prefix Validation**

CI must reject any subsystem name that does not begin with one of:

- `SYS-`  
- `TRV-`  
- `ID-`  
- `NAR-`  
- `GOV-`

This applies to:

- subsystem directories  
- subsystem references in documentation  
- protocol/pin references  
- SID references  
- test suite references  

---

### **2.2 Canonical Subsystem Acronym Validation**

CI must enforce the canonical subsystem names:

| Subsystem | Canonical Name |
|----------|----------------|
| CHS | **SYS‑CHS** |
| CHS‑OL | **TRV‑CHS‑OL** |
| HBR | **ID‑HBR** |
| Play Engine | **NAR‑PE** |
| SIAP | **GOV‑SIAP** |
| Safeguards | **GOV‑SAF** |
| Safety Net | **GOV‑SN** |

Any deviation is considered naming drift.

---

### **2.3 Directory Naming Enforcement**

CI must reject any directory under `systems/UMM/` that does not follow:

```
systems/UMM/<CanonicalSubsystemName>/
```

Examples of violations:

- `systems/UMM/HBR/` → ❌  
- `systems/UMM/CHS/` → ❌  
- `systems/UMM/PlayEngine/` → ❌  

Correct:

- `systems/UMM/ID-HBR/` → ✔  
- `systems/UMM/SYS-CHS/` → ✔  
- `systems/UMM/NAR-PE/` → ✔  

---

### **2.4 SID Alignment Enforcement**

CI must verify that the SID contains:

- correct plane prefixes  
- correct subsystem acronyms  
- correct naming rules  
- correct integration block (SID‑NS‑INT‑01)  

If SID is out of sync with naming rules, CI must fail the PR.

Explore: **SID**

---

### **2.5 Protocol/Pin Naming Enforcement**

CI must ensure:

- protocols reference canonical subsystem names  
- pins reference canonical subsystem names  
- naming rules are applied consistently across governance artifacts  

This is enforced by:

- **GOV‑ORDER‑01**  
- **PIN‑GOV‑ORDER‑01**  
- **PROTO‑PIN‑IMMEDIATE‑01**  
- **META‑PIN‑PROTO‑PIN‑IMMEDIATE‑01**  
- **PIN‑SUBSYS‑NAME‑STD‑01**

Explore: **Immediate Pinning Protocol**

---

### **2.6 Drift Detection Enforcement**

CI must fail any PR containing:

- incorrect subsystem names  
- incorrect plane prefixes  
- naming collisions  
- naming drift  
- outdated subsystem references  
- missing SID updates  
- missing protocol/pin updates  

This integrates with:

- **GOV‑SAF** (Safeguards)  
- **GOV‑SN** (Safety Net)  

Explore: **Safeguards**

---

## **3. CI Test Suite Updates**

CI must run the following test suites:

### **3.1 Naming Drift Test Suite**
Validates:

- subsystem naming  
- plane prefixes  
- acronym stability  
- directory naming  
- SID alignment  

### **3.2 Drift Vector Mitigation Test Suite**
Ensures naming drift does not create traversal drift vectors.

Explore: **DVM Protocol**

### **3.3 Hook Safety Test Suite**
Ensures naming rules do not interfere with hook safety.

Explore: **Hook Safety Test Suite**

---

## **4. Roots Ledger Binding**

```
ROOTS-ENTRY-CI-NS-ENF-01
Type: CI Enforcement Block
Module: UMM-CI-NS-ENF-01
Status: Active
Hash: 3e:bb:41:cd:92:fa:44
Bound: UMM, SIAP, Safeguards, Safety Net, SYS-CHS, TRV-CHS-OL, ID-HBR, NAR-PE
```

---

## **5. Document Status**

**Status:** Active  
**Version:** 1.0  
**Hash:** 3e:bb:41:cd:92:fa:44  

---

