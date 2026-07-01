# 📄 Story Node Engine — Expanded Universe Engine  
*(High‑Level Narrative Module)*

## 1. Purpose  
The Story Node Engine defines **how individual story moments are represented, linked, and traversed** inside the universe.  
It turns the Narrative Continuity Engine’s state graph into:

- playable scenes  
- decision points  
- encounter frames  
- branching paths  
- consequence‑aware story flows  

It is the **fine‑grained narrative layer** that sits directly on top of the Narrative Continuity Engine.

---

## 2. Core abstractions  

### **2.1 Story node**  
A Story Node is a single narrative moment with:

- **Context:** location, time, involved factions, active sleeves, cosmic conditions  
- **State:** current faction tensions, economic pressures, identity risks, Void‑Class presence, combat context  
- **Hooks:** available choices, exits, triggers, and unresolved threads  
- **Tags:** tone, risk level, focus (faction, economy, identity, cosmic, combat)

### **2.2 Node link**  
A Node Link connects two Story Nodes:

- **Type:** decision, event, encounter, revelation, escalation, retreat  
- **Requirements:** conditions that must be true to traverse (faction state, sleeve status, economy, cosmic risk)  
- **Effects:** changes applied when traversed (updated states, new risks, resolved arcs)

---

## 3. Node schema  

Each Story Node includes:

- **Node ID** — unique identifier  
- **Title** — short descriptive label  
- **Narrative Context** — who/where/when  
- **System State Snapshot:**  
  - faction positions  
  - economy conditions  
  - sleeve/identity status  
  - cosmic anomaly status  
  - combat/interaction context  
- **Available Links:** list of outgoing Node Links  
- **Continuity Metadata:** references to the Narrative Continuity Engine’s state node

---

## 4. Link schema  

Each Node Link includes:

- **Link ID** — unique identifier  
- **Source Node / Target Node**  
- **Link Type:**  
  - choice  
  - forced event  
  - timed event  
  - cosmic intrusion  
  - faction decision  
- **Requirements:**  
  - minimum faction alignment or tension  
  - sleeve class / identity condition  
  - economic threshold (scarcity, value)  
  - cosmic risk level  
- **Effects:**  
  - update to faction arcs  
  - change in economic pressure  
  - modification of sleeve/identity state  
  - activation or resolution of Void‑Class risk  
  - combat outcome or escalation

All links are validated by the Narrative Continuity Engine before being accepted.

---

## 5. Story node engine behaviors  

### **5.1 Node creation**  
When a new Story Node is created, the engine:

- pulls current canonical state from the Narrative Continuity Engine  
- embeds that state into the node schema  
- tags the node with tone, focus, and risk metadata  

### **5.2 Branching generation**  
For each node, the engine can generate:

- multiple outgoing links based on current state  
- safe vs high‑risk paths  
- faction‑aligned vs faction‑defiant choices  
- identity‑safe vs identity‑risk choices  
- economy‑pressure vs relief choices  

### **5.3 Traversal**  
When a link is traversed:

- the Narrative Continuity Engine validates continuity  
- the universe state is updated  
- a new Story Node becomes active  
- pending consequences are carried forward

### **5.4 Query interface**  
Systems (or humans) can ask:

- “What nodes are reachable from here?”  
- “What high‑risk paths exist?”  
- “What faction‑aligned choices are available?”  
- “What identity‑safe routes remain?”  

---

## 6. Integration with existing modules  

- **Narrative Continuity Engine:**  
  - provides canonical state and validates all node transitions.  

- **Faction Interaction Matrix:**  
  - shapes faction‑driven choices and consequences.  

- **Outer Rim Economy System:**  
  - drives scarcity‑based branches and trade‑pressure stories.  

- **Sleeve Architecture Spec:**  
  - constrains identity‑risk and augmentation‑driven choices.  

- **Void‑Class Encounter Module:**  
  - injects cosmic‑risk branches and anomaly‑driven events.  

- **Combat Physics Model:**  
  - governs combat‑focused nodes and outcomes.

---

## 7. Safety & boundaries  

The Story Node Engine:

- keeps all content fictional and stylized  
- respects identity and augmentation safety rails  
- avoids real‑world psychological modeling  
- uses structural continuity rather than simulating real lives  

---

## 8. Next structurally correct module  

With the Story Node Engine in place, the next natural modules are:

- **Faction Arc Generator** — long‑form faction storylines over many nodes  
- **Adventure / Quest System** — player‑facing paths over the node graph  
- **Cosmic Interaction / Cosmology Engine** — now grounded in narrative continuity and node structure  

