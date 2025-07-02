# Autonomous Maze Solving Robot Simulation

This repository contains the code to produce a **Gazebo Classic Simulation** of a robot that navigates its way through a simple maze **autonomously**.

The software tools mainly used in building this project are :

- *slam_toolbox* ROS2 package
- Navigation2 Stack
- Python3 Interpreter
- Basic ROS2 Framework
- Gazebo Classic Simulator
- *turtlebot3_gazebo* ROS2 package

Operating System :
- Ubuntu (*you can use the latest version available*) 

In order to deploy this project successfully, all the above listed softwares must be installed in your Ubuntu OS.



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
    
    - Open a new terminal inside the **Autonomous Maze Solving Turtlebot3 Simulation** directory and run the following commands:
        ```bash
        source install/setup.bash
        ros2 launch turtlebot tb3_maze_navigation.launch.py
        ```

  


    - Open a second parallel terminal inside the **Autonomous Maze Solving Turtlebot3 Simulation** directory (while keeping the previous terminal alive) and run the following command from it :
        ```bash
        source install/setup.bash
        ros2 turtlebot maze_solver.py
        ```


## Output

Once you have followed all the mentioned steps inside the **Deployment** section, the following **simulation output** can be seen in the **Gazebo Classic Simulator** window.

<figure class="video_container">
  <video controls="true" allowfullscreen="true" poster="Thumbnail.png">
    <source src="Gazebo_Sim_Recording.mp4" type="video/mp4">
  </video>
</figure>

You can also see the robot following ***the same*** trajectory in the ***2D maze map*** of the **RViz2** environment simultaneously. I could not screen record the **RViz2** simulation to show you - due to my computer hardware limitations.


## References

- [Official Github Account of Robotis: ROBOTIS-GIT](https://github.com/ROBOTIS-GIT)
- [Official Github Account of ROS Planning: ros-planning ](https://github.com/ros-planning)
 
