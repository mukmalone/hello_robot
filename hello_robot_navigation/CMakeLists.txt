cmake_minimum_required(VERSION 3.0.2)
project(hello_robot_navigation)

find_package(catkin REQUIRED COMPONENTS
  amcl
  map_server
  move_base
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)