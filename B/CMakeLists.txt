add_library(B B.cpp)

add_subdirectory(../D buildD1) #由于D不是B的子目录，因此需要指定第二个参数build_dir
target_link_libraries(B D)


# 为了外部调用B的库能自动包含B的头文件
target_include_directories(
    B INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}
)