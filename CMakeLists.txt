cmake_minimum_required(VERSION 2.8.3)
project(dynamic_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  roscpp
  std_msgs
  nav_msgs
  geometry_msgs
  sensor_msgs
)

add_message_files(
   FILES
   TrajectoryArray.msg
   Trajectory.msg
   State.msg
   FullState.msg
   ObstacleArray.msg
   Obstacle.msg
   RSFCArray.msg
   RSFC.msg
   PlanningReport.msg
)


## Generate added messages and services with any dependencies listed here
 generate_messages(
   DEPENDENCIES
   std_msgs
   nav_msgs
   sensor_msgs
   geometry_msgs
   roscpp
 )


catkin_package(
  CATKIN_DEPENDS roscpp std_msgs message_runtime message_generation)

