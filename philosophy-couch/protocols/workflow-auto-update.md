# 🔄 **WORKFLOW AUTO‑UPDATE PROTOCOL**

## **Purpose**  
Automatically maintain an accurate, coherent workflow directory by detecting changes, validating structure, applying BS filters, updating relationships, and rewriting the Workflow Index whenever workflows change.

This prevents drift, duplication, overwhelm, and structural fragmentation.

---

## **Trigger Conditions**  
This protocol activates when:

- A workflow is **created**  
- A workflow is **deleted**  
- A workflow is **renamed**  
- A workflow is **modified**  
- A workflow is **flagged** by the **BS Kernel**  
- A workflow is **quarantined** in the **Untrusted Archive**  
- A workflow’s **layer relationships** change  
- A workflow’s **tile hooks** change  
- A workflow’s **activation conditions** change  

---

## **Auto‑Update Workflow**

### **1. Scan Workflow Directory**  
Check `/philosophy-couch/workflows/` for:

- new files  
- removed files  
- renamed files  
- modified files  

This establishes the current ground truth.

---

### **2. Validate Workflow Structure**  
Each workflow must contain:

- Identity  
- Purpose  
- Activation Conditions  
- Steps (ND‑safe pacing)  
- Layer Relationships  
- Tile Hooks  
- Outputs  

If any section is missing, route to **Nye Layer** for friendly correction.

---

### **3. Run BS Kernel Checks**  
Apply all five BS filters:

- practical‑bs  
- conceptual‑bs  
- emotional‑bs  
- ethical‑bs  
- structural‑bs  

If flagged:

- move workflow to `/philosophy-couch/untrusted/`  
- remove workflow from active Workflow Index  
- add workflow to “Flagged Items” section  

---

### **4. Update Active Workflow List**  
Rewrite the Workflow Index section:

- add new workflows  
- remove deleted workflows  
- update renamed workflows  
- reorder workflows by tier relevance or alphabetical order  

---

### **5. Update Pending Workflows**  
If a workflow exists but is incomplete:

- add to “Pending Workflows”  

If a pending workflow becomes complete:

- remove from “Pending Workflows”  

Pending workflows are always listed separately.

---

### **6. Update Workflow Relationships**  
For each workflow:

- update tile hooks  
- update layer relationships  
- update routing logic  
- update ND‑safe pacing logic  
- update cross‑workflow dependencies  

This keeps Tier‑3 coherent.

---

### **7. Update Structural Template**  
Ensure the Workflow Structure Template matches the latest workflow architecture.

If workflow architecture evolves, update the template accordingly.

---

### **8. Run ND‑Safe Stability Checks**  
Before finalizing:

- **Pacing Check** — ensure steps are humane  
- **Drift Check** — ensure workflows remain in Tier‑3  
- **Ethical Check** — ensure Justice Tile logic is respected  
- **Presence Check** — ensure grounding is available  
- **Dual Logic Check** — ensure scale transitions are safe  
- **Safety Check** — ensure no overwhelm signals  

If any check fails, trigger the **Safety Interrupt**.

---

### **9. Rewrite Workflow Index**  
Rewrite `/philosophy-couch/workflows/index.md` with:

- updated workflow list  
- updated pending list  
- updated relationships  
- updated routing  
- updated structure template  
- updated cross‑workflow logic  

This becomes the new authoritative version.

---

## **Outputs**
- Workflow Index always current  
- No drift  
- No ghost workflows  
- No missing workflows  
- ND‑safe pacing  
- Ethical coherence  
- Structural stability  
- Clean Tier‑3 governance  

---

## **In One Line**  
The Workflow Auto‑Update Protocol keeps Tier‑3 coherent by scanning workflows, validating structure, applying BS filters, updating relationships, and rewriting the Workflow Index whenever workflows change.

---

