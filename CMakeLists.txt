cmake_minimum_required(VERSION 3.17)
project(SDL2test)

set(CMAKE_CXX_STANDARD 11)

#include_directories(include)
add_subdirectory(SDL-mirror)
include_directories(SDL-mirror/include)

add_executable(SDL2test main.cpp)

target_link_libraries(SDL2test SDL2main SDL2-static)