# **WebXR Schema v1.0**  
### *NDH → WebXR Integration Surface (XRSession, XRInputSource, Haptics, Layers, Anchors, Accessibility)*

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

to **WebXR**, using:

- `XRSession`  
- `XRInputSource`  
- WebXR Haptics  
- WebXR Layers  
- Anchors API  
- Web Audio spatial cues  
- Accessibility patterns  

This is the **ninth major Phase‑10 integration surface**.

---

# **II. WebXR Namespace Structure**

```
NDH.WebXR
NDH.WebXR.Sensory
NDH.WebXR.Haptics
NDH.WebXR.Input
NDH.WebXR.Spatial
NDH.WebXR.Accessibility
NDH.WebXR.Crossmaps
NDH.WebXR.Stability
```

Each namespace corresponds to a Phase‑10 layer.

---

# **III. Core Data Structures**

### **1. Sensory Aperture Payload**
```javascript
class WXRSensoryAperturePayload {
  constructor(cueAmplitude, volatility, holonomy, adjacencyField) {
    this.cueAmplitude = cueAmplitude;   // χ
    this.volatility = volatility;       // ν
    this.holonomy = holonomy;           // η
    this.adjacencyField = adjacencyField; // φ [x,y,z]
  }
}
```

---

### **2. Basin Modulation Payload**
```javascript
const WXR_BASIN = {
  CALM: "calm",
  WONDER: "wonder",
  CURIOSITY: "curiosity",
  REFLECTION: "reflection"
};

class WXRBasinPayload {
  constructor(basin, volatilityEnvelope, holonomyRange, adjacencyHint) {
    this.basin = basin;
    this.volatilityEnvelope = volatilityEnvelope;
    this.holonomyRange = holonomyRange;
    this.adjacencyHint = adjacencyHint;
  }
}
```

---

### **3. Accessibility Operator Payload**
```javascript
const WXR_OPERATOR = {
  SIMPLIFY: "simplify",
  EXPAND: "expand",
  REFRAME: "reframe",
  SURFACE: "surface"
};

class WXROperatorPayload {
  constructor(op, loadReduction, contextGain, perspectiveShift, structureReveal) {
    this.op = op;
    this.loadReduction = loadReduction;
    this.contextGain = contextGain;
    this.perspectiveShift = perspectiveShift;
    this.structureReveal = structureReveal;
  }
}
```

---

### **4. Stability Envelope**
```javascript
class WXRStabilityEnvelope {
  constructor(maxVolatility, minHolonomy, adjacencyIntegrity, dignityConstraint) {
    this.maxVolatility = maxVolatility;
    this.minHolonomy = minHolonomy;
    this.adjacencyIntegrity = adjacencyIntegrity;
    this.dignityConstraint = dignityConstraint;
  }
}
```

---

# **IV. WebXR API Endpoints**

### **1. Request Sensory Aperture**
```javascript
function getAperture(session) { /* returns WXRSensoryAperturePayload */ }
```

### **2. Request Basin Modulation**
```javascript
function getBasinState(session) { /* returns WXRBasinPayload */ }
```

### **3. Apply Accessibility Operator**
```javascript
function applyOperator(session, op) { /* returns WXROperatorPayload */ }
```

### **4. Request Stability Envelope**
```javascript
function getStabilityEnvelope(session) { /* returns WXRStabilityEnvelope */ }
```

### **5. Crossmap Translation**
```javascript
function translateToWebXRLayer(ndhObject) { /* returns XRLayer */ }
```

---

# **V. WebXR Input Integration**

### **Adjacency‑Driven Input Modulation**
```javascript
function applyAdjacencyToInputSource(inputSource, adjacencyField) { }
```

### **Holonomy‑Aware Input Behavior**
```javascript
function modulateInputHolonomy(inputSource, holonomy) { }
```

---

# **VI. WebXR Haptic Integration**

### **Basic Haptic Pulse**
```javascript
function applyHaptics(inputSource, amplitude, duration) { }
```

### **Basin‑Modulated Haptics**
```javascript
function applyBasinHaptics(inputSource, basinPayload) { }
```

---

# **VII. WebXR Spatial Integration**

### **Adjacency‑Driven Anchors**
```javascript
function createAdjacencyAnchor(session, adjacencyField) { }
```

### **Holonomy‑Aware Transform Modulation**
```javascript
function modulateTransformWithHolonomy(space, holonomy) { }
```

---

# **VIII. Web Audio Spatial Integration**

### **Adjacency‑Driven Spatial Cue**
```javascript
function applySpatialCue(audioNode, adjacencyField, holonomy) { }
```

---

# **IX. Crossmap Translation Layer**

### **NDH → WebXR Layer Export**
```javascript
function exportToWebXRLayer(ndhObject) { }
```

### **NDH → DOM / Canvas Binding**
```javascript
function bindNDHObjectToCanvas(ndhObject, canvas) { }
```

---

# **X. Stability Exchange Protocol (SEP)**

### **Runtime Negotiation**
```javascript
function negotiateStability(session, envelope) { }
```

### **Scene Stability Verification**
```javascript
function verifySceneStability(session, envelope) { }
```

---

# **XI. Closing Statement**
This schema is:

- Phase‑10 compliant  
- invariant‑preserving  
- holonomy‑safe  
- volatility‑regulated  
- adjacency‑integrity‑aligned  
- WebXR‑ready  

It is the **ninth and final major integration surface** NDH exposes.

---

