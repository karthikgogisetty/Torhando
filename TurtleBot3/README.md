# 🐢 TurtleBot3 Simulation & PI Controller — TorHando

This module demonstrates the implementation of closed-loop control on the TurtleBot3 robot in a simulated ROS + Gazebo environment. It is designed to achieve **Level 3 autonomy** by dynamically reducing positional error using a PI controller.

---

## 🎯 Objective

- Simulate TurtleBot3 in a virtual environment
- Move from home position to target dynamically
- Implement **Proportional-Integral (PI)** control
- Visualize movement and odometry feedback

---

## 🧰 Environment Setup

Ensure you have ROS Noetic and necessary TurtleBot3 packages:

```bash
# Step 1: Install required packages
sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-keyboard \
ros-noetic-rgbd-launch ros-noetic-amcl ros-noetic-map-server \
ros-noetic-move-base ros-noetic-urdf ros-noetic-gmapping ros-noetic-navigation

# Step 2: Install lidar driver
sudo apt install ros-noetic-hls-lfcd-lds-driver

# Step 3: Setup workspace and clone required packages
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git

# Step 4: Build and source
cd ~/catkin_ws
catkin_make
source devel/setup.bash
```

## ⚙️ Controller Logic
- Publishes velocity commands to /cmd_vel
- Subscribes to /odom for real-time feedback

Implements PI logic:

* P term: Error × Kp
* I term: Accumulated error × Ki
`error` = **goal_position - current_position**
`integral` += **error**
`control_signal` = `Kp` * `error` + `Ki` * `integral`

## 📊 PID Theory Summary
* *P (Proportional):* Immediate reaction to error
* *I (Integral):* Eliminates steady-state error
* *D (Derivative):* (Optional) Prevents overshooting

## 🎥 Output
The PI controller ensures smooth convergence to the goal. The test videos show: Minimal deviation
Gradual slowdown as it nears target, Repeatable stable performance

## Scope
Integrate with my [**_ArdiunoPlaybook**](https://github.com/karthikgogisetty/_ArduinoPlayground/tree/main) [Code of PID](https://github.com/karthikgogisetty/_ArduinoPlayground/tree/main/PID_) 
