cmake_minimum_required(VERSION 3.12.2)

# this command will add application HelloWorld to build list
add_executable(HelloWorld main.cpp)

target_compile_definitions(HelloWorld PUBLIC PARROT=32)
