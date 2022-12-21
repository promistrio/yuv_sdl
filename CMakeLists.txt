cmake_minimum_required(VERSION 3.7)

project(SDL2Test)


set(OpenGL_GL_PREFERENCE GLVND)

find_package(SDL2 REQUIRED)
find_package(OpenGL REQUIRED)


include_directories(${SDL2_INCLUDE_DIRS})
include_directories(${OPENGL_INCLUDE_DIR})

add_executable(SDL2Test src/main.cpp)
target_link_libraries(SDL2Test ${SDL2_LIBRARIES})
target_link_libraries(SDL2Test ${OPENGL_LIBRARIES})