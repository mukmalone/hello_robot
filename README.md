# hello_robot Xacro and URDF #

This repository hosts the source code for the ROS < hello_robot > package which builds the model for my first robot.

Below is the picture of the base that I will be building the URDF for.  The goals of this repository are:
- roughly model the base and attach ROS controllers to the wheel so it can be driven in gazebo
- add a laser sensor to the simulation 

The actual robot will have a RPLIDAR A1 laser senor and mecancum wheels.

![image info](./pictures/robotBase.png)


![image info](./pictures/URDF.png)


![image info](./pictures/Rviz.png)

![image info](./pictures/gazebo.png)

![image info](./pictures/drivingRobot.gif)

## Key concepts covered ##
- creating a URDF from scratch
- using Xacro to clean up the URDF and parameterize the creation of the robot
- importing URDF into Gazebo
- moving the robot in Gazebo
- adding a laser sensor to the model
- visualizing the laser scanner in RViz



