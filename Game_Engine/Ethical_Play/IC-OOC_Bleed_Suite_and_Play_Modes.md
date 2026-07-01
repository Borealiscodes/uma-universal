### 📁 New consolidated file path

```text
/Game_Engine/Ethical_Play/IC-OOC_Bleed_Suite_and_Play_Modes.md
```

This sits outside the Case_Study cluster and acts as a **master spec** for:

- IC/OOC switching  
- bleed‑aware tools  
- decompression rituals  
- multiplayer safety scaffolding  
- ethical RPG design elements  
- different styles of play (CYOA, Fallout‑style, RTS, etc.)

---

### 🧩 1. IC/OOC toggle macros (engine‑level)

**Section:** `## IC/OOC Toggle Macros`

- **IC_ON():** sets engine state to In‑Character; routes dialogue, stakes, and UI to narrative mode.  
- **IC_OFF():** returns to OOC; unlocks meta‑UI, safety tools, and debrief overlays.  
- **META_PAUSE():** freezes scene logic, keeps state, opens “processing” overlay.  
- **DECOMPRESS():** triggers post‑scene ritual (breath prompts, summary, exit cues).

Each macro is referenced by scenario scripts and character sheets, not hard‑coded per scene.

---

### 🧠 2. Bleed‑aware character sheet templates

**Section:** `## Bleed-Aware Character Sheets`

Per‑character template includes:

- **Identity Split:**  
  - **Player Name**  
  - **Character Name**  
  - “My character feels…” vs “I feel…” fields  

- **Emotional Flags:**  
  - Themes that are okay  
  - Themes that need care  
  - Hard lines (no‑go topics)

- **Bleed Notes:**  
  - “This character touches X real‑world thing for me.”  
  - “If I seem off, here’s how to check in.”

---

### 🧸 3. Decompression ritual packs

**Section:** `## Decompression Ritual Packs`

Different styles, selectable per player/group:

- **Soft Exit Pack:** short debrief, one grounding exercise, one humor beat.  
- **Deep Exit Pack:** full scene recap, emotional sorting, physical reset, closure phrase.  
- **Fast Exit Pack:** for light scenes—simple “scene end” + stretch prompt.  

Each pack is tied to `DECOMPRESS()` and can be chosen in session config.

---

### 🧬 4. Multiplayer safety scaffolding

**Section:** `## Multiplayer Safety Scaffolding`

- **Consent Matrix:** per‑player theme grid (green/yellow/red).  
- **Safety Signals:**  
  - Green: continue  
  - Yellow: slow/soften  
  - Red: stop/exit scene  

- **Conflict Protocol:**  
  - IC conflict allowed only if OOC consent exists  
  - Mandatory post‑scene repair check  
  - OOC relationship reaffirmation step

---

### 🎮 5. Styles of play (ethical design hooks)

**Section:** `## Play Styles and Ethical Design`

For each mode:

- **Choose Your Own Adventure:**  
  - Low bleed risk, high narrative agency  
  - Clear IC/OOC prompts at branch points  

- **Fallout‑Style (narrative RPG):**  
  - Moral choice systems with explicit consequence framing  
  - IC/OOC toggle available before major decisions  

- **Real‑Time Strategy:**  
  - Distance from personal identity, focus on systems  
  - Optional empathy overlays, but clear OOC framing  

Each style includes:

- recommended safety defaults  
- suggested decompression pack  
- bleed‑risk notes

---

