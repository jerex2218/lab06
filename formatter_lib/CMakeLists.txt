cmake_minimum_required(VERSION 3.10...3.28)
project(formatter_lib)


set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter_lib STATIC formatter.cpp)
target_include_directories(formatter_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

install(TARGETS formatter_lib
    ARCHIVE DESTINATION lib
)
