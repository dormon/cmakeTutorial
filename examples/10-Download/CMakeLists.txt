cmake_minimum_required(VERSION 3.13.0)

include(FetchContent)

FetchContent_Declare(MealyMachine     GIT_REPOSITORY https://github.com/dormon/MealyMachine.git   )
FetchContent_Declare(TxtUtils         GIT_REPOSITORY https://github.com/dormon/TxtUtils.git       )
FetchContent_Declare(ArgumentViewer   GIT_REPOSITORY https://github.com/dormon/ArgumentViewer.git )

FetchContent_GetProperties(MealyMachine)
if(NOT MealyMachine_POPULATED)
  FetchContent_Populate(MealyMachine)
  add_subdirectory(${mealymachine_SOURCE_DIR} ${mealymachine_BINARY_DIR})
endif()

FetchContent_GetProperties(TxtUtils)
if(NOT TxtUtils_POPULATED)
  FetchContent_Populate(TxtUtils)
  add_subdirectory(${txtutils_SOURCE_DIR} ${txtutils_BINARY_DIR})
endif()

FetchContent_GetProperties(ArgumentViewer)
if(NOT ArgumentViewer_POPULATED)
  FetchContent_Populate(ArgumentViewer)
  add_subdirectory(${argumentviewer_SOURCE_DIR} ${argumentviewer_BINARY_DIR})
endif()

add_executable(as main.cpp)
target_link_libraries(as ArgumentViewer::ArgumentViewer)
