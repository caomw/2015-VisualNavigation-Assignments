cmake_minimum_required(VERSION 2.8.3)
project(euroc_simulation_server)

add_definitions(-std=c++0x)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  mav_msgs
  euroc_comm
  roscpp
  sensor_msgs
  rosbag
)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

catkin_package(  
  CATKIN_DEPENDS 
    geometry_msgs 
    mav_msgs 
    euroc_comm
    roscpp 
    sensor_msgs 
    rosbag
  DEPENDS Eigen
)
  
add_subdirectory(src/t1)
add_subdirectory(src/t2)
add_subdirectory(src/t3)
add_subdirectory(src/t4)
