# **NDH Governance Spine — Public‑Facing Overview**

The NDH Governance Spine is the framework that ensures the NDH system remains stable, consistent, and safe to evolve. It defines how changes are proposed, reviewed, approved, and integrated, and it protects core architectural components from accidental modification or drift.

This governance model is designed to be transparent, predictable, and easy for contributors to understand.

---

## **1. Governance Notice**  
The Governance Notice explains the purpose of NDH governance and outlines the rules that protect core system components. It describes:

- which files are considered governance‑critical  
- why they are protected  
- how changes must be submitted  
- who is responsible for approving modifications  

This notice acts as the top‑level contract for contributors.

---

## **2. Protected‑Systems Directory**  
NDH maintains a dedicated directory for governance‑critical files.  
These files define the system’s stability, architecture, and long‑term behavior.

To prevent accidental changes, this directory is protected by:

- branch protection rules  
- repository rulesets  
- CODEOWNERS  
- required pull requests  
- required status checks  

Only authorized maintainers may modify these files.

---

## **3. CODEOWNERS**  
The CODEOWNERS file identifies the individuals responsible for reviewing and approving changes to governance‑critical components.

This ensures:

- every change receives qualified review  
- architectural consistency is maintained  
- contributors know who to contact for guidance  

CODEOWNERS is a key part of NDH’s accountability model.

---

## **4. Drift Anchor Diagram**  
The Drift Anchor Diagram describes the stability principles that keep NDH from drifting into inconsistent or unintended states.

It outlines:

- the system’s fixed points  
- boundaries that must not be crossed  
- conditions that preserve architectural integrity  

This diagram helps contributors understand how NDH maintains coherence over time.

---

## **5. Handshake Protocol**  
The Handshake Protocol defines the required steps for proposing and merging changes:

1. Submit a pull request  
2. Participate in discussion  
3. Resolve all conversations  
4. Receive approval from CODEOWNERS  
5. Pass required checks  
6. Merge into the protected branch  

This ensures that every change is reviewed, discussed, and validated.

---

## **6. Deprecated Subsystems**  
NDH maintains a list of deprecated subsystems that are no longer part of the active architecture.

This prevents:

- accidental reintroduction of outdated components  
- confusion about system boundaries  
- regressions caused by legacy code  

The list provides clarity for contributors and maintainers.

---

## **7. Branch Protection & Rulesets**  
NDH uses GitHub’s protection features to enforce governance rules at the repository level.

These include:

- requiring pull requests  
- requiring status checks  
- requiring conversation resolution  
- blocking force pushes  
- restricting direct updates  
- restricting deletions  
- restricting branch creation  

These rules ensure that governance‑critical branches remain stable and protected.

---

# **Why This Matters**
The NDH Governance Spine ensures that:

- contributors understand how to participate  
- maintainers can protect core architecture  
- changes are reviewed and validated  
- the system remains stable as it evolves  
- accidental drift or regressions are prevented  

It provides a clear, predictable structure for collaboration.

---

