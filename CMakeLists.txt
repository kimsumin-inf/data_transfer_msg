cmake_minimum_required(VERSION 3.0.2)
project(data_transfer_msg)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

 add_message_files(FILES traffic_light.msg delivery_state.msg delivery_mission.msg)
 
  generate_messages(
   DEPENDENCIES
   std_msgs
 )

catkin_package(
  CATKIN_DEPENDS 
  std_msgs
  message_runtime
)

