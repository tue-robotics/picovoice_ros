cmake_minimum_required(VERSION 3.5)
project(picovoice_msgs)

find_package(catkin REQUIRED COMPONENTS
  actionlib_msgs
  message_generation
)

add_message_files(FILES
  KeyValue.msg
  Keyword.msg
)

add_action_files(FILES
  GetIntent.action
  GetKeyword.action
)

generate_messages(DEPENDENCIES
  actionlib_msgs
)

catkin_package(CATKIN_DEPENDS
  actionlib_msgs
  message_runtime
)
