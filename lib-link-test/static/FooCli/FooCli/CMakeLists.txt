cmake_minimum_required(VERSION 3.5)

project(FooCli LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(METHOD1 ON)

add_executable(FooCli main.cpp)

if(METHOD1)
  add_library(Foo STATIC IMPORTED GLOBAL)

  set_target_properties(Foo
    PROPERTIES
      IMPORTED_LOCATION ${CMAKE_SOURCE_DIR}/lib/libFoo.a
  )
  target_link_libraries(FooCli Foo)
else()
  target_link_libraries(FooCli ${CMAKE_SOURCE_DIR}/lib/libFoo.a)
endif()

target_include_directories(FooCli PRIVATE include/)

