cmake_minimum_required(VERSION 3.16)
project(CatchTest)

set(CMAKE_CXX_STANDARD 17)

set(LIB_SOURCE_FILES sample_lib.cpp sample_lib.h)
add_library(sample_lib ${LIB_SOURCE_FILES})

set (TEST_SOURCE_FILES sample_test.cpp)
add_executable(test_runner ${TEST_SOURCE_FILES})
target_link_libraries(test_runner sample_lib)