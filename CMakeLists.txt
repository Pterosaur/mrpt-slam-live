cmake_minimum_required(VERSION 3.6)
project(slam-live)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories(/usr/local/include/eigen3/)

LINK_LIBRARIES(
        mrpt-obs
        mrpt-maps
        mrpt-base
        mrpt-opengl
        mrpt-gui
        mrpt-slam
        mrpt-hwdrivers)

set(SOURCE_FILES main.cpp)
add_executable(slam-live ${SOURCE_FILES})