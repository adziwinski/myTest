cmake_minimum_required(VERSION 2.8.9)
project(myTest)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

#include_directories("include")
add_executable(myTest test.cpp)
target_link_libraries(myTest ${CONAN_LIBS})
add_library(myTypes CONAN_PKG::types)
#add_library(myTypes INTERFACE)
#target_link_libraries(myTest INTERFACE CONAN_PKG::types)
target_link_libraries(myTest myTypes)

