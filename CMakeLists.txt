cmake_minimum_required(VERSION 3.24)
project(ogl_playground)

set(CMAKE_CXX_STANDARD 17)

find_package(GLEW REQUIRED)
find_package(glfw3 CONFIG REQUIRED)
find_package(assimp CONFIG REQUIRED)

add_executable(ogl_playground main.cpp)

target_link_libraries(ogl_playground PRIVATE GLEW::GLEW)
target_link_libraries(ogl_playground PRIVATE glfw)
target_link_libraries(ogl_playground PRIVATE assimp::assimp)