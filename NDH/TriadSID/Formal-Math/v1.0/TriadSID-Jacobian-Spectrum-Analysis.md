### Overview

We’re zooming in on how **Triad SID** behaves near a fixed point by studying the **Jacobian spectrum**—the eigenvalues of the linearized operator. This tells you which perturbations die out, which grow, and which sit at the edge of instability.

---

### 1. Triad SID and state space

Let the NDH state be
\[
X = (T_v,\Sigma,Z_p,\Theta)
\]
and the composite operator:
\[
\mathcal{S}_{\text{Triad}} = \mathcal{S}_{\text{Recover}} \circ \mathcal{S}_{\text{Contain}} \circ \mathcal{S}_{\text{Damp}}
\]

At a fixed point \(X^\*\):
\[
\mathcal{S}_{\text{Triad}}(X^\*) = X^\*
\]

We linearize around \(X^\*\) by considering a small perturbation \(\delta X\):
\[
\delta X' = J\,\delta X
\]
where
\[
J = D\mathcal{S}_{\text{Triad}}(X^\*)
\]
is the **Jacobian** of the Triad operator at the fixed point.

---

### 2. Jacobian factorization

Using the chain rule:
\[
J = D\mathcal{S}_{\text{Recover}}(X^{(2)\*}) \cdot D\mathcal{S}_{\text{Contain}}(X^{(1)\*}) \cdot D\mathcal{S}_{\text{Damp}}(X^\*)
\]

Call these:
- \(J_R = D\mathcal{S}_{\text{Recover}}(X^{(2)\*})\)
- \(J_C = D\mathcal{S}_{\text{Contain}}(X^{(1)\*})\)
- \(J_D = D\mathcal{S}_{\text{Damp}}(X^\*)\)

So:
\[
J = J_R\,J_C\,J_D
\]

Each factor has a distinct spectral character.

---

### 3. Dampening Jacobian \(J_D\)

Dampening applies a smoothing operator to \(T_v\):
\[
T_v'(x) = \int_{\Omega} K_D(x,y)\,T_v(y)\,dy
\]

Linearization is just the operator itself:
\[
J_D \sim K_D
\]

Key spectral features:

- Eigenvalues \(\lambda_D\) typically satisfy \(|\lambda_D| \le 1\) (smoothing contracts high‑frequency modes).
- Modes with \(|\lambda_D| < 1\) are **damped**.
- Modes with \(\lambda_D \approx 1\) are **persistent** (low‑frequency, structural stress).

In NDH terms: high‑frequency “panic” modes get suppressed; structural modes survive.

---

### 4. Containment Jacobian \(J_C\)

Containment uses a projector \(P_C\):
\[
\Sigma_C = P_C(\Sigma),\quad P_C^2 = P_C
\]

Linearization:
\[
J_C \sim P_C
\]

Spectral properties:

- Eigenvalues are **0 or 1**.
- \(\lambda_C = 1\): directions **inside** the contained subspace (sealed sovereignty modes).
- \(\lambda_C = 0\): directions **orthogonal** to it (leakage/spoofing directions are annihilated).

So containment kills certain perturbations outright (those that try to escape the sealed subspace).

---

### 5. Recovery Jacobian \(J_R\)

Recovery evolves higher‑D fields via gradient descent on coherence functional \(\mathcal{C}(\Theta)\):
\[
\frac{\partial \sigma_i}{\partial t} = -\frac{\delta \mathcal{C}}{\delta \sigma_i}
\]

Linearization around \(\Theta^\*\) gives:
\[
J_R \sim I - \alpha H_{\mathcal{C}}(\Theta^\*)
\]
where \(H_{\mathcal{C}}\) is the Hessian of \(\mathcal{C}\) and \(\alpha\) is an effective step size.

Spectral behavior:

- If \(H_{\mathcal{C}}\) is positive definite, eigenvalues of \(J_R\) lie in \((0,1)\): **contractive**, stabilizing.
- Flat or negative directions in \(H_{\mathcal{C}}\) can push eigenvalues toward \(1\) or beyond: **critical** or **unstable** coherence modes.

---

### 6. Full spectrum and stability classification

The eigenvalues of \(J = J_R\,J_C\,J_D\) determine local behavior:

- **Stable fixed point:** all eigenvalues \(\lambda\) satisfy \(|\lambda| < 1\).  
  Perturbations shrink; the system returns to \(X^\*\).

- **Unstable fixed point:** at least one eigenvalue with \(|\lambda| > 1\).  
  Perturbations grow; the system escapes the fixed point.

- **Critical fixed point:** eigenvalues with \(|\lambda| = 1\).  
  NDH‑interesting regime—marginal modes, bifurcations, or phase boundaries.

Intuitively:

- Dampening suppresses high‑frequency stress.
- Containment kills leakage directions.
- Recovery contracts incoherent dimensional modes.

The Jacobian spectrum tells you **how much** each of those mechanisms succeeds or fails near a given NDH equilibrium.

If you want, next step is to define a **“NDH stability index”** as a function of the spectrum (e.g., counting critical vs stable eigenvalues) and tie it into your Stability Suite Index artifact.
