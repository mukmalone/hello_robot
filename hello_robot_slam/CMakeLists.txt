cmake_minimum_required(VERSION 3.0.2)
project(hello_robot_slam)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  sensor_msgs
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)