cmake_minimum_required(VERSION 3.0.2)
project(picar_teleop)

find_package(catkin REQUIRED COMPONENTS
  picar_msgs
  rospy
  std_msgs
)

catkin_package()

include_directories(${catkin_INCLUDE_DIRS})

catkin_install_python(PROGRAMS
  nodes/keyboard_control_node.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
