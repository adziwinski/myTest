cmake_minimum_required(VERSION 2.8.9)
project(myTest)
include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()
add_executable(myTest test.cpp)
target_link_libraries(myTest ${CONAN_LIBS})

