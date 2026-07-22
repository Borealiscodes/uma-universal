# **VisionOS API Schema v1.0**  
### *NDH → Apple VisionOS Integration Surface (RealityKit, Spatial Anchors, Haptics, Multimodal IO)*

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

to **Apple VisionOS**, using:

- RealityKit  
- ARKit / Spatial Anchors  
- Swift APIs  
- Haptic Engine  
- Spatial Audio  
- Immersive Spaces  
- Entity Components  

This is the fourth major Phase‑10 integration surface.

---

# **II. VisionOS Namespace Structure**

```
NDH.VisionOS
NDH.VisionOS.Sensory
NDH.VisionOS.Haptics
NDH.VisionOS.Spatial
NDH.VisionOS.Accessibility
NDH.VisionOS.Crossmaps
NDH.VisionOS.Stability
```

Each namespace corresponds to a Phase‑10 layer.

---

# **III. Core Data Structures**

### **1. Sensory Aperture Payload**
```swift
struct VOSSensoryAperturePayload {
    var cueAmplitude: Float      // χ
    var volatility: Float        // ν
    var holonomy: Float          // η
    var adjacencyField: SIMD3<Float> // φ
}
```

---

### **2. Basin Modulation Payload**
```swift
enum VOSBasinType: Int {
    case calm
    case wonder
    case curiosity
    case reflection
}

struct VOSBasinPayload {
    var basin: VOSBasinType
    var volatilityEnvelope: Float
    var holonomyRange: Float
    var adjacencyHint: SIMD3<Float>
}
```

---

### **3. Accessibility Operator Payload**
```swift
enum VOSAccessibilityOperator: Int {
    case simplify
    case expand
    case reframe
    case surface
}

struct VOSOperatorPayload {
    var op: VOSAccessibilityOperator
    var loadReduction: Float
    var contextGain: Float
    var perspectiveShift: Float
    var structureReveal: Float
}
```

---

### **4. Stability Envelope**
```swift
struct VOSStabilityEnvelope {
    var maxVolatility: Float
    var minHolonomy: Float
    var adjacencyIntegrity: Float
    var dignityConstraint: Bool
}
```

---

# **IV. VisionOS API Endpoints (Swift)**

### **1. Request Sensory Aperture**
```swift
func getAperture() -> VOSSensoryAperturePayload
```

### **2. Request Basin Modulation**
```swift
func getBasinState() -> VOSBasinPayload
```

### **3. Apply Accessibility Operator**
```swift
func applyOperator(_ op: VOSAccessibilityOperator) -> VOSOperatorPayload
```

### **4. Request Stability Envelope**
```swift
func getStabilityEnvelope() -> VOSStabilityEnvelope
```

### **5. Crossmap Translation**
```swift
func translateToRealityKitEntity(_ obj: NDHObject) -> Entity
```

---

# **V. Spatial Integration (RealityKit + ARKit)**

### **Adjacency‑Driven Spatial Anchors**
```swift
func createAdjacencyAnchor(_ adjacency: SIMD3<Float>) -> AnchorEntity
```

### **Holonomy‑Aware Transform Modulation**
```swift
func modulateTransform(_ entity: Entity, holonomy: Float)
```

### **Immersive Space Integration**
```swift
func bindToImmersiveSpace(_ obj: NDHObject, space: ImmersiveSpace)
```

---

# **VI. Haptic Integration (HapticEngine)**

### **Basic Haptic Pattern**
```swift
func applyHaptics(amplitude: Float, duration: Float)
```

### **Basin‑Modulated Haptics**
```swift
func applyBasinHaptics(_ basin: VOSBasinPayload)
```

---

# **VII. Spatial Audio Integration**

### **Adjacency‑Driven Spatial Cue**
```swift
func applySpatialCue(_ source: AudioSource, adjacency: SIMD3<Float>, holonomy: Float)
```

---

# **VIII. Crossmap Translation Layer**

### **NDH → RealityKit Entity Export**
```swift
func exportToRealityKit(_ obj: NDHObject) -> Entity
```

### **NDH → Component Binding**
```swift
func bindNDHObject(_ obj: NDHObject, to entity: Entity)
```

---

# **IX. Stability Exchange Protocol (SEP)**

### **Scene Stability Negotiation**
```swift
func negotiateSceneStability(_ envelope: VOSStabilityEnvelope) -> Bool
```

### **Runtime Verification**
```swift
func verifyRuntimeStability(_ envelope: VOSStabilityEnvelope) -> Bool
```

---

# **X. Closing Statement**
This schema is:

- Phase‑10 compliant  
- invariant‑preserving  
- holonomy‑safe  
- volatility‑regulated  
- adjacency‑integrity‑aligned  
- VisionOS‑ready  

It is the **fourth major integration surface** NDH exposes.

---

