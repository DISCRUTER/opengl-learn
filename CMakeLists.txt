cmake_minimum_required(VERSION 3.10.0)
project(opengl VERSION 0.1.0 LANGUAGES C CXX)

# copying resources into binary directory
file(COPY "${CMAKE_CURRENT_SOURCE_DIR}/src/resources" DESTINATION "${CMAKE_CURRENT_BINARY_DIR}")
file(COPY "${CMAKE_CURRENT_SOURCE_DIR}/src/shaders" DESTINATION "${CMAKE_CURRENT_BINARY_DIR}")

add_executable(opengl 
    src/main.cpp
    src/glad.c
    src/stb_image.cpp
)

target_include_directories(opengl PRIVATE include)

target_link_libraries(opengl glfw)
