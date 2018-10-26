cmake_minimum_required(VERSION 3.13.0)
#search for Vars library
find_package(Vars CONFIG REQUIRED)

add_executable(app main.cpp)
#app needs Vars library for building and linking
#Vars library provides Vars::Vars target
#Vars::Vars target contain every information about
#library (includes, paths to *.so/*.dll *.lib/*.a, defs...
target_link_libraries(app PUBLIC Vars::Vars)
