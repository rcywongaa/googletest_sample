set(PROJ_SRC
    gtest_main.cc
    sample1.cc
)

find_package (Threads)

add_executable(googletest_sample ${PROJ_SRC})
target_link_libraries(googletest_sample ${CMAKE_THREAD_LIBS_INIT} ${PROJECT_SOURCE_DIR}/lib/libgmock_main.a ${PROJECT_SOURCE_DIR}/lib/libgtest_main.a)
