cmake_minimum_required(VERSION 3.22)
PROJECT(fuzzy)
AUX_SOURCE_DIRECTORY(src SOURCES)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/lib)
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
link_directories(lib)
add_library(fuzzy SHARED ${SOURCES})
target_include_directories(fuzzy PUBLIC include)
include_directories(include)
add_executable(test main.cpp)
target_link_libraries(test libfuzzy.so)

