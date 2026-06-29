## 1. Meta layer identity

**Meta layer:**  
The meta layer describes, maps, and verifies the architecture.  
It does not execute movement, routing, or state; it defines structure, relationships, and constraints.

---

## 2. Meta layer components

The meta layer consists of:

- **Meta Index of Meta Index Tool**  
- **Meta Index Stability Report**  
- **Meta Index Mapping Coherence Report**  
- **Meta Index Drift Report**  
- **MVS Pre‑Flight Checklist**  
- **MVS Protocol**  
- **MVS Completion Report** (when created)  
- **Meta Pinning Functions**  
- **Pinning Lifecycle Index**  
- **Pins directory** (`/UMM/Meta/Pins/`)  
- **Meta Layer Interaction Map** (this document)

Each component is descriptive and structural, not operative.

---

## 3. Interactions with subsystems

Meta layer → subsystems:

- **Thoroughfare** — meta describes movement identity and precedence, but does not define movement.  
- **Integration** — meta describes routing roles and boundaries, but does not route.  
- **Cosmology** — meta describes state roles and containment, but does not hold state.  
- **Warm Plane / Sparkle Plane** — meta describes containment and drift, but does not generate affective or symbolic content.

Subsystems → meta layer:

- subsystems may be **referenced** by meta documents  
- subsystems do **not** modify meta documents  
- subsystems do **not** read meta documents for execution logic

---

## 4. Interactions with MVS

Meta layer ↔ MVS:

- **MVS Pre‑Flight Checklist** uses meta indexes, drift, stability, and coherence reports to verify readiness.  
- **MVS Protocol** relies on meta‑layer guarantees (containment, identity, boundaries).  
- **MVS Completion Report** (when present) records system state for Manifest and future meta operations.

MVS does not:

- define new meta structures  
- modify meta documents  
- alter pins or pinning functions

---

## 5. Interactions with pins

Meta layer ↔ pins:

- **Meta Pinning Functions** defines what pins are and how they behave.  
- **Pinning Lifecycle Index** defines how pins are created, verified, activated, maintained, and retired.  
- **Pins** provide stable sequences and invariants for Manifest and MVS.

Pins:

- are read by meta documents, MVS, and Manifest  
- are never modified by subsystems  
- never contain operative logic

---

## 6. Interactions with Manifest

Meta layer ↔ Manifest:

- Manifest uses meta indexes, MVS reports, and pins as **reference objects**.  
- Manifest does not redefine meta‑layer rules.  
- Manifest describes the system to humans, based on meta‑layer structure and guarantees.

Meta layer provides:

- the structural map  
- the constraints  
- the invariants  
- the referential anchors

Manifest provides:

- the human‑facing description  
- the “how to read this system” guidance

---

## 7. Drift and safety in the meta layer

Meta layer drift occurs when:

- meta documents define movement, recursion, or planes  
- meta documents contain affective or symbolic grammar  
- pins are placed outside `/UMM/Meta/Pins/`  
- MVS or subsystems modify meta documents  
- Manifest logic bleeds into meta documents

Drift must be corrected by:

- restoring neutral, structural language  
- re‑anchoring documents with movement‑first and corridor‑precedence anchors  
- relocating misplaced files to their correct directories

---

Corridors define precedence; this subsystem follows movement and does not generate recursion.
