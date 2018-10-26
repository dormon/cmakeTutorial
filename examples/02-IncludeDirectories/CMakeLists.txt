cmake_minimum_required(VERSION 3.12.2)

add_executable(HelloWorld src/main.cpp include/header.h)

target_include_directories(HelloWorld PUBLIC include)
