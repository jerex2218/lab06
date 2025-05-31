# Top-level CMakeLists.txt
cmake_minimum_required(VERSION 3.10)
project(solver)

# Add version definition
if(NOT DEFINED PRINT_VERSION)
    set(PRINT_VERSION "1.0.0")
endif()

# Set version before include(CPack)
set(CMAKE_PROJECT_VERSION ${PRINT_VERSION})

# ... [rest of your CMake code] ...

# Move this to AFTER setting variables
include(CPack)
