cmake_minimum_required(VERSION 3.5.0)
project(MyProject)

add_executable(${PROJECT_NAME} A.cpp)


add_subdirectory(B)
target_link_libraries(${PROJECT_NAME} B)

add_subdirectory(C)
target_link_libraries(${PROJECT_NAME} C)

add_subdirectory(D)