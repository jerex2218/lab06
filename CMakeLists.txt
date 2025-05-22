cmake_minimum_required(VERSION 3.28)
project(SolverProject LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


include(CPack)
set(CPACK_PACKAGE_NAME "solver")
set(CPACK_PACKAGE_VERSION "1.0.0")
set(CPACK_PACKAGE_VENDOR "My Company")
set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Timur Stromenko <timurstromenko@gmail.com>")


set(CPACK_WIX_UPGRADE_GUID "663c600f-fe9c-4076-bcd4-9dd507d64eb9")  
set(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_SOURCE_DIR}/LICENSE.txt")


add_subdirectory(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)
add_subdirectory(solver_application)
