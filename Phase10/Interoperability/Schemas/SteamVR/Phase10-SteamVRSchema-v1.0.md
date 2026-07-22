# **SteamVR Schema v1.0**  
### *NDH → SteamVR Integration Surface (OpenVR, Lighthouse Tracking, Controller Models, Haptics, Spatial IO)*

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

to **SteamVR**, using:

- OpenVR API  
- Lighthouse tracking  
- Controller models (Index, Vive, Knuckles)  
- SteamVR Input  
- SteamVR Haptics  
- SteamVR Action Manifest  
- Spatial overlays  

This is the **eighth major Phase‑10 integration surface**.

---

# **II. SteamVR Namespace Structure**

```
NDH.SteamVR
NDH.SteamVR.Sensory
NDH.SteamVR.Haptics
NDH.SteamVR.Actions
NDH.SteamVR.Spatial
NDH.SteamVR.Accessibility
NDH.SteamVR.Crossmaps
NDH.SteamVR.Stability
```

Each namespace corresponds to a Phase‑10 layer.

---

# **III. Core Data Structures**

### **1. Sensory Aperture Payload**
```cpp
struct SVRSensoryAperturePayload {
    float cueAmplitude;      // χ
    float volatility;        // ν
    float holonomy;          // η
    vr::HmdVector3_t adjacencyField; // φ
};
```

---

### **2. Basin Modulation Payload**
```cpp
enum class SVRBasinType {
    Calm,
    Wonder,
    Curiosity,
    Reflection
};

struct SVRBasinPayload {
    SVRBasinType basin;
    float volatilityEnvelope;
    float holonomyRange;
    vr::HmdVector3_t adjacencyHint;
};
```

---

### **3. Accessibility Operator Payload**
```cpp
enum class SVROperator {
    Simplify,
    Expand,
    Reframe,
    Surface
};

struct SVROperatorPayload {
    SVROperator op;
    float loadReduction;
    float contextGain;
    float perspectiveShift;
    float structureReveal;
};
```

---

### **4. Stability Envelope**
```cpp
struct SVRStabilityEnvelope {
    float maxVolatility;
    float minHolonomy;
    float adjacencyIntegrity;
    bool dignityConstraint;
};
```

---

# **IV. SteamVR API Endpoints (OpenVR C++)**

### **1. Request Sensory Aperture**
```cpp
SVRSensoryAperturePayload NDH_SteamVR_GetAperture(vr::IVRSystem* system);
```

### **2. Request Basin Modulation**
```cpp
SVRBasinPayload NDH_SteamVR_GetBasinState(vr::IVRSystem* system);
```

### **3. Apply Accessibility Operator**
```cpp
SVROperatorPayload NDH_SteamVR_ApplyOperator(vr::IVRSystem* system, SVROperator op);
```

### **4. Request Stability Envelope**
```cpp
SVRStabilityEnvelope NDH_SteamVR_GetStabilityEnvelope(vr::IVRSystem* system);
```

### **5. Crossmap Translation**
```cpp
vr::VROverlayHandle_t NDH_SteamVR_TranslateToOverlay(NDHObject* obj);
```

---

# **V. SteamVR Input Integration**

### **Action Manifest Generation**
```cpp
void NDH_SteamVR_GenerateActionManifest(const SVRSensoryAperturePayload& aperture);
```

### **Adjacency‑Driven Action Binding**
```cpp
void NDH_SteamVR_ApplyAdjacencyToAction(const char* actionName, vr::HmdVector3_t adjacencyField);
```

---

# **VI. SteamVR Haptic Integration**

### **Basic Haptic Pulse**
```cpp
void NDH_SteamVR_ApplyHaptics(vr::TrackedDeviceIndex_t device, float amplitude, float duration);
```

### **Knuckles / Index Controller Haptics**
```cpp
void NDH_SteamVR_ApplyKnucklesHaptics(vr::TrackedDeviceIndex_t device, float amplitude, float frequency);
```

### **Basin‑Modulated Haptics**
```cpp
void NDH_SteamVR_ApplyBasinHaptics(vr::TrackedDeviceIndex_t device, const SVRBasinPayload& basin);
```

---

# **VII. Lighthouse Tracking Integration**

### **Adjacency‑Driven Pose Modulation**
```cpp
void NDH_SteamVR_ModulatePose(vr::TrackedDevicePose_t& pose, const vr::HmdVector3_t& adjacencyField);
```

### **Holonomy‑Aware Tracking Adjustment**
```cpp
void NDH_SteamVR_ModulateTracking(vr::TrackedDevicePose_t& pose, float holonomy);
```

---

# **VIII. Spatial Overlay Integration**

### **NDH → SteamVR Overlay Export**
```cpp
vr::VROverlayHandle_t NDH_SteamVR_ExportOverlay(NDHObject* obj);
```

### **Overlay Placement via Adjacency**
```cpp
void NDH_SteamVR_PlaceOverlay(vr::VROverlayHandle_t overlay, const vr::HmdVector3_t& adjacencyField);
```

---

# **IX. Stability Exchange Protocol (SEP)**

### **Runtime Negotiation**
```cpp
bool NDH_SteamVR_NegotiateStability(const SVRStabilityEnvelope& env);
```

### **Scene Stability Verification**
```cpp
bool NDH_SteamVR_VerifySceneStability(const SVRStabilityEnvelope& env);
```

---

# **X. Closing Statement**
This schema is:

- Phase‑10 compliant  
- invariant‑preserving  
- holonomy‑safe  
- volatility‑regulated  
- adjacency‑integrity‑aligned  
- SteamVR‑ready  

It is the **eighth major integration surface** NDH exposes.

---

