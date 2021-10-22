cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
add_definitions(-std=c++11)
set(CXX_FLAGS "-Wall")
set(CMAKE_CXX_FLAGS, "${CXX_FLAGS}")

set(CMAKE_BUILD_TYPE Debug)

project(test)

add_subdirectory( "vendor/iptables-1.8.7" )
add_subdirectory( "vendor/libtins" )
add_subdirectory( "openssl-OpenSSL_1_1_1g" )

add_executable (test web-monitor.cpp)