cmake_minimum_required(VERSION 3.17)
project(sdl-static)

set(CMAKE_CXX_STANDARD 17)

#include_directories(include)
add_subdirectory(SDL-mirror)
#include_directories(SDL-mirror/include)

add_library(sdl INTERFACE)
target_link_libraries(sdl INTERFACE SDL2main SDL2-static)

file(GLOB SOURCES src/*.c)
include_directories(src)
add_library(sdl-bgi STATIC ${SOURCES})
target_link_libraries(sdl-bgi sdl)

add_executable(sdl-static main.cpp)

target_link_libraries(sdl-static sdl-bgi sdl)

#target_link_libraries(sdl-static SDL2main SDL2-static)