cmake_minimum_required(VERSION 2.8.9)
project(myTest)

include(cmake/packagemanager.cmake)

add_executable(myTest test.cpp)
target_link_libraries(myTest ${CONAN_LIBS})