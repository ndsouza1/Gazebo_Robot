cmake_minimum_required(	VERSION  2.8  FATAL_ERROR)

find_package(gazebo REQUIRED)
include_dIrectories(${GAZEBO_INCLUDE_DIRS})
link_directories(${GAZEBO_LIBRARY_DIRS})
list(APPEND  CMAKE_CXX_FLAGS "${GAZEBO_CXX_FLAGS}")

add_library(world SHARED script/world.cpp)
target_link_libraries(world ${GAZEBO_LIBRARIES})