# Autonomous Maze Solving Robot Simulation

This repository contains the code to produce a **Gazebo Classic Simulation** of a robot that navigates its way through a simple maze **autonomously**.

Operating System :
- Ubuntu (*you can use the latest version available*) 

## Deployment

To deploy this project, please follow the below mentioned steps.



- Open a **new terminal** inside the folder.

- **Clone this repository** inside the folder by running the following terminal command.

    ```bash
    gh repo clone amaan-ee-iitr/mazeSolver
    ```

- This will create a new folder named **mazeSolver**.

- Go inside the **mazeSolver** folder through the previously opened terminal.

    ```
    cd mazeSolver/
    ```

- Next, we need to build this project, run the following command to build this project

    ```bash
    colcon build
    ```
    
    This will generate 3 (three) new folders inside the **mazeSolver** folder namely - **build**, **install** and **log**.

- Close the previous terminal.

- Next, deploy the project
    
    - Open a new terminal inside the **mazeSolver** directory and run the following commands:
        ```bash
        source install/setup.bash
        ros2 launch turtlebot tb3_maze_navigation.launch.py
        ```

  


    - Open a second parallel terminal inside the **mazeSolver** directory (while keeping the previous terminal alive) and run the following command from it :
        ```bash
        source install/setup.bash
        ros2 turtlebot maze_solver.py
        ```

## References

- [Official Github Account of Robotis: ROBOTIS-GIT](https://github.com/ROBOTIS-GIT)
- [Official Github Account of ROS Planning: ros-planning ](https://github.com/ros-planning)
 
