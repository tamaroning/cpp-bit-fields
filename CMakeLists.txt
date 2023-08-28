cmake_minimum_required(VERSION 3.16)
project(cpp-bit-fields)
set(CMAKE_CXX_STANDARD 11)
enable_testing()

include_directories(${CMAKE_SOURCE_DIR})

add_library(
    cpp-bit-fields
    bf_asm.cpp
    cmp_base.cpp
    ex_traits.cpp
    var_asm.cpp
)

add_executable(cpp-bit-fields-test
    testbf.cpp)

add_test(NAME smoke COMMAND cpp-bit-fields-test)
