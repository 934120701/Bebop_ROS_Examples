cmake_minimum_required(VERSION 2.8.3)
project(odometry)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp std_msgs nav_msgs)
## OpenCV package
#find_package(OpenCV REQUIRED)

## Declare ROS messages and services
##add_message_files(FILES Num.msg)
##add_service_files(FILES AddTwoInts.srv)

## Generate added messages and services
#generate_messages(DEPENDENCIES std_msgs)

## Declare a catkin package
catkin_package()

## Build talker and listener
include_directories(include ${catkin_INCLUDE_DIRS})
## OpenCV directories
#include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(odometry src/MessageReceiver.cpp)
target_link_libraries(odometry ${catkin_LIBRARIES})

