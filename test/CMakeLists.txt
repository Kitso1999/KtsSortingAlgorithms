include(FetchContent)

FetchContent_Declare(
        GoogleTest
        GIT_REPOSITORY https://github.com/google/googletest.git
        GIT_TAG a6ce08abf746c0aaa577520d6d1f6ea2abeeb61d
)

FetchContent_MakeAvailable(GoogleTest)

add_executable(test-sorts test_sorts.cpp)
target_link_libraries(test-sorts PRIVATE sorting_algorithms gtest_main)

include(GoogleTest)
gtest_discover_tests(test-sorts)