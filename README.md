# BuildFlow 🏗️

[![Blender](https://img.shields.io/badge/Blender-%23F5792A.svg?style=for-the-badge&logo=blender&logoColor=white)](https://www.blender.org)
[![Procedural](https://img.shields.io/badge/Procedural-Geometry%20Nodes-blue?style=for-the-badge)]()

**BuildFlow** is a powerful procedural system built inside Blender using Geometry Nodes. It is designed to automatically generate high-quality, full-CG architectural construction time-lapse animations from your own master plans and 3D assets. 

---
Download for free here : https://www.turbosquid.com/3d-models/3d-buildflow-procedural-timelapse-animation-2584245
## 📺 Previews & Video Guides

### Project Showcase
Click the image below to watch the cinematic procedural time-lapse animation showcase on YouTube:
[![BuildFlow Procedural timelapse animation in Blender](https://img.shields.io/badge/YouTube-Watch%20Showcase-red?style=for-the-badge&logo=youtube)](https://youtu.be/L6SQys0yTuY)

<a href="https://youtu.be/L6SQys0yTuY" target="_blank">
  <img src="https://i.ytimg.com/vi/L6SQys0yTuY/maxresdefault.jpg" alt="BuildFlow Showcase Preview" width="100%" style="border-radius: 8px; margin-bottom: 20px;" />
</a>

### Video Tutorial
Click the image below to watch the comprehensive, step-by-step setup and user guide on YouTube:
[![Buildflow Tutorial](https://img.shields.io/badge/YouTube-Watch%20Tutorial-yellow?style=for-the-badge&logo=youtube)](https://youtu.be/BNWJKnQGaZ4)

<a href="https://youtu.be/BNWJKnQGaZ4" target="_blank">
  <img src="https://i.ytimg.com/vi/BNWJKnQGaZ4/maxresdefault.jpg" alt="BuildFlow Tutorial Preview" width="100%" style="border-radius: 8px;" />
</a>

---

## ✨ Features

- 🏢 **Custom Architecture Support:** Seamlessly swap the template models with your own project meshes.
- 📐 **Fully Procedural Scaffolding & Growth:** Control building phases, floors count, floor height, and material transitions via simple sliders.
- 🏗️ **Procedural Construction Equipment:** Automated construction cranes that procedurally rotate and animate on every frame to simulate active time-lapse work.
- 🌾 **Environment Dynamics:** Built-in Geometry Nodes wind simulation setup for trees and foliage scattering.
- 🚗 **Populated Master Plans:** Easy scattering and path animation for vehicles, props, safety fences, and crowds.

---

## 📖 Step-by-Step Tutorial

To adapt **BuildFlow** to your own architectural project, follow these structural rules outlined in the video guide:

### 1. Asset Organization (Crucial)
Before feeding your building into the Geometry Node setup, you must split your 3D architecture model into **three distinct collections** at the scene coordinates **(0,0,0)**:
- `Main` — Contains the primary structural elements (outer walls, floors).
- `Details` — External architectural design elements, excluding interior partitions.
- `Interior Walls` — Dedicated specifically to internal separations to ensure realistic wall-rising boolean animations.

*Note: If you want to use the animated vegetation system, place your trees into the designated `props tree` collection to receive the procedural wind properties.*

### 2. Configuring the Master Plan & Props
- **Ground Transition:** Use the `Boolean` slider to keyframe the procedural transition phase between your basic master plan plane and the finalized dirt/concrete environment textures.
- **Paths & Roads:** Draw curves named `geo_nodes_road` to procedurally plot custom road pathways.
- **Vehicles & Fences:** Adjust scattering steps and randomize density using specific asset sliders. Use the movement sliders to animate traffic flux. Assign a vertex group to your layout plane's edges to align perimeter fences perfectly.

### 3. Rigging Your Custom Building
- Create a new mesh polygon mimicking the general footprint/shape of your target building and center its origin point.
- Assign the main **BuildFlow** Geometry Nodes modifier to this polygon.
- Inside the modifier panel preferences, link your predefined `Main`, `Details`, and `Interior Walls` collections into their respective input slots.
- Use the **Offset** parameters to pull or compress the bounding growth logic slightly inside your physical walls to prevent texture clipping or exposed floor meshes at early build stages.
- Adjust procedural floors count, floor height, polygon generation randomness, and material blending vectors. All core controls are color-coded in **green** within the modifier layout, indicating they are ready to be keyframed for custom animation timing.

### 4. Animating the Cranes
- Cranes are bound to simple target path-lines. You can move or copy these lines anywhere around your site.
- The system automatically triggers randomized rotation angles on every individual frame playback to natively reproduce erratic, fast-forward time-lapse behavior.

---

## 🛠️ Requirements
- **Blender 4.x** (or newer versions featuring advanced Geometry Nodes support).
