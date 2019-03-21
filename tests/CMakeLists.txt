include_directories(../src)

include_directories(.)

add_executable(tests
        # tests
        adapters1_tests.cpp
        btree1_tests.cpp
        # sources 
        ../src/btree.cpp
        ../src/btree.h
        ../src/btree_adapters.h
        ../src/utils.h
        # gtest sources
        gtest/gtest-all.cc
        gtest/gtest_main.cc
        )

# add pthread for unix systems
if (UNIX)
    target_link_libraries(tests pthread)
endif ()
