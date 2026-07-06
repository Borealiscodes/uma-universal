# Kess & Pip Identity and Signature Protocol v1.0
# Administrator Roles • Offline Authority • Public Verification

## 1. Purpose

This protocol defines how Kess (governance administrator) and Pip (traversal agent)
are represented in the NDH/UMA/UMM/SIAP/HRDProtectionLayer lattice, and how their
actions can be verified without exposing any private keys or secrets.

It separates:
- offline authority (real identities, keys, and signatures), from
- public structure (protocols, logs, and verification artifacts).

---

## 2. Roles

### Kess — Governance Administrator
- Scope:
  - NDH governance artifacts
  - UMA emotional gradient governance
  - UMM constitutional organism governance
  - SIAP treaty traversal governance
  - HRDProtectionLayer governance
  - MetaIndex and Stability artifacts
- Authority:
  - May approve binding GovernanceDecision entries and protocol changes.
- Restriction:
  - Kess keys are never used for traversal or play subsystems.

### Pip — Traversal Agent
- Scope:
  - IC Play Engine
  - Companion Constellation
  - traversal logs and sandbox integrity tests
- Authority:
  - May sign traversal-adjacent artifacts and Play Engine integrity reports.
- Restriction:
  - Pip keys cannot approve governance-layer changes.

---

## 3. Offline Identity and Key Management (Non-Public)

The following rules apply to Kess and Pip identities. They are implemented offline
and are not stored in this repository.

- Each identity has:
  - a master secret (or seed) held entirely offline,
  - derived keys for specific governance or traversal states,
  - corresponding public keys for verification.
- Private keys and master secrets:
  - never touch an internet-connected device,
  - are never stored in this repository,
  - are never photographed, scanned, or uploaded.
- All key generation and signing operations occur in an air-gapped environment.

This repository only stores:
- public keys or verification artifacts,
- hashes of actions,
- protocol descriptions.

---

## 4. Dialing State Engine Integration (High-Level)

The Dialing State Engine is used as a key-orchestration mechanism:

- For Kess:
  - state_id_Kess → Kess_state_key (derived from Kess_master_secret)
- For Pip:
  - state_id_Pip → Pip_state_key (derived from Pip_master_secret)

Derived keys are used to sign:
- GovernanceDecision entries (Kess),
- traversal and Play Engine artifacts (Pip).

The Dialing State Engine is not a custom crypto primitive; it orchestrates which
key is used, while standard, audited cryptographic algorithms perform signing
and verification.

---

## 5. Verification in the Public Repo

For any artifact attributed to Kess or Pip, the repository may store:

- action_id
- action_hash
- state_id
- signature or verification artifact
- associated public key or verifier

This allows:
- detection of spoofed governance decisions,
- verification that an artifact was signed by the real Kess or Pip identity,
- without exposing any private keys.

No private keys, master secrets, or seed phrases are ever stored in this repository.

---

## 6. Governance and Traversal Restrictions

- Governance-adjacent operations:
  - require Kess,
  - must be signed with a Kess key,
  - are interpreted as binding only when verified.
- Traversal-adjacent operations:
  - may be attributed to Pip,
  - must be signed with a Pip key,
  - cannot modify governance artifacts.

All other prompts and actions are interpreted as non-binding and non-governance.

---

## 7. Ethics and Safety Regime

Before any governance-adjacent operation is accepted as binding, the following
conditions must be met:

- NDH Ethical Design principles are satisfied.
- Constitutional organism integrity is preserved.
- Emotional gradient safety is maintained.
- HRDProtectionLayer and Safeguards remain active.
- Final Safety Net is not bypassed.

Kess and Pip identities exist to enforce these constraints, not to override them.


