cmake_minimum_required(VERSION 3.5.0)
project(MyProject)

include_directories("${CMAKE_SOURCE_DIR}")
include_directories("${CMAKE_SOURCE_DIR}/D")

add_subdirectory(A)
add_subdirectory(B)
add_subdirectory(C)
add_subdirectory(D)
