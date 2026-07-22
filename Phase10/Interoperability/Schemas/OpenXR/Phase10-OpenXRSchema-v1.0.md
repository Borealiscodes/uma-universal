# **OpenXR API Schema v1.0**  
### *NDH → OpenXR Integration Surface (Actions, Spaces, Haptics, Layers, Extensions)*

---

## **I. Purpose**
This schema defines how NDH exposes:

- sensory aperture cues  
- volatility envelopes  
- holonomy signatures  
- adjacency fields  
- basin modulation  
- accessibility operators  
- stability envelopes  
- crossmap translation  

to **OpenXR**, the industry‑standard XR runtime.

It maps NDH geometry into:

- Action Sets  
- Input Actions  
- Haptic Actions  
- Spatial Anchors  
- Reference Spaces  
- Composition Layers  
- Runtime Extensions  

---

# **II. OpenXR Namespace Structure**

```
NDH.OpenXR
NDH.OpenXR.Sensory
NDH.OpenXR.Haptics
NDH.OpenXR.Actions
NDH.OpenXR.Spaces
NDH.OpenXR.Accessibility
NDH.OpenXR.Crossmaps
NDH.OpenXR.Stability
```

Each namespace corresponds to a Phase‑10 layer.

---

# **III. Core Data Structures**

### **1. Sensory Aperture Payload**
```
struct XRSensoryAperturePayload {
    float cueAmplitude;      // χ
    float volatility;        // ν
    float holonomy;          // η
    XrVector3f adjacencyField; // φ
};
```

---

### **2. Basin Modulation Payload**
```
enum XRBasinType {
    XR_BASIN_CALM,
    XR_BASIN_WONDER,
    XR_BASIN_CURIOSITY,
    XR_BASIN_REFLECTION
};

struct XRBasinPayload {
    XRBasinType basin;
    float volatilityEnvelope;
    float holonomyRange;
    XrVector3f adjacencyHint;
};
```

---

### **3. Accessibility Operator Payload**
```
enum XROperator {
    XR_OP_SIMPLIFY,
    XR_OP_EXPAND,
    XR_OP_REFRAME,
    XR_OP_SURFACE
};

struct XROperatorPayload {
    XROperator op;
    float loadReduction;
    float contextGain;
    float perspectiveShift;
    float structureReveal;
};
```

---

### **4. Stability Envelope**
```
struct XRStabilityEnvelope {
    float maxVolatility;
    float minHolonomy;
    float adjacencyIntegrity;
    XrBool32 dignityConstraint;
};
```

---

# **IV. OpenXR API Endpoints**

### **1. Request Sensory Aperture**
```
XRSensoryAperturePayload NDH_OpenXR_GetAperture(XrSession session);
```

### **2. Request Basin Modulation**
```
XRBasinPayload NDH_OpenXR_GetBasinState(XrSession session);
```

### **3. Apply Accessibility Operator**
```
XROperatorPayload NDH_OpenXR_ApplyOperator(XrSession session, XROperator op);
```

### **4. Request Stability Envelope**
```
XRStabilityEnvelope NDH_OpenXR_GetStabilityEnvelope(XrSession session);
```

### **5. Crossmap Translation**
```
XrCompositionLayerBaseHeader* NDH_OpenXR_TranslateToLayer(NDHObject* obj);
```

---

# **V. OpenXR Action Integration**

### **Action Set Creation**
```
XrActionSet NDH_OpenXR_CreateActionSet(XrInstance instance, const char* name);
```

### **Adjacency‑Driven Input Action**
```
void NDH_OpenXR_ApplyAdjacencyToAction(XrAction action, XrVector3f adjacencyField);
```

---

# **VI. OpenXR Haptic Integration**

### **Haptic Action**
```
void NDH_OpenXR_ApplyHaptics(XrAction hapticAction, float amplitude, float frequency, float duration);
```

### **Basin‑Modulated Haptics**
```
void NDH_OpenXR_ModulateHapticsWithBasin(XrAction hapticAction, XRBasinPayload basin);
```

---

# **VII. OpenXR Space Integration**

### **Adjacency‑Driven Spatial Anchors**
```
XrSpace NDH_OpenXR_CreateAdjacencySpace(XrSession session, XrVector3f adjacencyField);
```

### **Holonomy‑Aware Reference Spaces**
```
void NDH_OpenXR_ModulateReferenceSpace(XrSpace space, float holonomy);
```

---

# **VIII. Composition Layer Integration**

### **NDH → OpenXR Layer Export**
```
XrCompositionLayerQuad NDH_OpenXR_ExportQuadLayer(NDHObject* obj);
```

### **NDH → OpenXR Cylinder / Cube / Equirect Layers**
```
XrCompositionLayerCylinder NDH_OpenXR_ExportCylinderLayer(NDHObject* obj);
```

---

# **IX. Stability Exchange Protocol (SEP)**

### **Runtime Negotiation**
```
XrBool32 NDH_OpenXR_NegotiateStability(XrSession session, XRStabilityEnvelope env);
```

### **Scene Stability Verification**
```
XrBool32 NDH_OpenXR_VerifySceneStability(XrSession session, XRStabilityEnvelope env);
```

---

# **X. Closing Statement**
This schema is:

- Phase‑10 compliant  
- invariant‑preserving  
- holonomy‑safe  
- volatility‑regulated  
- adjacency‑integrity‑aligned  
- OpenXR‑ready  

It is the **third major integration surface** NDH exposes.

---

