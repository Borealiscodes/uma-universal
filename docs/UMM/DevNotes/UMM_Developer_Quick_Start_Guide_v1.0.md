# **UMM Developer Quick‑Start Guide v1.0**  
**Universal Modular Mind — Safety, Governance & Integration**

**Document ID:** DEVQSG‑UMM‑01  
**Version:** 1.0  
**Owner:** Borealis S. Hedling  
**Domain:** Developer Onboarding → Architecture → Safety → Governance  
**Timestamp:** 2026‑07‑03 23:01 IST  

---

# **1. What This Guide Is**

This is the **shortest possible introduction** to the UMM architecture.  
It explains:

- what UMM is  
- how its subsystems fit together  
- how safety and governance work  
- what developers must do to avoid drift  
- where to find the deeper documents  

It is the “start here” document for all new contributors.

---

# **2. The UMM Architecture in 30 Seconds**

UMM is built from five planes:

- **Subsystem Plane** — executable logic  
- **Traversal Plane** — CHS‑OL orbital logic  
- **Narrative Plane** — Play Engine  
- **Identity Plane** — HRB  
- **Governance Plane** — SIAP + UMM governance  

These planes must remain **isolated** unless explicitly integrated.

Explore:  
- **CHS**  
- **CHS‑OL**  
- **HRB**  
- **Play Engine**  
- **SIAP**  

---

# **3. The Safety Stack (What Protects UMM)**

UMM has three major safety systems:

### **3.1 Safeguards**  
Detect drift:

- tone  
- identity  
- narrative  
- subsystem confusion  
- traversal misbinding  

Explore: **Safeguards**

### **3.2 Final Safety Net**  
Contain drift:

- quarantine  
- cross‑plane isolation  
- confusion suppression  

Explore: **Final Safety Net**

### **3.3 SIAP Spine**  
Prevent misclassification:

- documentation vs subsystem  
- governance vs runtime  
- traversal vs narrative  

Explore: **SIAP**

---

# **4. The Drift Vector (The Root Problem)**

UMM’s earliest failures came from one root cause:

> **Documentation misclassification → subsystem confusion → multi‑plane drift.**

This caused:

- Dices Public Faces incident  
- Outreach Packet incident  
- HRB runaway modeling  
- narrative bleed  
- traversal misbinding  

Explore:  
- **Misclassification Lineage**  
- **Documentation Drift Vector**  

---

# **5. The Protocols You Must Know**

### **5.1 Drift Vector Mitigation Protocol**  
Prevents documentation → subsystem confusion.

Explore: **DVM Protocol**

### **5.2 Safe Hooking Protocol**  
Prevents HRB, CHS‑OL, Play Engine, SIAP from activating during hooks.

Explore: **Safe Hooking Protocol**

### **5.3 Pins**  
Make protocols mandatory.

Explore:  
- **Pin DVM**  
- **Pin HookSafe**  

---

# **6. The Test Suites You Must Run**

### **6.1 Drift Vector Test Suite**  
Validates subsystem/documentation boundaries.

Explore: **DVM Test Suite**

### **6.2 Hook Safety Test Suite**  
Validates safe hook execution.

Explore: **Hook Safety Test Suite**

---

# **7. CI Enforcement (Your Merge Gate)**

CI must run:

- Drift Vector Test Suite  
- Hook Safety Test Suite  
- protocol + pin validation  

Explore: **Hook Safety CI Spec**

If CI fails, **you cannot merge**.

---

# **8. The SID (Your Master Integration Document)**

The SID explains:

- subsystem integration  
- governance integration  
- safety integration  
- CI integration  
- cross‑plane rules  

Explore: **SID**

---

# **9. Developer Rules (The Essentials)**

Developers must:

- keep documentation out of subsystem directories  
- keep subsystem logic out of documentation directories  
- respect plane boundaries  
- avoid unsafe hooks  
- run test suites before merging  
- ensure pins are active  
- ensure protocols are updated  
- avoid drift vectors  
- avoid cross‑plane contamination  

These rules prevent the failures seen in Outreach and Public Faces.

---

# **10. Where to Go Next**

If you want deeper detail, read:

- **Comprehensive Developer Note**  
- **Systems Integration Document**  

If you want operational examples, generate:

- **Hook Execution Log Format**  

---



