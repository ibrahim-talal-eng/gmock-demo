cmake_minimum_required(VERSION 3.10)
project(gmock_demo)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(GTest REQUIRED)

add_executable(registration_service_test registration_service_test.cpp registration_service.cpp)
target_link_libraries(registration_service_test PRIVATE GTest::gmock_main)
