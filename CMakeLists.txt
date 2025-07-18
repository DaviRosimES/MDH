cmake_minimum_required(VERSION 3.22)
project(MDH)

set(CMAKE_CXX_STANDARD 20)

include(FetchContent)

FetchContent_Declare(
        googletest
        URL https://github.com/google/googletest/archive/refs/heads/main.zip
)

# Prevent overriding the parent project's compiler/linker settings
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)

FetchContent_MakeAvailable(googletest)

enable_testing()

add_executable(MDH main.cpp
        src/datafeeder.cpp
        include/datafeeder.h)


# Testes
add_executable(Tests
        tests/test_datafeeder.cpp
)

target_link_libraries(Tests
        GTest::gtest_main
)

include(GoogleTest)
gtest_discover_tests(Tests)