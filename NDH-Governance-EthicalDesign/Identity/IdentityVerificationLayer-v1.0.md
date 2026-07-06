### Identity Verification Layer v1.0  
**Kess & Pip • State Epochs • Signature Blocks • Repo Verification**

---

## 1. Purpose

This document defines how identity verification works in the NDH/UMA/UMM/SIAP/HRDProtectionLayer lattice for:

- **Kess** (Governance Administrator)  
- **Pip** (Traversal Agent)

It specifies:

- how public keys appear in the repo,  
- how signatures are attached to artifacts,  
- how `state_id` (Dialing State Engine epochs) are recorded,  
- how contributors verify authenticity,  
- how governance decisions become binding,  
- how traversal artifacts remain non‑governance.

No private keys, seeds, or master secrets are described or stored here.

---

## 2. Identity Objects

### 2.1 Kess Identity Object

**Label:** `Kess`  
**Type:** Governance Administrator Identity  
**Fields (repo‑visible):**

- **kess_identity_id:** canonical identifier (e.g., `KESS-ADMIN-1`)  
- **kess_public_key:** public key or verifier artifact  
- **kess_key_scheme:** description of the signature scheme (e.g., “standard audited signature algorithm”)  
- **kess_state_ids:** list of known governance epochs (e.g., `KESS-STATE-001`, `KESS-STATE-002`)  

No private key material is stored in the repo.

### 2.2 Pip Identity Object

**Label:** `Pip`  
**Type:** Traversal Agent Identity  
**Fields (repo‑visible):**

- **pip_identity_id:** canonical identifier (e.g., `PIP-TRAVERSAL-1`)  
- **pip_public_key:** public key or verifier artifact  
- **pip_key_scheme:** description of the signature scheme  
- **pip_state_ids:** list of known traversal epochs (e.g., `PIP-STATE-001`, `PIP-STATE-002`)  

No private key material is stored in the repo.

---

## 3. Dialing State Engine Epochs

The Dialing State Engine selects **which derived key** is used for a given action via `state_id`.

### 3.1 Governance Epochs (Kess)

- **state_id_Kess:**  
  - Format: `KESS-STATE-XXX`  
  - Meaning: governance epoch (e.g., “PreflightAudit epoch”, “SID readiness epoch”)  
  - Each `state_id_Kess` corresponds to a **derived Kess key** held offline.

### 3.2 Traversal Epochs (Pip)

- **state_id_Pip:**  
  - Format: `PIP-STATE-XXX`  
  - Meaning: traversal epoch (e.g., “PlayEngine FunMode epoch”, “StandardMode tandem epoch”)  
  - Each `state_id_Pip` corresponds to a **derived Pip key** held offline.

The Dialing State Engine:

- **does not** generate keys,  
- **does not** perform cryptography,  
- **only** selects which epoch/key is used.

---

## 4. Signature Blocks (Repo Format)

For any artifact attributed to Kess or Pip, the repo may include a **Signature Block**.

### 4.1 Kess Signature Block (GovernanceDecision)

Example structure:

```text
[SignatureBlock-Kess]

action_id: GOVDEC-2026-07-06-001
action_hash: <hash-of-artifact-content>
identity_id: KESS-ADMIN-1
state_id: KESS-STATE-001
signature: <signature-by-Kess-state-key>
public_key_ref: KESS-PUBKEY-1
scheme: <audited-signature-scheme-name>
timestamp: 2026-07-06T21:13:00Z
binding: true
```

**Rules:**

- `binding: true` only when:
  - signature verifies against `public_key_ref`,  
  - `identity_id` is Kess,  
  - `state_id` is a valid governance epoch,  
  - ethics and safety regime conditions are met.

### 4.2 Pip Signature Block (Traversal Artifact)

Example structure:

```text
[SignatureBlock-Pip]

action_id: TRAV-2026-07-06-ICPLAY-001
action_hash: <hash-of-artifact-content>
identity_id: PIP-TRAVERSAL-1
state_id: PIP-STATE-001
signature: <signature-by-Pip-state-key>
public_key_ref: PIP-PUBKEY-1
scheme: <audited-signature-scheme-name>
timestamp: 2026-07-06T21:30:00Z
binding: false
```

**Rules:**

- `binding: false` for governance.  
- Pip signatures **cannot** make governance decisions binding.  
- Pip signatures attest traversal integrity only.

---

## 5. Verification Procedure (Repo‑Visible)

For any artifact with a Signature Block:

1. **Compute `action_hash`** from the artifact content.  
2. **Compare** with stored `action_hash` in the Signature Block.  
3. **Retrieve `public_key_ref`** and associated public key.  
4. **Verify `signature`** using the specified `scheme`.  
5. **Check `identity_id` and `state_id`:**
   - If `identity_id = KESS-ADMIN-1` and `binding = true` → governance decision may be treated as binding.  
   - If `identity_id = PIP-TRAVERSAL-1` → traversal artifact only, non‑governance.  
6. **Confirm ethics & safety regime conditions** (Section 7 below) before treating any governance decision as binding.

No private keys are ever used or stored in the repo during verification.

---

## 6. Governance vs Traversal Binding Rules

- **Governance‑adjacent operations:**
  - require a valid Kess Signature Block,  
  - must verify successfully,  
  - must have `binding: true`,  
  - must satisfy ethics & safety regime conditions.

- **Traversal‑adjacent operations:**
  - may have a Pip Signature Block,  
  - are always `binding: false` for governance,  
  - cannot modify governance artifacts.

- **All other prompts and artifacts:**
  - are interpreted as **non‑binding** and **non‑governance**,  
  - even if they mention Kess or Pip by name.

---

## 7. Ethics and Safety Regime (Precondition for Binding)

Before any governance decision is accepted as binding, the following must be true:

- NDH Ethical Design principles are satisfied.  
- Constitutional organism integrity is preserved.  
- Emotional gradient safety is maintained.  
- HRDProtectionLayer is active.  
- Safeguards are active.  
- Final Safety Net is not bypassed.

Kess and Pip identities exist to **enforce** these constraints, not to override them.

---

## 8. Non‑Storage of Secrets

This layer explicitly confirms:

- No private keys, master secrets, or seed phrases are stored in this repository.  
- All key generation, derivation, and signing operations occur offline.  
- The repo only stores:
  - public keys or verification artifacts,  
  - hashes of actions,  
  - Signature Blocks,  
  - protocol descriptions.

This completes the **public identification and verification layer** without exposing any sensitive material.
