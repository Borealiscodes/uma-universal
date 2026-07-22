# **iOS Taptic Engine Schema v1.0**  
### *NDH → iOS Integration Surface (CoreHaptics, UIFeedbackGenerator, Spatial Audio, Accessibility)*

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

to **iOS haptic and sensory systems**, using:

- CoreHaptics  
- UIFeedbackGenerator  
- CHHapticPattern  
- CHHapticEvent  
- Spatial Audio  
- Accessibility haptic patterns  

This is the sixth major Phase‑10 integration surface.

---

# **II. iOS Namespace Structure**

```
NDH.iOS
NDH.iOS.Sensory
NDH.iOS.Haptics
NDH.iOS.Accessibility
NDH.iOS.Crossmaps
NDH.iOS.Stability
```

Each namespace corresponds to a Phase‑10 layer.

---

# **III. Core Data Structures**

### **1. Sensory Aperture Payload**
```swift
struct IOSSensoryAperturePayload {
    var cueAmplitude: Float      // χ
    var volatility: Float        // ν
    var holonomy: Float          // η
    var adjacencyField: SIMD3<Float> // φ
}
```

---

### **2. Basin Modulation Payload**
```swift
enum IOSBasinType: Int {
    case calm
    case wonder
    case curiosity
    case reflection
}

struct IOSBasinPayload {
    var basin: IOSBasinType
    var volatilityEnvelope: Float
    var holonomyRange: Float
    var adjacencyHint: SIMD3<Float>
}
```

---

### **3. Accessibility Operator Payload**
```swift
enum IOSAccessibilityOperator: Int {
    case simplify
    case expand
    case reframe
    case surface
}

struct IOSOperatorPayload {
    var op: IOSAccessibilityOperator
    var loadReduction: Float
    var contextGain: Float
    var perspectiveShift: Float
    var structureReveal: Float
}
```

---

### **4. Stability Envelope**
```swift
struct IOSStabilityEnvelope {
    var maxVolatility: Float
    var minHolonomy: Float
    var adjacencyIntegrity: Float
    var dignityConstraint: Bool
}
```

---

# **IV. iOS API Endpoints (Swift)**

### **1. Request Sensory Aperture**
```swift
func getAperture() -> IOSSensoryAperturePayload
```

### **2. Request Basin Modulation**
```swift
func getBasinState() -> IOSBasinPayload
```

### **3. Apply Accessibility Operator**
```swift
func applyOperator(_ op: IOSAccessibilityOperator) -> IOSOperatorPayload
```

### **4. Request Stability Envelope**
```swift
func getStabilityEnvelope() -> IOSStabilityEnvelope
```

### **5. Crossmap Translation**
```swift
func translateToiOSObject(_ obj: NDHObject) -> Any
```

---

# **V. CoreHaptics Integration**

### **Basic Haptic Pattern**
```swift
func applyHaptics(intensity: Float, sharpness: Float, duration: TimeInterval)
```

### **CHHapticEvent Pattern**
```swift
func applyHapticEvent(_ event: CHHapticEvent)
```

### **Amplitude Curve**
```swift
func applyAmplitudeCurve(_ curve: [Float], times: [TimeInterval])
```

### **Basin‑Modulated Haptics**
```swift
func applyBasinHaptics(_ basin: IOSBasinPayload)
```

---

# **VI. UIFeedbackGenerator Integration**

### **Simplify Operator → Light Impact**
```swift
func applySimplifyFeedback()
```

### **Expand Operator → Medium Impact**
```swift
func applyExpandFeedback()
```

### **Reframe Operator → Heavy Impact**
```swift
func applyReframeFeedback()
```

### **Surface Operator → Selection Change**
```swift
func applySurfaceFeedback()
```

---

# **VII. Spatial Audio Integration**

### **Adjacency‑Driven Spatial Cue**
```swift
func applySpatialCue(_ source: AVAudioPlayerNode, adjacency: SIMD3<Float>, holonomy: Float)
```

---

# **VIII. Crossmap Translation Layer**

### **NDH → iOS Object Export**
```swift
func exportToiOS(_ obj: NDHObject) -> Any
```

### **NDH → Accessibility Binding**
```swift
func bindNDHObjectToAccessibility(_ obj: NDHObject)
```

---

# **IX. Stability Exchange Protocol (SEP)**

### **Runtime Negotiation**
```swift
func negotiateStability(_ envelope: IOSStabilityEnvelope) -> Bool
```

### **Scene Stability Verification**
```swift
func verifyRuntimeStability(_ envelope: IOSStabilityEnvelope) -> Bool
```

---

# **X. Closing Statement**
This schema is:

- Phase‑10 compliant  
- invariant‑preserving  
- holonomy‑safe  
- volatility‑regulated  
- adjacency‑integrity‑aligned  
- iOS‑ready  

It is the **sixth major integration surface** NDH exposes.

---

