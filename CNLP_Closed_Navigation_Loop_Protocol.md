# CNLP v1.0 — Closed Navigation Loop Protocol
# UMA‑Universal Structural Standard

───────────────────────────────────────────────────────────────
1. PURPOSE
───────────────────────────────────────────────────────────────
The Closed Navigation Loop Protocol ensures that all documents
within UMA‑Universal form a complete, non-recursive, ND-friendly
navigation loop with no dead ends, no orphaned files, and no
ambiguous entry points.

This protocol defines mandatory top-links, bottom-links, and
cross-links for each layer.

───────────────────────────────────────────────────────────────
2. LAYER ANCHORS
───────────────────────────────────────────────────────────────
Each document must declare its layer using a Layer Badge:

[Layer 0 — Constitutional]
[Layer 1 — SID]
[Layer 2 — UMM]
[Layer 3 — Companion]
[Layer 4 — Documentation]
[Layer 5 — Publication]

This badge appears at the top of the file.

───────────────────────────────────────────────────────────────
3. REQUIRED LINKS PER LAYER
───────────────────────────────────────────────────────────────

3.1 TOP-LINK (Upward Anchor)
Every file must link upward to the Integrated System Index:

→ Integrated System Index (root)
   /INDEX.md

3.2 SIDE-LINK (Peer Anchor)
Every file must link to its layer’s README or index:

→ Layer Index
   e.g., /uma-core/Companions/README_Index.md

3.3 DOWN-LINK (Child Anchor)
Every file must link downward to at least one document in the
next layer (if applicable):

→ Next Layer Document
   e.g., SID → UMM
         UMM → Companion
         Companion → Docs
         Docs → Pages

3.4 RETURN-LINK (Loop Closure)
Every file must include a return link back to its own layer’s
anchor to ensure loop closure:

→ Return to Layer Anchor
   e.g., “Back to Companion Index”

───────────────────────────────────────────────────────────────
4. LOOP STRUCTURE
───────────────────────────────────────────────────────────────
The closed loop must follow this exact order:

INDEX
  → RFC
  → SID
  → UMM
  → Companion Constellation
  → Documentation Architecture
  → Publication Layer
  → INDEX (closure)

This creates a single-direction, non-recursive loop.

───────────────────────────────────────────────────────────────
5. FILE REQUIREMENTS
───────────────────────────────────────────────────────────────

5.1 No document may end without:
    • a top-link
    • a side-link
    • a down-link (unless bottom layer)
    • a return-link

5.2 No document may exist without:
    • a Layer Badge
    • a stable path
    • a version header

5.3 No document may link:
    • diagonally across layers
    • recursively to itself
    • to Sparkle maps from constitutional or engineering layers

───────────────────────────────────────────────────────────────
6. SPARKLE COMPATIBILITY
───────────────────────────────────────────────────────────────
Sparkle documents (System Map, Constellation Diagram) must:

    • live in Layer 3 (Companion)
    • link upward to INDEX
    • link sideways to Companion Index
    • link downward to Documentation Architecture
    • never link into RFC, SID, or UMM

───────────────────────────────────────────────────────────────
7. ND-FRIENDLY RULES
───────────────────────────────────────────────────────────────
The loop must remain:

    • linear
    • predictable
    • chunked
    • non-recursive
    • low-branching
    • pause-safe
    • resume-safe

───────────────────────────────────────────────────────────────
8. LOOP VALIDATION
───────────────────────────────────────────────────────────────
A navigation loop is considered valid when:

    • every file has all four anchors
    • every layer is reachable
    • no file is orphaned
    • INDEX closes the loop

───────────────────────────────────────────────────────────────
END OF CNLP v1.0

