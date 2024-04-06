add_library(C C.cpp)

target_link_libraries(C D)


# 为了外部调用C的库能自动包含C的头文件
target_include_directories(
    C INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}
)