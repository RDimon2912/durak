cmake_minimum_required(VERSION 3.8)

project(server)

set(CMAKE_CXX_STANDARD 11)


set(SOURCE_FILES main.cpp chat_message.hpp)

find_package(Boost COMPONENTS system REQUIRED)
include_directories(${Boost_INCLUDE_DIRS})

add_executable(server ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} ${Boost_LIBRARIES})
