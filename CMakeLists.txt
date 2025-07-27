cmake_minimum_required(VERSION 4.0.0)
project (opengl_learn)

find_package(OpenGL REQUIRED)

add_executable(opengl_learn 
    src/main.c 
    glad/src/gl.c
)

target_include_directories(opengl_learn PRIVATE
    glad/include
)

target_link_libraries(opengl_learn
    glfw
    m
    dl
)
