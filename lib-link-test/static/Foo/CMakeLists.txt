cmake_minimum_required(VERSION 3.5)

project(Foo LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(Foo STATIC
  Foo.cpp
  Foo.h
)

target_compile_definitions(Foo PRIVATE FOO_LIBRARY)
