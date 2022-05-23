project(Mission)
cmake_minimum_required(VERSION 3.22)
SET(LIBRARY_OUTPUT_PATH ${Mission_SOURCE_DIR}/lib)
#add_library(ApiTest SHARED Mission2/ApiTest.cpp)
add_library(ApiTest STATIC Mission2/ApiTest.cpp)
INCLUDE_DIRECTORIES(${Mission_SOURCE_DIR})
add_executable(mission1 Missoin1/main.cpp)
add_executable(mission2 Mission2/main.cpp)
target_link_libraries(mission2 ApiTest)


