cmake_minimum_required(VERSION 3.13.0)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_INCLUDE_CURRENT_DIR_IN_INTERFACE ON)

add_library(engine STATIC engine.h engine.cpp)
