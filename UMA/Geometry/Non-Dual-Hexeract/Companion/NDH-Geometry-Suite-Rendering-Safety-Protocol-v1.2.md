# **NDH Geometry Suite — Rendering Safety Protocol v1.2**  
### *Cross‑Platform Rendering Stability Rules for NDH Geometry (SVG/PNG) in Desktop, Mobile, and Fallback Contexts*  
### *Anchored to:* NDH‑Integration‑Spec‑v1.0  
### *Anchor‑Pin:* **NDH‑PEP‑RS‑v1.0**  
### *Pin‑Class:* Rendering‑Safety (RS)  
### *Registry:* NDH‑Pin‑Registry‑v1.2

```text
<metadata>
version: v1.2
rendering: governed
pin-anchor: NDH-PEP-RS-v1.0
fallback-mode: png
svg-primary: true
mobile-safe: true
geometry-safe-mode: true
auto-index-compatible: true
registry-version: NDH-Pin-Registry-v1.2
</metadata>
```

---

## ⭐ 0. Purpose

Rendering Safety Protocol v1.2 defines the **rules, constraints, and guarantees** that ensure NDH geometry renders safely and consistently across:

- desktop browsers  
- mobile browsers  
- GitHub mobile sandbox  
- SVG primary rendering  
- PNG fallback rendering  
- geometry‑safe mode  

It prevents:

- blank SVGs on mobile  
- broken overlays  
- invisible traversal paths  
- missing pin anchors  
- singularity markers failing to render  
- integration coordinates disappearing  

It is anchored by **NDH‑PEP‑RS‑v1.0**, making rendering behavior a **governed NDH invariant**.

---

## ⭐ 1. Rendering Contexts

NDH geometry must support four rendering contexts:

### **1.1 Desktop (Primary)**
- SVG primary  
- PNG fallback  
- full overlays  
- full metadata  

### **1.2 Mobile (Primary Fallback)**
- PNG primary  
- SVG secondary  
- simplified overlays  
- geometry‑safe mode  

### **1.3 GitHub Mobile Sandbox**
- PNG only  
- high‑contrast mode  
- simplified traversal paths  

### **1.4 Failure Mode**
If SVG fails:

- PNG must render  
- overlays must remain visible  
- pin anchors must remain visible  
- singularity markers must remain visible  

This behavior is enforced by **PEP‑RS**.

---

## ⭐ 2. Rendering Safety Rules (v1.2)

### **Rule 1 — Every geometry artifact must have both SVG and PNG**
This prevents rendering gaps.

### **Rule 2 — SVG must contain full overlays**
Including:

- traversal paths  
- pin anchors  
- singularity thresholds  
- integration coordinates  

### **Rule 3 — PNG must contain simplified overlays**
To ensure visibility on mobile.

### **Rule 4 — PNG must be high‑contrast**
To ensure visibility in GitHub mobile sandbox.

### **Rule 5 — All geometry must include rendering metadata**
SVG `<metadata>`  
PNG EXIF  

### **Rule 6 — Geometry must degrade gracefully**
If SVG fails:

- PNG must render  
- overlays must remain visible  
- no geometry may disappear  

### **Rule 7 — Geometry must be dimension‑safe**
Identity → Behavior → Continuity → Cosmology → Narrative → Teleology → Hexeract

### **Rule 8 — Geometry must be traversal‑safe**
All overlays must follow:

- **Traversal Protocol v1.1**  
- operator sequence  
- recursion convergence  

### **Rule 9 — Geometry must be pin‑safe**
All anchors must follow:

- **Pin Registry v1.2**  
- PEP‑RS, PEP‑TC, PEP‑IC, PEP‑SC  
- pin class markers  

### **Rule 10 — Geometry must be singularity‑safe**
Cosmology, Teleology, and Hexeract must include:

- stellar singularity markers  
- supermassive singularity markers  
- CHS projection boundaries  

---

## ⭐ 3. SVG Rendering Requirements

SVG files must include:

### **3.1 Full Overlays**
- traversal  
- pins  
- singularity  
- integration  

### **3.2 Metadata Block**
Inside `<metadata>`:

```
version: v1.2
rendering: svg-primary
fallback: png
mobile-safe: true
pin-anchor: NDH-PEP-RS-v1.0
```

### **3.3 Layer Ordering**
1. base geometry  
2. traversal paths  
3. pin anchors  
4. singularity thresholds  
5. integration coordinates  
6. metadata  

### **3.4 Failure‑Mode Guarantee**
If any overlay fails:

- SVG must still render base geometry  
- PNG must remain available  

---

## ⭐ 4. PNG Rendering Requirements

PNG files must include:

### **4.1 High‑Contrast Mode**
Required for mobile.

### **4.2 Simplified Overlays**
- thicker traversal lines  
- thicker pin anchors  
- simplified singularity markers  
- simplified integration nodes  

### **4.3 Metadata Block (EXIF)**

```
version: v1.2
rendering: png-primary
svg-secondary: true
mobile-safe: true
pin-anchor: NDH-PEP-RS-v1.0
```

### **4.4 Geometry‑Safe Mode**
PNG must remain readable even if:

- screen brightness is low  
- GitHub mobile strips color layers  
- overlays are compressed  

---

## ⭐ 5. Rendering Failure Protocol

If SVG fails to render:

### **Step 1 — Switch to PNG**
PNG must be present and visible.

### **Step 2 — Preserve overlays**
Traversal, pins, singularity, and integration must remain visible.

### **Step 3 — Maintain dimensional fidelity**
No axis may lose visibility.

### **Step 4 — Maintain NDH coherence**
No geometry may break NDH operator sequence.

---

## ⭐ 6. Rendering Validation Checklist

Before geometry is accepted:

- SVG renders on desktop  
- PNG renders on mobile  
- overlays visible in both  
- metadata present in both  
- pin anchors visible  
- singularity markers visible  
- integration coordinates visible  
- traversal paths visible  
- auto‑index generator validates geometry  

---

## ⭐ 7. Versioning

```
Version: v1.2
Status: Active
Class: NDH / Geometry / Rendering Safety
Anchor-Pin: NDH-PEP-RS-v1.0
Registry: NDH-Pin-Registry-v1.2
Anchor: NDH-Integration-Spec-v1.0
```

---

## ⭐ 8. Synthesis

> **Rendering Safety Protocol v1.2 ensures NDH geometry is stable, visible, and coherent across desktop, mobile, SVG, PNG, fallback, and failure contexts.  
It is now fully anchored to NDH‑PEP‑RS‑v1.0, completing the rendering governance spine.**

---

