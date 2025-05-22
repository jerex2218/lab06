cmake_minimum_required(VERSION 3.10...3.28)
project(solver_application)


add_executable(solver
    equation.cpp
)


target_include_directories(solver
    PRIVATE ${CMAKE_SOURCE_DIR}/formatter_ex_lib
    PRIVATE ${CMAKE_SOURCE_DIR}/solver_lib
)


target_link_libraries(solver
    PRIVATE formatter_ex_lib
    PRIVATE solver_lib
)


install(TARGETS solver
    DESTINATION bin
)
