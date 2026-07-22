# **Unreal API Schema v1.0**  
### *NDH → Unreal Engine Integration Surface (C++, Blueprint, MetaSound, XR, Haptics)*

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

to **Unreal Engine** via:

- C++  
- Blueprint  
- USTRUCT / UObject  
- DataAssets  
- Enhanced Input  
- XR frameworks  
- MetaSound  
- Haptic interfaces  

---

# **II. Unreal Namespace Structure**

```
namespace NDHUnreal
{
    namespace Sensory { }
    namespace Haptics { }
    namespace XR { }
    namespace Accessibility { }
    namespace Crossmaps { }
    namespace Stability { }
}
```

Each namespace corresponds to a Phase‑10 layer.

---

# **III. Core Data Structures**

### **1. Sensory Aperture Payload**
```cpp
USTRUCT(BlueprintType)
struct FSensoryAperturePayload
{
    GENERATED_BODY()

    UPROPERTY(BlueprintReadWrite)
    float CueAmplitude;     // χ

    UPROPERTY(BlueprintReadWrite)
    float Volatility;       // ν

    UPROPERTY(BlueprintReadWrite)
    float Holonomy;         // η

    UPROPERTY(BlueprintReadWrite)
    FVector AdjacencyField; // φ
};
```

---

### **2. Basin Modulation Payload**
```cpp
UENUM(BlueprintType)
enum class EBasinType : uint8
{
    Calm,
    Wonder,
    Curiosity,
    Reflection
};

USTRUCT(BlueprintType)
struct FBasinPayload
{
    GENERATED_BODY()

    UPROPERTY(BlueprintReadWrite)
    EBasinType Basin;

    UPROPERTY(BlueprintReadWrite)
    float VolatilityEnvelope;

    UPROPERTY(BlueprintReadWrite)
    float HolonomyRange;

    UPROPERTY(BlueprintReadWrite)
    FVector AdjacencyHint;
};
```

---

### **3. Accessibility Operator Payload**
```cpp
UENUM(BlueprintType)
enum class EAccessibilityOperator : uint8
{
    Simplify,
    Expand,
    Reframe,
    Surface
};

USTRUCT(BlueprintType)
struct FOperatorPayload
{
    GENERATED_BODY()

    UPROPERTY(BlueprintReadWrite)
    EAccessibilityOperator Operator;

    UPROPERTY(BlueprintReadWrite)
    float LoadReduction;

    UPROPERTY(BlueprintReadWrite)
    float ContextGain;

    UPROPERTY(BlueprintReadWrite)
    float PerspectiveShift;

    UPROPERTY(BlueprintReadWrite)
    float StructureReveal;
};
```

---

### **4. Stability Envelope**
```cpp
USTRUCT(BlueprintType)
struct FStabilityEnvelope
{
    GENERATED_BODY()

    UPROPERTY(BlueprintReadWrite)
    float MaxVolatility;

    UPROPERTY(BlueprintReadWrite)
    float MinHolonomy;

    UPROPERTY(BlueprintReadWrite)
    float AdjacencyIntegrity;

    UPROPERTY(BlueprintReadWrite)
    bool DignityConstraint;
};
```

---

# **IV. Unreal API Endpoints (C++ + Blueprint)**

### **1. Request Sensory Aperture**
```cpp
UFUNCTION(BlueprintCallable)
FSensoryAperturePayload GetAperture();
```

### **2. Request Basin Modulation**
```cpp
UFUNCTION(BlueprintCallable)
FBasinPayload GetBasinState();
```

### **3. Apply Accessibility Operator**
```cpp
UFUNCTION(BlueprintCallable)
FOperatorPayload ApplyOperator(EAccessibilityOperator Operator);
```

### **4. Request Stability Envelope**
```cpp
UFUNCTION(BlueprintCallable)
FStabilityEnvelope GetStabilityEnvelope();
```

### **5. Crossmap Translation**
```cpp
UFUNCTION(BlueprintCallable)
UObject* TranslateToUnrealObject(UNDHObject* NDHObject);
```

---

# **V. XR Integration**

### **Enhanced Input**
```cpp
void ApplyAdjacencyToXRController(const FInputActionValue& ActionValue, const FVector& AdjacencyField);
```

### **Unreal XR Framework**
```cpp
void ModulateXRInteraction(UPrimitiveComponent* Component, const FBasinPayload& Basin);
```

---

# **VI. Haptic Integration**

### **Gamepad**
```cpp
void ApplyHapticsToGamepad(float Amplitude, float Duration);
```

### **XR Controllers**
```cpp
void ApplyXRHaptics(float Amplitude, float Frequency);
```

---

# **VII. MetaSound Integration**

```cpp
void ApplySpatialCueToMetaSound(UMetaSoundSource* Source, const FVector& AdjacencyField, float Holonomy);
```

---

# **VIII. Crossmap Translation Layer**

### **DataAsset Export**
```cpp
UDataAsset* ExportToDataAsset(UNDHObject* NDHObject);
```

### **Blueprint Binding**
```cpp
void BindNDHObjectToBlueprint(UNDHObject* NDHObject, UObject* BlueprintObject);
```

---

# **IX. Stability Exchange Protocol (SEP)**

### **Chaos Physics**
```cpp
bool NegotiateWithChaosPhysics(UPrimitiveComponent* Component, const FStabilityEnvelope& Envelope);
```

### **Unreal Scene Runtime**
```cpp
bool VerifySceneStability(UWorld* World, const FStabilityEnvelope& Envelope);
```

---

# **X. Closing Statement**
This schema is:

- Phase‑10 compliant  
- invariant‑preserving  
- holonomy‑safe  
- volatility‑regulated  
- adjacency‑integrity‑aligned  
- Unreal‑ready  

It is the **second major integration surface** NDH exposes.

---

