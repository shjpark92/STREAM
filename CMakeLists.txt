cmake_minimum_required(VERSION 3.17.2)
project(STREAM)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${GCC_COVERAGE_COMPILE_FLAGS}")
set(GCC_COVERAGE_COMPILE_FLAGS "-save-temps")

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/CMake)

include_directories("${PROJECT_BINARY_DIR}")
include_directories("${PROJECT_SOURCE_DIR}/STREAM")
add_subdirectory(STREAM)

set(C_SOURCE STREAM/stream.c)
add_executable(stream_c.o ${C_SOURCE})
