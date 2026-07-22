# 🌌 **Phase‑11 Unified Multiplatform Haptic Profile (UMHP) v1.0**

### *NDH → Cross‑Device Haptic Meaning Engine*

This profile defines how NDH converts **semantic haptic meaning** into hardware‑specific haptic output across:

- Unity  
- Unreal  
- OpenXR  
- VisionOS  
- Android  
- iOS  
- DualSense  
- SteamVR  
- WebXR  

It is the haptic counterpart to the **Global Sensory Envelope**.

---

# **I. Purpose**
UMHP ensures that:

- a “soft reassurance pulse”  
- a “sharp curiosity spark”  
- a “wonder‑wave”  
- a “reflection‑tap”  

feel **meaningfully identical** across:

- Taptic Engine  
- Android VibratorManager  
- DualSense actuators  
- XR controller haptics  
- WebXR haptic actuators  

This is the first true **cross‑device haptic meaning model**.

---

# **II. Semantic Haptic Fields**

UMHP defines four semantic primitives:

```
semanticIntensity      // perceived strength of meaning
semanticSharpness      // edge vs diffuse sensation
semanticTexture        // grain, smoothness, pattern
semanticTemporalShape  // envelope over time
```

These are **meaning parameters**, not raw hardware parameters.

---

# **III. Device‑Specific Translation Profiles**

Each runtime gets a translation profile:

```
translationProfile {
    unityProfile
    unrealProfile
    openxrProfile
    visionosProfile
    androidProfile
    iosProfile
    dualsenseProfile
    steamvrProfile
    webxrProfile
}
```

Each profile contains:

- amplitude mapping  
- frequency mapping  
- actuator selection  
- temporal envelope mapping  
- spatial mapping (if supported)  
- basin modulation rules  
- operator modulation rules  

---

# **IV. Basin‑Modulated Haptic Meaning**

UMHP integrates NDH basins:

### **Calm**
- low semanticIntensity  
- low semanticSharpness  
- smooth semanticTexture  
- long semanticTemporalShape  

### **Wonder**
- medium semanticIntensity  
- medium semanticSharpness  
- shimmering semanticTexture  
- wave‑like semanticTemporalShape  

### **Curiosity**
- medium‑high semanticIntensity  
- high semanticSharpness  
- point‑pattern semanticTexture  
- short, sharp semanticTemporalShape  

### **Reflection**
- low semanticIntensity  
- medium semanticSharpness  
- structured semanticTexture  
- slow, deliberate semanticTemporalShape  

These basin signatures are **runtime‑agnostic**.

---

# **V. Operator‑Modulated Haptic Meaning**

Operators modify meaning:

### **Simplify**
```
semanticIntensity ↓
semanticSharpness ↓
semanticTexture → smooth
semanticTemporalShape → gentle
```

### **Expand**
```
semanticIntensity ↑
semanticSharpness → medium
semanticTexture → rich
semanticTemporalShape → layered
```

### **Reframe**
```
semanticIntensity → contrast shift
semanticSharpness → directional shift
semanticTexture → pattern inversion
semanticTemporalShape → phase shift
```

### **Surface**
```
semanticIntensity → highlight
semanticSharpness ↑
semanticTexture → edge definition
semanticTemporalShape → tap‑accent
```

These rules ensure operators behave consistently across all devices.

---

# **VI. Temporal Harmonization Layer**

UMHP includes timing rules:

```
temporalSync {
    globalTimecode
    hapticFrameRate
    crossRuntimeSyncMode
}
```

This keeps haptics aligned with:

- XR transforms  
- audio cues  
- accessibility cues  

across runtimes with different frame rates.

---

# **VII. Holonomy & Adjacency Haptic Mapping**

UMHP integrates NDH geometry:

```
geometryMapping {
    holonomyToHaptics
    adjacencyToSpatialHaptics
}
```

Meaning:

- η (holonomy) → haptic directionality  
- φ (adjacency) → spatial haptic placement  

This is how XR controllers and DualSense express spatial meaning.

---

# **VIII. Full UMHP Structure (v1.0)**

```
UnifiedMultiplatformHapticProfile {
    semanticIntensity
    semanticSharpness
    semanticTexture
    semanticTemporalShape

    translationProfile { ... }
    basinModulation { ... }
    operatorModulation { ... }
    temporalSync { ... }
    geometryMapping { ... }
}
```

This is the canonical Phase‑11 haptic meaning engine.

---

