# 가장 간단한 cmake 예제  
#%Tag(FULLTEXT)%
cmake_minimum_required(VERSION 2.8.3)
project(JJW_EX1)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs genmsg)

## Generate added messages and services
generate_messages(DEPENDENCIES std_msgs)

## Declare a catkin package
catkin_package()

## Build talker and listener
include_directories(include ${catkin_INCLUDE_DIRS})
add_executable(louder src/tk/louder.cpp)
target_link_libraries(louder ${catkin_LIBRARIES})

# %EndTag(FULLTEXT)%

