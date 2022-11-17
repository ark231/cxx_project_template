cmake_minimum_required(VERSION 3.5)

project(
    hoge
    VERSION 0.1
    LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(hoge main.cpp)

# include(cmake/CPM.cmake)

# find_package()

# cpmaddpackage()

# target_link_libraries()

target_compile_options(
    rubiks_cube_solver PRIVATE $<$<CXX_COMPILER_ID:Clang>:-Wall -Weverything> $<$<CXX_COMPILER_ID:GNU>:-Wall -Wextra >
                               $<$<CXX_COMPILER_ID:MSVC>:/W4>)
