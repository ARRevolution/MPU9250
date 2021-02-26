cmake_minimum_required(VERSION 2.8.3)
project(mpu9250)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  sensor_msgs
  tf
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(mpu9250_node src/mpu9250.cpp)
target_link_libraries(mpu9250_node ${catkin_LIBRARIES})

