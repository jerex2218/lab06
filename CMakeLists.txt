cmake_minimum_required(VERSION 3.28)
project(SolverProject LANGUAGES CXX)

# Настройки компилятора
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Настройки CPack (должны быть ПЕРЕД include(CPack))
set(CPACK_PACKAGE_NAME "solver")
set(CPACK_PACKAGE_VERSION "1.0.0")
set(CPACK_PACKAGE_VENDOR "Timur Stromenko")
set(CPACK_PACKAGE_CONTACT "Timur Stromenko <timurstromenko@gmail.com>")
set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Timur Stromenko <timurstromenko@gmail.com>")
set(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_SOURCE_DIR}/LICENSE")

# Включаем CPack после всех настроек
include(CPack)

# Подпроекты
add_subdirectory(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)
add_subdirectory(solver_application)
