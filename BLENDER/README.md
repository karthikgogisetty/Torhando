# 🧱 Blender Simulations — TorHando

This module contains 3D models, scenes, and simulation setups created using Blender. It was primarily used to visualize robot behavior, end-effector motion, and interactions in a virtual environment before moving to physical prototypes.

---

## 🎯 Purpose

Blender helps simulate:
- End-effector motion
- Grasping and object manipulation
- Mechanical design feasibility
- Physics-based animations and renders

---

## 📁 Folder Structure

| Folder       | Description |
|--------------|-------------|
| `Files/`     | Contains `.blend` files and project assets (textures, images, etc.) |
| `README.md`  | This file |

---

## 🛠 Requirements

- Blender 2.9x or newer (recommended)
- Physics engine enabled for simulations (rigid body, soft body, collision)

---

## 📦 Assets Used

- 3D meshes exported from CAD tools or designed directly in Blender
- STL or DAE formats used for interoperability with Gazebo/ROS
- Basic animation keyframes and scripting (Python in Blender)

---

## ▶️ Running a Simulation

1. Open Blender and load a `.blend` file from `Files/`.
2. Hit **Spacebar** or **Play** button to run animation.
3. Modify timelines, constraints, or physics properties to simulate behaviors.

---

## 💡 Notes

- Use Blender’s **Python Scripting tab** to automate animations or export steps.
- Blender is also useful to create camera trajectories, which can later be simulated in Gazebo or ROS.

---

## 🔄 Cross-Integration

- CAD meshes from [CAD](../CAD) folder were often used here for material and texture preview.
- Simulated outputs help refine the trajectory logic implemented in [RPi4](../RPi4) and [ROS Files](../ROS%20Files).

---