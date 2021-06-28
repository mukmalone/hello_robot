# hello_robot #

My project was fortunate to be selected for recognition during my coursework with [Lentin Joesph](https://www.linkedin.com/in/lentinjoseph/).  You can check out his great course and books here: https://robocademy.com/

![image info](./pictures/4.png)

## Description ##

This repository hosts the source code for the ROS < hello_robot > package which builds the model for my first robot.

Below is the picture of the base that I will be building the URDF for.  The goals of this repository are:
- roughly model the base and attach ROS controllers to the wheel so it can be driven in gazebo
- add a laser sensor to the simulation 

[![IMAGE ALT TEXT](http://img.youtube.com/vi/sEv-iHaviXk/0.jpg)](https://youtu.be/sEv-iHaviXk "hello_robot home service full stack demonstration")

## Key concepts covered ##
- creating a URDF from scratch
- using Xacro to clean up the URDF and parameterize the creation of the robot
- importing URDF into Gazebo
- moving the robot in Gazebo
- adding a laser sensor to the model
- visualizing the laser scanner in RViz
- configuring Gazebo controls
- configuring Navigation and SLAM packages
- tuning parameters
- building physical robot

### Usage ###
#### View hello_robot in RVIZ ####
- `roslaunch hello_robot_description hello_robot_rviz.launch`
#### View & drive hello_robot in Gazebo ####
- `roslaunch hello_robot_gazebo hello_robot_world.launch`
#### SLAM GMapping with hello_robot ####
- in one terminal `roslaunch hello_robot_gazebo hello_robot_world.launch`
- in 2nd terminat `roslaunch hello_robot_slam hello_robot_slam.launch`
- save map using `rosrun map_server map_saver -f nameOfMap
#### Navigation with hello_robot ####
- in one terminal `roslaunch hello_robot_gazebo hello_robot_world.launch`
- in 2nd terminal `roslaunch hello_robot_navigation hello_robot_navigation.launch`

Very quick video showing the SLAM and Navigation working.

[![IMAGE ALT TEXT](http://img.youtube.com/vi/5LuyBR_MqcY/0.jpg)](https://youtu.be/5LuyBR_MqcY "ROS SLAM GMapping & Navigation Implementation")

### Simulation ###

![image info](./pictures/URDF.png)


![image info](./pictures/Rviz.png)

![image info](./pictures/gazebo.png)

![image info](./pictures/drivingRobot.gif)

### Physical Robot ###

![image info](./pictures/base_assembly.png)

![image info](./pictures/wiring.png)

![image info](./pictures/robotBase.png)

### First drive of the actual robot ###

[![IMAGE ALT TEXT](http://img.youtube.com/vi/x3qpu2Kqpcg/0.jpg)](https://youtu.be/x3qpu2Kqpcg "First drive of Hello_Robot")
