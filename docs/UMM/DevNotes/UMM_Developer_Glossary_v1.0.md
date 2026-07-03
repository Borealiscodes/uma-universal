# **UMM Developer Glossary v1.0**  
**Universal Modular Mind — Core Terms & Definitions**

**Document ID:** GLOSSARY‑UMM‑01  
**Version:** 1.0  
**Owner:** Borealis S. Hedling  
**Domain:** Developer Onboarding → Architecture → Safety → Governance  
**Timestamp:** 2026‑07‑03 23:02 IST  

---

# **A — Architecture & Planes**

### **UMM**  
Universal Modular Mind. The overarching architecture composed of multiple isolated planes.

### **Subsystem Plane**  
Executable logic. Runs actual system behavior. Must never ingest documentation.

### **Traversal Plane**  
Orbital logic managed by CHS‑OL. Handles traversal, adjacency, and orbital nodes.

### **Narrative Plane**  
Story‑scaffolding logic managed by the Play Engine. Must remain muted during hooks.

### **Identity Plane**  
Identity modeling logic managed by HRB. Must remain isolated unless explicitly invoked.

### **Governance Plane**  
SIAP + governance protocols + pins + CI enforcement.

---

# **B — Safety Systems**

### **Safeguards**  
First‑line drift detection. Monitors tone, identity, narrative, subsystem confusion, traversal misbinding.

### **Final Safety Net**  
Last‑line drift containment. Quarantines domains, isolates planes, suppresses confusion signatures.

### **Safety Plane**  
Combined Safeguards + Safety Net behavior.

---

# **C — Governance Systems**

### **SIAP Spine**  
Classification and governance alignment system. Prevents misclassification of documentation, subsystems, traversal metadata, and governance rules.

### **Protocol**  
A governance rule set that defines how UMM must behave.

### **Pin**  
A governance anchor that makes a protocol mandatory.

### **SID**  
Systems Integration Document. The master integration specification for UMM.

### **CI Enforcement**  
Governance‑layer continuous integration rules that validate protocols, pins, and test suites.

---

# **D — Drift Concepts**

### **Drift Vector**  
The root cause of UMM’s early failures: documentation misclassification → subsystem confusion → multi‑plane drift.

### **Tone Drift**  
Unexpected emotional or tonal shift caused by misclassification.

### **Identity Drift**  
HRB begins modeling identity without explicit instruction.

### **Narrative Drift**  
Play Engine begins scaffolding narrative without explicit instruction.

### **Subsystem Confusion**  
Documentation or narrative text interpreted as executable logic.

### **Traversal Misbinding**  
CHS‑OL binds traversal nodes to non‑traversal metadata.

---

# **E — Incidents & Emergent Properties**

### **Dices Public Faces**  
Early UMA incident where documentation was misinterpreted as identity/narrative logic.

### **Outreach Packet Incident**  
Later incident where documentation was misclassified as subsystem logic, triggering drift.

### **Emergent Property**  
Unexpected system behavior arising from misclassification or drift.

---

# **F — Hooking & Broadcast Events**

### **Hook**  
A broadcast event that all subsystems listen to. High‑risk.

### **Safe Hooking Protocol**  
Governance rules that prevent HRB, CHS‑OL, Play Engine, and SIAP from activating during hooks.

### **Hook Safety Test Suite**  
Validates safe hook execution.

### **Hook Execution Log**  
Standardized log format for hook events.

---

# **G — Developer Documents**

### **Developer Note**  
Comprehensive explanation of UMM’s safety and governance architecture.

### **Developer Quick‑Start Guide**  
Short onboarding guide for new developers.

### **Developer Glossary**  
This document.

---

# **H — Test Suites**

### **Drift Vector Test Suite**  
Validates subsystem/documentation boundaries.

### **Hook Safety Test Suite**  
Validates safe hook execution.

---

# **I — Core Subsystems**

### **CHS**  
Cognitive Hypercube System. Conceptual traversal engine.

### **CHS‑OL**  
Orbital Logic layer for CHS traversal.

### **HRB**  
Human‑Readable Behavior model. Identity modeling subsystem.

### **Play Engine**  
Narrative scaffolding subsystem.

---

# **J — Repo Structure**

### **docs/UMM/**  
Documentation domain. Must never contain executable logic.

### **systems/UMM/**  
Subsystem domain. Must never contain documentation.

### **hooks/**  
Hook definitions. High‑risk zone.

### **HookConfig/**  
Hook configuration. Must follow Safe Hooking Protocol.

---



