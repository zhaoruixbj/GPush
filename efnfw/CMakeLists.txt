cmake_minimum_required(VERSION 2.6)
project(efnfw)
set(CMAKE_VERBOSE_MAKEFILE ON)
add_definitions("-Wall -g -fPIC")
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)
include_directories(${PROJECT_SOURCE_DIR})
file(GLOB_RECURSE EF_LIST base/*.cpp net/*.cpp)
add_library(efnfw SHARED ${EF_LIST})
