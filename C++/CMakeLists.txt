cmake_minimum_required(VERSION 3.22)
project(test)

set(CMAKE_CXX_STANDARD 14)

find_package(nlohmann_json REQUIRED)

add_executable(test server.cpp)

target_link_libraries(test PRIVATE nlohmann_json::nlohmann_json)

// g++ server.cpp -o serv --std=c++14 -I/usr/local/include -I/usr/include/nlohmann httplib.h 