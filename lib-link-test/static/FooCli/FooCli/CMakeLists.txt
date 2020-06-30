cmake_minimum_required(VERSION 3.5)

project(FooCli LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(FooCli main.cpp)

target_link_libraries(FooCli ${CMAKE_SOURCE_DIR}/lib/libFoo.a)

target_include_directories(FooCli PRIVATE include/)

