set(PROJ_SRC
    gtest_main.cc
    sample1.cc
    sample1_unittest.cc
)

find_package (Threads REQUIRED)

add_executable(googletest_sample ${PROJ_SRC})
target_link_libraries(googletest_sample ${CMAKE_THREAD_LIBS_INIT} ${PROJECT_SOURCE_DIR}/lib/libgmock_main.a ${PROJECT_SOURCE_DIR}/lib/libgtest_main.a)

# Use following if gtest is installed

#find_package (GTest REQUIRED)
#target_link_libraries(googletest_sample ${CMAKE_THREAD_LIBS_INIT} ${GTEST_BOTH_LIBRARIES} /usr/local/lib64/libgmock.a)
