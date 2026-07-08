### Math provenance anchor table (UMM Recall Gatekeeping)

| **Anchor** | **Type** | **Formal Object / Expression** | **Role in System** |
|-----------|----------|---------------------------------|--------------------|
| **A1: Continuity Space** | Space | \(\mathcal{C} \subseteq \mathbb{R}^n\) | Represents user continuity (identity, narrative, emotional baseline). |
| **A2: Snapshot Space** | Set | \(\mathcal{S} = \{s_i \mid i \in I\}\) | All captured, ND‑filtered snapshots. |
| **A3: Dimensional Bands** | Finite set | \(D = \{7D,8D,9D,10D,11D,12D,13D,14D\}\) | Governance layers for routing and constraints. |
| **A4: Routing Function** | Function | \(R : \mathcal{S} \to D\) | Assigns each snapshot to a dimensional band. |
| **A5: Retrieval Function** | Function | \(F : \mathcal{S} \times D \to \mathcal{C}\) | Continuity‑safe retrieval into \(\mathcal{C}\). |
| **A6: Continuity Non‑Extraction** | Axiom | \(\text{Extract}(s,c) = 0\) | No snapshot increases continuity extractability. |
| **A7: ND‑Safety Gradients** | Constraint | \(\frac{\partial E}{\partial s} = 0,\ \frac{\partial U}{\partial s} = 0\) | No emotional or urgency gradients from snapshots. |
| **A8: Constitutional Operators** | Operators | \(\mathsf{Del},\ \mathsf{Route},\ \mathsf{Vis}\) | Deletion, routing, visibility under user sovereignty. |
| **A9: Operator Commutativity** | Axiom | \(\mathsf{Del} \circ F = F \circ \mathsf{Del}\), etc. | Ensures user control is preserved under system actions. |
| **A10: Hyperboundary Seal** | Constraint | \(\text{MutualInfo}(s_1,s_2) \leq \delta\) | Bounds cross‑context inference between snapshots. |
| **A11: Continuity Drift Bound** | Stability | \(\|F(s,d) - c\| \leq \epsilon\) | Retrieval cannot significantly alter continuity state. |
| **A12: Narrative Coherence** | Invariant | \(\text{Coherence}(c,F(s,13D)) \geq \kappa\) | Ensures 13D retrieval preserves narrative integrity. |
| **A13: Overlay Operator** | Operator | \(\Omega(s) = (F(s,R(s)), R(s))\) | Couples continuity output with dimensional band. |
| **A14: Global Stability** | Condition | \(\sum_{d \in D} \text{Violation}(d) = 0\) | No dimensional invariant may be violated system‑wide. |

