# 🧠 ROS Navigation & Simulation — TorHando

This folder contains all ROS-related files including custom packages, launch files, configuration files, and simulation environments for TurtleBot2 and TurtleBot3 platforms. It showcases both Level 2 (PI controller) and Level 4 (autonomous navigation) autonomy.

---

## 🎯 Objective

Simulate and develop robot autonomy using:
- **ROS Noetic** middleware
- **Gazebo** for environment simulation
- **RViz** for real-time visualization
- Custom ROS nodes for control and navigation

---

## 📦 Key Packages

| Package Name             | Function |
|--------------------------|----------|
| `torhando/`              | Main robot package with launch, URDF, config, and nav parameters |
| `turtlebot_navigation/`  | Navigation stack using `move_base`, `DWA`, `navfn` |
| `kobuki_description/`    | URDF + meshes for Kobuki base simulation |
| `kobuki_gazebo_plugins/` | Gazebo plugins for TurtleBot2 |
| `turtlebot_description/` | Multi-sensor robot description models |

---

## 🧪 Simulation Levels

### 🟠 Level 2 Autonomy: PI Controller

- **Aim**: Follow a 2D trajectory using a closed-loop control system.
- **Approach**:
  - Custom `position_controller` node for velocity commands
  - Uses odometry as feedback
  - Visualized in RViz
---

### 🔵 Level 4 Autonomy: Navigation Stack

- **Aim**: Fully autonomous navigation to a goal while avoiding obstacles.
- **Tools**:
  - `move_base` for global/local planning
  - `DWA` as the local planner
  - `navfn` as the global planner
  - `amcl` for localization

---

## 🧭 Move Base Architecture

- **Costmaps**: Global + local costmaps updated with laser and depth data
- **Obstacle Avoidance**: Inflated grid zones prevent collisions
- **Trajectory Planning**: Using velocity samples scored against cost criteria

---

## 🗺️ Costmaps

| Type   | Description |
|--------|-------------|
| Global | Map-based planning |
| Local  | Real-time reactive planning |

---

## 🔧 Setup Instructions

```bash
cd ROS\ Files/turtle_sim_ws
catkin_make
source devel/setup.bash
roslaunch torhando torhando_world.launch
```

## 🧠 Concepts Covered

- Odometry Feedback
- Differential Drive Kinematics
- PI Control
- ROS Navigation Stack
- Sensor Fusion (LaserScan + Depth)
- DWA and Global Planning

## 📎 Related Folders

**RPi4:** For physical end-effector testing
**TurtleBot3:** TurtleBot3 simulation
**CAD:** 3D printed parts used for testing
**Arduino:** Low-level actuator control

## 🔗 References
- http://wiki.ros.org/move_base
- http://wiki.ros.org/dwa_local_planner
