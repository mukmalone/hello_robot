cmake_minimum_required(VERSION 3.0.2)
project(hello_robot_mbf)

find_package(catkin REQUIRED)
catkin_package()

install(PROGRAMS
  scripts/mbf_move_base_action.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)


include_directories()