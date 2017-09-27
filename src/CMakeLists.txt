set(PROJ_SRC
    gtest_main.cc
    sample1.cc
    sample1_unittest.cc
)

find_package (Threads REQUIRED)

add_executable(googletest_sample ${PROJ_SRC})
target_link_libraries(googletest_sample ${CMAKE_THREAD_LIBS_INIT} ${PROJECT_SOURCE_DIR}/lib/libgmock.a ${PROJECT_SOURCE_DIR}/lib/libgtest.a)

# Use following if gtest is installed

#find_package (GTest REQUIRED)
#find_library (GMOCK_LIBRARIES NAMES gmock)
#target_link_libraries(googletest_sample ${CMAKE_THREAD_LIBS_INIT} ${GTEST_BOTH_LIBRARIES} ${GMOCK_LIBRARIES})
