cmake_minimum_required(VERSION 3.10...3.28)
project(solver_lib)

add_library(solver_lib STATIC solver.cpp)
target_include_directories(solver_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

install(TARGETS solver_lib
    ARCHIVE DESTINATION lib
)
