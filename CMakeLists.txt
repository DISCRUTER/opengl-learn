cmake_minimum_required(VERSION 3.10.0)
project(opengl VERSION 0.1.0 LANGUAGES C CXX)

add_executable(opengl 
    src/main.cpp
    src/glad.c
)

target_include_directories(opengl PRIVATE include)

target_link_libraries(opengl glfw)
