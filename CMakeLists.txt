cmake_minimum_required(VERSION 2.8.3)
project(pr_control_msgs)

find_package(catkin REQUIRED COMPONENTS
  actionlib_msgs
  sensor_msgs
  std_msgs
)

add_action_files(
  DIRECTORY action
  FILES
    SetForceTorqueThreshold.action
    SetPosition.action
    Trigger.action
)

generate_messages(DEPENDENCIES
  actionlib_msgs
  sensor_msgs
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    actionlib_msgs
    sensor_msgs
    std_msgs
)
