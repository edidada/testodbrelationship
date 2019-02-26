cmake_minimum_required(VERSION 3.13)
project(testodbrelationship)

set(CMAKE_CXX_STANDARD 14)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -DDATABASE_MYSQL")

add_executable(testodbrelationship driver.cxx employee-odb.cxx)

target_link_libraries(testodbrelationship libodb-mysql.so)

target_link_libraries(testodbrelationship libodb.so)
