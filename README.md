# Synth Grid Engine

A blueprint-driven simulation shell where geometry becomes computation.

This project is an experimental system that treats space like a filesystem and entities like autonomous executors. The world itself becomes a programmable environment.

Inspired by:
- TRON Grid Worlds
- Geometry Wars style spatial computation
- Modular OS-like simulation environments

---

# Core Idea

Instead of building a fixed application, the engine loads **blueprints** that define how the world behaves.

The system consists of three blueprint layers:

1. **Shell Blueprint**
   Defines the world geometry.

2. **Module Blueprints**
   Attach systems into the world.

3. **Execution Layer**
   Deterministic simulation loop.

Geometry = storage  
Movement = computation  
Entities = executors  

---

# Architecture

Engine Core


Builds an octagon shell structure where modules can attach.

---

# Controls
```json
| Key | Action |
|----|----|
| WASD | Move master control |
| Mouse | Aim vector |
| C | Toggle reticle |
| ` | Toggle debug overlay |
| R | Reset |
```
---

# Running the Engine

1. Download the repository
2. Open index.html

in a browser.

No server required.

---

# Loading Blueprints

Upload blueprints into the runtime UI.

Recommended order:

1️⃣ Shell blueprint  

2️⃣ Ship module  

3️⃣ Scanner module  

4️⃣ HUD module (optional)  

---

# Blueprint Format

Example module blueprint

```json
{
  "moduleType": "scanner",
  "id": "SCAN_01",
  "style": "default",
  "config": {},
  "script": ""
}
```

---

# What people will understand it as

> A modular simulation engine where you build worlds by attaching blueprints instead of writing code.



