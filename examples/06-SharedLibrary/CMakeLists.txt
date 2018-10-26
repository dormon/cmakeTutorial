cmake_minimum_required(VERSION 3.13.0)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_INCLUDE_CURRENT_DIR_IN_INTERFACE ON)

add_library(engine SHARED engine.h engine.cpp)

#we need to generated *_export.h file that contains __declspec ...
include(GenerateExportHeader)
generate_export_header(engine EXPORT_FILE_NAME engine_export.h)

