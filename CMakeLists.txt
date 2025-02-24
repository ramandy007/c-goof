cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
add_definitions(-std=c++11)
set(CXX_FLAGS "-Wall")
set(CMAKE_CXX_FLAGS, "${CXX_FLAGS}")

set(CMAKE_BUILD_TYPE Debug)

project(test)

add_subdirectory( "vendor/iptables-1.2.10" )
add_subdirectory( "vendor/haproxy-1.0.1" )

add_executable (test web-monitor.cpp)
