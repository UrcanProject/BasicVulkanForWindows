cmake_minimum_required(VERSION 3.7)
project(Vulkan)

include_directories(./lib/glm ./lib/GLFW/include ./lib/1.0.42.1/Include)

link_directories(./lib/GLFW/lib-mingw ./lib/1.0.42.1/Lib32)

set(CMAKE_CXX_STANDARD 14)

set(SOURCE_FILES main.cpp)
add_executable(Vulkan ${SOURCE_FILES})

target_link_libraries(Vulkan glfw3 gdi32 opengl32 vulkan-1)