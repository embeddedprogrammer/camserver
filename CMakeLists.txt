cmake_minimum_required(VERSION 2.8)
project(camserver)

find_package(catkin REQUIRED cv_bridge genmsg image_transport sensor_msgs)

catkin_package()

find_package(OpenCV)

include_directories(include ${OpenCV_INCLUDE_DIRS})

# add the publisher example
add_executable(my_publisher src/my_publisher.cpp)
target_link_libraries(my_publisher ${catkin_LIBRARIES})
