cmake_minimum_required(VERSION 3.15)  # Повысьте версию для CPack
project(Solver_Project)

set(CMAKE_CXX_STANDARD 11)

add_subdirectory(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)

add_subdirectory(solver_application)


set(CPACK_DEBIAN_PACKAGE_DEPENDS "libfmt-dev")  
set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Timur Stromenko")
set(CPACK_RPM_PACKAGE_REQUIRES "fmt-devel")

set(CPACK_PACKAGE_NAME "solver")
set(CPACK_PACKAGE_VERSION "1.0.0")
set(CPACK_PACKAGE_VENDOR "My_Company")
set(CPACK_PACKAGE_CONTACT "timurstromenko@gmail.com")

include(CPack)
