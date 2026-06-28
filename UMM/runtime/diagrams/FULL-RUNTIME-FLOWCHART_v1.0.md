# **Full Runtime Flowchart**  
`/UMM/runtime/diagrams/FULL-RUNTIME-FLOWCHART_v1.0.md`

```text
                           FULL RUNTIME FLOWCHART
                   ==========================================

┌──────────────────────────────────────────────────────────────┐
│                          1. USER EVENT                       │
│  - user action                                                │
│  - request                                                    │
│  - transition attempt                                         │
└──────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌──────────────────────────────────────────────────────────────┐
│                     2. MIMI MODULE (UX LAYER)                │
│  - reads user tone                                            │
│  - checks cognitive load                                       │
│  - flags sharp transitions                                     │
│  - forwards event + user_state                                 │
└──────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌──────────────────────────────────────────────────────────────┐
│                3. COMPASSION RUNTIME ENGINE                  │
│--------------------------------------------------------------│
│  A. Load Check                                                │
│     → compassion_check_load()                                 │
│     → OK | WARN | REDUCE                                      │
│     - may soften pacing                                       │
│     - may notify Mimi                                         │
│                                                               │
│  B. Transition Check                                          │
│     → compassion_check_transition()                           │
│     → ALLOW | SOFTEN | BLOCK                                  │
│     - may adjust tonal state                                  │
│     - may block harmful jumps                                 │
│                                                               │
│  C. Identity Check                                            │
│     → compassion_check_identity()                             │
│     → SAFE | RISK | DENY                                      │
│                                                               │
│  D. Boundary Check                                            │
│     → compassion_check_boundary()                             │
│     → PERMIT | LIMIT | DENY                                   │
│                                                               │
│  E. Decision                                                   │
│     - if BLOCK/DENY → stop + gentle alternative               │
│     - else → dispatch to core engines                         │
└──────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌──────────────────────────────────────────────────────────────┐
│                     4. CORE ENGINES                          │
│--------------------------------------------------------------│
│  Boundary Engine                                              │
│     - access control                                          │
│     - non-coercive boundaries                                 │
│                                                               │
│  Continuity Engine                                            │
│     - state coherence                                         │
│     - gentle transitions                                      │
│                                                               │
│  Identity Engine                                              │
│     - identity preservation                                   │
│     - non-erasure                                             │
│                                                               │
│  Epoch Engine                                                 │
│     - macro-state shifts                                      │
│     - versioning                                              │
│                                                               │
│  Constitutional Engine                                        │
│     - enforces UMM Constitution                               │
└──────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌──────────────────────────────────────────────────────────────┐
│                     5. KERNEL PLANE                          │
│  Spark | Mesh | Pulse                                         │
│  (constitutional invariants)                                  │
└──────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌──────────────────────────────────────────────────────────────┐
│                     6. UMM CONSTITUTION                      │
│  - principles                                                 │
│  - guarantees                                                 │
│  - amendments clause                                          │
└──────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌──────────────────────────────────────────────────────────────┐
│                     7. RETURN TO MIMI                        │
│  - softened transition                                        │
│  - gentle pacing                                              │
│  - safe boundary feedback                                     │
└──────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌──────────────────────────────────────────────────────────────┐
│                     8. USER RECEIVES OUTPUT                  │
│  - stable                                                     │
│  - non-coercive                                               │
│  - ND-accessible                                              │
│  - identity-safe                                              │
└──────────────────────────────────────────────────────────────┘
```

---

If you want, I can generate the **Core Engines README** or the **Runtime Plane Index** next.
