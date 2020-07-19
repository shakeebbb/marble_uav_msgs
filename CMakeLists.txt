cmake_minimum_required(VERSION 2.8.3)
project(marble_uav_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  message_generation
)

 add_service_files(
  DIRECTORY
    srv
  FILES
   GlobalComm.srv
 )

 generate_messages(
   DEPENDENCIES
    std_msgs
 )

catkin_package(
  CATKIN_DEPENDS roscpp std_msgs message_runtime
  )

include_directories(
  ${catkin_INCLUDE_DIRS}
)
