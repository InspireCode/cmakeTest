add_library(C C.cpp)

add_subdirectory(../D buildD2) #由于D不是C的子目录，因此需要指定第二个参数build_dir
target_link_libraries(C D)


# 为了外部调用C的库能自动包含C的头文件
target_include_directories(
    C INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}
)