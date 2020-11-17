cmake_minimum_required(VERSION 3.17)

# set the project name
project(cmake_tut VERSION 1.0)

# specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

#include_directories(BEFORE "${MSYS2_HOME}/usr/include")
                          
configure_file(TutorialConfig.h.in TutorialConfig.h)

# add the executable
add_executable(cmake_tut main.cpp)

message(STATUS "MS: ${PROJECT_BINARY_DIR}")
target_include_directories(cmake_tut PUBLIC
                          "${PROJECT_BINARY_DIR}"
)

