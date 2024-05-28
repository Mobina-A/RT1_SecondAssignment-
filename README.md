# RT1_SecondAssignment
The second assignment of research track 1 course is about the use of a robot simulator in ROS. 

The tasks for this assignment are to move the robot in the environment to the goal position that chosen by user.
In this assignment we are using operator ROS custom messages, costum services, and actions.It is also required to create a launch file to start the simulation.

The main part of the assignment involves creating three nodes, which I have named node_a, node_b, and node_c. To set up the server and send the message, we need to create 'srv' and 'msg' files. Additionally, we have to modify the CMakeLists.txt and launch file ('assignment1.launch').

The tasks covered in each node are as follows:

* node_a: A node that implements an action client enabling users to set or cancel targets (x, y) or cancel it. The node uses the feedback/status of the action server to determine when the target has been reached. Additionally, the node publishes the robot position and velocity as a custom message (x, y, vel_x, vel_z), relying on the values published on the topic /odom.

* node_b: When called, the service node returns the coordinates of the last target sent by the user.

* node_c: This service node subscribes to the robot’s position and velocity (using the custom message) and implements a server to retrieve the distance of the robot from the target and the robot’s average speed.

Installing and running
----------------------
you have installed ROS and created your workspace you have to download the package second_assignment in the src folder of your workspace.

Run the following command from the shell:
```bash
$ https://github.com/CarmineD8/assignment_2_2023.git
```
Run the following command from the shell:\
```bash
$ git clone https://github.com/Mobina-A/RT1_SecondAssignment-.git
```
Then you have to run:
IMPORTANT: be sure to run the command above in the root folder of your workspace
```bash
$ catkin_make #properly build the workspace
```
In this state we can run the code thanks to the launch file you can simply run all the nodes using the command:
```bash
$ roslaunch assignment_2_2023 assignment1.launch
```

Flowchart of node_a
----------------------
![Tux, the Linux mascot](/FlowChart.jpg)


------------------------------------------------------------
# RT2_ SecondAssignment _ Jupyter
## ROS Robot Navigation and Visualization

This Jupyter Notebook provides an interface for controlling and visualizing a robot's navigation in a ROS environment.

## Features

* Set and cancel navigation goals.
* Visualize robot's position and path in real-time.
* Monitor the number of reached and canceled goals.

## Installation

```bash
 git clone https://github.com/Mobina-A/RT1_SecondAssignment-.git
```

```bash
 cd RT1_SecondAssignment
```

```bash
 pip install jupyros ipywidgets matplotlib numpy
```






