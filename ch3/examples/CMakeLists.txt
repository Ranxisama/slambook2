#include_directories("/usr/include/eigen3")
#add_executable(coordinateTransform coordinateTransform.cpp)
#
#find_package(Pangolin REQUIRED)
#include_directories(${Pangolin_INCLUDE_DIRS})
#add_executable(plotTrajectory plotTrajectory.cpp)
#target_link_libraries(plotTrajectory ${Pangolin_LIBRARIES})

cmake_minimum_required(VERSION 3.16)

project(examples)

set(CMAKE_CXX_STANDARD 11)

add_executable(plotTrajectory plotTrajectory.cpp)
target_link_libraries(plotTrajectory Pangolin)

include_directories("/usr/include/eigen3")

find_package(Pangolin 0.5 REQUIRED)
include_directories(${Pangolin_INCLUDE_DIRS})

find_package(OpenGL REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS})
target_link_libraries(plotTrajectory ${OPENGL_LIBRARIES})

find_package(GLEW REQUIRED)
include_directories(${GLEW_INCLUDE_DIRS})
target_link_libraries(plotTrajectory ${GLEW_LIBRARIES})
