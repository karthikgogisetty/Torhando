# 🤖 TorHando Robotics Project

TorHando is a modular, multi-platform robotics framework designed to integrate and simulate real-world robot behaviors using ROS, Gazebo, TurtleBot3, RPi4, Arduino, Blender, and CAD tools. It is built to explore different levels of robot autonomy — from direct control (Level 0) to full autonomy (Level 5) — through simulations and hardware prototypes.

---

## 🔧 Project Modules (Table of Contents)

| Folder | Description |
|--------|-------------|
| [ARDUINOFiles](./ARDUINOFiles) | Microcontroller-based control systems using Arduino. |
| [BLENDER](./BLENDER) | Blender files for 3D modeling and simulation of robots. |
| [BLENDER/Files](./BLENDER/Files) | Specific assets used in the Blender scenes. |
| [CADFiles](./CADFiles) | CAD designs and STL files for physical prototyping. |
| [ROSFiles](./ROSFiles) | Complete ROS workspace including Gazebo and move_base simulations for various autonomy levels. |
| [RPi4Files](./RPi4Files) | Raspberry Pi-based control scripts including a Telegram-based control bot. |
| [TurtleBot3](./TurtleBot3) | TurtleBot3 simulation and controller (PID/PI implementation) under ROS Noetic. |

---

## 🧠 Key Highlights

- **Level 2 & 4 Autonomy Implementations** in simulation and code.
- **PI/PID Controllers** for motion control via `/cmd_vel` and `/odom`.
- **Telegram Bot Integration** with Raspberry Pi for IoT-like control.
- **Move_base + DWA Planning** for obstacle navigation and trajectory planning.
- **URDF, Gazebo Worlds, RViz configs**, and costmap params for full-stack robot simulation.

---

## 🗂 ROS Submodules

Explore core ROS logic and models inside the main workspace:

- `ROS Files/turtle_sim_ws/src/kobuki_description`
- `ROS Files/turtle_sim_ws/src/torhando`
- `ROS Files/turtle_sim_ws/src/turtlebot_navigation`
- `ROS Files/turtle_sim_ws/src/turtlebot_description`

Each has its own launch files, URDFs, and controller nodes.

---

## 📦 Setup Instructions

```bash
# Clone the repo
git clone https://github.com/yourusername/TorHando.git
cd TorHando/ROS\ Files/turtle_sim_ws

# Build the workspace
catkin_make
source devel/setup.bash
```

## 📽️ Results & Demonstrations
Check the results folder for simulation output screenshots

📜 License
This project is under the MIT License.

🙌 Contributors
Project built by my team from Mechatronics Department, MAHE as part of academic and exploratory robotics research.
- @parzival897
- @Devineni-Shashank
- @arthurgomes4
- @Tejal-V-Shetty

**Note:** please check the old repo for a more detailed contribution: [Not maintained Torhando repo](https://github.com/KarthikGogisetty07/TorHando)