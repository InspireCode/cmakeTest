add_library(D D.cpp)

target_include_directories(
    D INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}
)
