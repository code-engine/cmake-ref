cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

project(CodeEngineExperiment VERSION 1.0.0)

add_subdirectory(Bar)
add_subdirectory(Baz)

add_executable(Foo Foo.cpp)

target_link_libraries(Foo PUBLIC Bar)

target_include_directories(Foo PUBLIC "${PROJECT_BINARY_DIR}" "${PROJECT_SOURCE_DIR}/Bar")
