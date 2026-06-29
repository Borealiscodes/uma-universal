# Soft Spiral Lantern — Math Appendix
(Visual Atlas — Step 5)

## 1. Mathematical Overview

This appendix formalizes the geometry of the Soft Spiral Lantern using non‑recursive, low‑load models. All equations are chosen to preserve stability, avoid fractal triggers, and maintain meta‑layer compliance.

---

## 2. Spiral Curvature Model

The spiral core is modeled as a gentle logarithmic spiral:



\[
r(\theta) = a \cdot e^{b\theta}
\]



Where:
- \( r(\theta) \) — radial distance from center  
- \( \theta \) — angle parameter  
- \( a > 0 \) — base radius (controls initial size)  
- \( 0 < b \ll 1 \) — small growth factor (ensures gentle expansion)

Constraints:
- \( \theta \) is bounded within a finite interval \([\theta_{\min}, \theta_{\max}]\)  
- \( b \) remains small to avoid tight, high‑load spirals  
- No self‑similar layering; spiral is single‑pass only

---

## 3. Intensity Decay Model

A soft radial intensity gradient is defined from core to lantern boundary:



\[
I(r) = I_0 \cdot e^{-kr}
\]



Where:
- \( I(r) \) — intensity at radius \( r \)  
- \( I_0 \) — core intensity (maximum)  
- \( k > 0 \) — decay constant (controls softness of glow)

Constraints:
- \( I(r) \) monotonically decreases as \( r \) increases  
- No oscillatory terms (no sinusoidal modulation)  
- Gradient remains smooth and non‑spiky

---

## 4. Stability Window Derivative

Curvature and intensity must remain within a low‑load stability window:



\[
\left|\frac{d^2 r(\theta)}{d\theta^2}\right| \leq C_r
\quad\text{and}\quad
\left|\frac{d I(r)}{dr}\right| \leq C_I
\]



Where:
- \( C_r \), \( C_I \) — stability constants defining maximum allowed curvature and intensity change

Constraints:
- No rapid curvature changes  
- No steep intensity gradients  
- Parameters \( a, b, k, I_0 \) chosen to satisfy these bounds

---

## 5. Recursion Limit Behavior

Recursion is explicitly disallowed:

- No iterative refinement of \( r(\theta) \)  
- No self‑referential definitions of \( I(r) \)  
- No fractal subdivision of the lantern boundary  
- All functions are single‑layer, closed‑form expressions

Formally:



\[
\forall f \in \{r(\theta), I(r)\}, \quad f \text{ is non‑recursive.}
\]



---

## 6. Drift Wave Constraint

To ensure drift‑safe behavior, no dynamic waveforms are encoded in the geometry:

- No time‑dependent terms (e.g., \( t \))  
- No sinusoidal modulation of radius or intensity  
- No oscillatory boundary deformation

Drift‑safe condition:



\[
\frac{\partial f}{\partial t} = 0
\quad\text{for all geometric and intensity functions } f.
\]



---

## 7. Math Appendix Status

**MATH APPENDIX — CONFIRMED & LOCKED**  
The Soft Spiral Lantern’s geometry is:

- Logarithmic, gentle, and non‑recursive  
- Intensity‑graded with smooth decay  
- Curvature‑bounded within a stability window  
- Free of drift‑inducing oscillations  
- Fully meta‑layer compliant

