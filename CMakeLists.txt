cmake_minimum_required(VERSION 2.8)

project(hello)

set(SOURCE_EXE main.cpp)

set(SOURCE_LIB hello.cpp)

set(SOURCE_LIB factorial.cpp)

add_library(hello STATIC ${SOURCE_LIB})

add_library(factorial STATIC ${SOURCE_LIB})

add_executable(main ${SOURCE_EXE})

target_link_libraries(main factorial hello)
