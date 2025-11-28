# 🕳️ Schwarzschild Black Hole Simulation (Web-Based)

A real-time, physically accurate visual simulation of a Schwarzschild black hole and its accretion disk.  
This project uses **WebGL (via Three.js)** and **custom GLSL fragment shaders** to solve the geodesic equations that describe how light curves around a massive object — all inside your browser.

> **Note:** The physics engine, shader math, and rendering logic were generated using **Google Gemini**.

---

## 🚀 Features

- **Raymarching in Curved Spacetime**  
  Simulates non-Euclidean geometry by integrating geodesics instead of using standard 3D rays.

- **Gravitational Lensing**  
  Produces Einstein Rings & realistic space-warping around the black hole.

- **Volumetric Accretion Disk**  
  Not a flat texture — a fully volumetric sampled field with noise-based turbulence.

- **Relativistic Beaming (Doppler Shift)**  
  Approaching side appears bright/blue; receding side becomes dim/red.

- **Gravitational Redshift**  
  Light near the event horizon fades to deep red as it loses energy.

- **Photon Ring Visualization**  
  Shows the unstable orbit at ~1.5 Schwarzschild radii.

- **Adaptive Step-Size Integration**  
  Higher precision near the event horizon; faster simulation in empty space.

---

## 🛠️ Technology Stack

- **HTML5 / JavaScript** – Core structure  
- **Three.js** – WebGL setup & user interaction  
- **GLSL (Fragment Shader)** – 99% of the physics + rendering pipeline runs on GPU  

---

## 📐 The Physics (How It Works)

Traditional 3D engines assume straight-line light travel.  
This simulation instead performs **raymarching with geodesic integration**:

1. **Camera emits a ray for each pixel**
2. **Ray marches forward in tiny steps**
3. At every step:
   - Gravity is computed from the **Schwarzschild metric**
   - Ray velocity is updated (curved path)
4. If the ray intersects the accretion disk:
   - Gas density, rotation velocity & temperature determine pixel color

**Simplified gravitational acceleration**  

---

## 🎮 Controls

- **Left Click + Drag** → Orbit camera  
- **Scroll Wheel** → Zoom (get dangerously close!)

---


## 🤖 Credits

- **Concept & Prompt Engineering:** **DÁNISH**  
- **Physics & Shader Code Generation:** Google Gemini  

Created as part of an exploration into **AI-assisted GPU graphics and relativistic rendering**.

---
