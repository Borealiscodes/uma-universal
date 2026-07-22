# **Unity API Schema v1.0**  
### *NDH → Unity Integration Surface (C#, XR, Haptics, Multimodal IO)*

---

## **I. Purpose**
This schema defines how NDH exposes:

- sensory aperture cues  
- volatility envelopes  
- holonomy signatures  
- adjacency fields  
- basin modulation  
- accessibility operators  

to **Unity** via:

- C#  
- ScriptableObjects  
- XR Interaction Toolkit  
- Input System  
- DOTS (optional)  
- Haptics (Gamepad, XR controllers)  
- Spatial audio (Unity AudioSource + Dolby Atmos plugin)  

---

# **II. Namespace Structure**

```
NDH.Unity
NDH.Unity.Sensory
NDH.Unity.Haptics
NDH.Unity.XR
NDH.Unity.Accessibility
NDH.Unity.Crossmaps
NDH.Unity.Stability
```

Each namespace corresponds to a Phase‑10 layer.

---

# **III. Core Data Structures**

### **1. Sensory Aperture Payload**
```
struct SensoryAperturePayload {
    float cueAmplitude;      // χ
    float volatility;        // ν
    float holonomy;          // η
    Vector3 adjacencyField;  // φ
}
```

### **2. Basin Modulation Payload**
```
enum BasinType { Calm, Wonder, Curiosity, Reflection }

struct BasinPayload {
    BasinType basin;
    float volatilityEnvelope;
    float holonomyRange;
    Vector3 adjacencyHint;
}
```

### **3. Accessibility Operator Payload**
```
enum AccessibilityOperator { Simplify, Expand, Reframe, Surface }

struct OperatorPayload {
    AccessibilityOperator op;
    float loadReduction;
    float contextGain;
    float perspectiveShift;
    float structureReveal;
}
```

### **4. Stability Envelope**
```
struct StabilityEnvelope {
    float maxVolatility;
    float minHolonomy;
    float adjacencyIntegrity;
    bool dignityConstraint;
}
```

---

# **IV. Unity API Endpoints**

### **1. Request Sensory Aperture**
```
SensoryAperturePayload NDH.Unity.Sensory.GetAperture();
```

### **2. Request Basin Modulation**
```
BasinPayload NDH.Unity.Sensory.GetBasinState();
```

### **3. Apply Accessibility Operator**
```
OperatorPayload NDH.Unity.Accessibility.ApplyOperator(AccessibilityOperator op);
```

### **4. Request Stability Envelope**
```
StabilityEnvelope NDH.Unity.Stability.GetEnvelope();
```

### **5. Request Crossmap Translation**
```
ScriptableObject NDH.Unity.Crossmaps.TranslateToUnityObject(NDHObject obj);
```

---

# **V. XR Integration**

### **XR Input System**
```
void NDH.Unity.XR.ApplyAdjacencyToXRController(InputDevice device, Vector3 adjacencyField);
```

### **XR Interaction Toolkit**
```
void NDH.Unity.XR.ModulateXRInteraction(XRBaseInteractable interactable, BasinPayload basin);
```

---

# **VI. Haptic Integration**

### **Gamepad**
```
void NDH.Unity.Haptics.ApplyHaptics(Gamepad pad, float amplitude, float duration);
```

### **XR Controllers**
```
void NDH.Unity.Haptics.ApplyXRHaptics(InputDevice device, float amplitude, float frequency);
```

---

# **VII. Spatial Audio Integration (Dolby‑compatible)**

```
void NDH.Unity.Audio.ApplySpatialCue(AudioSource source, Vector3 adjacencyField, float holonomy);
```

---

# **VIII. Crossmap Translation Layer**

### **Unity ScriptableObject Export**
```
ScriptableObject NDH.Unity.Crossmaps.Export(NDHObject obj);
```

### **Unity Prefab Integration**
```
GameObject NDH.Unity.Crossmaps.BindToPrefab(NDHObject obj, GameObject prefab);
```

---

# **IX. Stability Exchange Protocol (SEP)**

### **Unity Physics**
```
bool NDH.Unity.Stability.NegotiateWithPhysics(Rigidbody rb, StabilityEnvelope env);
```

### **Unity Scene Runtime**
```
bool NDH.Unity.Stability.VerifySceneStability(Scene scene, StabilityEnvelope env);
```

---

# **X. Closing Statement**
This schema is:

- Phase‑10 compliant  
- invariant‑preserving  
- holonomy‑safe  
- volatility‑regulated  
- adjacency‑integrity‑aligned  
- Unity‑ready  

It is the **first concrete integration surface** NDH exposes.

---


