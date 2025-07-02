# MazeSolver

This repository contains the code to run a simulation of a TurtleBot3 solving a maze using **Gazebo Classic** and **ROS 2 Humble**.

---

## 🚀 Deployment Instructions

Follow the steps below to set up and run the project.

### 1. Clone the Repository

Open a terminal in the directory where you want to clone the project and run:

```bash
gh repo clone amaan-ee-iitr/mazeSolver
cd mazeSolver/
```

### 2. Build the Project

Run the following command to build the project using `colcon`:

```bash
colcon build
```

This will create three new folders inside the `mazeSolver` directory: `build`, `install`, and `log`.

> ✅ Once the build is complete, close this terminal.

### 3. Launch the Simulation

Open a **new terminal**, navigate to the `mazeSolver` directory, and run:

```bash
source install/setup.bash
ros2 launch turtlebot tb3_maze_navigation.launch.py
```

This will launch the Gazebo Classic simulation environment.

### 4. Start the Maze Solver Node

Open a **second terminal** (do not close the previous one), navigate to the `mazeSolver` directory again, and run:

```bash
source install/setup.bash
ros2 run turtlebot maze_solver.py
```

---

## 🧪 Output

After deployment, you will see the simulation in **Gazebo Classic**. Additionally, **RViZ2** will open alongside to visualize the 2D maze map.

> 🎯 Define the starting point of the TurtleBot using the `2D Pose Estimate` tool in RViz2.

The robot will then begin navigating the maze autonomously.

---

## 📚 References

- [ROBOTIS-GIT Official GitHub](https://github.com/ROBOTIS-GIT)
