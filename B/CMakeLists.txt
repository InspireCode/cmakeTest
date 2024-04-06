add_library(B B.cpp)

target_link_libraries(B D)


# 为了外部调用B的库能自动包含B的头文件
target_include_directories(
    B INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}
)