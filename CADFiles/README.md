# 🛠️ CAD Designs — TorHando

This folder contains mechanical designs created using CAD software to prototype parts of the robot such as its chassis, brackets, joints, and custom attachments. These designs were either used for 3D printing or referenced in Blender/URDF visualizations.

---

## 🎯 Purpose

- Create 3D-printable parts (robotic arms, base frames, brackets)
- Prototype the design of the mobile base, end-effector, and mounts
- Export geometries for use in Blender, Gazebo, and ROS

---

## 📁 Folder Structure

| File/Folder | Description |
|-------------|-------------|
| `.stl` / `.step` files | Standard formats used for slicing/3D printing |
| `.f3d`, `.sldprt` | Native design files (e.g., Fusion360, SolidWorks) |
| `README.md` | This file |

---

## 🧰 Tools Used

- Autodesk Fusion360 (Primary)
- SolidWorks
- FreeCAD (for STL conversion)

---

## 🔄 Integration

- STL/DAE files were used in:
  - [BLENDER](../BLENDER) for rendering
  - [ROS Files](../ROS%20Files) as visual/collision meshes in URDF
- Measurements and spacing align with real-world TurtleBot3 and Kobuki platforms

---

## 🖨️ 3D Printing

Recommended settings for PLA:
- Layer Height: 0.2 mm
- Infill: 20–40%
- Supports: As required
- Bed Temp: 60°C | Nozzle Temp: 200°C

---

## 💡 Tips

- Use mesh simplification before importing large STL files into Gazebo or Blender.
- Maintain consistent scaling (typically in meters) for ROS compatibility.

---

## 📎 Related

- Used alongside [RPi4](../RPi4) and [Arduino](../Arduino) modules to build the physical robot.
- Refer to [ROSFiles](../ROSFiles) for simulation setups using these models.
