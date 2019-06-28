cmake_minimum_required(VERSION 3.0.0)
project(googletest_sample)

include_directories(include)

find_package (Threads REQUIRED)

#target_link_libraries(googletest_sample ${CMAKE_THREAD_LIBS_INIT} ${PROJECT_SOURCE_DIR}/lib/libgmock.a ${PROJECT_SOURCE_DIR}/lib/libgtest.a)

# Use following if gtest is installed
add_subdirectory(/usr/src/googletest gtest)
add_executable(googletest_sample
    src/gtest_main.cc
    src/sample1.cc
    src/sample1_unittest.cc
)
target_link_libraries(googletest_sample ${CMAKE_THREAD_LIBS_INIT} gtest)

