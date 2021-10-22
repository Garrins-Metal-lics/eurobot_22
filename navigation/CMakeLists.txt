cmake_minimum_required(VERSION 3.0.2)
project(navigation)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
)

catkin_package(  
)

###########
## Build ##
###########

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

#############
## Install ##
#############

## Mark executable scripts (Python etc.) for installation
## in contrast to setup.py, you can choose the destination
catkin_install_python(PROGRAMS
  scripts/primer_node.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
