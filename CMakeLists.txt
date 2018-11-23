cmake_minimum_required(VERSION 3.12)
project(CLTests)
set(CMAKE_CXX_STANDARD 14)
include(FindOpenCL.cmake)

find_package(OPENCL REQUIRED)
include_directories(${OPENCL_INCLUDE_DIRS})

add_executable(CLTests main.cpp)
target_link_libraries(CLTests ${OPENCL_LIBRARIES})