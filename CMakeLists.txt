cmake_minimum_required(VERSION 3.17)
project(SDL2test)

set(CMAKE_CXX_STANDARD 11)

#include_directories(include)
add_subdirectory(sdl2)
include_directories(sdl2/include)

add_executable(SDL2test main.cpp)

target_link_libraries(SDL2test SDL2main SDL2-static)